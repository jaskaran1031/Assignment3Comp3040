## Manitoba towns' info API
This API provides information of each city/town in Manitoba, including population, the number of hospitals, the number of police stations, the number of museums, and the number of universities/colleges. 

### API documentation

#### Endpoints and Parameters

There are two endpoints for this API using `GET` request.

#### `/documentation`
- parameter: **town**  (string), the name of the town in Manitoba. Required.
- sample request: ```https://www.manitobatowninfo.com/documentation?town=winnipeg```
- response: 
    ```
    {
        "results" :
        {
            "town" : "Winnipeg",
            "population" : "70,000",
            "hospitals" : "10",
            "police-stations": "20"
            "museums" : "8",
            "universities/colleges" : "3",
        },
        "status":"OK"
    }
    ```

#### `/population`
- parameters: **comparison** (string), the value must be one of `"less"`, `"more"`, or `"equal"`. Required.  
**size** (int), the number of people in a town. Required.
- sample request: ```https://www.manitobatowninfo.com/polulation?comparison=less&size=1000```
- response:
```
    {
        "results" :
        {
            "town" : "Melita",
            "population" : "800",
            "hospitals" : "1",
            "police-stations": "1"
            "museums" : "0",
            "universities/colleges" : "0",
        },
        {
            "town" : "Oak Bluff",
            "population" : "880",
            "hospitals" : "1",
            "police-stations": "1"
            "museums" : "0",
            "universities/colleges" : "0",
        },
        {
            "town" : "Teulon",
            "population" : "900",
            "hospitals" : "1",
            "police-stations": "1"
            "museums" : "0",
            "universities/colleges" : "0",
        },
        "status":""OK
    }
```
