{
  "info": {
    "name": "Go To Assist Seeit Get details for multiple GoToAssist Seeit sessions",
    "_postman_id": "cf37afe0-dadf-413f-adc4-09af49080a51",
    "description": "<p>This endpoint allows you to get all relevant details for mulitple GoToAssist Seeit sessions. Session details are available for 90 days.</p></p>The fields and their values in the response depend on session status and the time elapsed since session end; e.g. session data like snapshots or the session recording are only available for 72 hours.</p><p>The results will be paged, with paging customizable to match your requirements.</p>",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Sessions",
      "item": [
        {
          "id": "d7dd0bbd-fd88-4d7c-8c3b-863a39452e27",
          "name": "sessions.get",
          "request": {
            "url": "http://api.citrixonline.com/seeit/v1/sessions?endTime=%7B%7D&No Name=%7B%7D&page=%7B%7D&size=%7B%7D&sort=%7B%7D&startTime=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "<p>This endpoint allows you to get all relevant details for mulitple GoToAssist Seeit sessions. Session details are available for 90 days.</p></p>The fields and their values in the response depend on session status and the time elapsed since session end; e.g. session data like snapshots or the session recording are only available for 72 hours.</p><p>The results will be paged, with paging customizable to match your requirements.</p>"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "66f11161-0bf6-4ab8-a937-84be484168c3"
            }
          ]
        }
      ]
    }
  ]
}