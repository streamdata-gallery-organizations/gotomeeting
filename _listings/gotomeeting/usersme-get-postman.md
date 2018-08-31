{
  "info": {
    "name": "SCIM Get Current User",
    "_postman_id": "b3a662f6-2d4b-4ab5-8bab-90a9116f890d",
    "description": "Queries the identity of the current authenticated user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Users",
      "item": [
        {
          "id": "ad6629cb-5b5d-46eb-9e0a-b5efda0e7fac",
          "name": "getMe",
          "request": {
            "url": "http://api.citrixonline.com/identity/v1/Users/me?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Queries the identity of the current authenticated user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ff566d37-0ac3-4c5b-96ff-0ec7e2e8f226"
            }
          ]
        }
      ]
    }
  ]
}