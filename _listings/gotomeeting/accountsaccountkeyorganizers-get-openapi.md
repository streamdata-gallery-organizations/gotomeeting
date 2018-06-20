---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: 'Go To Training DEPRECATED: Get Organizers'
  description: 'DEPRECATED: Please use the Admin API call ''Get all users'' instead.
    For details see https://developer.citrixonline.com/get-all-users.'
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: 1.0.0
host: api.citrixonline.com
basePath: /G2T/rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /accounts/{accountKey}/organizers:
    get:
      summary: 'DEPRECATED: Get Organizers'
      description: 'DEPRECATED: Please use the Admin API call ''Get all users'' instead.
        For details see https://developer.citrixonline.com/get-all-users.'
      operationId: getAllOrganisers
      x-api-path-slug: accountsaccountkeyorganizers-get
      parameters:
      - in: path
        name: accountKey
        description: The key of the multi-user account
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Accounts
      - AccountKey
      - Organizers
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---