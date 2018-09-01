{
  "info": {
    "name": "Stack Exchange Get Questions Unanswered",
    "_postman_id": "62a15377-82db-4d46-8c4e-710e966cdbfc",
    "description": "Returns questions the site considers to be unanswered.\n \nNote that just because a question has an answer, that does not mean it is considered answered. While the rules are subject to change, at this time a question must have at least one upvoted answer to be considered answered.\n \nTo constrain questions returned to those with a set of tags, use the tagged parameter with a semi-colon delimited list of tags. This is an and contraint, passing tagged=c;java will return only those questions with both tags. As such, passing more than 5 tags will always return zero results.\n \nCompare with /questions/no-answers.\n \nThis method corresponds roughly with the unanswered tab.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authentication",
      "item": [
        {
          "id": "7793a84f-5543-4306-b9e4-24a971165827",
          "name": "reads-the-properties-for-a-set-of-access-tokens-accesstokens-can-contain-up-to-20-access-tokens-thes",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "access-tokens/:accessTokens"
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
                }
              ],
              "variable": [
                {
                  "id": "accessTokens",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Reads the properties for a set of access tokens.\n \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a23f1b54-78f2-4e97-9ac0-a7b77636568a"
            }
          ]
        },
        {
          "id": "c1595948-b31e-4ba9-9d2b-96a392914c32",
          "name": "immediately-expires-the-access-tokens-passed-this-method-is-meant-to-allow-an-application-to-discard",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "access-tokens/:accessTokens/invalidate"
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
                }
              ],
              "variable": [
                {
                  "id": "accessTokens",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Immediately expires the access tokens passed. This method is meant to allow an application to discard any active access tokens it no longer needs.\n \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eebd8999-2ec3-44e9-8fc9-f88ba49c137f"
            }
          ]
        },
        {
          "id": "e45a5d2b-c89b-4cca-995e-dab1b9026d80",
          "name": "passing-valid-access-tokens-to-this-method-causes-the-application-that-created-them-to-be-deauthoriz",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "apps/:accessTokens/de-authenticate"
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
                }
              ],
              "variable": [
                {
                  "id": "accessTokens",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Passing valid access_tokens to this method causes the application that created them to be de-authorized by the user associated with each access_token. This will remove the application from their apps tab, and cause all other existing access_tokens to be destroyed.\n \nThis method is meant for uninstalling applications, recovering from access_token leaks, or simply as a stronger form of /access-tokens/{accessTokens}/invalidate.\n \nNothing prevents a user from re-authenticate to an application that has de-authenticated itself, the user will be prompted to approve the application again however.\n \n{accessTokens} can contain up to 20 access tokens. These are obtained by authenticating a user using OAuth 2.0.\n \nThis method returns a list of access_tokens."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f573b757-4c07-4db1-889f-8cdc315de2a5"
            }
          ]
        }
      ]
    },
    {
      "name": "Answers",
      "item": [
        {
          "id": "8d3319ed-ec1a-4bf1-9417-78cb30e78009",
          "name": "returns-all-the-undeleted-answers-in-the-system-the-sorts-accepted-by-this-method-operate-on-the-fol",
          "request": {
            "url": "http://api.stackexchange.com/2.2/answers?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all the undeleted answers in the system.\n \nThe sorts accepted by this method operate on the follow fields of the answer object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of answers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7e98a9eb-3566-4716-bc8f-620c25e9fb58"
            }
          ]
        },
        {
          "id": "638f2874-4c61-4962-b9b1-8128d34702c1",
          "name": "gets-the-set-of-answers-identified-by-ids-this-is-meant-for-batch-fetcing-of-questions-a-useful-tric",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "answers/:ids"
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
            "description": "Gets the set of answers identified by ids.\n \nThis is meant for batch fetcing of questions. A useful trick to poll for updates is to sort by activity, with a minimum date of the last time you polled.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for answer_id on answer objects.\n \nThe sorts accepted by this method operate on the follow fields of the answer object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of answers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d8912cf3-dab8-463f-a5f6-e012a091643b"
            }
          ]
        },
        {
          "id": "928ab96d-a0a3-46e7-90d8-4e66ce2526d0",
          "name": "gets-the-comments-on-a-set-of-answers-if-you-know-that-you-have-an-answer-id-and-need-the-comments-u",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "answers/:ids/comments"
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
            "description": "Gets the comments on a set of answers.\n \nIf you know that you have an answer id and need the comments, use this method. If you know you have a question id, use /questions/{id}/comments. If you are unsure, use /posts/{id}/comments.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for answer_id on answer objects.\n \nThe sorts accepted by this method operate on the follow fields of the comment object:\n - creation - creation_date\n - votes - score\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec0c64e6-f6d4-45f5-97de-c981e0ff087b"
            }
          ]
        },
        {
          "id": "79971314-6808-4628-9a9c-6be82ed75756",
          "name": "returns-the-answers-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-l",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/answers?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the answers owned by the user associated with the given access_token.\n \nThis method returns a list of answers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4831b5a0-02dd-46ce-80a7-2add5d771134"
            }
          ]
        }
      ]
    },
    {
      "name": "Badges",
      "item": [
        {
          "id": "93881e5f-323f-4df9-abdf-752ac27f692b",
          "name": "returns-all-the-badges-in-the-system-badge-sorts-are-a-tad-complicated-for-the-purposes-of-sorting-a",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all the badges in the system.\n \nBadge sorts are a tad complicated. For the purposes of sorting (and min/max) tag_based is considered to be greater than named.\n \nThis means that you can get a list of all tag based badges by passing min=tag_based, and conversely all the named badges by passing max=named, with sort=type.\n \nFor ranks, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "83b6e92c-623d-4a8a-a18d-d120c63b4cd2"
            }
          ]
        },
        {
          "id": "2736c5e1-3c44-4c2a-a0ec-f3478d31f7c9",
          "name": "gets-all-explicitly-named-badges-in-the-system-a-named-badged-stands-in-opposition-to-a-tagbased-bad",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges/name?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all explicitly named badges in the system.\n \nA named badged stands in opposition to a tag-based badge. These are referred to as general badges on the sites themselves.\n \nFor the rank sort, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ddaa000c-dfdb-4e44-89d4-df88fff35011"
            }
          ]
        },
        {
          "id": "ee2cb197-7289-4df8-9d65-4d3199690dbe",
          "name": "returns-recently-awarded-badges-in-the-system-as-these-badges-have-been-awarded-they-will-have-the-b",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges/recipients?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns recently awarded badges in the system.\n \nAs these badges have been awarded, they will have the badge.user property set.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f3e1a38e-07ee-40fa-9b9d-22b790fef433"
            }
          ]
        },
        {
          "id": "89ba0c50-c166-4c9c-bd0b-dca2fde0dd45",
          "name": "returns-the-badges-that-are-awarded-for-participation-in-specific-tags-for-the-rank-sort-bronze-is-g",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges/tags?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the badges that are awarded for participation in specific tags.\n \nFor the rank sort, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d16fd01c-90d3-4d23-a619-e33b2811da85"
            }
          ]
        },
        {
          "id": "7f8ccd02-1fd1-4796-b76d-65f3bde670af",
          "name": "gets-the-badges-identified-in-id-note-that-badge-ids-are-not-constant-across-sites-and-thus-should-b",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "badges/:ids"
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
            "description": "Gets the badges identified in id.\n \nNote that badge ids are not constant across sites, and thus should be looked up via the /badges method. A badge id on a single site is, however, guaranteed to be stable.\n \nBadge sorts are a tad complicated. For the purposes of sorting (and min/max) tag_based is considered to be greater than named.\n \nThis means that you can get a list of all tag based badges by passing min=tag_based, and conversely all the named badges by passing max=named, with sort=type.\n \nFor ranks, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for badge_id on badge objects.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3ea4e9cd-0692-474e-8b69-ec9740fdd9bf"
            }
          ]
        },
        {
          "id": "4b7d12db-df35-4823-a91b-d94eccce29c0",
          "name": "returns-recently-awarded-badges-in-the-system-constrained-to-a-certain-set-of-badges-as-these-badges",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "badges/:ids/recipients"
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
            "description": "Returns recently awarded badges in the system, constrained to a certain set of badges.\n \nAs these badges have been awarded, they will have the badge.user property set.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for badge_id on badge objects.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ae1b58d-e3e8-4be8-8d52-1841f3787f5e"
            }
          ]
        },
        {
          "id": "1e39ed97-37ef-4588-8a94-7d2cb804e99f",
          "name": "returns-the-badges-earned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-l",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/badges?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the badges earned by the user associated with the given access_token.\n \nThis method returns a list of badges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ffdf6a91-7fe5-43cf-b1de-0363159692dc"
            }
          ]
        }
      ]
    },
    {
      "name": "Comments",
      "item": [
        {
          "id": "eec33c48-1ba1-4ceb-8c32-a5dac239a4bc",
          "name": "gets-all-the-comments-on-the-site-if-youre-filtering-for-interesting-comments-by-score-creation-date",
          "request": {
            "url": "http://api.stackexchange.com/2.2/comments?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all the comments on the site.\n \nIf you're filtering for interesting comments (by score, creation date, etc.) make use of the sort paramter with appropriate min and max values.\n \nIf you're looking to query conversations between users, instead use the /users/{ids}/mentioned and /users/{ids}/comments/{toid} methods.\n \nThe sorts accepted by this method operate on the follow fields of the comment object:\n - creation - creation_date\n - votes - score\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "86f4861b-7fb3-45a0-bdb7-743495368941"
            }
          ]
        },
        {
          "id": "87d298c4-d37b-4e99-9aec-8dfecd4e2550",
          "name": "gets-the-comments-identified-in-id-this-method-is-most-useful-if-you-have-a-cache-of-comment-ids-obt",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "comments/:ids"
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
            "description": "Gets the comments identified in id.\n \nThis method is most useful if you have a cache of comment ids obtained through other means (such as /questions/{id}/comments) but suspect the data may be stale.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for comment_id on comment objects.\n \nThe sorts accepted by this method operate on the follow fields of the comment object:\n - creation - creation_date\n - votes - score\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c8e09df1-47db-48a8-bc9c-d941afb450b2"
            }
          ]
        },
        {
          "id": "fdcc0379-16a3-4b1d-b67f-31855ba1a5e0",
          "name": "deletes-a-comment-use-an-access-token-with-write-access-to-delete-a-comment-in-practice-this-method-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "comments/:id/delete"
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
                  "key": "preview",
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
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a comment.\n \nUse an access_token with write_access to delete a comment.\n \nIn practice, this method will never return an object."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1527bd4c-0f41-43be-b8b5-b7c6057032cd"
            }
          ]
        },
        {
          "id": "dc1b8703-e8d8-4b24-8f50-049607d40899",
          "name": "edit-an-existing-comment-use-an-access-token-with-write-access-to-edit-an-existing-comment-this-meth",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "comments/:id/edit"
              ],
              "query": [
                {
                  "key": "body",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "key": "preview",
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
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Edit an existing comment.\n \nUse an access_token with write_access to edit an existing comment.\n \nThis method return the created comment."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3c1d8ab6-e58f-47b0-8cfd-0fb556a98359"
            }
          ]
        },
        {
          "id": "80849316-dc06-4526-a25e-f02e4a19bc89",
          "name": "returns-the-comments-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/comments?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the comments owned by the user associated with the given access_token.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c954a01b-b5e7-4e18-9cbe-8f665860a3ba"
            }
          ]
        },
        {
          "id": "d56ca463-d520-4493-862a-e36cc2176cf6",
          "name": "returns-the-comments-owned-by-the-user-associated-with-the-given-access-token-that-are-in-reply-to-t",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "me/comments/:toId"
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
                  "id": "toId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the comments owned by the user associated with the given access_token that are in reply to the user identified by {toId}.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "66995611-e680-4b71-953f-c5bedf9bbb0d"
            }
          ]
        }
      ]
    },
    {
      "name": "Errors",
      "item": [
        {
          "id": "cdf31ec7-3a6e-4f8b-a105-f82566989ca3",
          "name": "returns-the-various-error-codes-that-can-be-produced-by-the-api-this-method-is-provided-for-discover",
          "request": {
            "url": "http://api.stackexchange.com/2.2/errors?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the various error codes that can be produced by the API.\n \nThis method is provided for discovery, documentation, and testing purposes, it is not expected many applications will consume it during normal operation.\n \nFor testing purposes, look into the /errors/{id} method which simulates errors given a code.\n \nThis method returns a list of errors."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f7ce809a-6d8b-4eda-8c12-64e357d3f020"
            }
          ]
        },
        {
          "id": "574bddfb-db04-4baa-ac55-1dbe5def85fa",
          "name": "this-method-allows-you-to-generate-an-error-this-method-is-only-intended-for-use-when-testing-an-app",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "errors/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "This method allows you to generate an error.\n \nThis method is only intended for use when testing an application or library. Unlike other methods in the API, its contract is not frozen, and new error codes may be added at any time.\n \nThis method results in an error, which will be expressed with a 400 HTTP status code and setting the error* properties on the wrapper object."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "72cde85d-68c3-46a9-841f-8d280dbc14ed"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "de16d89b-f43f-4581-8fb5-88a307e0528b",
          "name": "returns-a-stream-of-events-that-have-occurred-on-the-site-the-api-considers-the-following-events--po",
          "request": {
            "url": "http://api.stackexchange.com/2.2/events?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&since=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a stream of events that have occurred on the site.\n \nThe API considers the following \"events\":\n - posting a question\n - posting an answer\n - posting a comment\n - editing a post\n - creating a user\n  \n \nEvents are only accessible for 15 minutes after they occurred, and by default only events in the last 5 minutes are returned. You can specify the age of the oldest event returned by setting the since parameter.\n \nIt is advised that developers batch events by ids and make as few subsequent requests to other methods as possible.\n \nThis method returns a list of events."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "22ee5b74-4182-4a43-8f68-0a64e656c068"
            }
          ]
        }
      ]
    },
    {
      "name": "Files",
      "item": [
        {
          "id": "dd85ed30-b8e1-444c-868e-c8e16a6afee7",
          "name": "creates-a-new-filter-given-a-list-of-includes-excludes-a-base-filter-and-whether-or-not-this-filter-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/filters/create?base=%7B%7D&exclude=%7B%7D&include=%7B%7D&unsafe=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new filter given a list of includes, excludes, a base filter, and whether or not this filter should be \"unsafe\".\n \nFilter \"safety\" is defined as follows. Any string returned as a result of an API call with a safe filter will be inline-able into HTML without script-injection concerns. That is to say, no additional sanitizing (encoding, HTML tag stripping, etc.) will be necessary on returned strings. Applications that wish to handle sanitizing themselves should create an unsafe filter. All filters are safe by default, under the assumption that double-encoding bugs are more desirable than script injections.\n \nIf no base filter is specified, the default filter is assumed. When building a filter from scratch, the none built-in filter is useful.\n \nWhen the size of the parameters being sent to this method grows to large, problems can occur. This method will accept POST requests to mitigate this.\n \nIt is not expected that many applications will call this method at runtime, filters should be pre-calculated and \"baked in\" in the common cases. Furthermore, there are a number of built-in filters which cover common use cases.\n \nThis method returns a single filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3a88b3b3-502b-40d7-a841-7eed6413ea9d"
            }
          ]
        },
        {
          "id": "83550eb2-17ff-469a-bf0e-91e28455844d",
          "name": "returns-the-fields-included-by-the-given-filters-and-the-safeness-of-those-filters-it-is-not-expecte",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "filters/:filters"
              ],
              "variable": [
                {
                  "id": "filters",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the fields included by the given filters, and the \"safeness\" of those filters.\n \nIt is not expected that this method will be consumed by many applications at runtime, it is provided to aid in debugging.\n \n{filters} can contain up to 20 semicolon delimited filters. Filters are obtained via calls to /filters/create, or by using a built-in filter.\n \nThis method returns a list of filters."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "834ef823-f7ab-4492-bb8f-a6be379523e3"
            }
          ]
        }
      ]
    },
    {
      "name": "Email",
      "item": [
        {
          "id": "140fd409-8da9-4726-a6a1-23739aee87a2",
          "name": "returns-a-users-inbox-this-method-requires-an-access-token-with-a-scope-containing-read-inbox-this-m",
          "request": {
            "url": "http://api.stackexchange.com/2.2/inbox?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of inbox items."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "808d2472-0435-4968-b744-f894be4ffd94"
            }
          ]
        },
        {
          "id": "0414bc15-2b59-4b56-ba74-65da1637deed",
          "name": "returns-the-unread-items-in-a-users-inbox-this-method-requires-an-access-token-with-a-scope-containi",
          "request": {
            "url": "http://api.stackexchange.com/2.2/inbox/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&since=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the unread items in a user's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of inbox items."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eec3aa5f-6128-415a-b5de-7165771a1f23"
            }
          ]
        },
        {
          "id": "6c162a1a-d064-44d9-9940-b4aaf581dbf3",
          "name": "returns-the-user-identified-by-access-tokens-inbox-this-method-requires-an-access-token-with-a-scope",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/inbox?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the user identified by access_token's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of inbox items."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8d00ef75-b1be-4ff8-a6f3-baf6815a9da6"
            }
          ]
        },
        {
          "id": "0512af29-e8c3-43e6-b4cb-1de46cdec1ed",
          "name": "returns-the-unread-items-in-the-user-identified-by-access-tokens-inbox-this-method-requires-an-acces",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/inbox/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&since=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the unread items in the user identified by access_token's inbox.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of inbox items."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "45d2f395-f4bb-4ab4-a75d-455d8b735b6e"
            }
          ]
        }
      ]
    },
    {
      "name": "Information",
      "item": [
        {
          "id": "a1b39656-33c4-4493-95db-598ff6c001bb",
          "name": "returns-a-collection-of-statistics-about-the-site-data-to-facilitate-persite-customization-discover-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/info?site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a collection of statistics about the site.\n \nData to facilitate per-site customization, discover related sites, and aggregate statistics is all returned by this method.\n \nThis data is cached very aggressively, by design. Query sparingly, ideally no more than once an hour.\n \nThis method returns an info object."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "43670fe3-1f8b-4ffd-ab8b-da7cb08930b7"
            }
          ]
        }
      ]
    },
    {
      "name": "Self",
      "item": [
        {
          "id": "e6666933-5ecb-451b-add3-bdad579a91e8",
          "name": "returns-the-user-associated-with-the-passed-access-token-this-method-returns-a-user",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the user associated with the passed access_token.\n \nThis method returns a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5de472fa-b559-41bd-ab52-933e953a3258"
            }
          ]
        }
      ]
    },
    {
      "name": "Associated",
      "item": [
        {
          "id": "5f1e2b44-05b9-4416-b4c4-b6774b2f79a9",
          "name": "returns-all-of-a-users-associated-accounts-given-an-access-token-for-them-this-method-returns-a-list",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/associated?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all of a user's associated accounts, given an access_token for them.\n \nThis method returns a list of network users."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "23d35a1d-010b-4619-9a44-33b1a4f5b288"
            }
          ]
        }
      ]
    },
    {
      "name": "Favorites",
      "item": [
        {
          "id": "09da1c5d-251a-4537-9688-b6e3acc51551",
          "name": "returns-the-questions-favorites-by-the-user-associated-with-the-given-access-token-this-method-retur",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/favorites?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the questions favorites by the user associated with the given access_token.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7c977015-6597-4075-969e-d36cc906a80c"
            }
          ]
        }
      ]
    },
    {
      "name": "Mentioned",
      "item": [
        {
          "id": "69f263ea-3556-47cf-b434-521a8f2073fb",
          "name": "returns-the-comments-mentioning-the-user-associated-with-the-given-access-token-this-method-returns-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/mentioned?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the comments mentioning the user associated with the given access_token.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fcaf64e7-6cfb-46d2-b130-3755e372635a"
            }
          ]
        }
      ]
    },
    {
      "name": "Merges",
      "item": [
        {
          "id": "450a85a2-4ed6-4dd9-9c25-416eed4a5e06",
          "name": "returns-a-record-of-merges-that-have-occurred-involving-a-user-identified-by-an-access-token-this-me",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/merges?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a record of merges that have occurred involving a user identified by an access_token.\n \nThis method allows you to take now invalid account ids and find what account they've become, or take currently valid account ids and find which ids were equivalent in the past.\n \nThis is most useful when confirming that an account_id is in fact \"new\" to an application.\n \nAccount merges can happen for a wide range of reasons, applications should not make assumptions that merges have particular causes.\n \nNote that accounts are managed at a network level, users on a site may be merged due to an account level merge but there is no guarantee that a merge has an effect on any particular site.\n \nThis method returns a list of account_merge."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1b254574-98cc-42e0-bab2-47941d8b6c28"
            }
          ]
        }
      ]
    },
    {
      "name": "Notifications",
      "item": [
        {
          "id": "d0e0b0f4-29af-4c8d-b0e0-eb9308718008",
          "name": "returns-a-users-notifications-given-an-access-token-this-method-requires-an-access-token-with-a-scop",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/notifications?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's notifications, given an access_token.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0a55d816-0ed6-4410-8fc2-0aae5141e72a"
            }
          ]
        },
        {
          "id": "2d78ef63-d00a-4d22-bbef-7cd4ca3dc615",
          "name": "returns-a-users-unread-notifications-given-an-access-token-this-method-requires-an-access-token-with",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/notifications/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's unread notifications, given an access_token.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "94e6c754-af01-4646-9bc8-3169b4c8fd8b"
            }
          ]
        },
        {
          "id": "63bfd335-2330-49fd-9781-dd178fea2e3f",
          "name": "returns-a-users-notifications-this-method-requires-an-access-token-with-a-scope-containing-read-inbo",
          "request": {
            "url": "http://api.stackexchange.com/2.2/notifications?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's notifications.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9f1cfbf3-4f01-497a-af7d-1728fb581701"
            }
          ]
        },
        {
          "id": "10b3edf6-c937-449c-b8e5-4ba5379e41b4",
          "name": "returns-a-users-unread-notifications-this-method-requires-an-access-token-with-a-scope-containing-re",
          "request": {
            "url": "http://api.stackexchange.com/2.2/notifications/unread?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a user's unread notifications.\n \nThis method requires an access_token, with a scope containing \"read_inbox\".\n \nThis method returns a list of notifications."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6025d6b8-527e-470f-bdda-af4c8f127460"
            }
          ]
        }
      ]
    },
    {
      "name": "Privileges",
      "item": [
        {
          "id": "cce0828f-5963-4e81-ad4e-4f01d51d1306",
          "name": "returns-the-privileges-the-user-identified-by-access-token-has-this-method-returns-a-list-of-privile",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/privileges?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the privileges the user identified by access_token has.\n \nThis method returns a list of privileges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c2ec1341-030e-4433-831c-ab560b8223a7"
            }
          ]
        },
        {
          "id": "bd034a34-310c-468e-9ff3-80ce0e9a45e3",
          "name": "returns-the-earnable-privileges-on-a-site-privileges-define-abilities-a-user-can-earn-via-reputation",
          "request": {
            "url": "http://api.stackexchange.com/2.2/privileges?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the earnable privileges on a site.\n \nPrivileges define abilities a user can earn (via reputation) on any Stack Exchange site.\n \nWhile fairly stable, over time they do change. New ones are introduced with new features, and the reputation requirements change as a site matures.\n \nThis method returns a list of privileges."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cb499501-f415-4cb1-a7ba-ab4e663c3764"
            }
          ]
        }
      ]
    },
    {
      "name": "Questions",
      "item": [
        {
          "id": "b7640e8e-90e7-4558-b992-cb55316db326",
          "name": "returns-the-questions-owned-by-the-user-associated-with-the-given-access-token-this-method-returns-a",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/questions?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the questions owned by the user associated with the given access_token.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5f80a599-e57f-401c-8b2c-cc87b8772385"
            }
          ]
        },
        {
          "id": "7beaf4e3-74a8-4036-b569-f988f96466e9",
          "name": "returns-the-questions-that-have-active-bounties-offered-by-the-user-associated-with-the-given-access",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/questions/featured?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "