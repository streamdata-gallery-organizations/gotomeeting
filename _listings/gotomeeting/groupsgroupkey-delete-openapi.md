---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: SCIM Delete Group
  description: Deletes a group from the organization (but not from the account). The
    group must be in the organization. This call requires the role ROLE_ORG_WRITE.
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: N/A
host: api.citrixonline.com
basePath: /identity/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Groups:
    get:
      summary: Get Groups
      description: Queries multiple group identities in the organization domain. Filtering,
        sorting and pagination are available. This call requires the role ROLE_ORG_READ.
      operationId: getGroups
      x-api-path-slug: groups-get
      parameters:
      - in: query
        name: filter
        description: Without a filter, all groups are returned
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
    post:
      summary: Create Group
      description: Creates a new organization group and adds it to the user domain.
        Member groups and member users must be in the organization. This call requires
        the role ROLE_ORG_WRITE.
      operationId: createGroup
      x-api-path-slug: groups-post
      parameters:
      - in: body
        name: body
        description: The details of the group to create
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
  /Groups/{groupKey}:
    delete:
      summary: Delete Group
      description: Deletes a group from the organization (but not from the account).
        The group must be in the organization. This call requires the role ROLE_ORG_WRITE.
      operationId: deleteGroup
      x-api-path-slug: groupsgroupkey-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
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