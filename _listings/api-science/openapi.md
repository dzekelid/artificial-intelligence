swagger: "2.0"
x-collection-name: API Science
x-complete: 1
info:
  title: API Science
  version: 1.0.0
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