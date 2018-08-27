{
  "info": {
    "name": "Data.gov API Get Reuses Badges",
    "_postman_id": "ffb08384-5dc1-41e5-9bab-07fc29cb621a",
    "description": "List all available reuse badges and their labels",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "reuses",
      "item": [
        {
          "id": "23809412-0c98-4f86-ad21-5d239dced2ff",
          "name": "getReusesBadges",
          "request": {
            "url": "http://catalog.data.gov/api/3/reuses/badges/",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all available reuse badges and their labels"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dc51a606-b409-4378-9a09-1fba884c6e73"
            }
          ]
        }
      ]
    }
  ]
}