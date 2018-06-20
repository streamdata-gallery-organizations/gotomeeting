{
  "info": {
    "name": "SCIM Get User Schema",
    "_postman_id": "739c65f8-393d-420c-a4bb-a865f7f21c6c",
    "description": "Queries the user schema. The user schema is defined in SCIM Core Schema (http://www.simplecloud.info/specs/draft-scim-core-schema-01.html#resource-schema).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Schemas",
      "item": [
        {
          "id": "1af4b5a4-f2ed-4ed8-9291-711397320d30",
          "name": "getUserSchema",
          "request": {
            "url": "http://api.citrixonline.com/identity/v1/Schemas/Users?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Queries the user schema. The user schema is defined in SCIM Core Schema (http://www.simplecloud.info/specs/draft-scim-core-schema-01.html#resource-schema)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5c41168a-b050-4ad6-91bf-4f89f6ce7182"
            }
          ]
        }
      ]
    }
  ]
}