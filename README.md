# AWNPy

AWNPy is a small pure python wrapper around the AgWeatherNet (https://weather.wsu.edu/) API. It is useful for retrieving meteorological data at AWN weather stations. This project was created with code from MesoPy (https://github.com/mesowx/MesoPy).

**Before using AWNPy, you will need to register with AgWeatherNet and obtain permission to access the API** Once you have permission you will need your AgWeatherNet username and password: 
```
m = AWN(username='YOUR USERNAME', password='YOUR PASSWORD')
```
## Installation

1. Download the source folder and place `AWNPy.py` into your working directory

## Usage
#### Retrieving data:
You can request different types of observations by simply creating a Meso object and calling a function:

```
from AWNPy import AWN
m = AWN(username='YOUR USERNAME', password='YOUR PASSWORD')
stationdata = m.stationdata(STATION_ID='330092', START=datetime(2020,5,1,0,0), END=datetime(2020,5,2,0,0))
```

#### Function List:
1. `metadata()` - Retrieve a list of station metadata based on search parameters.
2. `stationdata()` - Get station data for a specified station (or all stations) within a time range. 
3. `stationlocator()` - Find stations using a specified lat/lon. 

## Documentation
Each function is **well** documented in the docstrings. In an interactive interpreter, simply type `help(SOME_FUNC)` or in your code, type `SOME_FUNC.__doc__` 

## Support and Credits
Most code from AWNPy is based on MesoPy. The [MesoWest group] is led by  Dr. John Horel at the University of Utah. Additional facilities were provided by the [Western Region] of the National Weather Service. AWNPy is built by Joe Zagrodnik at WSU AgWeatherNet and the API is maintained by Sean Hill. 
