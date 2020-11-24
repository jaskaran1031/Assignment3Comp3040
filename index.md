## Manitoba towns' info API
This API provides information of each city/town in Manitoba, including population, the number of hospitals, the number of police stations, the number of museums, and the number of universities/colleges. 

### API documentation

#### Endpoints and Parameters

There are two endpoints for this API, both using a `GET` request.

#### `/documentation`
- parameter:    

**town**  (string), the name of the town in Manitoba. Required.
- sample request: ```https://www.manitobatowninfo.com/documentation?town=winnipeg``` 
    - response: 
    ```
    {
        "results" :
        {
            "town" : "Winnipeg",
            "population" : "749,534",
            "hospitals" : "9",
            "police-stations": "4"
            "museums" : "40",
            "universities/colleges" : "8",
        },
        "status":"OK"
    }
    ```
- sample request: ```https://www.manitobatowninfo.com/documentation?town=wiinipegg```   
    - response:
    ```
    {
        "results" : ""
        "status":"ERROR"
    }
    ```

#### `/population`
- parameters:  

**comparison** (string), the value must be one of `"less"`, `"more"`, or `"equal"`. Required.  
**size** (int), the number of people in a town. Required.
- sample request: ```https://www.manitobatowninfo.com/population?comparison=less&size=1000```
    - response:
```
    {
        "results" :
        {
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
        }    
        "status":""OK
    }
```
