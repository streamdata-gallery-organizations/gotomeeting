{
  "info": {
    "name": "SCIM Get Groups",
    "_postman_id": "23a8c286-fa17-45e6-86fd-bff97cc58a7d",
    "description": "Queries multiple group identities in the organization domain. Filtering, sorting and pagination are available. This call requires the role ROLE_ORG_READ.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Groups",
      "item": [
        {
          "id": "75cf6054-12e8-4c4d-8ae6-ef4dbd0419c9",
          "name": "getGroups",
          "request": {
            "url": "http://api.citrixonline.com/identity/v1/Groups?filter=%7B%7D&No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Queries multiple group identities in the organization domain. Filtering, sorting and pagination are available. This call requires the role ROLE_ORG_READ."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b5a0edee-2416-434f-b419-80fc6f3300ca"
            }
          ]
        }
      ]
    }
  ]
}