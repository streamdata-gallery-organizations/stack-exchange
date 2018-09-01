{
  "info": {
    "name": "Stack Exchange Get User Reputation History Full",
    "_postman_id": "4e09386b-5ebd-43c6-9754-a9c100b9e4a2",
    "description": "Returns a user's full reputation history, including private events.\n \nThis method requires an access_token, with a scope containing \"private_info\".\n \nThis method returns a list of reputation_history.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "b032adde-7a76-4598-a99c-cbb37d7a4a59",
          "name": "returns-a-users-full-reputation-history-including-private-events-this-method-requires-an-access-toke",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:id/reputation-history/full"
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
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's full reputation history, including private events"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "81c981e4-a70a-4795-8e0b-cc93331a2e7d"
            }
          ]
        }
      ]
    }
  ]
}