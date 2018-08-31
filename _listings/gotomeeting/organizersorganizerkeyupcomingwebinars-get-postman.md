{
  "info": {
    "name": "Go To Webinar Get upcoming webinars",
    "_postman_id": "1bcded03-83d2-4bd3-a9b6-b56181bbb5ea",
    "description": "Returns webinars scheduled for the future for the specified organizer and webinars of other organizers where the specified organizer is a co-organizer.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accounts",
      "item": [
        {
          "id": "ac0b0e74-adfe-4d3b-8c57-6aea952de719",
          "name": "getAllAccountWebinars",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "accounts/:accountKey/webinars"
              ],
              "query": [
                {
                  "key": "fromTime",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "size",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "toTime",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "accountKey",
                  "value": "accountKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the list of webinars for an account within a given date range. __*Page*__ and __*size*__ parameters are optional. Default __*page*__ is 0 and default __*size*__ is 20. For technical reasons, this call cannot be executed from this documentation. Please use the curl command to execute it."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ca4aca6b-cabe-42f8-b794-41e459a3a3f1"
            }
          ]
        }
      ]
    },
    {
      "name": "Organizers",
      "item": [
        {
          "id": "2b86f1a6-a92b-4f3d-8a13-49efd7cd5218",
          "name": "getHistoricalWebinars",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/historicalWebinars"
              ],
              "query": [
                {
                  "key": "fromTime",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "toTime",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "organizerKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns details for completed webinars for the specified organizer and completed webinars of other organizers where the specified organizer is a co-organizer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8bbd5c44-ea9a-40c5-ae2f-febb13888292"
            }
          ]
        },
        {
          "id": "45c034e3-3b5c-4061-945e-69d67bcd8684",
          "name": "getOrganizerSessions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/sessions"
              ],
              "query": [
                {
                  "key": "fromTime",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "toTime",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "organizerKey",
                  "value": "organizerKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve all completed sessions of all the webinars of a given organizer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "911c6498-2da3-4d06-ac1e-0a19dcc78a54"
            }
          ]
        },
        {
          "id": "ecbe9f35-aad2-4dc4-b76e-1158e183dc01",
          "name": "getUpcomingWebinars",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2W",
                "rest",
                "organizers/:organizerKey/upcomingWebinars"
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
                  "id": "organizerKey",
                  "value": "organizerKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns webinars scheduled for the future for the specified organizer and webinars of other organizers where the specified organizer is a co-organizer."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ff776345-e33a-4505-813d-22464a337cee"
            }
          ]
        }
      ]
    }
  ]
}