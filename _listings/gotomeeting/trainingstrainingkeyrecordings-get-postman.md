{
  "info": {
    "name": "Go To Training Get Online Recordings for Training",
    "_postman_id": "9a3c776d-263f-4754-a420-2a513c6c9816",
    "description": "This call retrieves information on all online recordings for a given training. If there are none, it returns an empty list.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Trainings",
      "item": [
        {
          "id": "55290f44-b845-4f86-91df-099958c276bd",
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
              "id": "354f5156-3118-4640-a482-589aa845ee96"
            }
          ]
        }
      ]
    }
  ]
}