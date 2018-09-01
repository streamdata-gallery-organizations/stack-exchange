{
  "info": {
    "name": "Stack Exchange Get Error",
    "_postman_id": "79d8d419-3f9c-464b-8452-004f1e04d160",
    "description": "This method allows you to generate an error.\n \nThis method is only intended for use when testing an application or library. Unlike other methods in the API, its contract is not frozen, and new error codes may be added at any time.\n \nThis method results in an error, which will be expressed with a 400 HTTP status code and setting the error* properties on the wrapper object.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "errors",
      "item": [
        {
          "id": "2f2654ca-63ef-409b-a26c-8f6a03e564ea",
          "name": "this-method-allows-you-to-generate-an-error-this-method-is-only-intended-for-use-when-testing-an-app",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "errors/:id"
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
            "description": "This method allows you to generate an error"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "caf891dd-fcaf-4a88-947b-3c6f276efa8d"
            }
          ]
        }
      ]
    }
  ]
}