# demandforecast

Azure ML Studio, https://studio.azureml.net/
New experiment, search template by "forecast"
Select "Forecasting Model for Microsoft Dynamics 365 Business Central"

Change orginal R code from

#Number of forecast predictions

horizon <- as.numeric(dataset2$HORIZON)

to

#Number of forecast predictions

if(is.null(dataset2$HORIZON)) { 
horizon <- 3;
} else {
horizon <- as.numeric(dataset2$HORIZON)
}

This will default the forecasting horizon to 3.
