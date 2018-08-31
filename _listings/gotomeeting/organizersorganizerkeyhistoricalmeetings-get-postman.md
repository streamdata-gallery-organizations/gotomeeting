{
  "info": {
    "name": "Go To Meeting Get historical meetings by organizer",
    "_postman_id": "e64db773-6b3a-49e3-8b65-e46cca84fa70",
    "description": "Get historical meetings for the specified organizer that started within the specified date/time range. Remark: Meetings which are still ongoing at the time of the request are NOT contained in the result array.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Groups",
      "item": [
        {
          "id": "fccec6b3-6d7f-4331-9790-bba2abdb3b5f",
          "name": "get-historical-meetings-for-the-specified-group-that-started-within-the-specified-datetime-range--th",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2M",
                "rest",
                "groups/:groupKey/historicalMeetings"
              ],
              "query": [
                {
                  "key": "endDate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startDate",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "groupKey",
                  "value": "groupKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get historical meetings for the specified group that started within the specified date/time range. This API call is only available to users with the admin role. This API call is restricted to groups with a maximum of 50 organizers. Remark: Meetings which are still ongoing at the time of the request are NOT contained in the result array."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e96f6993-11f1-48c1-8826-2d4ea56ca5d8"
            }
          ]
        }
      ]
    },
    {
      "name": "HistoricalMeetings",
      "item": [
        {
          "id": "52a5605b-c918-4ed4-bd2a-94796192c610",
          "name": "get-historical-meetings-for-the-currently-authenticated-organizer-that-started-within-the-specified-",
          "request": {
            "url": "http://api.citrixonline.com/G2M/rest/historicalMeetings?endDate=%7B%7D&No Name=%7B%7D&startDate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get historical meetings for the currently authenticated organizer that started within the specified date/time range. Remark: Meetings which are still ongoing at the time of the request are NOT contained in the result array."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a78825f9-2959-47e9-8f91-a88416ab9756"
            }
          ]
        }
      ]
    },
    {
      "name": "Organizers",
      "item": [
        {
          "id": "6381fda9-02da-4e51-8507-0ca2f0677d90",
          "name": "get-historical-meetings-for-the-specified-organizer-that-started-within-the-specified-datetime-range",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2M",
                "rest",
                "organizers/:organizerKey/historicalMeetings"
              ],
              "query": [
                {
                  "key": "endDate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startDate",
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
            "description": "Get historical meetings for the specified organizer that started within the specified date/time range. Remark: Meetings which are still ongoing at the time of the request are NOT contained in the result array."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "265e4bee-ee5e-45d1-b358-9d2732463ac8"
            }
          ]
        }
      ]
    }
  ]
}