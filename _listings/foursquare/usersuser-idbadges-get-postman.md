{
  "info": {
    "name": "Foursquare Get Users Badges",
    "_postman_id": "d94eeebe-64cc-4564-abdc-c55d514f58e9",
    "description": "users/search (POST)",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Users",
      "item": [
        {
          "id": "fb5ee50a-d89c-413d-b627-7357b75caaed",
          "name": "userssearch-post",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.foursquare.com",
              "path": [
                "v2",
                "users/:USER_ID/badges"
              ],
              "query": [
                {
                  "key": "v",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "USER_ID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "users/search (POST)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "73f86de0-8384-46b3-a17c-2bdb37c6ce96"
            }
          ]
        }
      ]
    }
  ]
}