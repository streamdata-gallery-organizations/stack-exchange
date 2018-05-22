{
  "info": {
    "name": "Stack Exchange Get User Merges",
    "_postman_id": "7dc09e4e-b03a-460d-98b9-39626a14a106",
    "description": "Returns a record of merges that have occurred involving the passed account ids.\n \nThis method allows you to take now invalid account ids and find what account they've become, or take currently valid account ids and find which ids were equivalent in the past.\n \nThis is most useful when confirming that an account_id is in fact \"new\" to an application.\n \nAccount merges can happen for a wide range of reasons, applications should not make assumptions that merges have particular causes.\n \nNote that accounts are managed at a network level, users on a site may be merged due to an account level merge but there is no guarantee that a merge has an effect on any particular site.\n \nThis method returns a list of account_merge.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "8f66578e-47aa-421e-868f-7e66ab044fb9",
          "name": "returns-a-record-of-merges-that-have-occurred-involving-the-passed-account-ids-this-method-allows-yo",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:ids/merges"
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
            "description": "Returns a record of merges that have occurred involving the passed account ids"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4bd9f2b1-034d-4d4b-9f49-637d342ea28c"
            }
          ]
        }
      ]
    }
  ]
}