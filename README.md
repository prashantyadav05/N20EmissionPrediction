# Agricultural N<sub>2</sub>O flux Prediction:

## Problem statement : To predict agricultural Nitrous oxide $(N_2 O)$ emissions from intensively managed cropping systems.

Nitrous Oxide is one of the potent greenhouse gas that is accumulating in the atmosphere at extraordinary rates. This can be largely attributed to intensification of agricultural cropping systems where the cultivated soil contribute almost 60% of the agricultural flux.
Though there were previous attempts at identifying and quantifying the agricultural Nitrous Oxide flux, these attempts could only predict the results with an R2-score ranging from 25-40%. The model used in this app is aimed at outperforming the previous models and has been able to succesfully produce the results with almost 78% R2-score.

## Feature Information
* Date - Gas Sampling days.
* Year - Calender year.
* Experiment - Long term experiments
* DataUse - Data to be used for experiment.
* Month - Month of year.
* Vegetation - Periodicity of crop cultivation.
* N20 - Atmospheric Nitrous Oxide  concentration in ppb/yr.
* N_rate - Nitrogen fertilizer application rate in kg/ha.
* PP2 - Cumulative precipitation in the last two days before gas sampling in mm.
* PP7 - Cumulative precipitation in the last week before gas sampling in mm.
* AirT - Mean daily air temperature in °C.
* DAF_TD - Days after top-dressed Nitrogen fertilization.
* WFPS25cm - Water filled pore space in the top 25cm soil layer. (Approximation of soil Oxygen limitation.
* NH4 -  Ammonium Nitrogen content in the top 25cm soil layer in kg/ha.
* NO3 - Nitrate Nitrogen content in the top 25cm soil layer in kg/ha.
* Clay - Clay content in g/kg.
* SOM  - Soil organic matter concentration in %.

## Model Used
The app uses a machine learning model known as "Random Forest Regressor" for making the prediction. Random Forest belongs to tree based ensemble models category and hence it is tough to interpret the final output of the model. 
Hence, I have used an explainable AI tool known as "SHAP" for understanding the model and interpreting the output.

## Challenges faced
* The data that quantified Nitrous Oxide flux was heavily right skewed and also contained few negative values.  
* The data for Water frontage pore space, Ammonia and Nitrate had some values missing.  
* Vegetation data was highly imbalanced with almost 84% of the data were recorded for Corn. Data for Wheat and Soy constituted only about 8.5 and 7.5% each.

## Building the app
The app was built using Python3.8 and with the help of Streamlit library. Other major libraries used include Numpy, Pandas, Matplotlib, Scikit-learn and Shap. The app is currently deployed on heroku.  
