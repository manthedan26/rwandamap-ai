# RwandaMap AI 🇷🇼

### SchoolMap AI Rwanda

**Find. Understand. Connect.**

Developed by **Manthedan** · *Innovation for a better tomorrow*

RwandaMap AI is an AI-powered digital mapping platform that makes important information about Rwanda's institutions, services, schools and communities easier to discover and understand.

Its first application, **SchoolMap AI Rwanda**, is an education-focused system that combines school data, geographic visualization and artificial intelligence to explore education access across Rwanda.

## Features

- 🇷🇼 Interactive map of Rwanda (drag, pinch and zoom)
- 🏫 School mapping with real school names
- 🔎 Search and filters by province, district and sector
- 📊 Official national indicators (MINEDUC 2024/2025)
- 🤖 AI assistant that answers in **Kinyarwanda, English and French**
- 🧠 Education access-gap analysis
- 📚 Data sources and methodology shown in the app
- 📥 Import your own school list (CSV or GeoJSON) and export what you see
- 🌗 Light and dark mode
- 📱 Works on phones, tablets and computers

## Pages (tabs)

Home (Manthedan) → Overview → School Map → AI Access Gap → Insights → Sources → About

## Run it

No build step. Open `index.html` in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Publish with GitHub Pages

1. Create a new repository and upload all files in this folder (keep `index.html` at the root).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then **Save**.
4. After a minute your site is live at `https://<your-username>.github.io/<repository-name>/`.

## Data

- **National figures** come from the MINEDUC *Education Statistical Yearbook 2024/2025*: 4,996 schools, 4,822,507 learners, 83.7% of schools with internet, pupil/classroom ratio 51:1. Population projections used by MINEDUC come from NISR.
- **School names and locations** appear only from real records:
  - Press **Load all schools from OpenStreetMap** in the School Map tab (needs internet), or
  - Press **Import data** and choose a CSV (see `data/schools_template.csv`) or GeoJSON file, or
  - Add verified records to `data/schools.js`.
- OpenStreetMap is crowd-sourced and incomplete, so it will not match the official 4,996 schools. The app shows how many are loaded versus the official total.
- The Rwanda outline in `script.js` is simplified. Use official boundary data for survey-accurate borders.

### CSV format

```csv
name,type,province,district,sector,lat,lng
St. Ignatius School,Unclassified,Kigali City,,,-1.93583,30.11861
```

## Data principle

The presence or absence of a school does not prove that an area has an education problem. RwandaMap AI uses visualization and AI to find patterns that may need further investigation. It supports decision-making and does not replace official statistics or expert judgment.

## Project structure

```
index.html            Main structure and content
style.css             Design, layout and responsiveness
script.js             Map, tabs, assistant and import logic
favicon.svg           App icon
data/schools.js       Verified school records
data/schools_template.csv   Import template
```

## Optional: connect a language model

The assistant works offline with rules. To use a hosted AI model, set `window.RM_AI_ENDPOINT` to your own server URL. The server receives `{question, language, context}` and returns `{reply}`. **Never put an AI API key in these files.**

## Technology

HTML · CSS · JavaScript · SVG maps · public datasets · OpenStreetMap · optional AI/API integration · GitHub Pages

## Vision

A smarter and more connected Rwanda where people can easily discover, understand and use important information through digital technology.

## Mission

To combine data, maps and artificial intelligence to make information more accessible and support better evidence-based decisions.

## Credits and licence

Developed by **MANZI BRIAN BONHEUR**, Manthedan. © 2026 Manthedan. All rights reserved (see `LICENSE`).
School data © OpenStreetMap contributors (ODbL). Statistics: MINEDUC and NISR.

**Made for Rwanda 🇷🇼**
