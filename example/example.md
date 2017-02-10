#Usage Example

##[Yangon Bus Service Public Data](https://data.opendevelopmentmekong.net/dataset/yangon-bus-service-public-data?type=dataset)

Bus stops by services (Resource_id = **ce59387c-2020-40c3-aa3d-e9aac55fca3a**)

####Get All Bus Stops

https://data.opendevelopmentmekong.net/api/action/datastore_search?resource_id=ce59387c-2020-40c3-aa3d-e9aac55fca3a

####Get Bus Stops by Service

https://data.opendevelopmentmekong.net/api/action/datastore_search?resource_id=ce59387c-2020-40c3-aa3d-e9aac55fca3a&filters={"service_name":1}

####Get Services by Bus Stops 

https://data.opendevelopmentmekong.net/api/action/datastore_search?resource_id=ce59387c-2020-40c3-aa3d-e9aac55fca3a&filters={"bus_stop_id":2011}

####Serach by Bus Stops Name

https://data.opendevelopmentmekong.net/api/action/datastore_search?resource_id=ce59387c-2020-40c3-aa3d-e9aac55fca3a&q={"name_mm":"အောင်ချမ်းသာ"}

####Full Text Search

https://data.opendevelopmentmekong.net/api/action/datastore_search?resource_id=ce59387c-2020-40c3-aa3d-e9aac55fca3a&q=အောင်ချမ်းသာ

######Response

```json
{
    "help": "https://data.opendevelopmentmekong.net/api/3/action/help_show?name=datastore_search",
    "success": true,
    "result": {
        "resource_id": "ce59387c-2020-40c3-aa3d-e9aac55fca3a",
        "fields": [
            {
                "type": "int4",
                "id": "_id"
            },
            {
                "type": "numeric",
                "id": "service_name"
            },
            ...
         ],
        "records": [
          {
            "name_mm": "လှည်းကူးဈေး",
            "township_mm": "လှည်းကူး",
            "sequence": "1",
            "service_name": "1",
            "road_en": "No. 1 Main Road",
            "bus_stop_id": "2011",
            "lat": "17.096823",
            "name_en": "Hlegu Zay",
            "_id": 1,
            "road_mm": "အမှတ်(၁)လမ်းမ",
            "lng": "96.219456",
            "township_en": "Hlegu"
          },
          {
            "name_mm": "သဉ္ဇာဦး",
            "township_mm": "လှည်းကူး",
            "sequence": "2",
            "service_name": "1",
            "road_en": "No. 1 Main Road",
            "bus_stop_id": "2013",
            "lat": "17.098546",
            "name_en": "Tin Zar Oo",
            "_id": 2,
            "road_mm": "အမှတ်(၁)လမ်းမ",
            "lng": "96.223276",
            "township_en": "Hlegu"
          },
          ...
        ],
        "_links": {
            "start": "/api/3/action/datastore_search?resource_id=ce59387c-2020-40c3-aa3d-e9aac55fca3a",
            "next": "/api/3/action/datastore_search?offset=100&resource_id=ce59387c-2020-40c3-aa3d-e9aac55fca3a"
        },
        "total": 4711
	}
}
```

Get Postman collection for this example : https://www.getpostman.com/collections/74ac198c2fb7d99530f3