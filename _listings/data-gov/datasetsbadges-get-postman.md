{
  "info": {
    "name": "Data.gov API Get Datasets Badges",
    "_postman_id": "f3c23d6d-0902-41b7-a7cb-66ad27325d73",
    "description": "List all available dataset badges and their labels",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "datasets",
      "item": [
        {
          "id": "02a9456c-e9f0-434b-90bd-b09d1a0597e6",
          "name": "getDatasetsBadges",
          "request": {
            "url": "http://catalog.data.gov/api/3/datasets/badges/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all available dataset badges and their labels"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ad6c7f57-edc2-4453-83b2-901d9c69023d"
            }
          ]
        }
      ]
    }
  ]
}