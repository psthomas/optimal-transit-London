## optimal-transit-London


This project uses a genetic algorithm to optimize a trip through London using Google Transit diretions. The final map can be seen [here](http://psthomas.github.io/optimal-transit-London/).

The original [genetic algorithm](https://github.com/rhiever/Data-Analysis-and-Machine-Learning-Projects/tree/master/optimal-road-trip)
was developed by Randall Olson https://github.com/rhiever, who blogged about it [here](http://www.randalolson.com/2015/03/08/computing-the-optimal-road-trip-across-the-u-s/).  This version modifies the original by switching the travel mode to Transit, specifying a departure time, and altering the HTML and JavaScript to focus on London.  

See [here](https://github.com/rhiever/Data-Analysis-and-Machine-Learning-Projects) for the licence and usage terms.   

In order to run this code, you need a version of Python (2.5+) installed, along with
the pandas and googlemaps libraries.  Pip works best for these installations.  

You also need to generate an API Key for the googlemaps API, and paste it
into the appropriate location in line 19 of [OptimalRoadTripHtmlSaveAndDisplay.py](https://github.com/psthomas/optimal-road-trip-WI/blob/master/OptimalRoadTripHtmlSaveAndDisplay.py).  Directions for generating a key can be found [here](https://github.com/googlemaps/google-maps-services-python#api-keys).  Make sure you also 
enable the Google Distance Matrix API on your developer account, otherwise
your requests will be rejected.  

If you add new locations, or create an entirely transit trip, make sure to 
delete [my-waypoints-dist-dur.tsv](https://github.com/psthomas/optimal-transit-London/blob/master/my-waypoints-dist-dur.tsv) from your local file before running the 
code.  The python code searches for this file, and if it doesn't find it, 
accesses google maps for the route distances and outputs a new .tsv file
afterwards.  

A more detailed writeup of how the genetic algorithm works is available [here](https://github.com/psthomas/optimal-road-trip-WI/blob/master/Computing%20the%20optimal%20road%20trip%20across%20the%20U.S..ipynb).
