---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: SCIM Replace Group
  description: Updates an existing group. The request must include the full group
    definition. To modify one or more values without sending the full definition,
    see "Update Group". Member groups and member users must be in the organization.
    This call requires the role ROLE_ORG_WRITE.
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
    get:
      summary: Get Group
      description: Queries group details in the organization domain. This call requires
        the role ROLE_ORG_READ.
      operationId: getGroup
      x-api-path-slug: groupsgroupkey-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Groups
      - GroupKey
    patch:
      summary: Update Group
      description: Updates one or more values of an existing group without sending
        the full definition. Member groups and member users must be in the organization.
        This call requires the role ROLE_ORG_WRITE.
      operationId: updateGroup
      x-api-path-slug: groupsgroupkey-patch
      parameters:
      - in: body
        name: body
        description: The group data to update
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
    put:
      summary: Replace Group
      description: Updates an existing group. The request must include the full group
        definition. To modify one or more values without sending the full definition,
        see "Update Group". Member groups and member users must be in the organization.
        This call requires the role ROLE_ORG_WRITE.
      operationId: replaceGroup
      x-api-path-slug: groupsgroupkey-put
      parameters:
      - in: body
        name: body
        description: The new group definition
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