---
swagger: "2.0"
x-collection-name: Pingdom
x-complete: 0
info:
  title: Summary API Get Intervals of Average Response Time and Uptime During a Given
    Interval
  description: |-
    For a given interval in time, return a list of sub intervals with the given resolution. Useful for generating graphs. A sub interval may be a week,
         a day or an hour depending on the choosen resolution.
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? |2-

        /api/{version}/analysis/{checkid}
  : ? |2-

          get
    : summary: Get Root Cause Analysis Results List
      description: Returns a list of the latest root cause analysis results for a
        specified check.
      operationId: get-root-cause-analysis-results-list
      x-api-path-slug: apiversionanalysischeckid-get
      parameters:
      - in: query
        name: from
        description: Return only results with timestamp of first test greater or equal
          to this value
        type: <td>integer</td>
      - in: query
        name: limit
        description: Limits the number of returned results to the specified quantity
        type: <td>integer</td>
      - in: query
        name: offset
        description: Offset for listing
        type: <td>integer</td>
      - in: query
        name: to
        description: Return only results with timestamp of first test less or equal
          to this value
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
      - Analysis
  ? |2-

        /api/{version}/checks
  : ? |2-

          get
    : summary: Get Check List
      description: Returns a list overview of all checks.
      operationId: |2-

        getApiVersionChecks
      x-api-path-slug: apiversionchecks-get
      parameters:
      - in: query
        name: include_tags
        description: Include tag list for each check
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
        name: tags
        description: Tag list separated by commas
        type: <td>string</td>
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
        200:
          description: OK
      tags:
      - Checks
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
  ? |2-

        /api/{version}/settings
  : ? |2-

          get
    : summary: Get Account Settings
      description: Returns all account-specific settings.
      operationId: get-account-settings
      x-api-path-slug: apiversionsettings-get
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
      - Settings
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
  ? |2-

        /api/{version}/summary.performance/{checkid}
  : ? |2-

          get
    : summary: Get Intervals of Average Response Time and Uptime During a Given Interval
      description: |-
        For a given interval in time, return a list of sub intervals with the given resolution. Useful for generating graphs. A sub interval may be a week,
             a day or an hour depending on the choosen resolution.
      operationId: get-intervals-of-average-response-time-and-uptime-during-a-given-interval
      x-api-path-slug: apiversionsummary-performancecheckid-get
      parameters:
      - in: query
        name: from
        description: Start time of period
        type: <td>integer</td>
      - in: query
        name: includeuptime
        description: Include uptime information
        type: <td>boolean</td>
      - in: query
        name: order
        description: Sorting order of sub intervals
        type: <td>string (asc,desc)</td>
      - in: query
        name: probes
        description: Filter to only use results from a list of probes
        type: <td>string</td>
      - in: query
        name: resolution
        description: Interval size
        type: <td>string (hour, day, week)</td>
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
host: api.pingdom.com
basePath: /
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