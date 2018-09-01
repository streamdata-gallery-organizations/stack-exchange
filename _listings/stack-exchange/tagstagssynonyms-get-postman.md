{
  "info": {
    "name": "Stack Exchange Get Tags Synonyms",
    "_postman_id": "1c7d0045-b9a1-4f06-b77f-d739e7b4cb03",
    "description": "Gets all the synonyms that point to the tags identified in {tags}. If you're looking to discover all the tag synonyms on a site, use the /tags/synonyms methods instead of call this method on all tags.\n \n{tags} can contain up to 20 individual tags per request.\n \nThe sorts accepted by this method operate on the follow fields of the tag_synonym object:\n - creation - creation_date\n - applied - applied_count\n - activity - last_applied_date\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of tag synonyms.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "36dee925-9ab0-4509-9184-43d28cc244e1",
          "name": "gets-all-the-synonyms-that-point-to-the-tags-identified-in-tags-if-youre-looking-to-discover-all-the",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "tags/:tags/synonyms"
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
            "description": "Gets all the synonyms that point to the tags identified in {tags}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3bb74c0c-0b6e-4457-b5d9-e5eb01a4a74a"
            }
          ]
        }
      ]
    }
  ]
}