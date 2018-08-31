---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Training Get Training
  description: Uses the organizer key and training key to retrieve information on
    a scheduled training.
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
  /sessions/{uuid}:
    get:
      summary: Get details for a single GoToAssist Seeit session
      description: <p>This endpoint allows you to get all relevant details for a single
        GoToAssist Seeit session. Session details are available for 90 days.</p><p>The
        fields and their values in the response depend on session status and the time
        elapsed since session end; e.g. session data like snapshots or the session
        recording are only available for 72 hours.</p>
      operationId: sessions.uuid.get
      x-api-path-slug: sessionsuuid-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: uuid
        description: the uuid returned when creating the session
      responses:
        200:
          description: OK
      tags:
      - Sessions
      - Uuid
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
    post:
      summary: Create meeting
      description: Create a new meeting based on the parameters specified.
      operationId: create-a-new-meeting-based-on-the-parameters-specified-
      x-api-path-slug: meetings-post
      parameters:
      - in: body
        name: body
        description: The meeting details
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Meetings
  /meetings/{meetingId}:
    delete:
      summary: Delete meeting
      description: Deletes the meeting identified by the meetingId.
      operationId: deletes-the-meeting-identified-by-the-meetingid-
      x-api-path-slug: meetingsmeetingid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Meetings
      - MeetingId
    get:
      summary: Get meeting
      description: Returns the meeting details for the specified meeting.
      operationId: returns-the-meeting-details-for-the-specified-meeting-
      x-api-path-slug: meetingsmeetingid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Meetings
      - MeetingId
    put:
      summary: Update meeting
      description: Updates an existing meeting specified by meetingId.
      operationId: updates-an-existing-meeting-specified-by-meetingid-
      x-api-path-slug: meetingsmeetingid-put
      parameters:
      - in: body
        name: body
        description: The meeting details
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Meetings
      - MeetingId
  /meetings/{meetingId}/attendees:
    get:
      summary: Get attendees by meeting
      description: List all attendees for specified meetingId of historical meeting.
        The historical meetings can be fetched using 'Get historical meetings', 'Get
        historical meetings by organizer', and 'Get historical meetings by group'.
        For users with the admin role this call returns attendees for any meeting.
        For any other user the call will return attendees for meetings on which the
        user is a valid organizer.
      operationId: list-all-attendees-for-specified-meetingid-of-historical-meeting--the-historical-meetings-can-be-fet
      x-api-path-slug: meetingsmeetingidattendees-get
      parameters:
      - in: path
        name: meetingId
        description: The meeting ID
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Meetings
      - MeetingId
      - Attendees
  /meetings/{meetingId}/start:
    get:
      summary: Start meeting
      description: Returns a host URL that can be used to start a meeting. When this
        URL is opened in a web browser, the GoToMeeting client will be downloaded
        and launched and the meeting will start. The end user is not required to login
        to a client.
      operationId: returns-a-host-url-that-can-be-used-to-start-a-meeting--when-this-url-is-opened-in-a-web-browser-the
      x-api-path-slug: meetingsmeetingidstart-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Meetings
      - MeetingId
      - Start
  /organizers:
    delete:
      summary: Delete organizer by email
      description: Deletes the individual organizer specified by the email address.
        This API call is only available to users with the admin role.
      operationId: deletes-the-individual-organizer-specified-by-the-email-address--this-api-call-is-only-available-to-
      x-api-path-slug: organizers-delete
      parameters:
      - in: query
        name: email
        description: The email address of the organizer
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
    get:
      summary: Get organizer by email / Get all organizers
      description: Gets the individual organizer specified by the organizer's email
        address. If an email address is not specified, all organizers are returned.
        This API call is only available to users with the admin role.
      operationId: gets-the-individual-organizer-specified-by-the-organizers-email-address--if-an-email-address-is-not-
      x-api-path-slug: organizers-get
      parameters:
      - in: query
        name: email
        description: The email address of the organizer
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
    post:
      summary: Create organizer
      description: Creates a new organizer and sends an email to the email address
        defined in the request. This API call is only available to users with the
        admin role. You may also pass 'G2W' or 'G2T' or 'OPENVOICE' as productType
        variables, creating organizers for those products. A G2W or G2T organizer
        will also have access to G2M.
      operationId: creates-a-new-organizer-and-sends-an-email-to-the-email-address-defined-in-the-request--this-api-cal
      x-api-path-slug: organizers-post
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
      - Organizers
  /organizers/{organizerKey}:
    delete:
      summary: Delete organizer
      description: Deletes the individual organizer specified by the organizer key.
        This API call is only available to users with the admin role.
      operationId: deletes-the-individual-organizer-specified-by-the-organizer-key--this-api-call-is-only-available-to-
      x-api-path-slug: organizersorganizerkey-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
    get:
      summary: Get organizer
      description: Returns the individual organizer specified by the key. This API
        call is only available to users with the admin role. Non-admin users can only
        make this call for their own organizerKey.
      operationId: returns-the-individual-organizer-specified-by-the-key--this-api-call-is-only-available-to-users-with
      x-api-path-slug: organizersorganizerkey-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
    put:
      summary: Update organizer
      description: Updates the products of the specified organizer. To add a product
        (G2M, G2W, G2T, OPENVOICE) for the organizer, the call must be sent once for
        each product you want to add. To remove all products for the organizer, set
        status to 'suspended'. The call is limited to users with the admin role.
      operationId: updates-the-products-of-the-specified-organizer--to-add-a-product-g2m-g2w-g2t-openvoice-for-the-orga
      x-api-path-slug: organizersorganizerkey-put
      parameters:
      - in: body
        name: body
        description: The organizers status
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
  /organizers/{organizerKey}/attendees:
    get:
      summary: Get attendees by organizer
      description: Lists all attendees for all meetings within a specified date range
        for a specified organizer. This API call is only available to users with the
        admin role.
      operationId: lists-all-attendees-for-all-meetings-within-a-specified-date-range-for-a-specified-organizer--this-a
      x-api-path-slug: organizersorganizerkeyattendees-get
      parameters:
      - in: query
        name: endDate
        description: A required end of date range in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: startDate
        description: A required start of date range in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Attendees
  /organizers/{organizerKey}/historicalMeetings:
    get:
      summary: Get historical meetings by organizer
      description: 'Get historical meetings for the specified organizer that started
        within the specified date/time range. Remark: Meetings which are still ongoing
        at the time of the request are NOT contained in the result array.'
      operationId: get-historical-meetings-for-the-specified-organizer-that-started-within-the-specified-datetime-range
      x-api-path-slug: organizersorganizerkeyhistoricalmeetings-get
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
      - Organizers
      - OrganizerKey
      - HistoricalMeetings
  /organizers/{organizerKey}/meetings:
    get:
      summary: 'DEPRECATED: Get meetings by organizer'
      description: 'DEPRECATED: Please use the new API calls ''Get historical meetings
        by organizer'' and ''Get upcoming meetings by organizer''. Gets future (scheduled)
        or past (history) meetings for a specified organizer. Include ''history=true''
        and the past start and end dates in the URL to retrieve past meetings. Enter
        ''scheduled=true'' (without dates) to get scheduled meetings.'
      operationId: deprecated-please-use-the-new-api-calls-get-historical-meetings-by-organizer-and-get-upcoming-meetin
      x-api-path-slug: organizersorganizerkeymeetings-get
      parameters:
      - in: query
        name: endDate
        description: If history is true, required end of date range, in ISO8601 UTC
          format, e
      - in: query
        name: history
        description: When true, returns all past meetings within date range
      - in: query
        name: No Name
      - in: query
        name: scheduled
        description: When true, returns all future meetings
      - in: query
        name: startDate
        description: If history is true, required start of date range, in ISO8601
          UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Meetings
  /organizers/{organizerKey}/upcomingMeetings:
    get:
      summary: Get upcoming meetings by organizer
      description: Get upcoming meetings for a specified organizer. This API call
        is only available to users with the admin role.
      operationId: get-upcoming-meetings-for-a-specified-organizer--this-api-call-is-only-available-to-users-with-the-a
      x-api-path-slug: organizersorganizerkeyupcomingmeetings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - UpcomingMeetings
  /upcomingMeetings:
    get:
      summary: Get upcoming meetings
      description: Gets upcoming meetings for the current authenticated organizer.
      operationId: gets-upcoming-meetings-for-the-current-authenticated-organizer-
      x-api-path-slug: upcomingmeetings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - UpcomingMeetings
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
  /organizers/{organizerKey}/trainings:
    get:
      summary: Get Trainings
      description: This call retrieves information on all scheduled trainings for
        a given organizer. The trainings are returned in the order in which they were
        created. Completed trainings are not included; ongoing trainings with past
        sessions are included along with the past sessions. If the organizer does
        not have any scheduled trainings, the response will be empty.
      operationId: getAllTrainings
      x-api-path-slug: organizersorganizerkeytrainings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Trainings
    post:
      summary: Create Training
      description: Schedules a training of one or more sessions. The call requires
        a training's name, at least one start and end time, and optionally may include
        additional sessions, a description, additional organizers (presenters), and
        registration settings. You can only add organizers to a training if you have
        a multi-user account. Once a training has been created with this method, you
        can accept registrations to the training. Registration is for the entire training
        - all sessions. (The GoToTraining admin site enables you to create trainings
        that allow participants to register for individual sessions as well as automatically
        create weekly or monthly events.) Registration settings controls whether you
        allow web registration for this training, and whether a confirmation email
        is sent to the registrant following registration. Disabling the confirmation
        email is an API-only setting. If the user registers through the GoToTraining
        website, a confirmation email is sent. If the user is manually approved by
        the training administrator through the GoToTraining web site, the confirmation
        email is sent. It is recommended that you disable web registration if you
        disable confirmation emails. The response contains a trainingKey for the scheduled
        training.
      operationId: scheduleTraining
      x-api-path-slug: organizersorganizerkeytrainings-post
      parameters:
      - in: body
        name: body
        description: The details of the training to create
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Trainings
  /organizers/{organizerKey}/trainings/{trainingKey}:
    delete:
      summary: Delete Training
      description: 'Deletes a scheduled or completed training. For scheduled trainings,
        it deletes all scheduled sessions of the training. For completed trainings,
        the sessions remain in the database. No email is sent to organizers or registrants,
        but when participants attempt to start or join the training, they are directed
        to a page that states: Training Not Found: The training you are trying to
        join is no longer available.'
      operationId: cancelTraining
      x-api-path-slug: organizersorganizerkeytrainingstrainingkey-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Trainings
      - TrainingKey
    get:
      summary: Get Training
      description: Uses the organizer key and training key to retrieve information
        on a scheduled training.
      operationId: getTraining
      x-api-path-slug: organizersorganizerkeytrainingstrainingkey-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Trainings
      - TrainingKey
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