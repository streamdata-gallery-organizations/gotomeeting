{
  "info": {
    "name": "Go To Meeting Get attendees by group",
    "_postman_id": "eedb7fe3-4446-4f16-9f97-428a61b916cc",
    "description": "Returns all attendees for all meetings within specified date range held by organizers within the specified group. This API call is only available to users with the admin role. This API call can be used only for groups with maximum 50 organizers.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Groups",
      "item": [
        {
          "id": "9214f688-01f5-46e7-a9d3-2b2dcf3f196f",
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
              "id": "d3d93e06-2c89-4d15-b6f1-5096dbb94a54"
            }
          ]
        },
        {
          "id": "4b589e67-d3a9-430d-b957-1085c6af74b8",
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
              "id": "11923459-40b5-4adc-b8cc-4da7fa216854"
            }
          ]
        }
      ]
    }
  ]
}