This is for assginment 3

- This API provides information of each city/ town in Manitoba, including population, the number of hospitals, the number of police stations, the number of museums
- www.manitobainfo.com
- endpoint:   
https://manitobainfo.com/town/all   
https://manitobainfo.com/town/random   
https://manitobainfo.com/town/winnipeg   

- sample requests: https://manitobainfo.com/town/winnipeg   


- parameters: cityName(String), required
- response: 

```
 {
    "results" :
    {
        "town" : "winnipeg",
        "population" : "700,00",
        "hospitals" : "10",
        "museums" : "8",
        "universities/colleges" : 3,
    }
 }
 ```
