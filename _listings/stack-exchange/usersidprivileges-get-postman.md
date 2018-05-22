{
  "info": {
    "name": "Stack Exchange Get User Preveleges",
    "_postman_id": "9706902c-880f-4e69-8b8f-803a0178424f",
    "description": "Returns the privileges a user has.\n \nApplications are encouraged to calculate privileges themselves, without repeated queries to this method. A simple check against the results returned by /privileges and user.user_type would be sufficient.\n \n{id} can contain only a single, to find it programatically look for user_id on user or shallow_user objects.\n \nThis method returns a list of privileges.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "4de9837b-965a-4db0-b4bd-b9681cc9b4c8",
          "name": "returns-the-privileges-a-user-has-applications-are-encouraged-to-calculate-privileges-themselves-wit",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:id/privileges"
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
            "description": "Returns the privileges a user has"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a41340a7-bf1f-4544-81d2-d19bf3288731"
            }
          ]
        }
      ]
    }
  ]
}