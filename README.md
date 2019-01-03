# Brewery Map

This simple HTML page reads in brewery names from a google sheet, looks them up using the google maps places library, and then maps them on a google map.

To run this you will need to populate your API_KEY and SHEET_ID.

```
var API_KEY = "API_KEY";
var SHEET_ID = "SHEET_ID";
```

The Google sheet is formatted as below. The first column does not matter and is ignored. The second column is used to extract the states which are appended to the brewery name for searching. Every row after that is a unique brewery.

You can adjust the columns/rows in the API call that is used to fetch the data.

| Total breweries: 5         | Total States: 2      |
|----------------------------|----------------------|
| Wisconsin (3)              | Illinois (2)         |
| Lakefront Brewery          | Revolution Brewery   |
| Milwaukee Brewing Company  | Goose Island Brewing |
| Eagle Park Brewing Company |                      |

## Site

Pretty basic site - the map will occupy 100% of the page. Below the map will be a list of all of the breweries that it mapped. When the map loads there is an overlay of a loading page that show progress as it loads all of the breweries. This can take some time as there are limits to how quickly you can call the google APIs. if you reach a limi the javascript will take a 10 second pause and then resume.

The map will look like the below.

![Brewery Map](images/map.png "Brewery Map")