{
  "info": {
    "name": "Stack Exchange Get Tags FAQ",
    "_postman_id": "b6d96d00-5b5d-4703-af9d-516441dddb7f",
    "description": "Returns the frequently asked questions for the given set of tags in {tags}.\n \nFor a question to be returned, it must have all the tags in {tags} and be considered \"frequently asked\". The exact algorithm for determining whether a question is considered a FAQ is subject to change at any time.\n \n{tags} can contain up to 5 individual tags per request.\n \nThis method returns a list of questions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "7596e0de-c69e-4247-9f0d-c28b1dc5bdc7",
          "name": "returns-the-frequently-asked-questions-for-the-given-set-of-tags-in-tags-for-a-question-to-be-return",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "tags/:tags/faq"
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
                  "id": "tags",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the frequently asked questions for the given set of tags in {tags}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fcbf4ce4-7449-4857-a63f-a1eb72e2b124"
            }
          ]
        }
      ]
    }
  ]
}