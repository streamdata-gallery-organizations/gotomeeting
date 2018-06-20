{
  "info": {
    "name": "Go To Assist Seeit Create a GoToAssist Seeit session",
    "_postman_id": "2db9bfe6-881a-466a-9d34-454a5309dadc",
    "description": "This endpoint allows you to create a GoToAssist Seeit session. The session logically exists but is not started until you open the returned startUrl in a suitable browser.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Sessions",
      "item": [
        {
          "id": "de74484d-6666-4d84-a876-71812df80080",
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
              "id": "f419c885-e1fe-4a4f-b247-4cd7344b4020"
            }
          ]
        },
        {
          "id": "a995d4f3-3769-4f92-9b54-c7205dff31ac",
          "name": "sessions.post",
          "request": {
            "url": "http://api.citrixonline.com/seeit/v1/sessions?No Name=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint allows you to create a GoToAssist Seeit session. The session logically exists but is not started until you open the returned startUrl in a suitable browser."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aca7d839-c8a8-4234-9bb8-a6b57a113ae2"
            }
          ]
        }
      ]
    }
  ]
}