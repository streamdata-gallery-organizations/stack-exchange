{
  "info": {
    "name": "Stack Exchange Invalidate Acces Tokens",
    "_postman_id": "444fbade-db96-4a94-8987-f353cee55f9c",
    "description": "Immediately expires the access tokens passed. This method is meant to allow an application to discard any active access tokens it no longer needs.\n \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "authentication",
      "item": [
        {
          "id": "b26dfbec-6d16-4a92-b466-9d17b47dd86e",
          "name": "immediately-expires-the-access-tokens-passed-this-method-is-meant-to-allow-an-application-to-discard",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "access-tokens/:accessTokens/invalidate"
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
            "description": "Immediately expires the access tokens passed"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "96baaddd-a685-4e69-b9d3-c2a5981b66e1"
            }
          ]
        }
      ]
    }
  ]
}