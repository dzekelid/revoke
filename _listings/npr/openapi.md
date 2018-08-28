swagger: "2.0"
x-collection-name: NPR
x-complete: 1
info:
  title: NPR One API Reference
  description: npr-one-is-a-smart-application-that-brings-the-best-of-npr-and-member-station-programming-newscasts-podcasts-and-stories-together-to-create-a-new-experience-for-listening--it-provides-an-editorcurated-and-localized-mobile-listening-experience-based-on-the-content-the-listener-chooses-likes-shares-and-enjoys--the-api-provides-all-of-the-content-and-customization-in-a-simple-structured-way-that-is-easy-for-applicationdevelopers-to-implement-
  termsOfService: http://dev.npr.org/develop/terms-of-use
  contact:
    name: NPR One Enterprise Team
    url: http://dev.npr.org
    email: NPROneEnterprise@npr.org
  version: 1.0.0
host: api.npr.org
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /authorization/v2/token/revoke:
    post:
      summary: Revoke an existing OAuth2 access token
      description: |-
        Our implementation follows the proposed IETF specification [RFC-7009](https://tools.ietf.org/html/rfc7009).

        If your client application offers the ability to for a logged-in user to log out, and you have access to a long-lived
        `client_credentials` token (i.e. you have generated one that you are storing securely for the lifetime of the entire app
        install), we suggest (but do not require) that you call this endpoint and revoke the access token belonging to the
        logged-in user as part of your logout process. If you do not already have a long-lived `client_credentials` token,
        please don't generate one just for the purposes of calling this endpoint.

        If you are building a prototype application, we also recommend that you use this endpoint to clean up access tokens
        that you generate during the testing of your app and do not intend to reuse.

        Note that revoking an access token will automatically revoke any refresh tokens associated with it, and vice-versa.
      operationId: revokeToken
      x-api-path-slug: authorizationv2tokenrevoke-post
      parameters:
      - in: header
        name: Authorization
        description: A `client_credentials` access token from the same client application
          as the token being revoked
      - in: formData
        name: token
        description: The access token or refresh token that the client wants to have
          revoked
      - in: formData
        name: token_type_hint
        description: A hint about the type of the token submitted for revocation
      responses:
        200:
          description: OK
      tags:
      - News
      - Authorization
      - Token
      - Revoke