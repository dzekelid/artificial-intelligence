{
  "info": {
    "name": "BMC Software API Get Actions (Alerts) List",
    "_postman_id": "67d7a5c9-69e5-4e9e-8497-4a495042cb17",
    "description": "Returns a list of actions (alerts) that have been generated for your account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Actions",
      "item": [
        {
          "id": "76ce5420-b753-4472-9f25-cc146b039583",
          "name": "get-all-available-action-types",
          "request": {
            "url": "http://example.com/api/v1/actions",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all known action types"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3ae31461-7136-47c6-af0d-eb8802e2d638"
            }
          ]
        },
        {
          "id": "6c68fb25-272d-4645-8b40-3a4ccd85d843",
          "name": "get-all-installed-actions",
          "request": {
            "url": "http://example.com/api/v1/actions/installed",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all actions that are installed for the project"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2e71485e-3511-4952-9794-7390c9bb5be7"
            }
          ]
        },
        {
          "id": "8d7a54e9-9345-41f7-8c62-0f4ce7faea74",
          "name": "install-action",
          "request": {
            "url": "http://example.com/api/v1/actions/installed",
            "method": "PUT",
            "body": {
              "mode": "raw"
            },
            "description": "Installs an action"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "37de1941-4d09-4470-83e6-b25de906d19f"
            }
          ]
        },
        {
          "id": "62d63cbd-388f-4705-b40e-cd91d7142c09",
          "name": "get-details-of-an-installed-action",
          "request": {
            "url": "http://example.com/api/v1/actions/installed/:actionId?actionId\nName of plugin=actionId%0AName%20of%20plugin",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a single action definition"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ca08ee5e-410b-459f-98a8-ab247e89ea77"
            }
          ]
        },
        {
          "id": "08a23f19-b79a-4549-beac-196e922f40a1",
          "name": "uninstall-action",
          "request": {
            "url": "http://example.com/api/v1/actions/installed/:actionId",
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Uninstalls an action and remove it from the associated alarms(s)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b995e34c-cab9-4d16-b6a8-4c52e933e9e5"
            }
          ]
        },
        {
          "id": "e78171d2-0607-46d3-b8fe-72499795313c",
          "name": "get-all-alarms-using-an-action",
          "request": {
            "url": "http://example.com/api/v1/actions/installed/:actionId/alarms",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get alarms that are using this action installed for the project"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3261e56a-40f9-41a5-87d7-41a11752881d"
            }
          ]
        },
        {
          "id": "67e90822-a56f-476f-be51-f9500a641b37",
          "name": "get-action",
          "request": {
            "url": "http://example.com/api/v1/actions/:action?action\nName of plugin=action%0AName%20of%20plugin",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets a single action type"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9b76480b-8141-404f-ba83-222fafba05f4"
            }
          ]
        }
      ]
    }
  ]
}