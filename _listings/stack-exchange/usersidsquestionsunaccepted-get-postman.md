{
  "info": {
    "name": "Stack Exchange Get User Questions Unnacepted",
    "_postman_id": "75e47857-58e2-4913-bd60-ed596a05044c",
    "description": "Gets the questions asked by the users in {ids} which have at least one answer, but no accepted answer.\n \nQuestions returned by this method have answers, but the owner has not opted to accept any of them.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for user_id on user or shallow_user objects.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "92276f98-e36e-49c2-aa00-db271a962181",
          "name": "gets-the-questions-asked-by-the-users-in-ids-which-have-at-least-one-answer-but-no-accepted-answer-q",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "users/:ids/questions/unaccepted"
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
            "description": "Gets the questions asked by the users in {ids} which have at least one answer, but no accepted answer"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5ba38aac-6779-40bf-9ac9-ffdfe1b371a2"
            }
          ]
        }
      ]
    }
  ]
}