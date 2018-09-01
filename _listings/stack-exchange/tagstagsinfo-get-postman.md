{
  "info": {
    "name": "Stack Exchange Get Tags Info",
    "_postman_id": "f5f4b420-5907-4dd4-a524-b313bd2abd7b",
    "description": "Returns tag objects representing the tags in {tags} found on the site.\n \nThis method diverges from the standard naming patterns to avoid to conflicting with existing methods, due to the free form nature of tag names.\n \nThis method returns a list of tags.\n \nThe sorts accepted by this method operate on the follow fields of the tag object:\n - popular - count\n - activity - the creation_date of the last question asked with the tag\n - name - name\n  popular is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "4e9f23e7-b586-4e38-b25f-83d6fe0204b9",
          "name": "returns-tag-objects-representing-the-tags-in-tags-found-on-the-site-this-method-diverges-from-the-st",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "tags/:tags/info"
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
                  "key": "fromdate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "max",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "min",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "order",
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
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "todate",
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
            "description": "Returns tag objects representing the tags in {tags} found on the site"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "533ba98f-e56f-4079-b755-a5edc3407b59"
            }
          ]
        }
      ]
    }
  ]
}