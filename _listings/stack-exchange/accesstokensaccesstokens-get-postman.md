{
  "info": {
    "name": "Stack Exchange Get Acces Tokens",
    "_postman_id": "91feee04-7f84-4696-8ff2-85f5fd22df9f",
    "description": "Reads the properties for a set of access tokens.\n \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "authentication",
      "item": [
        {
          "id": "35254659-0866-4393-8106-19cef6145ef5",
          "name": "reads-the-properties-for-a-set-of-access-tokens-accesstokens-can-contain-up-to-20-access-tokens-thes",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "access-tokens/:accessTokens"
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
                  "id": "accessTokens",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Reads the properties for a set of access tokens"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "11a9d879-2e32-4082-b549-41daf3f7e440"
            }
          ]
        }
      ]
    }
  ]
}