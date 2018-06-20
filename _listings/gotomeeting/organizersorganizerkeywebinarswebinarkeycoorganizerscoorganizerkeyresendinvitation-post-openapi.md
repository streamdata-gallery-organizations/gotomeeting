---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Webinar Resend invitation
  description: Resends an invitation email to the specified co-organizer
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
  /organizers/{organizerKey}/webinars/{webinarKey}/audio:
    get:
      summary: Get audio information
      description: Retrieves the audio/conferencing information for a specific webinar.
      operationId: getAudioInformation
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyaudio-get
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
      - Audio
    post:
      summary: Update audio information
      description: Updates the audio/conferencing settings for a specific webinar
      operationId: updateAudioInformation
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeyaudio-post
      parameters:
      - in: body
        name: body
        description: The audio/conferencing settings
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
      - Audio
  /organizers/{organizerKey}/webinars/{webinarKey}/coorganizers:
    get:
      summary: Get co-organizers
      description: Returns the co-organizers for the specified webinar. The original
        organizer who created the webinar is filtered out of the list. If the webinar
        has no co-organizers, an empty array is returned. Co-organizers that do not
        have a GoToWebinar account are returned as external co-organizers. For those
        organizers no surname is returned.
      operationId: getCoorganizers
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-get
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
      - Coorganizers
    post:
      summary: Create co-organizers
      description: Creates co-organizers for the specified webinar. For co-organizers
        that have a GoToWebinar account you have to set the parameter 'external' to
        'false'. In this case you have to pass the parameter 'organizerKey' only.
        For co-organizers that have no GoToWebinar account you have to set the parameter
        'external' to 'true'. In this case you have to pass the parameters 'givenName'
        and 'email'. Since there is no parameter for 'surname' you should pass first
        and last name to the parameter 'givenName'.
      operationId: createCoorganizers
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-post
      parameters:
      - in: body
        name: body
        description: The co-organizer details
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
      - WebinarKey
      - Coorganizers
  /organizers/{organizerKey}/webinars/{webinarKey}/coorganizers/{coorganizerKey}:
    delete:
      summary: Delete co-organizer
      description: Deletes an internal co-organizer specified by the coorganizerKey
        (memberKey).
      operationId: deleteCoorganizer
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete
      parameters:
      - in: query
        name: external
        description: By default only internal co-organizers (with a GoToWebinar account)
          can be deleted
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
      - Coorganizers
      - CoorganizerKey
  /organizers/{organizerKey}/webinars/{webinarKey}/coorganizers/{coorganizerKey}/resendInvitation:
    post:
      summary: Resend invitation
      description: Resends an invitation email to the specified co-organizer
      operationId: resendCoorganizerInvitation
      x-api-path-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post
      parameters:
      - in: query
        name: external
        description: By default only internal co-organizers (with a GoToWebinar account)
          will retrieve the resent invitation email
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
      - Coorganizers
      - CoorganizerKey
      - ResendInvitation
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