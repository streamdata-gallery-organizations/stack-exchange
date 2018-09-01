{
  "info": {
    "name": "Stack Exchange Get User Reputation History",
    "_postman_id": "b506944d-1a75-4491-9e71-4af4d5cdaa17",
    "description": "Returns users' public reputation history.\n \nThis method returns a list of reputation_history.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "b045a81f-a82a-4b0e-8aef-73a03d351a2b",
          "name": "returns-users-public-reputation-history-this-method-returns-a-list-of-reputation-history",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:ids/reputation-history"
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
                },
                {
                  "key": "site",
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
            "description": "Returns users' public reputation history"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fc8805ca-a263-4cc2-97f4-fcba677dda2a"
            }
          ]
        }
      ]
    }
  ]
}