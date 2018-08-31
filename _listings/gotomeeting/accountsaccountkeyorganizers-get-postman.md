{
  "info": {
    "name": "Go To Training DEPRECATED: Get Organizers",
    "_postman_id": "9688f43c-c8b8-42c1-bc0b-04aafd5e56af",
    "description": "DEPRECATED: Please use the Admin API call 'Get all users' instead. For details see https://developer.citrixonline.com/get-all-users.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accounts",
      "item": [
        {
          "id": "87b13533-e8ac-4dc8-afd4-00889e09a478",
          "name": "getAllOrganisers",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2T",
                "rest",
                "accounts/:accountKey/organizers"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "accountKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "DEPRECATED: Please use the Admin API call 'Get all users' instead. For details see https://developer.citrixonline.com/get-all-users."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d0f0e6e8-741f-4f3f-a640-4df8bc357540"
            }
          ]
        }
      ]
    }
  ]
}