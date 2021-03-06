---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Webinar Get attendees for all webinar sessions
  description: Returns all attendees for all sessions of the specified webinar.
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: 1.0.0
host: api.citrixonline.com
basePath: /G2W/rest
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
  /organizers/{organizerKey}/trainings/{trainingKey}/manageUrl:
    get:
      summary: Get Management URL for Training
      description: A request for a direct URL to the admin portal for a specific training.
        The request identifies the organizer and the training; the response provides
        a link the organizer can use to manage or launch the training in the admin
        portal. The training organizer will be required to log in. You can schedule
        and manage the training (e.g., add tests, polls and training materials) from
        the URL provided in the response.
      operationId: getManageTrainingURL
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeymanageurl-get
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
      - ManageUrl
  /organizers/{organizerKey}/trainings/{trainingKey}/nameDescription:
    put:
      summary: Update Training Name and Description
      description: Request to update a scheduled training name and description.
      operationId: updateTrainingNameDescription
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeynamedescription-put
      parameters:
      - in: body
        name: body
        description: The new name and description for the training
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
      - TrainingKey
      - NameDescription
  /organizers/{organizerKey}/trainings/{trainingKey}/organizers:
    get:
      summary: Get Training Organizers
      description: Retrieves organizer details for a specific training. This is only
        applicable to multi-user accounts with sharing enabled (co-organizers).
      operationId: getOrganisersForTraining
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeyorganizers-get
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
      - Organizers
    put:
      summary: Update Training Organizers
      description: Replaces the co-organizers for a specific training. The scheduling
        organizer cannot be unassigned. Organizers will be notified via email if the
        notifyOrganizers parameter is set to true. Replaced organizers are not notified.
        This method is only applicable to multi-user accounts with sharing enabled
        (co-organizers).
      operationId: updateOrganisersForTraining
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeyorganizers-put
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
      - TrainingKey
      - Organizers
  /organizers/{organizerKey}/trainings/{trainingKey}/registrants:
    get:
      summary: Get Training Registrants
      description: 'Retrieves details on all registrants for a specific training.
        Registrants can be:<br>WAITING - registrant registered and is awaiting approval
        (where organizer has required approval)<br>APPROVED - registrant registered
        and is approved<br>DENIED - registrant registered and was not approved.<br><br>IMPORTANT:
        The registrant data caches are typically updated immediately and the data
        will be returned in the response. However, the update can take as long as
        two hours.'
      operationId: getRegistrants
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeyregistrants-get
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
      - Registrants
    post:
      summary: Register for Training
      description: 'Registers one person, identified by a unique email address, for
        a training. Approval is automatic unless payment or approval is required.
        The response contains the Confirmation page URL and Join URL for the registrant.
        NOTE: If some registrants do not receive a confirmation email, the emails
        could be getting blocked by their email server due to spam filtering or a
        grey-listing setting.'
      operationId: registerForTraining
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeyregistrants-post
      parameters:
      - in: body
        name: body
        description: The details of the registrant to create
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
      - TrainingKey
      - Registrants
  /organizers/{organizerKey}/trainings/{trainingKey}/registrants/{registrantKey}:
    delete:
      summary: Cancel Registration
      description: This call cancels a registration in a scheduled training for a
        specific registrant. If the registrant has paid for the training, a cancellation
        cannot be completed with this method; it must be completed on the external
        admin site. No notification is sent to the registrant or the organizer by
        default. The registrant can re-register if needed.
      operationId: cancelRegistration
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeyregistrantsregistrantkey-delete
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
      - Registrants
      - RegistrantKey
    get:
      summary: Get Registrant
      description: 'Retrieves details for specific registrant in a specific training.
        Registrants can be:<br>WAITING - registrant registered and is awaiting approval
        (where organizer has required approval)<br>APPROVED - registrant registered
        and is approved<br>DENIED - registrant registered and was not approved.<br><br>IMPORTANT:
        The registrant data caches are typically updated immediately and the data
        will be returned in the response. However, the update can take as long as
        two hours.'
      operationId: getRegistrant
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeyregistrantsregistrantkey-get
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
      - Registrants
      - RegistrantKey
  /organizers/{organizerKey}/trainings/{trainingKey}/registrationSettings:
    put:
      summary: Update Training Registration Settings
      description: An API request to automatically enable or disable web registrations
        and confirmation emails to registrants.
      operationId: updateRegistrationSettingsForTraining
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeyregistrationsettings-put
      parameters:
      - in: body
        name: body
        description: The new registration settings for the training
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
      - TrainingKey
      - RegistrationSettings
  /organizers/{organizerKey}/trainings/{trainingKey}/startUrl:
    get:
      summary: Get Start Url
      description: Returns a URL that can be used to start a training. When this URL
        is opened in a web browser, the GoToTraining client will be downloaded and
        launched and the training will start after the organizer logs in with its
        credentials.
      operationId: getStartUrl
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeystarturl-get
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
      - StartUrl
  /organizers/{organizerKey}/trainings/{trainingKey}/times:
    put:
      summary: Update Training Times
      description: A request to update a scheduled training's start and end times.
        If the request contains 'notifyTrainers = true' and 'notifyRegistrants = true',
        both organizers and registrants are notified. The response provides the number
        of notified trainers and registrants.
      operationId: updateTrainingTimes
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeytimes-put
      parameters:
      - in: body
        name: body
        description: The new start and end times for the scheduled training
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
      - TrainingKey
      - Times
  /reports/organizers/{organizerKey}/sessions:
    post:
      summary: Get Sessions by Date Range
      description: This call returns all session details over a given date range for
        a given organizer. A session is a completed training event.
      operationId: getSessionDetailsForDateRange
      x-api-path-slug: reportsorganizersorganizerkeysessions-post
      parameters:
      - in: body
        name: body
        description: The start and end times for the time range over which to retrieve
          training sessions
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Reports
      - Organizers
      - OrganizerKey
      - Sessions
  /reports/organizers/{organizerKey}/sessions/{sessionKey}/attendees:
    get:
      summary: Get Attendance Details
      description: This call retrieves a list of registrants from a specific completed
        training session. The response includes the registrants' email addresses,
        and if they attended, it includes the duration of each period of their attendance
        in minutes, and the times at which they joined and left. If a registrant does
        not attend, they appear at the bottom of the listing with timeInSession =
        0.
      operationId: getAttendanceDetails
      x-api-path-slug: reportsorganizersorganizerkeysessionssessionkeyattendees-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: sessionKey
        description: The key of the training session
      responses:
        200:
          description: OK
      tags:
      - Reports
      - Organizers
      - OrganizerKey
      - Sessions
      - SessionKey
      - Attendees
  /reports/organizers/{organizerKey}/trainings/{trainingKey}:
    get:
      summary: Get Sessions By Training
      description: This call returns session details for a given training. A session
        is a completed training event. Each training may contain one or more sessions.
      operationId: getSessionDetailsForTraining
      x-api-path-slug: reportsorganizersorganizerkeytrainingstrainingkey-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Reports
      - Organizers
      - OrganizerKey
      - Trainings
      - TrainingKey
  /trainings/{trainingKey}/recordings:
    get:
      summary: Get Online Recordings for Training
      description: This call retrieves information on all online recordings for a
        given training. If there are none, it returns an empty list.
      operationId: getRecordingsForTraining
      x-api-path-slug: trainingstrainingkeyrecordings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Trainings
      - TrainingKey
      - Recordings
  /trainings/{trainingKey}/recordings/{recordingId}:
    get:
      summary: Get Download for Online Recordings
      description: This call provides the download for the given recording by returning
        a 302 redirect to the original file.
      operationId: getRecordingDownloadById
      x-api-path-slug: trainingstrainingkeyrecordingsrecordingid-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: recordingId
        description: the unique id of the recording
      responses:
        200:
          description: OK
      tags:
      - Trainings
      - TrainingKey
      - Recordings
      - RecordingId
  /trainings/{trainingKey}/start:
    get:
      summary: Start Training
      description: Returns a URL that can be used to start a training. When this URL
        is opened in a web browser, the GoToTraining client will be downloaded and
        launched and the training will start. A login of the organizer is not required.
      operationId: startTraining
      x-api-path-slug: trainingstrainingkeystart-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Trainings
      - TrainingKey
      - Start
  /accounts/{accountKey}/webinars:
    get:
      summary: Get all webinars for an account
      description: Retrieves the list of webinars for an account within a given date
        range. __*Page*__ and __*size*__ parameters are optional. Default __*page*__
        is 0 and default __*size*__ is 20. For technical reasons, this call cannot
        be executed from this documentation. Please use the curl command to execute
        it.
      operationId: getAllAccountWebinars
      x-api-path-slug: accountsaccountkeywebinars-get
      parameters:
      - in: query
        name: fromTime
        description: A required start of datetime range in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: page
        description: The page number to be displayed
      - in: query
        name: size
        description: The size of the page
      - in: query
        name: toTime
        description: A required end of datetime range in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Accounts
      - AccountKey
      - Webinars
  /organizers/{organizerKey}/historicalWebinars:
    get:
      summary: Get historical webinars
      description: Returns details for completed webinars for the specified organizer
        and completed webinars of other organizers where the specified organizer is
        a co-organizer.
      operationId: getHistoricalWebinars
      x-api-path-slug: organizersorganizerkeyhistoricalwebinars-get
      parameters:
      - in: query
        name: fromTime
        description: A required start of datetime range in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: toTime
        description: A required end of datetime range in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - HistoricalWebinars
  /organizers/{organizerKey}/sessions:
    get:
      summary: Get organizer sessions
      description: Retrieve all completed sessions of all the webinars of a given
        organizer.
      operationId: getOrganizerSessions
      x-api-path-slug: organizersorganizerkeysessions-get
      parameters:
      - in: query
        name: fromTime
        description: A required start of datetime range in ISO8601 UTC format, e
      - in: query
        name: No Name
      - in: query
        name: toTime
        description: A required end of datetime range in ISO8601 UTC format, e
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Sessions
  /organizers/{organizerKey}/upcomingWebinars:
    get:
      summary: Get upcoming webinars
      description: Returns webinars scheduled for the future for the specified organizer
        and webinars of other organizers where the specified organizer is a co-organizer.
      operationId: getUpcomingWebinars
      x-api-path-slug: organizersorganizerkeyupcomingwebinars-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - UpcomingWebinars
  /organizers/{organizerKey}/webinars:
    get:
      summary: Get all webinars
      description: Returns webinars scheduled for the future for a specified organizer.
      operationId: getAllWebinars
      x-api-path-slug: organizersorganizerkeywebinars-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
    post:
      summary: Create webinar
      description: 'Creates a single session webinar, a sequence of webinars or a
        series of webinars depending on the type field in the body: "single_session"
        creates a single webinar session, "sequence" creates a webinar with multiple
        meeting times where attendees are expected to be the same for all sessions,
        and "series" creates a webinar with multiple meetings times where attendees
        choose only one to attend. The default, if no type is declared, is single_session.
        A sequence webinar requires a "recurrenceStart" object consisting of a "startTime"
        and "endTime" key for the first webinar of the sequence, a "recurrencePattern"
        of "daily", "weekly", "monthly", and a "recurrenceEnd" which is the last date
        of the sequence (for example, 2016-12-01). A series webinar requires a "times"
        array with a discrete "startTime" and "endTime" for each webinar in the series.
        The call requires a webinar subject and description. The "isPasswordProtected"
        sets whether the webinar requires a password for attendees to join. If set
        to True, the organizer must go to Registration Settings at My Webinars (https://global.gotowebinar.com/webinars.tmpl)
        and add the password to the webinar, and send the password to the registrants.
        The response provides a numeric webinarKey in string format for the new webinar.
        Once a webinar has been created with this method, you can accept registrations.'
      operationId: createWebinar
      x-api-path-slug: organizersorganizerkeywebinars-post
      parameters:
      - in: body
        name: body
        description: The webinar details
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
      - Webinars
  /organizers/{organizerKey}/webinars/{webinarKey}:
    delete:
      summary: Cancel webinar
      description: Cancels a specific webinar. If the webinar is a series or sequence,
        this call deletes all scheduled sessions. To send cancellation emails to registrants
        set sendCancellationEmails=true in the request. When the cancellation emails
        are sent, the default generated message is used in the cancellation email
        body.
      operationId: cancelWebinar
      x-api-path-slug: organizersorganizerkeywebinarswebinarkey-delete
      parameters:
      - in: query
        name: No Name
      - in: query
        name: sendCancellationEmails
        description: Indicates whether cancellation notice emails should be sent
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
    get:
      summary: Get webinar
      description: Retrieve information on a specific webinar. If the type of the
        webinar is 'sequence', a sequence of future times will be provided. Webinars
        of type 'series' are treated the same as normal webinars - each session in
        the webinar series has a different webinarKey. If an organizer cancels a webinar,
        then a request to get that webinar would return a '404 Not Found' error.
      operationId: getWebinar
      x-api-path-slug: organizersorganizerkeywebinarswebinarkey-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
    put:
      summary: Update webinar
      description: Updates a webinar. The call requires at least one of the parameters
        in the request body. The request completely replaces the existing session,
        series, or sequence and so must include the full definition of each as for
        the Create call. Set notifyParticipants=true to send update emails to registrants.
      operationId: updateWebinar
      x-api-path-slug: organizersorganizerkeywebinarswebinarkey-put
      parameters:
      - in: body
        name: body
        description: The webinar details
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      - in: query
        name: notifyParticipants
        description: Defines whether to send notifications to participants
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
  /organizers/{organizerKey}/webinars/{webinarKey}/attendees:
    get:
      summary: Get attendees for all webinar sessions
      description: Returns all attendees for all sessions of the specified webinar.
      operationId: getAttendeesForAllWebinarSessions
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyattendees-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Webinars
      - WebinarKey
      - Attendees
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