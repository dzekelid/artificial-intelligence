---
swagger: "2.0"
x-collection-name: Pingdom
x-complete: 0
info:
  title: Summary API Get A Response Time / Uptime Average
  description: Get the average time / uptime value for a specified check and time
    period.
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

        /api/{version}/summary.average/{checkid}
  : ? |2-

          get
    : summary: Get A Response Time / Uptime Average
      description: Get the average time / uptime value for a specified check and time
        period.
      operationId: get-a-response-time--uptime-average
      x-api-path-slug: apiversionsummary-averagecheckid-get
      parameters:
      - in: query
        name: bycountry
        description: Split response times into country groups
        type: <td>boolean</td>
      - in: query
        name: byprobe
        description: Split response times into probe groups
        type: <td>boolean</td>
      - in: query
        name: from
        description: Start time of period
        type: <td>integer</td>
      - in: query
        name: includeuptime
        description: Include uptime information
        type: <td>boolean</td>
      - in: query
        name: probes
        description: Filter to only use results from a list of probes
        type: <td>string</td>
      - in: query
        name: to
        description: End time of period
        type: <td>integer</td>
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
      - Summary
x-streamrank:
  polling_total_time_average: "0"
  polling_size_download_average: "0"
  streaming_total_time_average: "0"
  streaming_size_download_average: "0"
  change_yes: "0"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "200"
  last_run: ~
  days_run: "0"
  minute_run: "0"
---