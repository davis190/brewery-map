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
| Wisconsin (3)              | Illinois (2)         |
| Lakefront Brewery          | Revolution Brewery   |
| Milwaukee Brewing Company  | Goose Island Brewing |
| Eagle Park Brewing Company |                      |