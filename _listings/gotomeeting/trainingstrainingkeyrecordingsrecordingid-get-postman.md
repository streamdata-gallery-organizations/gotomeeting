{
  "info": {
    "name": "Go To Training Get Download for Online Recordings",
    "_postman_id": "ad308173-5cf4-4df7-82e8-c6b715ec25b1",
    "description": "This call provides the download for the given recording by returning a 302 redirect to the original file.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Trainings",
      "item": [
        {
          "id": "6f9191ff-7984-453b-84cc-94121a19e7b9",
          "name": "getRecordingsForTraining",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2T",
                "rest",
                "trainings/:trainingKey/recordings"
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
                  "id": "trainingKey",
                  "value": "trainingKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This call retrieves information on all online recordings for a given training. If there are none, it returns an empty list."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ba5eeaf1-5daf-43b5-b451-776f1117d6b2"
            }
          ]
        },
        {
          "id": "b9173d5e-101c-4efd-84c2-668ed62c5746",
          "name": "getRecordingDownloadById",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2T",
                "rest",
                "trainings/:trainingKey/recordings/:recordingId"
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
                  "id": "recordingId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "trainingKey",
                  "value": "trainingKey",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This call provides the download for the given recording by returning a 302 redirect to the original file."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c4fa2ae2-be57-467f-a165-1bc034e0df79"
            }
          ]
        }
      ]
    }
  ]
}