{
  "info": {
    "name": "Stack Exchange De-Authenticate Token",
    "_postman_id": "ab966cd5-efbd-456b-93a7-8f79c5b51775",
    "description": "Passing valid access_tokens to this method causes the application that created them to be de-authorized by the user associated with each access_token. This will remove the application from their apps tab, and cause all other existing access_tokens to be destroyed.\n \nThis method is meant for uninstalling applications, recovering from access_token leaks, or simply as a stronger form of /access-tokens/{accessTokens}/invalidate.\n \nNothing prevents a user from re-authenticate to an application that has de-authenticated itself, the user will be prompted to approve the application again however.\n \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "authentication",
      "item": [
        {
          "id": "03026d19-a701-41c8-94ec-eb6475d48233",
          "name": "passing-valid-access-tokens-to-this-method-causes-the-application-that-created-them-to-be-deauthoriz",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "apps/:accessTokens/de-authenticate"
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
            "description": "Passing valid access_tokens to this method causes the application that created them to be de-authorized by the user associated with each access_token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "328f5e9f-bef0-4acf-8670-5e10d13d405e"
            }
          ]
        }
      ]
    }
  ]
}