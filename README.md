# Propane_vs_heatpump_model
In Ennis MT, my family has a large pole barn style shop. My dad is considering adding heat to the shop in order to keep it a constant 50 degrees. This project is supposed to help analyze the different appraoches in achieving this, by either adding a propane heat source or something else entirely (maybe a heat pump?!)

The first jupyter notebook file is a model that estimates the heat cost comparison between a conventional propane ceiling heater and a heat pump. This model takes a "heating hours" approach where it is assumed that the amount that either a furnace or heatpump will run is depenednet on the amount of time the outside weather is colder than 50 degrees. 

Consequently, the first chunk of the model is spent estimating the # of 'heating hours' that will be needed. For this model, the Ennis MT temp data from 2016 was used and was pulled using SQL from BigQuery.

From there, differing estimates on hour much within one heating hours, a given heater will be on was used to calculate the number of BTU's a given heater would have to use. 

BTUs were then converted into the given heater's energy unit (gallons of propane vs kwH) and an average price estimate was assigned. From there simple calculations were used to estimate the cost of each heater option for a given year.

In this model, it is estimated that a heat pump will prove less expensive over time because it is so efficient. However that is quite depenent on the price of electricity which may increase in the winter and will require a high upfront investment. 

Overall I think this model is a good foundation for future analysis and can be easily retofitted and advanced for other needs.
