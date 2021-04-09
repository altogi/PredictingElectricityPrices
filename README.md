# Predicting Power Prices in Spain

The current study deals with the processing and modelling of a dataset describing the power grid in Spain, in order to predict its hourly price evolution. The provided dataset contains the following timeseries with hourly granularity:
* date: date of the observation ”%Y-%m-%d”
* hour: hour of the observation, [0 - 23]
* fc demand: forecast of demand in MWh
* fc nuclear: forecast of nuclear power production in MWh
* import FR: forecast of the importing capacity from France to Spain in MWh
* export FR: forecast of the exporting capacity from Spain to France in MWh
* fc wind: forecast of wind power production in MWh
* fc solar pv: forecast of PV solar (solar panels) power production in MWh
* fc solar th: forecast of thermal solar power production in MWh
* price: power price for each hour in €/MWh. This is the target we want you to predict.

The objectives of the study are as follows:
* To examine the initial structure of the features in the dataset, with particular focus on the distribution of all numerical variables, the number of missing values and outliers in each variable, and the correlations existing betwen features and target.
* To extract relevant features from all features in the dataset representing temporal evolutions, in particular: season data, daylight data, holiday data, etc.
* To normalize and scale numerical features in order to set a common order of magnitude for all comparable features describing energy sources. This scaling must take into account as well the value bounds of all other features.
* To preliminarily study the prediction of price data with a set of simple models, in turn identifying processed features that are more relevant to the prediction.
* To examine relevant configurations of regression algorithms and hyperparameters by means of an extensive grid search, at the same time taking into account possible decompositions with PCA as well as different preprocessing methods.
* To evaluate the performance of the optimum configuration on the dataset employed, and to further predict the given evaluation dataset.
