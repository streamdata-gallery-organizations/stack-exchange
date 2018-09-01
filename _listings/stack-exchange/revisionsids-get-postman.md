{
  "info": {
    "name": "Stack Exchange Get Revisions",
    "_postman_id": "78ffd6c5-d2d7-4deb-b263-c6e0c36c2bac",
    "description": "Returns edit revisions identified by ids in {ids}.\n \n{ids} can contain up to 20 semicolon delimited ids, to find ids programatically look for revision_guid on revision objects. Note that unlike most other id types in the API, revision_guid is a string.\n \nThis method returns a list of revisions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "revisions",
      "item": [
        {
          "id": "f4ef356c-9c42-40ae-9a71-94406344a74a",
          "name": "returns-edit-revisions-identified-by-ids-in-ids-ids-can-contain-up-to-20-semicolon-delimited-ids-to-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "revisions/:ids"
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
            "description": "Returns edit revisions identified by ids in {ids}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ba3d2346-bdee-4e1a-aec1-ccbe304e2b58"
            }
          ]
        }
      ]
    }
  ]
}