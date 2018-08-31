{
  "info": {
    "name": "Go To Meeting DEPRECATED: Get historical meetings by group",
    "_postman_id": "8ef6157b-b8aa-47e0-9405-58cdcc2a3a4e",
    "description": "DEPRECATED: Please use the new API calls 'Get historical meetings by group' and 'Get upcoming meetings by group'. Get meetings for a specified group. Additional filters can be used to view only meetings within a specified date range. This API call is only available to users with the admin role.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Groups",
      "item": [
        {
          "id": "2b371e3a-f4b9-479e-929c-0f821986094c",
          "name": "list-all-groups-for-an-account--this-api-call-is-only-available-to-users-with-the-admin-role-",
          "request": {
            "url": "http://api.citrixonline.com/G2M/rest/groups?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all groups for an account. This API call is only available to users with the admin role."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "066208ec-800e-4d90-8452-62d477ae4fb2"
            }
          ]
        },
        {
          "id": "aa64d71d-1ee1-44e2-a339-130b6ee36e9b",
          "name": "returns-all-attendees-for-all-meetings-within-specified-date-range-held-by-organizers-within-the-spe",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2M",
                "rest",
                "groups/:groupKey/attendees"
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
            "description": "Returns all attendees for all meetings within specified date range held by organizers within the specified group. This API call is only available to users with the admin role. This API call can be used only for groups with maximum 50 organizers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0622d67d-8899-42df-94a7-ec1f1d0d5d3c"
            }
          ]
        },
        {
          "id": "fd209f49-6dd6-4b34-a336-1ac52632b0df",
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
              "id": "17114947-1052-4e03-9072-b90a2fe7cbf4"
            }
          ]
        },
        {
          "id": "b9f531f0-12e8-4e9b-816d-728fbff83fee",
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
              "id": "442eee5b-0cf3-4c69-ab92-c81b677817f8"
            }
          ]
        }
      ]
    }
  ]
}