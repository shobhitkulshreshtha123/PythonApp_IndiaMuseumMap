# PythonApp_IndiaMuseumMap
This simple app created on Python allows users to locate Museums of India. It uses Pandas, Numpy, Folium and Geopy libraries.

Datasource used for this app was extracted from Wikipedia: https://en.wikipedia.org/wiki/List_of_museums_in_India. The list of museums available on this link were 'as it is' copied and pasted in accompanying Excel Sheet. When the app is run, this excel sheet is loaded in a Pandas dataframe in variable called museum_list. Address column is created in this dataframe using name, city and state columns. This address column will be used later to search for the museum latitude and longitude.

We iterate through our museum list and search for geocode (Latitude and Logitude) using Nominatim available in Geopy library. If the geocodes are found, they are added in my_data_list.

We use Folium to create a map and add markers based on geocodes available in my_data_list. These markers, when hovered over, displays a shoutout on museum name and state name. When clicked, these markers return the address of museum.

This map gets saved in local machine as html using mapname.save('name.html') code at the end.

This app can be handy and if integrated with a web scraper for real time automatic updates. 



