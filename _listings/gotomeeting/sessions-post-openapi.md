---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Assist Seeit Create a GoToAssist Seeit session
  description: This endpoint allows you to create a GoToAssist Seeit session. The
    session logically exists but is not started until you open the returned startUrl
    in a suitable browser.
  version: 0.9.0
host: api.citrixonline.com
basePath: /seeit/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /sessions:
    get:
      summary: Get details for multiple GoToAssist Seeit sessions
      description: <p>This endpoint allows you to get all relevant details for mulitple
        GoToAssist Seeit sessions. Session details are available for 90 days.</p></p>The
        fields and their values in the response depend on session status and the time
        elapsed since session end; e.g. session data like snapshots or the session
        recording are only available for 72 hours.</p><p>The results will be paged,
        with paging customizable to match your requirements.</p>
      operationId: sessions.get
      x-api-path-slug: sessions-get
      parameters:
      - in: query
        name: endTime
        description: Optional end of date range as timestamp (will be compared against
          session creation time)
      - in: query
        name: No Name
      - in: query
        name: page
        description: Optional page number
      - in: query
        name: size
        description: Optional page size
      - in: query
        name: sort
        description: Optional sort criteria, i
      - in: query
        name: startTime
        description: Optional start of date range as timestamp (will be compared against
          session creation time)
      responses:
        200:
          description: OK
      tags:
      - Sessions
    post:
      summary: Create a GoToAssist Seeit session
      description: This endpoint allows you to create a GoToAssist Seeit session.
        The session logically exists but is not started until you open the returned
        startUrl in a suitable browser.
      operationId: sessions.post
      x-api-path-slug: sessions-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Sessions
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