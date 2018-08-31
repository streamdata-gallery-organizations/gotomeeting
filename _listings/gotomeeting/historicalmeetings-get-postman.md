{
  "info": {
    "name": "Go To Meeting Get historical meetings",
    "_postman_id": "8fde8f9f-4628-407c-9f2f-3b527e63d2f8",
    "description": "Get historical meetings for the currently authenticated organizer that started within the specified date/time range. Remark: Meetings which are still ongoing at the time of the request are NOT contained in the result array.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Groups",
      "item": [
        {
          "id": "c0960959-a198-4be4-8429-6c4c9a183713",
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
              "id": "46860ee5-0ff6-4ff4-aa66-70b0e6fdb6cd"
            }
          ]
        }
      ]
    },
    {
      "name": "HistoricalMeetings",
      "item": [
        {
          "id": "4a8a59a9-cde3-49e4-8557-a8332490264b",
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
              "id": "f9def9d3-8242-4780-819a-54e00dbec4da"
            }
          ]
        }
      ]
    }
  ]
}