{
  "info": {
    "name": "Stack Exchange My Write Permissions",
    "_postman_id": "dd26e1fc-694e-42da-82ee-5e5af2d00ed9",
    "description": "Returns the write permissions a user has via the api, given an access token.\n \nThe Stack Exchange API gives users the ability to create, edit, and delete certain types. This method returns whether the passed user is capable of performing those actions at all, as well as how many times a day they can.\n \nThis method does not consider the user's current quota (ie. if they've already exhausted it for today) nor any additional restrictions on write access, such as editing deleted comments.\n \nThis method returns a list of write_permissions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "write permissions",
      "item": [
        {
          "id": "c703ffa5-c5d1-4cc2-a47d-490b8d111295",
          "name": "returns-the-write-permissions-a-user-has-via-the-api-given-an-access-token-the-stack-exchange-api-gi",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/write-permissions?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the write permissions a user has via the api, given an access token"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d5a786ab-4811-4e9f-a426-21b2ec3e6dea"
            }
          ]
        }
      ]
    }
  ]
}