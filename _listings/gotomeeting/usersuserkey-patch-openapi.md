---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: SCIM Update User
  description: Changes a limited set (or all if you choose) of the user's data. The
    updated user email domain must be an existing organization email domain.
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
  /Schemas/Users:
    get:
      summary: Get User Schema
      description: Queries the user schema. The user schema is defined in SCIM Core
        Schema (http://www.simplecloud.info/specs/draft-scim-core-schema-01.html#resource-schema).
      operationId: getUserSchema
      x-api-path-slug: schemasusers-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Schemas
      - Users
  /ServiceProviderConfigs:
    get:
      summary: Get Service Provider Configurations
      description: Queries service provider configurations. The service provider configurations
        are defined in SCIM Core Schema (http://www.simplecloud.info/specs/draft-scim-core-schema-01.html#anchor6).
        This call returns a description, a documentationURL, name, and specURL.
      operationId: getServiceProviderConfigs
      x-api-path-slug: serviceproviderconfigs-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - ServiceProviderConfigs
  /Users:
    get:
      summary: Get Users
      description: Queries multiple user identities in the organization domain. Filtering
        is available.
      operationId: getUsers
      x-api-path-slug: users-get
      parameters:
      - in: query
        name: filter
        description: Without a filter, all users in a user domain are returned
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Users
    post:
      summary: Create User
      description: Creates a new organization user and adds them to the user domain.
        The user email domain must match an existing organization email domain.
      operationId: createUsers
      x-api-path-slug: users-post
      parameters:
      - in: body
        name: body
        description: The details of the user to create
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Users
  /Users/me:
    get:
      summary: Get Current User
      description: Queries the identity of the current authenticated user.
      operationId: getMe
      x-api-path-slug: usersme-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Users
      - Me
    patch:
      summary: Update Current User
      description: Changes a limited set (or all if you choose) of the current authenticated
        user's data. The updated user email domain must be an existing organization
        email domain.
      operationId: updateMe
      x-api-path-slug: usersme-patch
      parameters:
      - in: body
        name: body
        description: The new user data
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Users
      - Me
    put:
      summary: Replace Current User
      description: Changes the current authenticated user's displayName, locale, timezone,
        username and password. The request must include the full user definition (to
        modify one or more values without sending the full definition, see Update
        User). The replaced user email domain must be an existing organization email
        domain.
      operationId: replaceMe
      x-api-path-slug: usersme-put
      parameters:
      - in: body
        name: body
        description: The new user data
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Users
      - Me
  /Users/{userKey}:
    delete:
      summary: Delete User
      description: Deletes a user from the organization (but not from the account).
      operationId: deleteUser
      x-api-path-slug: usersuserkey-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Users
      - UserKey
    get:
      summary: Get User
      description: Queries user identity in the organization domain.
      operationId: getUser
      x-api-path-slug: usersuserkey-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Users
      - UserKey
    patch:
      summary: Update User
      description: Changes a limited set (or all if you choose) of the user's data.
        The updated user email domain must be an existing organization email domain.
      operationId: updateUser
      x-api-path-slug: usersuserkey-patch
      parameters:
      - in: body
        name: body
        description: The new user data
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Users
      - UserKey
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