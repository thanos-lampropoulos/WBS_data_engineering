## Title

data_engineering_Gans

## Description

The background setting for this project is the following, i.e. an e-scooter rental company called Gans wants to optimize scooter placement within the cities it operates and to this end would like to know in advance how the weather will look like as well as when tourists will be arriving.

The code in this project collects the following data for certain predefined cities of interest and stores them in a mySQL schema:

1. population of the city (via webscraping),
2. geographical coordinates of the city (via webscraping),
3. weather forecast for the city (via the openweather API),
4. airport name and ICAO code of the airport(s) serving the city (via the aerodatabox API),
5. inbound flights arriving at the airports serving the city (via the aerodatabox API).

## How to Install and Run the Project

- All functions are written in Python 3 and can be executed in the jupyter notebook provided.

- All dependencies are included in the jupyter notebook (must be imported by executing the respective cell).

- The mySQL code that creates the necessary mySQL schema is also present in the jupyter notebook, but needs to be executed on a local mySQL instance.

- The Python function that generates the mySQL connection string enables communication only with local mySQL instances.

- All code has been ported also to the Google Cloud Platform by changing the Python function that generates the mySQL connection string (not shown here). 

## How to Use the Project

Download the jupyter notebook and run it using Jupyter.

Please note that you will need to add to the provided code your own API keys.

## Known issues

- The webscraping part of this project collects data from Wikipedia. In certain Wikipedia entries, the html element containing the population value also contains additional elements (e.g. hyperlinks). As a result the code as is will not retrieve the population value. 

- All times for inbound flights are given in UTC. Reporting times in the local time zone for each airport has not yet been implemented.

## Credits

This project was created during my participation at the WBS data science bootcamp.

The background setting for this project was set by the instructor.

All code was written independently by me.
