# World-Development-Analytics
A mock project I worked on at Skillstorm. Since the actual code was largely cloud-based and I no longer have access to it, this is primarily a mix of documentation and libraries I wrote for the project. This was not for an actual company- but we treated it as if it was.

## [Team Juniper Design Document](https://github.com/rihop6/World-Development-Analytics/blob/main/Team%20Juniper%20Design%20Document.pdf)
This is the main design document for the project. To get the best idea of the project architecture, look here.

## [Data Dictionary](https://github.com/rihop6/World-Development-Analytics/tree/main/Data%20Dictionary)
Data Dictionary is a small library I wrote for Spark that was initially developed during the World Development Analytics project and then used on subsequent projects. It essentially is an abstraction layer that allows you to manage a large number of data sources from separate APIs in a lightweight manner. It has a list of all the APIs you bring in and can enact the same transformation across multiple dataframes built from those APIs. This allows you to very quickly create a pipeline for the Bronze to Silver layer for basic data cleaning tasks.

For example- a data point I dealt with in this project was Country names. Some APIs listed it in their data as 'Nation' some said 'Country' some said 'Country Code'. Using the DataDictionary.renameAll() function, you can rename 'Nation' and 'Country Code' columns to 'Country' in a single line of code. It had other capabilities, like standardizing dates to a specific format or standardizing the data type for specific columns.

This library is not complete. I only implemented features needed for the projects I worked on. Much more could be added to this, and it is missing some key features.
