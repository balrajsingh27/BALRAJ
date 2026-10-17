# Atmos — Weather Intelligence for Everyday Life

Atmos is a responsive weather and air-quality dashboard built with **HTML, CSS, and plain JavaScript**. It combines the required course-assignment features with a wider daily-planning experience, farmer-first tools, multilingual preferences, saved locations, and optional local personalisation.

## What's included

- **Everyday overview:** current modelled conditions, a seven-day forecast, hourly trends, air-quality estimates, weather heads-up cards, and practical suggestions.
- **Required comparison feature:** compare up to six places using current weather cards and hourly temperature / European AQI charts.
- **Saved places:** keep important locations in this browser, use one as the home forecast, or add it to comparisons.
- **Farmer-first planning:** choose a crop, growth stage, approximate field area, soil type, irrigation approach, and planned activity. Forecast-based prompts highlight possible rain, heat, wind, cold, and fieldwork considerations.
- **Daily task planner:** add, filter, complete, and delete tasks, including tasks that depend on weather.
- **Personalised experiences:** everyday life, farming, school/college, commuting/office, outdoor work, delivery/driving, business, and home/family.
- **Languages:** English, Hindi, and Punjabi for the main interface. Some rapidly changing forecast wording and detailed activity-specific prose can remain in English.
- **Optional adaptation:** if enabled, section visits and approximate active time can locally reorder suggestions. The app does not infer a person's profession as a fact.
- **Backup and recovery:** export local preferences and tasks to JSON and import an Atmos backup.
- **Accessibility / responsive layout:** keyboard-visible focus, semantic landmarks, status announcements, mobile navigation, and reduced-motion awareness.

## Files

Keep these three files in the **same folder**:

- `index.html` — page structure and dialogs
- `styles.css` — responsive styles
- `app.js` — API requests, charts, comparison, farming prompts, planner, favourites, preferences, and local storage

## Run it on your computer (beginner-friendly)

1. Download and extract the ZIP file.
2. Install [Visual Studio Code](https://code.visualstudio.com/) if it is not already installed.
3. In VS Code, choose **File → Open Folder** and select the extracted `atmos-smart-dashboard` folder.
4. Install the **Live Server** extension in VS Code.
5. Right-click `index.html` and select **Open with Live Server**.
6. Keep the folder's three files together. Do not rename one file unless you also update its reference in `index.html`.

A local web server is recommended instead of opening the HTML file directly. Internet access is needed for weather/geocoding requests and for the Chart.js CDN script.

## Public data sources

- Weather Forecast API: <https://open-meteo.com/en/docs>
- Air Quality API: <https://open-meteo.com/en/docs/air-quality-api>
- Geocoding API: <https://open-meteo.com/en/docs/geocoding-api>
- Chart.js: <https://www.chartjs.org/>

No API key is configured in the project. The UI links to Open-Meteo for attribution. Before a public or commercial launch, check the API provider's current usage terms, attribution requirements, and fair-use limits.

## Notes on interpretation and safety

- Weather and air-quality values are **forecast/model estimates**, not guaranteed measurements at the exact site and time.
- The European AQI and US AQI use different scales; compare values within the same index.
- The farm planner produces general prompts from weather thresholds. It cannot estimate actual root-zone moisture or guarantee irrigation timing, spraying safety, pesticide suitability, crop disease, sowing readiness, or harvest readiness. Follow local agricultural advisories, field observations, and all product labels.
- App-generated heads-up cards are not official severe-weather or emergency alerts. Follow local authorities and workplace safety procedures.
- Location access is optional. If the user chooses it, the browser provides coordinates for the forecast request. A text search can be used instead.
- Preferences, tasks, favourites, field details, and optional activity summaries are stored in browser `localStorage`. They do not automatically sync between devices. Clearing browser data can remove them; use the JSON backup if needed.
- The version is designed as a client-side course project. It does not provide account login, cloud synchronisation, guaranteed push notifications, or background alert delivery.

## Publish it

### GitHub Pages

1. Create a **public** repository on GitHub.
2. Upload `index.html`, `styles.css`, `app.js`, and `README.md` to the repository root.
3. Open the repository's **Settings → Pages**.
4. Under build/deployment, select **Deploy from a branch**, choose `main` and `/(root)`, then save.
5. Wait for GitHub Pages to publish, then open the public URL shown on the Pages screen and test the major features.

For another simple host, you can upload the same three app files to Netlify or another static-site host. Do not publish secrets; this project is not using any.

## Suggested assessment demonstration

1. Show the everyday homepage with forecast, air quality, hourly chart, and seven-day forecast.
2. Search and select another city.
3. Compare three or more cities and show both trend charts.
4. Save a place, revisit Saved places, and reload to demonstrate browser persistence.
5. Switch the interface to Hindi or Punjabi and set a different experience.
6. Open the Farm planner, select a crop and planned activity, then save the field profile.
7. Create, complete, filter, and delete a task in My day.
8. Show the optional activity-personalisation switch and local-data export/import settings.
9. Capture the deployed app as a **full-page PDF screenshot** for the submission form.

## Current implementation scope

This is a static client-side web application. It is intended as a substantial, maintainable assignment implementation rather than an artificial 5,000–15,000-line file-size target. The source is deliberately unminified and split by responsibility so it can be reviewed and debugged.
