{
  "info": {
    "name": "Stack Exchange Get Tags Wikis",
    "_postman_id": "2425013a-8e89-4252-9ae1-52ca26785a85",
    "description": "Returns the wikis that go with the given set of tags in {tags}.\n \nBe aware that not all tags have wikis.\n \n{tags} can contain up to 20 individual tags per request.\n \nThis method returns a list of tag wikis.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "6cdd4a51-273d-4042-8839-9672ef142c98",
          "name": "returns-the-wikis-that-go-with-the-given-set-of-tags-in-tags-be-aware-that-not-all-tags-have-wikis-t",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "tags/:tags/wikis"
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
            "description": "Returns the wikis that go with the given set of tags in {tags}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a03656e9-adac-48b9-9e0f-9896edbe7212"
            }
          ]
        }
      ]
    }
  ]
}