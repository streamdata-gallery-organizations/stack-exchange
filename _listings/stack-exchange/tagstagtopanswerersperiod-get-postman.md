{
  "info": {
    "name": "Stack Exchange",
    "_postman_id": "64859556-7f05-42ea-9491-91389df6b0c6",
    "description": "Stack Exchange is a network of 130+ Q&amp;A communities including Stack Overflow.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "0b76f2c7-5504-4d70-8ccc-804b0b2cf063",
          "name": "returns-the-top-30-answerers-active-in-a-single-tag-of-either-alltime-or-the-last-30-days-this-is-a-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "tags/:tag/top-answerers/:period"
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
                  "id": "period",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tag",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the top 30 answerers active in a single tag, of either all-time or the last 30 days"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "addc1221-dbf7-4419-bca4-4bd5ca9f11b8"
            }
          ]
        }
      ]
    }
  ]
}