{
  "info": {
    "name": "Data.gov API Delete Datasets Dataset Badges Badge Kind",
    "_postman_id": "3805e020-e74a-4ef6-93f0-e20147d4cc14",
    "description": "Delete a badge for a given dataset",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "datasets",
      "item": [
        {
          "id": "a0341198-e5f7-4313-9620-5016f52747d6",
          "name": "deleteDatasetsDatasetBadgesBadgeKind",
          "request": {
            "url": {
              "protocol": "http",
              "host": "catalog.data.gov",
              "path": [
                "api",
                "3",
                "datasets/:dataset/badges/:badge_kind/"
              ],
              "variable": [
                {
                  "id": "badge_kind",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "dataset",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Delete a badge for a given dataset"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2d0f3e09-1d7b-4319-bfa9-312602f42019"
            }
          ]
        }
      ]
    }
  ]
}