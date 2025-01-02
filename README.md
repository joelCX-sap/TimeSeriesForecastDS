# TimeSeriesForecastDS
Time Series forecast with Datasphere and ML PAL

Use case
We have chosen to go through a time-series forecasting example, as this is an extremely common requirement for the most diverse projects. Many standard applications from SAP already have time-series forecasting built in, such as SAP Analytics Cloud or SAP Integrated Business Planning. If you have a requirement, that goes beyond a standard application, you can leverage the SAP Business Technology Platform (BTP), ie SAP Datasphere and its embedded SAP HANA Cloud. Alternatively you can also work with a stand-alone SAP HANA Cloud instead, then please see this blog. 

In our case now we would like to forecast how many nights foreign tourists or business travellers will spend in Switzerland in the coming months. We are interested in the total numbers, but we also want to know how many nights different nationalities will spend in the country. 

Such forecasts of overnight stays can be useful for many purposes, for instance to help decide where to spend a Marketing budget. It can also help the hotel industry to have the right number of staff (and languages) working through the year.

These might just be examples we invented ourselves, based on data that is publicly available (thanks to the opendata.swiss portal!), but such time-series forecasts are used extremely often in the business world. We have used time-series forecasting in many diverse projects, from forecasting the Net Working Capital for Treasury departments to solar power production at a utilities company. 

All these use cases have in common, that in such a BTP project an expert (you!) creates a forecast that is then shared with the business users, who might not want to know all technical details of how the forecasts were created.

 

Architecture / prerequisites
To follow this blog's instructions, you need to have access to:

A productive instance of SAP Datasphere. Note that the free-tier or free-trial options of SAP Datasphere do not suffice, since these have only 2 virtual CPUs. The embedded Machine however requires the Script Server to be activated, which requires 3 virtual CPUs.
A Python environment. We explain how to set up miniconda, but if you already have an existing Python installation, you should be able to use this as well. Of course, you could also use the Business Application Studio on our Business Technology Platform. 
It helps if you have a bit of Python or scripting experience. But we hope this blog can also be a good entry point for someone who is just starting out with Python.
Motivation to get to know SAP HANA's Predictive Analysis Library. 
The overall architecture for this implementation is centered around SAP Datasphere.
