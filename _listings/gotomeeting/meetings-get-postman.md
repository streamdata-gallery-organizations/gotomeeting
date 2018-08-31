{
  "info": {
    "name": "Go To Meeting DEPRECATED: Get historical meetings",
    "_postman_id": "48d76578-35e9-4783-89cd-e1e88e4bc57e",
    "description": "DEPRECATED: Please use the new API calls 'Get historical meetings' and 'Get upcoming meetings'.  Gets historical meetings for the current authenticated organizer. Requires date range for filtering results to only meetings within specified dates. History searches will contain the parameter 'meetingInstanceKey' which is used in conjunction with the call 'Get Attendees by Meeting' to get attendee information for a past meeting.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Groups",
      "item": [
        {
          "id": "c25f3722-4fda-4c97-89fc-71898255f24d",
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
              "id": "8d972c99-d61f-4c3d-96d2-f7fda5c1fdf6"
            }
          ]
        },
        {
          "id": "ef051e7e-91ba-4dfb-9a60-aa93a80219d4",
          "name": "deprecated-please-use-the-new-api-calls-get-historical-meetings-by-group-and-get-upcoming-meetings-b",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2M",
                "rest",
                "groups/:groupKey/meetings"
              ],
              "query": [
                {
                  "key": "endDate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "history",
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
            "description": "DEPRECATED: Please use the new API calls 'Get historical meetings by group' and 'Get upcoming meetings by group'. Get meetings for a specified group. Additional filters can be used to view only meetings within a specified date range. This API call is only available to users with the admin role."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ef55bb90-395a-4305-bf09-84c9b18bde5f"
            }
          ]
        },
        {
          "id": "9966a7d7-cffd-4b36-8ba3-491637785ebb",
          "name": "get-upcoming-meetings-for-a-specified-group--this-api-call-is-only-available-to-users-with-the-admin",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2M",
                "rest",
                "groups/:groupKey/upcomingMeetings"
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
            "description": "Get upcoming meetings for a specified group. This API call is only available to users with the admin role. This API call can be used only for groups with maximum 50 organizers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9309e2ba-cb5d-490d-933b-1a5a5dcae1a8"
            }
          ]
        }
      ]
    },
    {
      "name": "HistoricalMeetings",
      "item": [
        {
          "id": "2ab2e1b6-8168-4b23-b4b8-77b61cca4951",
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
              "id": "fc3ef9c4-baf5-4143-9bd8-b84890cd7252"
            }
          ]
        }
      ]
    },
    {
      "name": "Meetings",
      "item": [
        {
          "id": "7b6b8188-983c-4a0b-ba83-b5b709fbba38",
          "name": "deprecated-please-use-the-new-api-calls-get-historical-meetings-and-get-upcoming-meetings---gets-his",
          "request": {
            "url": "http://api.citrixonline.com/G2M/rest/meetings?endDate=%7B%7D&history=%7B%7D&No Name=%7B%7D&startDate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "DEPRECATED: Please use the new API calls 'Get historical meetings' and 'Get upcoming meetings'.  Gets historical meetings for the current authenticated organizer. Requires date range for filtering results to only meetings within specified dates. History searches will contain the parameter 'meetingInstanceKey' which is used in conjunction with the call 'Get Attendees by Meeting' to get attendee information for a past meeting."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3ae6a209-f635-4aff-b7e8-6f2fddf2e9d8"
            }
          ]
        }
      ]
    }
  ]
}