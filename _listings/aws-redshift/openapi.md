---
swagger: "2.0"
x-collection-name: AWS Redshift
x-complete: 1
info:
  title: AWS Redshift API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=RevokeClusterSecurityGroupIngress:
    get:
      summary: Revoke Cluster Security Group Ingress
      description: |-
        Revokes an ingress rule in an Amazon Redshift security group for a previously authorized
                    IP range or Amazon EC2 security group.
      operationId: revokeClusterSecurityGroupIngress
      x-api-path-slug: actionrevokeclustersecuritygroupingress-get
      parameters:
      - in: query
        name: CIDRIP
        description: The IP range for which to revoke access
        type: string
      - in: query
        name: ClusterSecurityGroupName
        description: The name of the security Group from which to revoke the ingress
          rule
        type: string
      - in: query
        name: EC2SecurityGroupName
        description: The name of the EC2 Security Group whose access is to be revoked
        type: string
      - in: query
        name: EC2SecurityGroupOwnerId
        description: The AWS account number of the owner of the security group specified
          in the                EC2SecurityGroupName parameter
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cluster Security Group
  /?Action=RevokeSnapshotAccess:
    get:
      summary: Revoke Snapshot Access
      description: |-
        Removes the ability of the specified AWS customer account to restore the specified
                    snapshot.
      operationId: revokeSnapshotAccess
      x-api-path-slug: actionrevokesnapshotaccess-get
      parameters:
      - in: query
        name: AccountWithRestoreAccess
        description: The identifier of the AWS customer account that can no longer
          restore the specified            snapshot
        type: string
      - in: query
        name: SnapshotClusterIdentifier
        description: The identifier of the cluster the snapshot was created from
        type: string
      - in: query
        name: SnapshotIdentifier
        description: The identifier of the snapshot that the account can no longer
          access
        type: string
      responses:
        200:
          description: OK
      tags:
      - Snapshots
---