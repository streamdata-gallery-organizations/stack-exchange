{
  "info": {
    "name": "Stack Exchange Get Tags Related",
    "_postman_id": "bc001f44-4c26-4d6c-8b90-9fd3785bbbc6",
    "description": "Returns the tags that are most related to those in {tags}.\n \nIncluding multiple tags in {tags} is equivalent to asking for \"tags related to tag #1 and tag #2\" not \"tags related to tag #1 or tag #2\".\n \ncount on tag objects returned is the number of question with that tag that also share all those in {tags}.\n \n{tags} can contain up to 4 individual tags per request.\n \nThis method returns a list of tags.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "35096ff1-beff-4411-b3a2-5252a6989180",
          "name": "returns-the-tags-that-are-most-related-to-those-in-tags-including-multiple-tags-in-tags-is-equivalen",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "tags/:tags/related"
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
            "description": "Returns the tags that are most related to those in {tags}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4b62d83f-92dd-420c-84b9-cbf4a429571c"
            }
          ]
        }
      ]
    }
  ]
}