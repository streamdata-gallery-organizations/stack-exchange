{
  "info": {
    "name": "Stack Exchange Get User Associated",
    "_postman_id": "23a38105-c86a-4ad8-888d-a165e351af41",
    "description": "Returns all of a user's associated accounts, given their account_ids in {ids}.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for account_id on user objects.\n \nThis method returns a list of network_users.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "016598ec-2b14-4c1b-8ad0-d1aefc74c8e1",
          "name": "returns-all-of-a-users-associated-accounts-given-their-account-ids-in-ids-ids-can-contain-up-to-100-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:ids/associated"
              ],
              "query": [
                {
                  "key": "callback",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pagesize",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ids",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all of a user's associated accounts, given their account_ids in {ids}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30c5e607-e39e-4b76-aecc-467bc1519595"
            }
          ]
        }
      ]
    }
  ]
}