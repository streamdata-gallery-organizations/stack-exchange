{
  "info": {
    "name": "Stack Exchange Get Suggested Edit",
    "_postman_id": "41eebc4a-7a4e-4615-8d74-7e07d7e89af2",
    "description": "Returns suggested edits identified in ids.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for suggested_edit_id on suggested_edit objects.\n \nThe sorts accepted by this method operate on the follow fields of the suggested_edit object:\n - creation - creation_date\n - approval - approval_date Does not return unapproved suggested_edits\n - rejection - rejection_date Does not return unrejected suggested_edits\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of suggested-edits.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "suggested edits",
      "item": [
        {
          "id": "148728bb-93a1-4de8-b338-a0458735dafb",
          "name": "returns-suggested-edits-identified-in-ids-ids-can-contain-up-to-100-semicolon-delimited-ids-to-find-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "suggested-edits/:ids"
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
                  "id": "ids",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns suggested edits identified in ids"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "72b7473a-138c-476d-b5fa-724eff757dde"
            }
          ]
        }
      ]
    }
  ]
}