---
swagger: "2.0"
x-collection-name: Pingdom
x-complete: 0
info:
  title: Probes API Get Probe Server List
  description: Returns a list of all Pingdom probe servers for Uptime and Transaction
    checks.
  version: 1.0.0
host: api.pingdom.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? |2-

        /api/{version}/probes
  : ? |2-

          get
    : summary: Get Probe Server List
      description: Returns a list of all Pingdom probe servers for Uptime and Transaction
        checks.
      operationId: get-probe-server-list
      x-api-path-slug: apiversionprobes-get
      parameters:
      - in: query
        name: includedeleted
        description: Include old probes that are no longer in use
        type: <td>boolean</td>
      - in: query
        name: limit
        description: Limits the number of returned probes to the specified quantity
        type: <td>integer</td>
      - in: query
        name: offset
        description: Offset for listing
        type: <td>integer</td>
      - in: query
        name: onlyactive
        description: Return only active probes
        type: <td>boolean</td>
      responses:
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
      tags:
      - Proves
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