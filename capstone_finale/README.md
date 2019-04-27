# Assistance with choosing a location where to move to

__This project was created as a part of a final exam for Coursera's course "IBM Data Science Professional Certificate".__

### Introduction 
 I've spent a past year living in Warsaw, Poland and in a couple of months I'll be moving back to Prague, Czech Republic. Which brings the question of picking the right location where to move to. So I'm using this opportunity and creating a project that will help me with this. But I will make it so that it will also be useful for other people who might need some basic overview of areas in Prague.

 There are many things to consider when you are relocating yourself. But basically it all leads to finding an area where real estate renting values are acceptable and at the same time you can find there all the right venues (groceries, pubs, cinemas..) and easily accessible public transportation.

### Data

#### Locations
 I will start with collecting geo-locational information of 57 city districts, which will help me build choropleth map. I have found a geojson file which has all the necessary geometry values of polygons based on locational data.[1] This will be used as a main map on which everything will be build. Then I will use Nominatim libraries to get locations of each cadastral district, because those which already exists are corrupted or incomplete. This will help me to place clustered data on the right locations on the map.

#### Venues
 I'll use Foursquare API [2] to get a selection of venues in each cadastral district based on previous geolocation data, which will be later on processed, generalized and summarized so it will be easier to use for clusters.

#### Rents and extras
 Not all the interesting data can be found with FourSquare. To choose the right location I need to know an estimation of rents and I'm also curious about density of transportation [3] and of recycling/sorting waste [4] in all areas. To collect data about average rents in Prague I've found two separate web pages of several different real estate broker businesses who were collaborating on these data sets.[5]

 There might be some other extra data necessary, which will be mentioned in the notebook.

### Goal
 The aim of this project is to clean, sort and then merge all the data into one dataframe, that will give us all the necessary information, which will be displayed on the main map so when someone is trying to pick one of neighborhoods he can lean on visualized rents and grouped categories. And so it might help him narrow down all the choices.

### Requirements
 - Clone this repo to your computer.
 - Python 3
 - JupyterNotebook
 - Install the requirements using pip install -r requirements.txt. 
 - Create a file called private.py in this folder.
     - Add values called API_ID = "" and API_KEY = "" with your Foursquare credentials.



### References:

[1] http://opendata.praha.eu/dataset/ipr-mestske_casti

[2] https://foursquare.com/

[3] http://opendata.iprpraha.cz/CUR/DOP/DOP_PID_ZASTAVKY_B/WGS_84/DOP_PID_ZASTAVKY_B.json

[4] http://opendata.iprpraha.cz/CUR/ZPK/ZPK_O_Kont_TOitem_b/S_JTSK/ZPK_O_Kont_TOitem_b.json

[5] https://realitymix.centrum.cz/statistika-nemovitosti/byty-pronajem-prumerna-cena-pronajmu-1m2-mesic.html http://www.cenovamapa.eu/

