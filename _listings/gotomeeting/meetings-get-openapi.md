---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: 'Go To Meeting DEPRECATED: Get historical meetings'
  description: 'DEPRECATED: Please use the new API calls ''Get historical meetings''
    and ''Get upcoming meetings''.  Gets historical meetings for the current authenticated
    organizer. Requires date range for filtering results to only meetings within specified
    dates. History searches will contain the parameter ''meetingInstanceKey'' which
    is used in conjunction with the call ''Get Attendees by Meeting'' to get attendee
    information for a past meeting.'
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: 1.0.0
host: api.citrixonline.com
basePath: /G2M/rest
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /groups:
    get:
      summary: Get groups
      description: List all groups for an account. This API call is only available
        to users with the admin role.
      operationId: list-all-groups-for-an-account--this-api-call-is-only-available-to-users-with-the-admin-role-
      x-api-path-slug: groups-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
  /groups/{groupKey}/attendees:
    get:
      summary: Get attendees by group
      description: Returns all attendees for all meetings within specified date range
        held by organizers within the specified group. This API call is only available
        to users with the admin role. This API call can be used only for groups with
        maximum 50 organizers.
      operationId: returns-all-attendees-for-all-meetings-within-specified-date-range-held-by-organizers-within-the-spe
      x-api-path-slug: groupsgroupkeyattendees-get
      parameters:
      - in: query
        name: endDate
        description: End of date range, in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: startDate
        description: Start of date range, in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
      - Attendees
  /groups/{groupKey}/historicalMeetings:
    get:
      summary: Get historical meetings by group
      description: 'Get historical meetings for the specified group that started within
        the specified date/time range. This API call is only available to users with
        the admin role. This API call is restricted to groups with a maximum of 50
        organizers. Remark: Meetings which are still ongoing at the time of the request
        are NOT contained in the result array.'
      operationId: get-historical-meetings-for-the-specified-group-that-started-within-the-specified-datetime-range--th
      x-api-path-slug: groupsgroupkeyhistoricalmeetings-get
      parameters:
      - in: query
        name: endDate
        description: Required end of date range, in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: startDate
        description: Required start of date range, in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
      - HistoricalMeetings
  /groups/{groupKey}/meetings:
    get:
      summary: 'DEPRECATED: Get historical meetings by group'
      description: 'DEPRECATED: Please use the new API calls ''Get historical meetings
        by group'' and ''Get upcoming meetings by group''. Get meetings for a specified
        group. Additional filters can be used to view only meetings within a specified
        date range. This API call is only available to users with the admin role.'
      operationId: deprecated-please-use-the-new-api-calls-get-historical-meetings-by-group-and-get-upcoming-meetings-b
      x-api-path-slug: groupsgroupkeymeetings-get
      parameters:
      - in: query
        name: endDate
        description: If history=true, required end of date range, in ISO8601 UTC format,
          e
      - in: query
        name: history
        description: When true, returns all past meetings within date range
      - in: query
        name: No Name
      - in: query
        name: startDate
        description: If history=true, required start of date range, in ISO8601 UTC
          format, e
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
      - Meetings
  /groups/{groupKey}/organizers:
    get:
      summary: Get organizers by group
      description: Returns all the organizers within a specific group. This API call
        is only available to users with the admin role.
      operationId: returns-all-the-organizers-within-a-specific-group--this-api-call-is-only-available-to-users-with-th
      x-api-path-slug: groupsgroupkeyorganizers-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
      - Organizers
    post:
      summary: Create organizer in group
      description: Creates a new organizer and sends an email to the email address
        defined in request. This API call is only available to users with the admin
        role. You may also pass 'G2W' or 'G2T' or 'OPENVOICE' as productType variables,
        creating organizers for those products. A G2W or G2T organizer will also have
        access to G2M.
      operationId: creates-a-new-organizer-and-sends-an-email-to-the-email-address-defined-in-request--this-api-call-is
      x-api-path-slug: groupsgroupkeyorganizers-post
      parameters:
      - in: body
        name: body
        description: The details of the organizer to be created
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
      - Organizers
  /groups/{groupKey}/upcomingMeetings:
    get:
      summary: Get upcoming meetings by group
      description: Get upcoming meetings for a specified group. This API call is only
        available to users with the admin role. This API call can be used only for
        groups with maximum 50 organizers.
      operationId: get-upcoming-meetings-for-a-specified-group--this-api-call-is-only-available-to-users-with-the-admin
      x-api-path-slug: groupsgroupkeyupcomingmeetings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
      - UpcomingMeetings
  /historicalMeetings:
    get:
      summary: Get historical meetings
      description: 'Get historical meetings for the currently authenticated organizer
        that started within the specified date/time range. Remark: Meetings which
        are still ongoing at the time of the request are NOT contained in the result
        array.'
      operationId: get-historical-meetings-for-the-currently-authenticated-organizer-that-started-within-the-specified-
      x-api-path-slug: historicalmeetings-get
      parameters:
      - in: query
        name: endDate
        description: Required end of date range, in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: startDate
        description: Required start of date range, in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - HistoricalMeetings
  /meetings:
    get:
      summary: 'DEPRECATED: Get historical meetings'
      description: 'DEPRECATED: Please use the new API calls ''Get historical meetings''
        and ''Get upcoming meetings''.  Gets historical meetings for the current authenticated
        organizer. Requires date range for filtering results to only meetings within
        specified dates. History searches will contain the parameter ''meetingInstanceKey''
        which is used in conjunction with the call ''Get Attendees by Meeting'' to
        get attendee information for a past meeting.'
      operationId: deprecated-please-use-the-new-api-calls-get-historical-meetings-and-get-upcoming-meetings---gets-his
      x-api-path-slug: meetings-get
      parameters:
      - in: query
        name: endDate
        description: If history=true, required end of date range, in ISO8601 UTC format,
          e
      - in: query
        name: history
        description: When true, returns all past meetings within date range
      - in: query
        name: No Name
      - in: query
        name: startDate
        description: If history=true, required start of date range, in ISO8601 UTC
          format, e
      responses:
        200:
          description: OK
      tags:
      - Meetings
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