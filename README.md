# Geocoding  
The repository contains certain lines of code that uses the concept of "Multi-Step Data Analysis" and utilizes Google Maps API to find particular addresses along with the related serialized data to visualize the latter on a map.  


### Workflow  
The python file `geoload.py` is tasked with **creating** a database file *if not already present* (.sqlite in our case), **reading** the names of the colleges from the data file, **fetching** the address and the related serialized data from the network utilizing the Google Maps API or the "Service URL" provided to us as a secondary URL *in case we're not made available with an API KEY* : *py4e-data.dr-chuck.net* and **writing** the latter into the database file.  

`geodump.py` python file can be executed anytime to dump the latitude, longitude and the formatted address of all the addresses' written in our database file. However, the primary task of this file is to write the records in the `where.js` JavaScript file.


#### Database File  
The database we'll be using in this project is SQLite because of the "sqlite3" package already baked in python. Where this database might not be our first choice, SQLite is just right for the amount of data we aim to retrieve, probably more. The **address field** contains the address of the particular college and the **geodata field** contains the related serialized data (JSON in our case) of the particular address.  


#### Data File  
`where.data` is a **data file** which contains a name list of the addresses (names of universities in our case) we aim to mark on the map. This file could also be a database file such as *.sqlite* or *.sql*. This file is the origin of the project's workflow.  


### Visualization  
Finally if we'd want to visualize the colleges on a map, we'd simply run the **where.html** command in the command line which further opens our browser and displays the marks on a map.  
