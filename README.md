# TUSHONKA

**Mobile-first raid encounter analytics | React Native + Expo | Work in progress**

TUSHONKA is a planned Android and iOS application for recording raids and **suspected unfair-play encounters** in *Escape from Tarkov*. Its goal is to turn personal encounter logs into useful statistics by server, map, date, and time, and eventually estimate which combinations have lower reported encounter rates.

This repository currently contains the **original browser-based prototype**. The mobile rebuild has been selected, but **React Native, the Python API, and PostgreSQL are not implemented yet**.

## Current prototype

The existing HTML/CSS/JavaScript app includes:

- An encounter form recording server, time of day, and day of week
- Browser-local persistence with `localStorage`
- A paginated record viewer, deletion of individual entries, and a clear-all control
- Charts comparing reported encounters across servers, days, and time periods, using Chart.js
- Simple recommendations based on *raw report counts*

These recommendations are **not reliable risk estimates**: a server with fewer reports might simply have fewer raids logged. The mobile rebuild will record *all raids*, including those without suspicious encounters, so rates can be calculated with meaningful denominators.

**Current tools:** HTML, CSS, JavaScript, Bulma, Chart.js, browser `localStorage`.

## Mobile application direction

The next version will be a native mobile application, not merely a website wrapped in a WebView.

| Layer | Planned technology | Responsibility |
| --- | --- | --- |
| Mobile UI | React Native + Expo, TypeScript | Android/iOS forms, record history, filters, charts |
| API | Python + FastAPI | Validation, CRUD endpoints, analytics |
| Database | PostgreSQL | Persistent raids, encounter reports, server and map reference data |
| Testing | pytest; mobile component/integration tests | Verify API behavior and data calculations |
| Optional future web interface | React | A dashboard using the same API |

The existing JavaScript logic and prototype screens are references for the rebuild; **HTML/CSS DOM code cannot be dropped directly into React Native**.

## Planned features

### Raid logging
- Select server region and PvP map
- Record calendar date, hour block, and in-game day/night conditions
- Mark whether suspicious activity was encountered; optionally add notes
- Edit and delete entries; clearly confirm destructive bulk reset actions
- Record normal raids too, so the dataset is not limited to suspicious encounters

### Analytics
- Filter by map, server, date range, and time window
- Show total raids, suspected encounters, and encounter rates
- Display interactive charts and comparisons by server/map/time
- Suggest lower-*observed*-rate combinations only when sample sizes justify it
- Clearly indicate limited sample sizes, reporting bias, and uncertainty

### Data and usability
- Persistent records through a FastAPI/PostgreSQL backend
- Input validation and automated tests for key data operations
- Mobile-friendly accessibility and dark-mode interface
- Potential future offline logging, synchronization, and CSV export

The application logs **suspected** encounters based on user reports. These observations are not proof that any player cheated, and the application will not claim to identify or publicly accuse individual players.

## Proposed data model

A `raid` record will include a timestamp, server, map, in-game time category, and whether a suspected encounter occurred. An optional incident record can hold notes associated with a raid. Separate server/map reference tables will support standardized options and filtering.

Example rate: `suspected encounters / total recorded raids` for a selected map, region, and time window. This is a user-observed statistic, **not a population-wide cheating prevalence estimate**.

## Development roadmap

- [x] Build initial browser prototype with local logging, records, and charts
- [x] Choose React Native + Expo mobile architecture
- [ ] Preserve prototype and initialize Expo/TypeScript mobile project
- [ ] Implement map/server selection and raid/incident entry screens
- [ ] Create FastAPI endpoints and PostgreSQL schema
- [ ] Implement create, read, update, delete, and validation flows
- [ ] Add rate-based analytics and charts with sample-size context
- [ ] Add automated backend and mobile tests
- [ ] Test Android builds; prepare iOS builds and store requirements

## Running the current prototype

Until the native project exists, clone the repository and open `index.html` in a browser. The prototype saves records in that browser's local storage, so data **does not sync across devices** and may be lost if browser storage is cleared.

```bash
git clone https://github.com/treeewzrd/EFT-CHEATER-TRACKER.git
cd EFT-CHEATER-TRACKER
```

After the GitHub repository is renamed to `TUSHONKA`, the canonical clone URL will become `https://github.com/treeewzrd/TUSHONKA.git`.

## Repository status

**WIP / active redesign.** The current prototype demonstrates the initial interaction and reporting concept. The mobile app, backend, and database described above are the **planned implementation**, not existing production functionality.

## Disclaimer

TUSHONKA is an independent fan-made analytics project and is not affiliated with Battlestate Games or *Escape from Tarkov*. It does not provide anti-cheat detection or verified claims about individual players.
