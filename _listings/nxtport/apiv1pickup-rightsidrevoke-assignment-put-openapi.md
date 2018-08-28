---
swagger: "2.0"
x-collection-name: NxtPort
x-complete: 0
info:
  title: NxtPort T-mining Secure Container Release API Revoke Assignment
  description: Revoke the current PickupRight assignment. This must be used in case
    you did an assign of a PickupRight to a driver and you want to cancel this. This
    action is only possible as long as the PickupRight is not exercised.
  contact:
    name: T-Mining API support
    url: http://support.t-mining.be/
    email: support@t-mining.be
  version: 1.0.0
host: api.nxtport.eu
basePath: /blockchain
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/pickup_rights/{id}/revoke_assignment:
    put:
      summary: Revoke Assignment
      description: Revoke the current PickupRight assignment. This must be used in
        case you did an assign of a PickupRight to a driver and you want to cancel
        this. This action is only possible as long as the PickupRight is not exercised.
      operationId: putApiV1PickupRightsRevokeAssignment
      x-api-path-slug: apiv1pickup-rightsidrevoke-assignment-put
      parameters:
      - in: query
        name: api_token
        description: authentication token of user making the request
      - in: path
        name: id
        description: id of the PickupRight as reported by List PickupRights
      responses:
        200:
          description: OK
      tags:
      - Revoke
      - Assignment
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