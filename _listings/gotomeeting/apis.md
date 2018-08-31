---
name: GoToMeeting
x-slug: gotomeeting
description: Citrix enables business mobility through the secure delivery of apps
  and data to any device on any network.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
x-kinRank: "7"
x-alexaRank: "7422"
tags: GoToMeeting
created: "2018-08-30"
modified: "2018-08-30"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/apis.md
specificationVersion: "0.14"
apis:
- name: Go To Assist Seeit - Get details for multiple GoToAssist Seeit sessions
  x-api-slug: sessions-get
  description: <p>This endpoint allows you to get all relevant details for mulitple
    GoToAssist Seeit sessions. Session details are available for 90 days.</p></p>The
    fields and their values in the response depend on session status and the time
    elapsed since session end; e.g. session data like snapshots or the session recording
    are only available for 72 hours.</p><p>The results will be paged, with paging
    customizable to match your requirements.</p>
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//seeit/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/sessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/sessions-get-openapi.md
- name: Go To Assist Seeit - Create a GoToAssist Seeit session
  x-api-slug: sessions-post
  description: This endpoint allows you to create a GoToAssist Seeit session. The
    session logically exists but is not started until you open the returned startUrl
    in a suitable browser.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//seeit/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/sessions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/sessions-post-openapi.md
- name: Go To Assist Seeit - Get details for a single GoToAssist Seeit session
  x-api-slug: sessionsuuid-get
  description: <p>This endpoint allows you to get all relevant details for a single
    GoToAssist Seeit session. Session details are available for 90 days.</p><p>The
    fields and their values in the response depend on session status and the time
    elapsed since session end; e.g. session data like snapshots or the session recording
    are only available for 72 hours.</p>
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//seeit/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/sessionsuuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/sessionsuuid-get-openapi.md
- name: Go To Meeting - Get groups
  x-api-slug: groups-get
  description: List all groups for an account. This API call is only available to
    users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groups-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groups-get-openapi.md
- name: Go To Meeting - Get attendees by group
  x-api-slug: groupsgroupkeyattendees-get
  description: Returns all attendees for all meetings within specified date range
    held by organizers within the specified group. This API call is only available
    to users with the admin role. This API call can be used only for groups with maximum
    50 organizers.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeyattendees-get-openapi.md
- name: Go To Meeting - Get historical meetings by group
  x-api-slug: groupsgroupkeyhistoricalmeetings-get
  description: 'Get historical meetings for the specified group that started within
    the specified date/time range. This API call is only available to users with the
    admin role. This API call is restricted to groups with a maximum of 50 organizers.
    Remark: Meetings which are still ongoing at the time of the request are NOT contained
    in the result array.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeyhistoricalmeetings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeyhistoricalmeetings-get-openapi.md
- name: 'Go To Meeting - DEPRECATED: Get historical meetings by group'
  x-api-slug: groupsgroupkeymeetings-get
  description: 'DEPRECATED: Please use the new API calls ''Get historical meetings
    by group'' and ''Get upcoming meetings by group''. Get meetings for a specified
    group. Additional filters can be used to view only meetings within a specified
    date range. This API call is only available to users with the admin role.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeymeetings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeymeetings-get-openapi.md
- name: Go To Meeting - Get organizers by group
  x-api-slug: groupsgroupkeyorganizers-get
  description: Returns all the organizers within a specific group. This API call is
    only available to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeyorganizers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeyorganizers-get-openapi.md
- name: Go To Meeting - Create organizer in group
  x-api-slug: groupsgroupkeyorganizers-post
  description: Creates a new organizer and sends an email to the email address defined
    in request. This API call is only available to users with the admin role. You
    may also pass 'G2W' or 'G2T' or 'OPENVOICE' as productType variables, creating
    organizers for those products. A G2W or G2T organizer will also have access to
    G2M.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeyorganizers-post-openapi.md
- name: Go To Meeting - Get upcoming meetings by group
  x-api-slug: groupsgroupkeyupcomingmeetings-get
  description: Get upcoming meetings for a specified group. This API call is only
    available to users with the admin role. This API call can be used only for groups
    with maximum 50 organizers.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkeyupcomingmeetings-get-openapi.md
- name: Go To Meeting - Get historical meetings
  x-api-slug: historicalmeetings-get
  description: 'Get historical meetings for the currently authenticated organizer
    that started within the specified date/time range. Remark: Meetings which are
    still ongoing at the time of the request are NOT contained in the result array.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/historicalmeetings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/historicalmeetings-get-openapi.md
- name: 'Go To Meeting - DEPRECATED: Get historical meetings'
  x-api-slug: meetings-get
  description: 'DEPRECATED: Please use the new API calls ''Get historical meetings''
    and ''Get upcoming meetings''.  Gets historical meetings for the current authenticated
    organizer. Requires date range for filtering results to only meetings within specified
    dates. History searches will contain the parameter ''meetingInstanceKey'' which
    is used in conjunction with the call ''Get Attendees by Meeting'' to get attendee
    information for a past meeting.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/meetings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/meetings-get-openapi.md
- name: Go To Meeting - Create meeting
  x-api-slug: meetings-post
  description: Create a new meeting based on the parameters specified.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/meetings-post-openapi.md
- name: Go To Meeting - Delete meeting
  x-api-slug: meetingsmeetingid-delete
  description: Deletes the meeting identified by the meetingId.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/meetingsmeetingid-delete-openapi.md
- name: Go To Meeting - Get meeting
  x-api-slug: meetingsmeetingid-get
  description: Returns the meeting details for the specified meeting.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/meetingsmeetingid-get-openapi.md
- name: Go To Meeting - Update meeting
  x-api-slug: meetingsmeetingid-put
  description: Updates an existing meeting specified by meetingId.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/meetingsmeetingid-put-openapi.md
- name: Go To Meeting - Get attendees by meeting
  x-api-slug: meetingsmeetingidattendees-get
  description: List all attendees for specified meetingId of historical meeting. The
    historical meetings can be fetched using 'Get historical meetings', 'Get historical
    meetings by organizer', and 'Get historical meetings by group'. For users with
    the admin role this call returns attendees for any meeting. For any other user
    the call will return attendees for meetings on which the user is a valid organizer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/meetingsmeetingidattendees-get-openapi.md
- name: Go To Meeting - Start meeting
  x-api-slug: meetingsmeetingidstart-get
  description: Returns a host URL that can be used to start a meeting. When this URL
    is opened in a web browser, the GoToMeeting client will be downloaded and launched
    and the meeting will start. The end user is not required to login to a client.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/meetingsmeetingidstart-get-openapi.md
- name: Go To Meeting - Delete organizer by email
  x-api-slug: organizers-delete
  description: Deletes the individual organizer specified by the email address. This
    API call is only available to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizers-delete-openapi.md
- name: Go To Meeting - Get organizer by email / Get all organizers
  x-api-slug: organizers-get
  description: Gets the individual organizer specified by the organizer's email address.
    If an email address is not specified, all organizers are returned. This API call
    is only available to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizers-get-openapi.md
- name: Go To Meeting - Create organizer
  x-api-slug: organizers-post
  description: Creates a new organizer and sends an email to the email address defined
    in the request. This API call is only available to users with the admin role.
    You may also pass 'G2W' or 'G2T' or 'OPENVOICE' as productType variables, creating
    organizers for those products. A G2W or G2T organizer will also have access to
    G2M.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizers-post-openapi.md
- name: Go To Meeting - Delete organizer
  x-api-slug: organizersorganizerkey-delete
  description: Deletes the individual organizer specified by the organizer key. This
    API call is only available to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkey-delete-openapi.md
- name: Go To Meeting - Get organizer
  x-api-slug: organizersorganizerkey-get
  description: Returns the individual organizer specified by the key. This API call
    is only available to users with the admin role. Non-admin users can only make
    this call for their own organizerKey.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkey-get-openapi.md
- name: Go To Meeting - Update organizer
  x-api-slug: organizersorganizerkey-put
  description: Updates the products of the specified organizer. To add a product (G2M,
    G2W, G2T, OPENVOICE) for the organizer, the call must be sent once for each product
    you want to add. To remove all products for the organizer, set status to 'suspended'.
    The call is limited to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkey-put-openapi.md
- name: Go To Meeting - Get attendees by organizer
  x-api-slug: organizersorganizerkeyattendees-get
  description: Lists all attendees for all meetings within a specified date range
    for a specified organizer. This API call is only available to users with the admin
    role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeyattendees-get-openapi.md
- name: Go To Meeting - Get historical meetings by organizer
  x-api-slug: organizersorganizerkeyhistoricalmeetings-get
  description: 'Get historical meetings for the specified organizer that started within
    the specified date/time range. Remark: Meetings which are still ongoing at the
    time of the request are NOT contained in the result array.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeyhistoricalmeetings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeyhistoricalmeetings-get-openapi.md
- name: 'Go To Meeting - DEPRECATED: Get meetings by organizer'
  x-api-slug: organizersorganizerkeymeetings-get
  description: 'DEPRECATED: Please use the new API calls ''Get historical meetings
    by organizer'' and ''Get upcoming meetings by organizer''. Gets future (scheduled)
    or past (history) meetings for a specified organizer. Include ''history=true''
    and the past start and end dates in the URL to retrieve past meetings. Enter ''scheduled=true''
    (without dates) to get scheduled meetings.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeymeetings-get-openapi.md
- name: Go To Meeting - Get upcoming meetings by organizer
  x-api-slug: organizersorganizerkeyupcomingmeetings-get
  description: Get upcoming meetings for a specified organizer. This API call is only
    available to users with the admin role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeyupcomingmeetings-get-openapi.md
- name: Go To Meeting - Get upcoming meetings
  x-api-slug: upcomingmeetings-get
  description: Gets upcoming meetings for the current authenticated organizer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2M/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/upcomingmeetings-get-openapi.md
- name: 'Go To Training - DEPRECATED: Get Organizers'
  x-api-slug: accountsaccountkeyorganizers-get
  description: 'DEPRECATED: Please use the Admin API call ''Get all users'' instead.
    For details see https://developer.citrixonline.com/get-all-users.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/accountsaccountkeyorganizers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/accountsaccountkeyorganizers-get-openapi.md
- name: Go To Training - Get Trainings
  x-api-slug: organizersorganizerkeytrainings-get
  description: This call retrieves information on all scheduled trainings for a given
    organizer. The trainings are returned in the order in which they were created.
    Completed trainings are not included; ongoing trainings with past sessions are
    included along with the past sessions. If the organizer does not have any scheduled
    trainings, the response will be empty.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainings-get-openapi.md
- name: Go To Training - Create Training
  x-api-slug: organizersorganizerkeytrainings-post
  description: Schedules a training of one or more sessions. The call requires a training's
    name, at least one start and end time, and optionally may include additional sessions,
    a description, additional organizers (presenters), and registration settings.
    You can only add organizers to a training if you have a multi-user account. Once
    a training has been created with this method, you can accept registrations to
    the training. Registration is for the entire training - all sessions. (The GoToTraining
    admin site enables you to create trainings that allow participants to register
    for individual sessions as well as automatically create weekly or monthly events.)
    Registration settings controls whether you allow web registration for this training,
    and whether a confirmation email is sent to the registrant following registration.
    Disabling the confirmation email is an API-only setting. If the user registers
    through the GoToTraining website, a confirmation email is sent. If the user is
    manually approved by the training administrator through the GoToTraining web site,
    the confirmation email is sent. It is recommended that you disable web registration
    if you disable confirmation emails. The response contains a trainingKey for the
    scheduled training.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainings-post-openapi.md
- name: Go To Training - Delete Training
  x-api-slug: organizersorganizerkeytrainingstrainingkey-delete
  description: 'Deletes a scheduled or completed training. For scheduled trainings,
    it deletes all scheduled sessions of the training. For completed trainings, the
    sessions remain in the database. No email is sent to organizers or registrants,
    but when participants attempt to start or join the training, they are directed
    to a page that states: Training Not Found: The training you are trying to join
    is no longer available.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkey-delete-openapi.md
- name: Go To Training - Get Training
  x-api-slug: organizersorganizerkeytrainingstrainingkey-get
  description: Uses the organizer key and training key to retrieve information on
    a scheduled training.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkey-get-openapi.md
- name: Go To Training - Get Management URL for Training
  x-api-slug: organizersorganizerkeytrainingstrainingkeymanageurl-get
  description: A request for a direct URL to the admin portal for a specific training.
    The request identifies the organizer and the training; the response provides a
    link the organizer can use to manage or launch the training in the admin portal.
    The training organizer will be required to log in. You can schedule and manage
    the training (e.g., add tests, polls and training materials) from the URL provided
    in the response.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeymanageurl-get-openapi.md
- name: Go To Training - Update Training Name and Description
  x-api-slug: organizersorganizerkeytrainingstrainingkeynamedescription-put
  description: Request to update a scheduled training name and description.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeynamedescription-put-openapi.md
- name: Go To Training - Get Training Organizers
  x-api-slug: organizersorganizerkeytrainingstrainingkeyorganizers-get
  description: Retrieves organizer details for a specific training. This is only applicable
    to multi-user accounts with sharing enabled (co-organizers).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeyorganizers-get-openapi.md
- name: Go To Training - Update Training Organizers
  x-api-slug: organizersorganizerkeytrainingstrainingkeyorganizers-put
  description: Replaces the co-organizers for a specific training. The scheduling
    organizer cannot be unassigned. Organizers will be notified via email if the notifyOrganizers
    parameter is set to true. Replaced organizers are not notified. This method is
    only applicable to multi-user accounts with sharing enabled (co-organizers).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeyorganizers-put-openapi.md
- name: Go To Training - Get Training Registrants
  x-api-slug: organizersorganizerkeytrainingstrainingkeyregistrants-get
  description: 'Retrieves details on all registrants for a specific training. Registrants
    can be:<br>WAITING - registrant registered and is awaiting approval (where organizer
    has required approval)<br>APPROVED - registrant registered and is approved<br>DENIED
    - registrant registered and was not approved.<br><br>IMPORTANT: The registrant
    data caches are typically updated immediately and the data will be returned in
    the response. However, the update can take as long as two hours.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeyregistrants-get-openapi.md
- name: Go To Training - Register for Training
  x-api-slug: organizersorganizerkeytrainingstrainingkeyregistrants-post
  description: 'Registers one person, identified by a unique email address, for a
    training. Approval is automatic unless payment or approval is required. The response
    contains the Confirmation page URL and Join URL for the registrant. NOTE: If some
    registrants do not receive a confirmation email, the emails could be getting blocked
    by their email server due to spam filtering or a grey-listing setting.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeyregistrants-post-openapi.md
- name: Go To Training - Cancel Registration
  x-api-slug: organizersorganizerkeytrainingstrainingkeyregistrantsregistrantkey-delete
  description: This call cancels a registration in a scheduled training for a specific
    registrant. If the registrant has paid for the training, a cancellation cannot
    be completed with this method; it must be completed on the external admin site.
    No notification is sent to the registrant or the organizer by default. The registrant
    can re-register if needed.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeyregistrantsregistrantkey-delete-openapi.md
- name: Go To Training - Get Registrant
  x-api-slug: organizersorganizerkeytrainingstrainingkeyregistrantsregistrantkey-get
  description: 'Retrieves details for specific registrant in a specific training.
    Registrants can be:<br>WAITING - registrant registered and is awaiting approval
    (where organizer has required approval)<br>APPROVED - registrant registered and
    is approved<br>DENIED - registrant registered and was not approved.<br><br>IMPORTANT:
    The registrant data caches are typically updated immediately and the data will
    be returned in the response. However, the update can take as long as two hours.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeyregistrantsregistrantkey-get-openapi.md
- name: Go To Training - Update Training Registration Settings
  x-api-slug: organizersorganizerkeytrainingstrainingkeyregistrationsettings-put
  description: An API request to automatically enable or disable web registrations
    and confirmation emails to registrants.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeyregistrationsettings-put-openapi.md
- name: Go To Training - Get Start Url
  x-api-slug: organizersorganizerkeytrainingstrainingkeystarturl-get
  description: Returns a URL that can be used to start a training. When this URL is
    opened in a web browser, the GoToTraining client will be downloaded and launched
    and the training will start after the organizer logs in with its credentials.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeystarturl-get-openapi.md
- name: Go To Training - Update Training Times
  x-api-slug: organizersorganizerkeytrainingstrainingkeytimes-put
  description: A request to update a scheduled training's start and end times. If
    the request contains 'notifyTrainers = true' and 'notifyRegistrants = true', both
    organizers and registrants are notified. The response provides the number of notified
    trainers and registrants.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeytrainingstrainingkeytimes-put-openapi.md
- name: Go To Training - Get Sessions by Date Range
  x-api-slug: reportsorganizersorganizerkeysessions-post
  description: This call returns all session details over a given date range for a
    given organizer. A session is a completed training event.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/reportsorganizersorganizerkeysessions-post-openapi.md
- name: Go To Training - Get Attendance Details
  x-api-slug: reportsorganizersorganizerkeysessionssessionkeyattendees-get
  description: This call retrieves a list of registrants from a specific completed
    training session. The response includes the registrants' email addresses, and
    if they attended, it includes the duration of each period of their attendance
    in minutes, and the times at which they joined and left. If a registrant does
    not attend, they appear at the bottom of the listing with timeInSession = 0.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/reportsorganizersorganizerkeysessionssessionkeyattendees-get-openapi.md
- name: Go To Training - Get Sessions By Training
  x-api-slug: reportsorganizersorganizerkeytrainingstrainingkey-get
  description: This call returns session details for a given training. A session is
    a completed training event. Each training may contain one or more sessions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/reportsorganizersorganizerkeytrainingstrainingkey-get-openapi.md
- name: Go To Training - Get Online Recordings for Training
  x-api-slug: trainingstrainingkeyrecordings-get
  description: This call retrieves information on all online recordings for a given
    training. If there are none, it returns an empty list.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/trainingstrainingkeyrecordings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/trainingstrainingkeyrecordings-get-openapi.md
- name: Go To Training - Get Download for Online Recordings
  x-api-slug: trainingstrainingkeyrecordingsrecordingid-get
  description: This call provides the download for the given recording by returning
    a 302 redirect to the original file.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/trainingstrainingkeyrecordingsrecordingid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/trainingstrainingkeyrecordingsrecordingid-get-openapi.md
- name: Go To Training - Start Training
  x-api-slug: trainingstrainingkeystart-get
  description: Returns a URL that can be used to start a training. When this URL is
    opened in a web browser, the GoToTraining client will be downloaded and launched
    and the training will start. A login of the organizer is not required.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2T/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/trainingstrainingkeystart-get-openapi.md
- name: Go To Webinar - Get all webinars for an account
  x-api-slug: accountsaccountkeywebinars-get
  description: Retrieves the list of webinars for an account within a given date range.
    __*Page*__ and __*size*__ parameters are optional. Default __*page*__ is 0 and
    default __*size*__ is 20. For technical reasons, this call cannot be executed
    from this documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/accountsaccountkeywebinars-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/accountsaccountkeywebinars-get-openapi.md
- name: Go To Webinar - Get historical webinars
  x-api-slug: organizersorganizerkeyhistoricalwebinars-get
  description: Returns details for completed webinars for the specified organizer
    and completed webinars of other organizers where the specified organizer is a
    co-organizer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeyhistoricalwebinars-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeyhistoricalwebinars-get-openapi.md
- name: Go To Webinar - Get organizer sessions
  x-api-slug: organizersorganizerkeysessions-get
  description: Retrieve all completed sessions of all the webinars of a given organizer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeysessions-get-openapi.md
- name: Go To Webinar - Get upcoming webinars
  x-api-slug: organizersorganizerkeyupcomingwebinars-get
  description: Returns webinars scheduled for the future for the specified organizer
    and webinars of other organizers where the specified organizer is a co-organizer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeyupcomingwebinars-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeyupcomingwebinars-get-openapi.md
- name: Go To Webinar - Get all webinars
  x-api-slug: organizersorganizerkeywebinars-get
  description: Returns webinars scheduled for the future for a specified organizer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinars-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinars-get-openapi.md
- name: Go To Webinar - Create webinar
  x-api-slug: organizersorganizerkeywebinars-post
  description: 'Creates a single session webinar, a sequence of webinars or a series
    of webinars depending on the type field in the body: "single_session" creates
    a single webinar session, "sequence" creates a webinar with multiple meeting times
    where attendees are expected to be the same for all sessions, and "series" creates
    a webinar with multiple meetings times where attendees choose only one to attend.
    The default, if no type is declared, is single_session. A sequence webinar requires
    a "recurrenceStart" object consisting of a "startTime" and "endTime" key for the
    first webinar of the sequence, a "recurrencePattern" of "daily", "weekly", "monthly",
    and a "recurrenceEnd" which is the last date of the sequence (for example, 2016-12-01).
    A series webinar requires a "times" array with a discrete "startTime" and "endTime"
    for each webinar in the series. The call requires a webinar subject and description.
    The "isPasswordProtected" sets whether the webinar requires a password for attendees
    to join. If set to True, the organizer must go to Registration Settings at My
    Webinars (https://global.gotowebinar.com/webinars.tmpl) and add the password to
    the webinar, and send the password to the registrants. The response provides a
    numeric webinarKey in string format for the new webinar. Once a webinar has been
    created with this method, you can accept registrations.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinars-post-openapi.md
- name: Go To Webinar - Cancel webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-delete
  description: Cancels a specific webinar. If the webinar is a series or sequence,
    this call deletes all scheduled sessions. To send cancellation emails to registrants
    set sendCancellationEmails=true in the request. When the cancellation emails are
    sent, the default generated message is used in the cancellation email body.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-delete-openapi.md
- name: Go To Webinar - Get webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-get
  description: Retrieve information on a specific webinar. If the type of the webinar
    is 'sequence', a sequence of future times will be provided. Webinars of type 'series'
    are treated the same as normal webinars - each session in the webinar series has
    a different webinarKey. If an organizer cancels a webinar, then a request to get
    that webinar would return a '404 Not Found' error.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-get-openapi.md
- name: Go To Webinar - Update webinar
  x-api-slug: organizersorganizerkeywebinarswebinarkey-put
  description: Updates a webinar. The call requires at least one of the parameters
    in the request body. The request completely replaces the existing session, series,
    or sequence and so must include the full definition of each as for the Create
    call. Set notifyParticipants=true to send update emails to registrants.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkey-put-openapi.md
- name: Go To Webinar - Get attendees for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyattendees-get
  description: Returns all attendees for all sessions of the specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyattendees-get-openapi.md
- name: Go To Webinar - Get audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-get
  description: Retrieves the audio/conferencing information for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-get-openapi.md
- name: Go To Webinar - Update audio information
  x-api-slug: organizersorganizerkeywebinarswebinarkeyaudio-post
  description: Updates the audio/conferencing settings for a specific webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyaudio-post-openapi.md
- name: Go To Webinar - Get co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-get
  description: Returns the co-organizers for the specified webinar. The original organizer
    who created the webinar is filtered out of the list. If the webinar has no co-organizers,
    an empty array is returned. Co-organizers that do not have a GoToWebinar account
    are returned as external co-organizers. For those organizers no surname is returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-get-openapi.md
- name: Go To Webinar - Create co-organizers
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizers-post
  description: Creates co-organizers for the specified webinar. For co-organizers
    that have a GoToWebinar account you have to set the parameter 'external' to 'false'.
    In this case you have to pass the parameter 'organizerKey' only. For co-organizers
    that have no GoToWebinar account you have to set the parameter 'external' to 'true'.
    In this case you have to pass the parameters 'givenName' and 'email'. Since there
    is no parameter for 'surname' you should pass first and last name to the parameter
    'givenName'.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizers-post-openapi.md
- name: Go To Webinar - Delete co-organizer
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete
  description: Deletes an internal co-organizer specified by the coorganizerKey (memberKey).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkey-delete-openapi.md
- name: Go To Webinar - Resend invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post
  description: Resends an invitation email to the specified co-organizer
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeycoorganizerscoorganizerkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Get webinar meeting times
  x-api-slug: organizersorganizerkeywebinarswebinarkeymeetingtimes-get
  description: Retrieves the meeting times for a webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeymeetingtimes-get-openapi.md
- name: Go To Webinar - Get webinar panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-get
  description: Retrieves all the panelists for a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-get-openapi.md
- name: Go To Webinar - Create Panelists
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelists-post
  description: Create panelists for a specified webinar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelists-post-openapi.md
- name: Go To Webinar - Delete webinar panelist
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete
  description: Removes a webinar panelist.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkey-delete-openapi.md
- name: Go To Webinar - Resend panelist invitation
  x-api-slug: organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post
  description: Resend the panelist invitation email.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeypanelistspanelistkeyresendinvitation-post-openapi.md
- name: Go To Webinar - Get performance for all webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeyperformance-get
  description: Gets performance details for all sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyperformance-get-openapi.md
- name: Go To Webinar - Get registrants
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-get
  description: Retrieve registration details for all registrants of a specific webinar.
    Registrant details will not include all fields captured when creating the registrant.
    To see all data, use the API call 'Get Registrant'. Registrants can have one of
    the following states; <br>WAITING - registrant registered and is awaiting approval
    (where organizer has required approval), <br>APPROVED - registrant registered
    and is approved, and <br>DENIED - registrant registered and was denied.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-get-openapi.md
- name: Go To Webinar - Create registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrants-post
  description: 'Register an attendee for a scheduled webinar. The response contains
    the registrantKey and join URL for the registrant. An email will be sent to the
    registrant unless the organizer turns off the confirmation email setting from
    the GoToWebinar website. Please note that you must provide all required fields
    including custom fields defined during the webinar creation. Use the API call
    ''Get registration fields'' to get a list of all fields, if they are required,
    and their possible values. At this time there are two versions of the ''Create
    Registrant'' call. The first version only accepts firstName, lastName, and email
    and ignores all other fields. If you have custom fields or want to capture additional
    information this version won''t work for you. The second version allows you to
    pass all required and optional fields, including custom fields defined when creating
    the webinar. To use the second version you must pass the header value ''Accept:
    application/vnd.citrix.g2wapi-v1.1+json'' instead of ''Accept: application/json''.
    Leaving this header out results in the first version of the API call.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrants-post-openapi.md
- name: Go To Webinar - Get registration fields
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsfields-get
  description: Retrieve required, optional registration, and custom questions for
    a specified webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsfields-get-openapi.md
- name: Go To Webinar - Delete registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete
  description: Removes a webinar registrant from current registrations for the specified
    webinar. The webinar must be a scheduled, future webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-delete-openapi.md
- name: Go To Webinar - Get registrant
  x-api-slug: organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get
  description: Retrieve registration details for a specific registrant.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeyregistrantsregistrantkey-get-openapi.md
- name: Go To Webinar - Get webinar sessions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessions-get
  description: Retrieves details for all past sessions of a specific webinar.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessions-get-openapi.md
- name: Go To Webinar - Get webinar session
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkey-get
  description: Retrieves attendance details for a specific webinar session that has
    ended. If attendees attended the session ('registrantsAttended'), specific attendance
    details, such as attendenceTime for a registrant, will also be retrieved. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkey-get-openapi.md
- name: Go To Webinar - Get session attendees
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get
  description: Retrieve details for all attendees of a specific webinar session. For
    technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendees-get-openapi.md
- name: Go To Webinar - Get attendee
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get
  description: Retrieve registration details for a particular attendee of a specific
    webinar session. For technical reasons, this call cannot be executed from this
    documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkey-get-openapi.md
- name: Go To Webinar - Get attendee poll answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get
  description: Get poll answers from a particular attendee of a specific webinar session.
    For technical reasons, this call cannot be executed from this documentation. Please
    use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeypolls-get-openapi.md
- name: Go To Webinar - Get attendee questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get
  description: Get questions asked by an attendee during a webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeyquestions-get-openapi.md
- name: Go To Webinar - Get attendee survey answers
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get
  description: Retrieve survey answers from a particular attendee during a webinar
    session. For technical reasons, this call cannot be executed from this documentation.
    Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyattendeesregistrantkeysurveys-get-openapi.md
- name: Go To Webinar - Get session performance
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get
  description: Get performance details for a session. For technical reasons, this
    call cannot be executed from this documentation. Please use the curl command to
    execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyperformance-get-openapi.md
- name: Go To Webinar - Get session polls
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get
  description: Retrieve all collated attendee questions and answers for polls from
    a specific webinar session. For technical reasons, this call cannot be executed
    from this documentation. Please use the curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeypolls-get-openapi.md
- name: Go To Webinar - Get session questions
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get
  description: Retrieve questions and answers for a past webinar session. For technical
    reasons, this call cannot be executed from this documentation. Please use the
    curl command to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeyquestions-get-openapi.md
- name: Go To Webinar - Get session surveys
  x-api-slug: organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get
  description: Retrieve surveys for a past webinar session. For technical reasons,
    this call cannot be executed from this documentation. Please use the curl command
    to execute it.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//G2W/rest
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/organizersorganizerkeywebinarswebinarkeysessionssessionkeysurveys-get-openapi.md
- name: SCIM - Get Groups
  x-api-slug: groups-get
  description: Queries multiple group identities in the organization domain. Filtering,
    sorting and pagination are available. This call requires the role ROLE_ORG_READ.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groups-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groups-get-openapi.md
- name: SCIM - Create Group
  x-api-slug: groups-post
  description: Creates a new organization group and adds it to the user domain. Member
    groups and member users must be in the organization. This call requires the role
    ROLE_ORG_WRITE.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groups-post-openapi.md
- name: SCIM - Delete Group
  x-api-slug: groupsgroupkey-delete
  description: Deletes a group from the organization (but not from the account). The
    group must be in the organization. This call requires the role ROLE_ORG_WRITE.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkey-delete-openapi.md
- name: SCIM - Get Group
  x-api-slug: groupsgroupkey-get
  description: Queries group details in the organization domain. This call requires
    the role ROLE_ORG_READ.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkey-get-openapi.md
- name: SCIM - Update Group
  x-api-slug: groupsgroupkey-patch
  description: Updates one or more values of an existing group without sending the
    full definition. Member groups and member users must be in the organization. This
    call requires the role ROLE_ORG_WRITE.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkey-patch-openapi.md
- name: SCIM - Replace Group
  x-api-slug: groupsgroupkey-put
  description: Updates an existing group. The request must include the full group
    definition. To modify one or more values without sending the full definition,
    see "Update Group". Member groups and member users must be in the organization.
    This call requires the role ROLE_ORG_WRITE.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/groupsgroupkey-put-openapi.md
- name: SCIM - Get User Schema
  x-api-slug: schemasusers-get
  description: Queries the user schema. The user schema is defined in SCIM Core Schema
    (http://www.simplecloud.info/specs/draft-scim-core-schema-01.html#resource-schema).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/schemasusers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/schemasusers-get-openapi.md
- name: SCIM - Get Service Provider Configurations
  x-api-slug: serviceproviderconfigs-get
  description: Queries service provider configurations. The service provider configurations
    are defined in SCIM Core Schema (http://www.simplecloud.info/specs/draft-scim-core-schema-01.html#anchor6).
    This call returns a description, a documentationURL, name, and specURL.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/serviceproviderconfigs-get-openapi.md
- name: SCIM - Get Users
  x-api-slug: users-get
  description: Queries multiple user identities in the organization domain. Filtering
    is available.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/users-get-openapi.md
- name: SCIM - Create User
  x-api-slug: users-post
  description: Creates a new organization user and adds them to the user domain. The
    user email domain must match an existing organization email domain.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/users-post-openapi.md
- name: SCIM - Get Current User
  x-api-slug: usersme-get
  description: Queries the identity of the current authenticated user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/usersme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/usersme-get-openapi.md
- name: SCIM - Update Current User
  x-api-slug: usersme-patch
  description: Changes a limited set (or all if you choose) of the current authenticated
    user's data. The updated user email domain must be an existing organization email
    domain.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/usersme-patch-openapi.md
- name: SCIM - Replace Current User
  x-api-slug: usersme-put
  description: Changes the current authenticated user's displayName, locale, timezone,
    username and password. The request must include the full user definition (to modify
    one or more values without sending the full definition, see Update User). The
    replaced user email domain must be an existing organization email domain.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/usersme-put-openapi.md
- name: SCIM - Delete User
  x-api-slug: usersuserkey-delete
  description: Deletes a user from the organization (but not from the account).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/usersuserkey-delete-openapi.md
- name: SCIM - Get User
  x-api-slug: usersuserkey-get
  description: Queries user identity in the organization domain.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/usersuserkey-get-openapi.md
- name: SCIM - Update User
  x-api-slug: usersuserkey-patch
  description: Changes a limited set (or all if you choose) of the user's data. The
    updated user email domain must be an existing organization email domain.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/usersuserkey-patch-openapi.md
- name: SCIM - Replace User
  x-api-slug: usersuserkey-put
  description: Changes an existing user's displayName, locale, timezone, username
    and password. The request must include the full user definition (to modify one
    or more values without sending the full definition, see Update User). The replaced
    user email domain must be an existing organization email domain.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/731-gotomeeting.jpg
  humanURL: https://citrixonline.com
  baseURL: https://api.citrixonline.com//identity/v1
  tags: Office, Meetings, Collaboration, Video Conferencing, Video Conferencing, SaaS,
    Technology, Enterprise, API Provider, Meetings, Profiles, Conferences, Relative
    Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/gotomeeting/master/_listings/gotomeeting/usersuserkey-put-openapi.md
x-common:
- type: x-api-gallery
  url: http://google.url.shortener.api.gallery.streamdata.io
- type: x-api-stack
  url: http://gotomeeting.stack.network
- type: x-base
  url: https://api.citrixonline.com
- type: x-blog
  url: http://blogs.citrix.com/
- type: x-crunchbase
  url: https://crunchbase.com/organization/citrix-systems
- type: x-crunchbase
  url: http://www.crunchbase.com/company/citrix-systems
- type: x-developer
  url: https://developer.citrixonline.com/
- type: x-email
  url: secure@citrix.com
- type: x-email
  url: americasconsulting@citrix.com
- type: x-email
  url: poland@citrix.com
- type: x-email
  url: citrix_ru@citrix.com
- type: x-email
  url: Licensing-emea@eu.citrix.com
- type: x-email
  url: eduardo.fleites@citrix.com
- type: x-email
  url: CitrixReady@citrix.com
- type: x-email
  url: CSP@citrix.com
- type: x-email
  url: partneroperationsEMEA@eu.citrix.com
- type: x-github
  url: https://github.com/citrix
- type: x-twitter
  url: https://twitter.com/gotomeeting
- type: x-twitter
  url: https://twitter.com/citrix
- type: x-website
  url: https://citrixonline.com
- type: x-website
  url: http://citrixonline.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---