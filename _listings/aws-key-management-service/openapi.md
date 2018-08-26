---
swagger: "2.0"
x-collection-name: AWS Key Management Service
x-complete: 1
info:
  title: AWS Key Management Service API
  version: 1.0.0
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
---