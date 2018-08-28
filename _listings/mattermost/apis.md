---
name: Mattermost
x-slug: mattermost
description: Open source, private cloud Slack-alternative, Workplace messaging for
  web, PCs and phones. MIT-licensed. Hundreds of contributors. 14 languages. Secure,
  configurable, and scalable from teams to the enterprise.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
x-kinRank: "8"
x-alexaRank: "95684"
tags: Revoke
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/revoke/master/_listings/mattermost/apis.md
specificationVersion: "0.14"
apis:
- name: Mattermost API Reference - Revoke a user session
  x-api-slug: usersuser-idsessionsrevoke-post
  description: |-
    Revokes a user session from the provided user id and session id strings.
    ##### Permissions
    Must be logged in as the user being updated or have the `edit_other_users` permission.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4
  tags: Enterprise, SaaS, Technology, Cloud, API Provider, API Service Provider, Profiles,
    Relative Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/revoke/master/_listings/mattermost/usersuser-idsessionsrevoke-post-openapi.md
- name: Mattermost API Reference - Revoke all active sessions for a user
  x-api-slug: usersuser-idsessionsrevokeall-post
  description: |-
    Revokes all user sessions from the provided user id and session id strings.
    ##### Permissions
    Must be logged in as the user being updated or have the `edit_other_users` permission.
    __Minimum server version__: 4.4
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4
  tags: Enterprise, SaaS, Technology, Cloud, API Provider, API Service Provider, Profiles,
    Relative Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/revoke/master/_listings/mattermost/usersuser-idsessionsrevokeall-post-openapi.md
- name: Mattermost API Reference - Revoke a user access token
  x-api-slug: userstokensrevoke-post
  description: |-
    Revoke a user access token and delete any sessions using the token.

    __Minimum server version__: 4.1

    ##### Permissions
    Must have `revoke_user_access_token` permission. For non-self requests, must also have the `edit_other_users` permission.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4
  tags: Enterprise, SaaS, Technology, Cloud, API Provider, API Service Provider, Profiles,
    Relative Data, Service API, Networks
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/revoke/master/_listings/mattermost/userstokensrevoke-post-openapi.md
x-common:
- type: x-api-gallery
  url: http://matrix.api.gallery.streamdata.io
- type: x-api-stack
  url: http://mattermost.stack.network
- type: x-blog
  url: https://about.mattermost.com/blog/
- type: x-blog-rss
  url: https://about.mattermost.com/feed/
- type: x-crunchbase
  url: https://crunchbase.com/organization/mattermost
- type: x-developer
  url: https://api.mattermost.com/
- type: x-github
  url: https://github.com/mattermost
- type: x-pricing
  url: https://about.mattermost.com/pricing/
- type: x-security
  url: https://docs.mattermost.com/overview/security.html
- type: x-twitter
  url: https://twitter.com/mattermosthq
- type: x-website
  url: https://mattermost.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---