---
swagger: "2.0"
x-collection-name: API Science
x-complete: 0
info:
  title: API Science Get Contacts List
  version: 1.0.0
  description: Returns a list of all contacts.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? |2-

        /api/{version}/contacts
  : ? |2-

          get
    : summary: Get Contacts List
      description: Returns a list of all contacts.
      operationId: get-contacts-list
      x-api-path-slug: apiversioncontacts-get
      parameters:
      - in: query
        name: limit
        description: Limits the number of returned contacts to the specified quantity
        type: <td>integer</td>
      - in: query
        name: offset
        description: Offset for listing
        type: <td>integer</td>
      responses:
        200:
          description: OK
      tags:
      - Contacts
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