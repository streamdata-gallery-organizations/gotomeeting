{
  "info": {
    "name": "Go To Training Get Trainings",
    "_postman_id": "e3fc69f9-d5b3-4862-9b15-9d2e88fb7e20",
    "description": "This call retrieves information on all scheduled trainings for a given organizer. The trainings are returned in the order in which they were created. Completed trainings are not included; ongoing trainings with past sessions are included along with the past sessions. If the organizer does not have any scheduled trainings, the response will be empty.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Accounts",
      "item": [
        {
          "id": "40aa1c22-525f-4b01-a64f-a77152d35eac",
          "name": "getAllOrganisers",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2T",
                "rest",
                "accounts/:accountKey/organizers"
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
                  "id": "accountKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "DEPRECATED: Please use the Admin API call 'Get all users' instead. For details see https://developer.citrixonline.com/get-all-users."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "409364ac-766e-4421-a2ac-669958e93583"
            }
          ]
        }
      ]
    },
    {
      "name": "Organizers",
      "item": [
        {
          "id": "b4d18f0c-d515-442e-8ccd-dec5adc5f9a7",
          "name": "getAllTrainings",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.citrixonline.com",
              "path": [
                "G2T",
                "rest",
                "organizers/:organizerKey/trainings"
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
            "description": "This call retrieves information on all scheduled trainings for a given organizer. The trainings are returned in the order in which they were created. Completed trainings are not included; ongoing trainings with past sessions are included along with the past sessions. If the organizer does not have any scheduled trainings, the response will be empty."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6e280a58-9061-4d30-b5b7-fa6e37a6e15f"
            }
          ]
        }
      ]
    }
  ]
}