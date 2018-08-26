---
swagger: "2.0"
x-collection-name: AWS Key Management Service
x-complete: 0
info:
  title: AWS Key Management Service API Revoke Grant
  version: 1.0.0
  description: Revokes a grant.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=RevokeGrant:
    get:
      summary: Revoke Grant
      description: Revokes a grant.
      operationId: revokeGrant
      x-api-path-slug: actionrevokegrant-get
      parameters:
      - in: query
        name: GrantId
        description: Identifier of the grant to be revoked
        type: string
      - in: query
        name: KeyId
        description: A unique identifier for the customer master key associated with
          the grant
        type: string
      responses:
        200:
          description: OK
      tags:
      - Grants
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