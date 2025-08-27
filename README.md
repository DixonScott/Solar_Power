[![App Status](https://img.shields.io/badge/Render-ffffff?logo=render&color=blue&logoColor=ffffff)](https://solar-forecast-uk.onrender.com/)
[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
![Last commit](https://img.shields.io/github/last-commit/DixonScott/solar-forecast)

# Solar Forecast UK

This is an end-to-end machine learning project that predicts solar panel efficiency from weather forecasts. From gathering raw data via APIs to deploying a web app, this project showcases applied data science, and delivers a practical tool for prospective solar panel system owners and people looking for a quick estimate of the upcoming week's solar panel output.

## Demo

[Web App on Render](https://solar-forecast-uk.onrender.com/)

## How It Works
The project combines solar panel output data from PVOutput with historical weather forecasts from Open-Meteo. By merging this data on location and date, I created a dataset for training a random forest model, which predicts solar panel efficiency from weather conditions. This model powers the web app, which fetches the weather forecast from Open-Meteo for the upcoming 7 days to predict solar panel efficiency. The average prediction error is 0.75 hours (efficiency is measured as energy output (kWh) divided by the system power rating (kW)).

## Tech Stack
- **Languages:** Python, HTML, CSS, JavaScript
- **Key Libraries:** requests, pandas, scikit-learn, matplotlib
- **Web App:**
  - **Backend:** Flask
  - **Frontend:** Custom HTML/CSS/JavaScript, Leaflet.js
  - **Deployment:** Render

## Dataset
While the API from Open-Meteo is free to use, the API from PVOutput requires a small donation (some features are free, but they are not sufficient for this project). For this reason, the dataset is not provided here. In the future, I may add a synthetic dataset, and/or provide instructions for PVOutput donators to recreate my dataset.

## Future Work
High Priority:
- Improve model accuracy. This will require building a new dataset because I could not make any further improvement to the accuracy despite a lot of experimentation.
- Verify model performance by recording predictions for the upcoming week and comparing with the real values once available.

Low Priority:
- Expand the scope of the model from the UK to the world.
- Add features to the web app such as storing past predictions or providing confidence intervals.
- Interpret the model with visualisations.

## Acknowledgements
- [PVOutput](https://pvoutput.org) - for solar panel output data
- [Open-Meteo](https://open-meteo.com) - for weather data, provided under [Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)
- [Render](https://render.com) - for hosting the web app

## License

This project is licensed under the MIT License.