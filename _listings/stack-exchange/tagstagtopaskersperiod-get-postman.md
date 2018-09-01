{
  "info": {
    "name": "Stack Exchange Get Tags Top Askers",
    "_postman_id": "3df04bfe-3c5e-462f-aaa5-0a18cef33bc6",
    "description": "Returns the top 30 askers active in a single tag, of either all-time or the last 30 days.\n \nThis is a view onto the data presented on the tag info page on the sites.\n \nThis method returns a list of tag score objects.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "3d2d1b33-40d4-4bc3-af50-a16ffd44cf66",
          "name": "returns-the-top-30-askers-active-in-a-single-tag-of-either-alltime-or-the-last-30-days-this-is-a-vie",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "tags/:tag/top-askers/:period"
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
            "description": "Returns the top 30 askers active in a single tag, of either all-time or the last 30 days"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8bee50e9-67d4-474f-8171-03a274b9aa2f"
            }
          ]
        }
      ]
    }
  ]
}