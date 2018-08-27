{
  "info": {
    "name": "Data.gov API Delete Organizations Org Badges Badge Kind",
    "_postman_id": "d8e4b919-8da3-4826-85c1-dd8cd63505ed",
    "description": "Delete a badge for a given organization",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "organizations",
      "item": [
        {
          "id": "5e520ded-afe7-4f62-9a13-7d255cbfcc9a",
          "name": "deleteOrganizationsOrgBadgesBadgeKind",
          "request": {
            "url": {
              "protocol": "http",
              "host": "catalog.data.gov",
              "path": [
                "api",
                "3",
                "organizations/:org/badges/:badge_kind/"
              ],
              "variable": [
                {
                  "id": "badge_kind",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "org",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a badge for a given organization"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e33db3cc-6a59-4d6c-9c46-af4a129bb21d"
            }
          ]
        }
      ]
    }
  ]
}