# Traffic Congestion Prediction Optimization

## Project Overview
This project aims to predict traffic congestion levels in Istanbul districts using time series analysis with LSTM neural networks. Various datasets such as population, public transport, weather and traffic data were combined, cleaned and analyzed.

## Dataset
- The datasets can be found under the `data/` and `original_data/` folders.
- You can use processed data (`data/`) or raw data (`original_data/`) depending on what you want to do.
- Depending on the size we might not be able to upload all the data, in such case please consider only using final `data/all_data_merged.csv` dataset to run main notebooks.

## Prerequisites
- To run the notebooks and reproduce the results you need the Python libraries listed in `requirements.txt`.
- Especially the data of "hourly traffic in Istanbul" is considerably large, so we weren't able to upload it to github or ninova (can be seen in `.gitignore` file as well). If you want to use only the main LSTM optimization notebooks it is not required, but to run data manipulation notebooks you should download this data from: https://ulasav.csb.gov.tr/dataset/34-hourly-traffic-density-data-set and put directly into `original_data/` folder.

### Install requirements
```bash
pip install -r requirements.txt
```

## Project Contents
- **Data Cleaning:** Preparation and cleaning of raw datasets. Under the `data_manipulations/` folder you can find out specific notebooks for each dataset we have specified as:
    - `{bus, rayli}_data.ipynb` for bus and railway system data modifications
    - `{bus, rayli}_count_district.ipynb` for assigning bus and railway stop counts to districts
    - `{population_district, weather, traffic}_data.ipynb` for traffic, population and weather data modifications
    - `merge_{traffic_population, weather_traffic}.ipynb` for merging all the data togetger in a daily format

- **Modeling:** Training LSTM models with different optimization methods, in `main/` folder, we have used each model in different notebook for clarity as:
    - `main_{adam, bayes, pso, pso_mae}.ipynb` for training LSTM models with Adam, Bayesian and Particle Swarm Optimization methods.

- **Experimental Analysis:** Tried alternative techniques to improve the quality of optimization techniques and experiments:
    - `{pso_experiments}.ipynb` for Particle Swarm Optimization experiments explained in the report.

- **Visualization:** Evaluation of results and visual analysis.

## Outputs
The notebooks generate prediction results and visualizations comparing different optimization techniques on traffic congestion prediction.

## Notes
- If any errors occur, make sure that all library dependencies are installed and up to date.
- We will be sending an already activated notebook so you can also redownload it!

## Authors
Anıl Dervişoğlu, 150220344  
Ömer Faruk Zeybek, 150220743
