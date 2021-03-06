---
swagger: "2.0"
x-collection-name: Google Tag Manager
x-complete: 0
info:
  title: Google Tag Manager API Get User
  description: Gets a user's Account & Container Permissions.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /tagmanager/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /accounts/{accountId}/containers/{containerId}/versions:
    get:
      summary: Get Container Versions
      description: Lists all Container Versions of a GTM Container.
      operationId: tagmanager.accounts.containers.versions.list
      x-api-path-slug: accountsaccountidcontainerscontaineridversions-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      - in: query
        name: headers
        description: Retrieve headers only when true
      - in: query
        name: includeDeleted
        description: Also retrieve deleted (archived) versions when true
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Versions
    post:
      summary: Create Container Version
      description: Creates a Container Version.
      operationId: tagmanager.accounts.containers.versions.create
      x-api-path-slug: accountsaccountidcontainerscontaineridversions-post
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: containerId
        description: The GTM Container ID
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Versions
  /accounts/{accountId}/containers/{containerId}/versions/{containerVersionId}:
    delete:
      summary: Delete Container Version
      description: Deletes a Container Version.
      operationId: tagmanager.accounts.containers.versions.delete
      x-api-path-slug: accountsaccountidcontainerscontaineridversionscontainerversionid-delete
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      - in: path
        name: containerVersionId
        description: The GTM Container Version ID
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Versions
    get:
      summary: Get Container Version
      description: Gets a Container Version.
      operationId: tagmanager.accounts.containers.versions.get
      x-api-path-slug: accountsaccountidcontainerscontaineridversionscontainerversionid-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      - in: path
        name: containerVersionId
        description: The GTM Container Version ID
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Versions
    put:
      summary: Update Container Version
      description: Updates a Container Version.
      operationId: tagmanager.accounts.containers.versions.update
      x-api-path-slug: accountsaccountidcontainerscontaineridversionscontainerversionid-put
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: containerId
        description: The GTM Container ID
      - in: path
        name: containerVersionId
        description: The GTM Container Version ID
      - in: query
        name: fingerprint
        description: When provided, this fingerprint must match the fingerprint of
          the container version in storage
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Versions
  /accounts/{accountId}/containers/{containerId}/versions/{containerVersionId}/publish:
    post:
      summary: Publish Container Version
      description: Publishes a Container Version.
      operationId: tagmanager.accounts.containers.versions.publish
      x-api-path-slug: accountsaccountidcontainerscontaineridversionscontainerversionidpublish-post
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      - in: path
        name: containerVersionId
        description: The GTM Container Version ID
      - in: query
        name: fingerprint
        description: When provided, this fingerprint must match the fingerprint of
          the container version in storage
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Versions
  /accounts/{accountId}/containers/{containerId}/versions/{containerVersionId}/restore:
    post:
      summary: Restore Container Version
      description: Restores a Container Version. This will overwrite the container's
        current configuration (including its variables, triggers and tags). The operation
        will not have any effect on the version that is being served (i.e. the published
        version).
      operationId: tagmanager.accounts.containers.versions.restore
      x-api-path-slug: accountsaccountidcontainerscontaineridversionscontainerversionidrestore-post
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      - in: path
        name: containerVersionId
        description: The GTM Container Version ID
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Versions
  /accounts/{accountId}/containers/{containerId}/versions/{containerVersionId}/undelete:
    post:
      summary: Undelete Container Version
      description: Undeletes a Container Version.
      operationId: tagmanager.accounts.containers.versions.undelete
      x-api-path-slug: accountsaccountidcontainerscontaineridversionscontainerversionidundelete-post
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      - in: path
        name: containerVersionId
        description: The GTM Container Version ID
      responses:
        200:
          description: OK
      tags:
      - Containers
      - Versions
  /accounts/{accountId}/containers:
    get:
      summary: Get Conainers
      description: Lists all Containers that belongs to a GTM Account.
      operationId: tagmanager.accounts.containers.list
      x-api-path-slug: accountsaccountidcontainers-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      responses:
        200:
          description: OK
      tags:
      - Container
    post:
      summary: Create Container
      description: Creates a Container.
      operationId: tagmanager.accounts.containers.create
      x-api-path-slug: accountsaccountidcontainers-post
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Container
  /accounts/{accountId}/containers/{containerId}:
    delete:
      summary: Delete Container
      description: Deletes a Container.
      operationId: tagmanager.accounts.containers.delete
      x-api-path-slug: accountsaccountidcontainerscontainerid-delete
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      responses:
        200:
          description: OK
      tags:
      - Container
    get:
      summary: Get Container
      description: Gets a Container.
      operationId: tagmanager.accounts.containers.get
      x-api-path-slug: accountsaccountidcontainerscontainerid-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      responses:
        200:
          description: OK
      tags:
      - Container
    put:
      summary: Update Container
      description: Updates a Container.
      operationId: tagmanager.accounts.containers.update
      x-api-path-slug: accountsaccountidcontainerscontainerid-put
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: containerId
        description: The GTM Container ID
      - in: query
        name: fingerprint
        description: When provided, this fingerprint must match the fingerprint of
          the container in storage
      responses:
        200:
          description: OK
      tags:
      - Container
  /accounts/{accountId}/containers/{containerId}/environments:
    get:
      summary: Get GTM Environments
      description: Lists all GTM Environments of a GTM Container.
      operationId: tagmanager.accounts.containers.environments.list
      x-api-path-slug: accountsaccountidcontainerscontaineridenvironments-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      responses:
        200:
          description: OK
      tags:
      - GTM Environment
  /accounts/{accountId}/containers/{containerId}/folders:
    get:
      summary: Get GTM Folders
      description: Lists all GTM Folders of a Container.
      operationId: tagmanager.accounts.containers.folders.list
      x-api-path-slug: accountsaccountidcontainerscontaineridfolders-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      responses:
        200:
          description: OK
      tags:
      - GTM Folder
  /accounts/{accountId}/containers/{containerId}/tags:
    get:
      summary: Get GTM Tags
      description: Lists all GTM Tags of a Container.
      operationId: tagmanager.accounts.containers.tags.list
      x-api-path-slug: accountsaccountidcontainerscontaineridtags-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      responses:
        200:
          description: OK
      tags:
      - GTM Tag
  /accounts/{accountId}/containers/{containerId}/triggers:
    get:
      summary: Get GTM Triggers
      description: Lists all GTM Triggers of a Container.
      operationId: tagmanager.accounts.containers.triggers.list
      x-api-path-slug: accountsaccountidcontainerscontaineridtriggers-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      responses:
        200:
          description: OK
      tags:
      - GTM Trigger
  /accounts/{accountId}/containers/{containerId}/variables:
    get:
      summary: Get GTM Variables
      description: Lists all GTM Variables of a Container.
      operationId: tagmanager.accounts.containers.variables.list
      x-api-path-slug: accountsaccountidcontainerscontaineridvariables-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: containerId
        description: The GTM Container ID
      responses:
        200:
          description: OK
      tags:
      - GTM Variable
  /accounts/{accountId}/permissions:
    get:
      summary: Get User Permissions
      description: List all users that have access to the account along with Account
        and Container Permissions granted to each of them.
      operationId: tagmanager.accounts.permissions.list
      x-api-path-slug: accountsaccountidpermissions-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      responses:
        200:
          description: OK
      tags:
      - User Permission
    post:
      summary: Create User Permission
      description: Creates a user's Account & Container Permissions.
      operationId: tagmanager.accounts.permissions.create
      x-api-path-slug: accountsaccountidpermissions-post
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - User Permission
  /accounts/{accountId}/permissions/{permissionId}:
    get:
      summary: Get User
      description: Gets a user's Account & Container Permissions.
      operationId: tagmanager.accounts.permissions.get
      x-api-path-slug: accountsaccountidpermissionspermissionid-get
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: path
        name: permissionId
        description: The GTM User ID
      responses:
        200:
          description: OK
      tags:
      - User
    put:
      summary: Update User
      description: Updates a user's Account & Container Permissions.
      operationId: tagmanager.accounts.permissions.update
      x-api-path-slug: accountsaccountidpermissionspermissionid-put
      parameters:
      - in: path
        name: accountId
        description: The GTM Account ID
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: permissionId
        description: The GTM User ID
      responses:
        200:
          description: OK
      tags:
      - User
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