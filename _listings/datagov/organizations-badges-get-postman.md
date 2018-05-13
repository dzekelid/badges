{
  "info": {
    "name": "Data.gov API Get Organizations Badges",
    "_postman_id": "cf009758-32e4-47c2-a04b-aee156d37212",
    "description": "List all available organization badges and their labels",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "organizations",
      "item": [
        {
          "id": "814989df-4b0a-4628-9c58-e3fcb5aabf43",
          "name": "getOrganizationsBadges",
          "request": {
            "url": "http://catalog.data.gov/api/3/organizations/badges/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all available organization badges and their labels"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fd851aee-0167-4c70-974b-5428acc7334b"
            }
          ]
        }
      ]
    }
  ]
}