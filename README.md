# demandforecast
change orginal R code 

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
