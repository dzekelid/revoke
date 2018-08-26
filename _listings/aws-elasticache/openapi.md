---
swagger: "2.0"
x-collection-name: AWS ElastiCache
x-complete: 1
info:
  title: AWS ElastiCache API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=RevokeCacheSecurityGroupIngress:
    get:
      summary: Revoke Cache Security Group Ingress
      description: |-
        Revokes ingress from a cache
                    security group.
      operationId: revokeCacheSecurityGroupIngress
      x-api-path-slug: actionrevokecachesecuritygroupingress-get
      parameters:
      - in: query
        name: CacheSecurityGroupName
        description: The name of the cache security group to revoke ingress from
        type: string
      - in: query
        name: EC2SecurityGroupName
        description: The name of the Amazon EC2 security group to revoke access from
        type: string
      - in: query
        name: EC2SecurityGroupOwnerId
        description: The AWS account number of the Amazon EC2 security group owner
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cache Security Groups
---