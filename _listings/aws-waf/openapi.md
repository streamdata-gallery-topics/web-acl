---
swagger: "2.0"
x-collection-name: AWS WAF
x-complete: 1
info:
  title: AWS WAF API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AssociateWebACL:
    get:
      summary: Associate Web ACL
      description: 'Service: AWS WAF RegionalAssociates a web ACL with a resource.'
      operationId: associateWebACL
      x-api-path-slug: actionassociatewebacl-get
      parameters:
      - in: query
        name: ResourceArn
        description: The ARN (Amazon Resource Name) of the resource to be protected
        type: string
      - in: query
        name: WebACLId
        description: A unique identifier (ID) for the web ACL
        type: string
      responses:
        200:
          description: OK
      tags:
      - Web ACL
  /?Action=CreateWebACL:
    get:
      summary: Create Web ACL
      description: 'Service: AWS WAFCreates a WebACL, which contains the Rules that
        identify the CloudFront web requests that you want to allow, block, or count.'
      operationId: createWebACL
      x-api-path-slug: actioncreatewebacl-get
      parameters:
      - in: query
        name: ChangeToken
        description: The value returned by the most recent call to GetChangeToken
        type: string
      - in: query
        name: DefaultAction
        description: The action that you want  AWS WAF to take when a request doesnt
          match the criteria specified in any of the Rule objects that are associated
          with the WebACL
        type: string
      - in: query
        name: MetricName
        description: A friendly name or description for the metrics for this WebACL
        type: string
      - in: query
        name: Name
        description: A friendly name or description of the WebACL
        type: string
      responses:
        200:
          description: OK
      tags:
      - Web ACL
  /?Action=DeleteWebACL:
    get:
      summary: Delete Web ACL
      description: 'Service: AWS WAFPermanently deletes a.'
      operationId: deleteWebACL
      x-api-path-slug: actiondeletewebacl-get
      parameters:
      - in: query
        name: ChangeToken
        description: The value returned by the most recent call to GetChangeToken
        type: string
      - in: query
        name: WebACLId
        description: The WebACLId of the WebACL that you want to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Web ACL
  /?Action=DisassociateWebACL:
    get:
      summary: Disassociate Web ACL
      description: 'Service: AWS WAF RegionalRemoves a web ACL from the specified
        resource.'
      operationId: disassociateWebACL
      x-api-path-slug: actiondisassociatewebacl-get
      parameters:
      - in: query
        name: ResourceArn
        description: The ARN (Amazon Resource Name) of the resource from which the
          web ACL is being removed
        type: string
      responses:
        200:
          description: OK
      tags:
      - Web ACL
  /?Action=GetWebACL:
    get:
      summary: Get Web ACL
      description: 'Service: AWS WAFReturns the.'
      operationId: getWebACL
      x-api-path-slug: actiongetwebacl-get
      parameters:
      - in: query
        name: WebACLId
        description: The WebACLId of the WebACL that you want to get
        type: string
      responses:
        200:
          description: OK
      tags:
      - Web ACL
  /?Action=GetWebACLForResource:
    get:
      summary: Get Web ACLFor Resource
      description: 'Service: AWS WAF RegionalReturns the web ACL for the specified
        resource.'
      operationId: getWebACLForResource
      x-api-path-slug: actiongetwebaclforresource-get
      parameters:
      - in: query
        name: ResourceArn
        description: The ARN (Amazon Resource Name) of the resource for which to get
          the web ACL
        type: string
      responses:
        200:
          description: OK
      tags:
      - Web ACL
  /?Action=ListResourcesForWebACL:
    get:
      summary: List Resources For Web ACL
      description: 'Service: AWS WAF RegionalReturns an array of resources associated
        with the specified web ACL.'
      operationId: listResourcesForWebACL
      x-api-path-slug: actionlistresourcesforwebacl-get
      parameters:
      - in: query
        name: WebACLId
        description: The unique identifier (ID) of the web ACL for which to list the
          associated resources
        type: string
      responses:
        200:
          description: OK
      tags:
      - Web ACL
  /?Action=ListWebACLs:
    get:
      summary: List Web ACLs
      description: 'Service: AWS WAFReturns an array of.'
      operationId: listWebACLs
      x-api-path-slug: actionlistwebacls-get
      parameters:
      - in: query
        name: Limit
        description: Specifies the number of WebACL objects that you want AWS WAF
          to return for this request
        type: string
      - in: query
        name: NextMarker
        description: If you specify a value for Limit and you have more WebACL objects
          than the number that you specify for Limit, AWS WAF returns a NextMarker
          value in the response that allows you to list another group of WebACL objects
        type: string
      responses:
        200:
          description: OK
      tags:
      - Web ACL
  /?Action=UpdateWebACL:
    get:
      summary: Update Web ACL
      description: 'Service: AWS WAFInserts or deletes.'
      operationId: updateWebACL
      x-api-path-slug: actionupdatewebacl-get
      parameters:
      - in: query
        name: ChangeToken
        description: The value returned by the most recent call to GetChangeToken
        type: string
      - in: query
        name: DefaultAction
        description: A default action for the web ACL, either ALLOW or BLOCK
        type: string
      - in: query
        name: Updates
        description: An array of updates to make to the WebACL
        type: string
      - in: query
        name: WebACLId
        description: The WebACLId of the WebACL that you want to update
        type: string
      responses:
        200:
          description: OK
      tags:
      - Web ACL
---