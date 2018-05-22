{
  "info": {
    "name": "Stack Exchange Get Question Related",
    "_postman_id": "e645b967-44a6-45ec-939f-42d37504e840",
    "description": "Returns questions that the site considers related to those identified in {ids}.\n \nThe algorithm for determining if questions are related is not documented, and subject to change at any time. Futhermore, these values are very heavily cached, and may not update immediately after a question has been editted. It is also not guaranteed that a question will be considered related to any number (even non-zero) of questions, and a consumer should be able to handle a variable number of returned questions.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for question_id on question objects.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n - rank - a priority sort by site applies, subject to change at any time Does not accept min or max\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Authentication",
      "item": [
        {
          "id": "976a6251-b4cc-4cd2-a163-233b92c45ae2",
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
              "id": "e210a7d1-bec8-4c2f-bc2b-9bcc39642a5b"
            }
          ]
        },
        {
          "id": "7a847707-6476-4cac-a422-084595eedfb1",
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
              "id": "4c92f19d-7aa4-4d2e-a7f5-be4cff110193"
            }
          ]
        },
        {
          "id": "f0e815e4-d5f3-4f74-a26f-839534de6f81",
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
              "id": "aee53b45-3cdb-4849-b15e-58f3a7888d50"
            }
          ]
        }
      ]
    },
    {
      "name": "Answers",
      "item": [
        {
          "id": "6c1aac3f-ec2b-4774-ba93-e82403feddf7",
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
              "id": "974c1de7-3ef8-41bb-b5d0-b043d69f6433"
            }
          ]
        },
        {
          "id": "fbaf2866-f98c-448d-9658-82feac3562c3",
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
              "id": "1d374657-a808-4377-b4a9-fa5bf99fa5d1"
            }
          ]
        },
        {
          "id": "343633a5-894e-42b1-80af-258a7450e5a3",
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
              "id": "bd44d26b-56a3-4a61-bef1-c6f1d978e2e3"
            }
          ]
        },
        {
          "id": "0e795bb2-6ed7-4bf1-adc0-2cb042059d07",
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
              "id": "0a9fc7e4-ab57-4ffb-8790-3df85f3f315f"
            }
          ]
        }
      ]
    },
    {
      "name": "Badges",
      "item": [
        {
          "id": "ff9f139b-41c6-488a-b158-ca34747f4b5d",
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
              "id": "535db43a-0ebc-44fb-8b5b-c96c42f1c021"
            }
          ]
        },
        {
          "id": "8409d169-0b90-4217-bacb-049edc4aa38a",
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
              "id": "abfdb864-2046-46e8-9255-64d901b72c53"
            }
          ]
        },
        {
          "id": "3c00f05f-fa83-432f-b2c5-23f7b5200bfc",
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
              "id": "1c2e9520-b11b-4ace-8c29-6f38bff06b95"
            }
          ]
        },
        {
          "id": "a517c181-f11f-490c-8897-f5d5d367274f",
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
              "id": "eb352a42-a0ad-404e-957f-9d67f05de775"
            }
          ]
        },
        {
          "id": "6e49433c-cefd-4f22-911b-b0e44a6f0463",
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
              "id": "46880b6c-9971-45ec-9da5-23583eef9d4c"
            }
          ]
        },
        {
          "id": "5590adce-928a-4900-b4d3-116623123550",
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
              "id": "8d01de27-b6de-401d-bd74-6f21c7bfe3eb"
            }
          ]
        },
        {
          "id": "1a44c261-c85e-430b-98ea-b413643dafaf",
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
              "id": "0ff9e5c1-680d-4bac-8d38-35278c6ca77b"
            }
          ]
        }
      ]
    },
    {
      "name": "Comments",
      "item": [
        {
          "id": "53f54cc4-626e-49e4-ad62-a7df7e40fd5c",
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
              "id": "758e1f43-5076-4de1-81c5-b68af827f097"
            }
          ]
        },
        {
          "id": "bed9aec9-f0b0-402f-8829-746e326a63e7",
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
              "id": "6318061d-b0f1-463b-bed4-64c934cda2f8"
            }
          ]
        },
        {
          "id": "1c12d90b-9715-4391-8270-8e981eff97a2",
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
              "id": "bd2b7aa4-2c97-47b9-aab2-801c2146843d"
            }
          ]
        },
        {
          "id": "eb56024c-02fc-44d6-be63-f2fa3e78327a",
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
              "id": "82e59c8f-fbbe-4e3d-86c4-41ea2e2e10d6"
            }
          ]
        },
        {
          "id": "0f32c96b-4684-4c46-bbe4-8d3803c22154",
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
              "id": "efd287a5-a85b-4c17-ae4b-96ace4cc12f9"
            }
          ]
        },
        {
          "id": "9b9da23c-c8ba-40c1-b7c9-615cd81c0ebf",
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
              "id": "d4d36707-ae05-4db7-8ee0-54916d013318"
            }
          ]
        }
      ]
    },
    {
      "name": "Errors",
      "item": [
        {
          "id": "24139356-468b-4a96-b9e9-5fd242c89379",
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
              "id": "f3726d5c-3006-4802-8682-5052edc21225"
            }
          ]
        },
        {
          "id": "9c95346a-35c8-451d-ac13-f5a86acd7a8a",
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
              "id": "5be3bc26-9a8d-4f24-9d70-2f8502161830"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "30f9eb2e-5236-439c-bc30-52f22beca2b7",
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
              "id": "efe7d166-685e-407d-9a3e-084145f81c1e"
            }
          ]
        }
      ]
    },
    {
      "name": "Files",
      "item": [
        {
          "id": "23f2f1fa-5205-466e-b1c3-c5a6a7066b13",
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
              "id": "74c46b94-6829-44a4-a392-6d2f4b717bbd"
            }
          ]
        },
        {
          "id": "b119842f-2eab-4a7d-8275-b7a049a64c8c",
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
              "id": "3e24b7ba-1a5e-4b28-998c-1add72d2b8df"
            }
          ]
        }
      ]
    },
    {
      "name": "Email",
      "item": [
        {
          "id": "5dc83d11-9a04-4546-bc8b-7a8c0af7a6dc",
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
              "id": "c8d89c28-cd21-414d-95bd-ffd185b4a1b0"
            }
          ]
        },
        {
          "id": "ce3165b6-9219-480b-adca-94187fef4bdd",
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
              "id": "00a007c1-24be-4089-9118-870fbf15ced9"
            }
          ]
        },
        {
          "id": "28e9dd92-c44f-4e47-a553-04870e2993b3",
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
              "id": "4e2b6ec8-0a75-4c4f-9b60-f5bfbd1f99c6"
            }
          ]
        },
        {
          "id": "d6011e55-487d-498e-8aa6-bfe1a8dadaf1",
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
              "id": "027be670-1d6d-459e-a2f3-f4c75c8ecf98"
            }
          ]
        }
      ]
    },
    {
      "name": "Information",
      "item": [
        {
          "id": "803b4721-f45f-478d-b15b-edda9a319cef",
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
              "id": "461764a4-cd44-4f4b-b8fb-d1d8bd7613f0"
            }
          ]
        }
      ]
    },
    {
      "name": "Self",
      "item": [
        {
          "id": "690a7c0e-de97-4661-b75e-a7677f360f60",
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
              "id": "b987918c-ebfa-42c4-b1eb-e3d95e10bd34"
            }
          ]
        }
      ]
    },
    {
      "name": "Associated",
      "item": [
        {
          "id": "2ab40638-fa4b-488a-8ae3-60a26bd4d203",
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
              "id": "3bbbc84e-2b51-493b-be6d-66a03224e0a8"
            }
          ]
        }
      ]
    },
    {
      "name": "Favorites",
      "item": [
        {
          "id": "91e857fa-1ce8-4871-8891-719f54c1c3a1",
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
              "id": "c8ea8529-51e4-43b1-ab54-6266be8193cc"
            }
          ]
        }
      ]
    },
    {
      "name": "Mentioned",
      "item": [
        {
          "id": "64a4be76-d3f8-4caf-bb48-cf23e675630c",
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
              "id": "64d50f23-763f-4311-b19a-c1dbaa55064c"
            }
          ]
        }
      ]
    },
    {
      "name": "Merges",
      "item": [
        {
          "id": "6e45495a-4653-409a-817c-68ea476745ff",
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
              "id": "f325a7ff-13ad-4d88-861b-a1ae926008a4"
            }
          ]
        }
      ]
    },
    {
      "name": "Notifications",
      "item": [
        {
          "id": "40cece18-ab96-4857-bbb2-921c869dc033",
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
              "id": "f9fa485e-c364-49c1-abcf-0b1ed8af5d80"
            }
          ]
        },
        {
          "id": "ec2e6c7d-f47d-4e78-b556-1e7815395b0a",
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
              "id": "053af298-da6d-46f0-999c-b5988348e273"
            }
          ]
        },
        {
          "id": "16e925f7-fc47-49f8-b94e-16a388033ea7",
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
              "id": "a182f8ed-add7-4efd-911b-0e0c0feec7ea"
            }
          ]
        },
        {
          "id": "8bd07727-2bca-4907-b15c-5aaba5e4b74b",
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
              "id": "1f79e387-c290-479e-8d6c-eebecd2b4e9d"
            }
          ]
        }
      ]
    },
    {
      "name": "Privileges",
      "item": [
        {
          "id": "1f4168c8-3497-4b25-a6d0-aef5c9796dfc",
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
              "id": "9c24666d-9aa4-48da-8118-c9b00197906c"
            }
          ]
        },
        {
          "id": "551f7f32-0a6e-4dd8-9450-f1db775ac7ba",
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
              "id": "03e2f9dd-400c-476c-98b1-287dd9548087"
            }
          ]
        }
      ]
    },
    {
      "name": "Questions",
      "item": [
        {
          "id": "7df494b3-8500-4d84-b8a3-2800f49322e1",
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
              "id": "1300e235-93d4-4176-a9ec-1f680f3308b1"
            }
          ]
        },
        {
          "id": "c3667bc1-e07f-4a2f-b1ef-25d1d64887c6",
          "name": "returns-the-questions-that-have-active-bounties-offered-by-the-user-associated-with-the-given-access",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/questions/featured?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the questions that have active bounties offered by the user associated with the given access_token.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ad33e277-cfb6-415d-aac2-fa757bd0d185"
            }
          ]
        },
        {
          "id": "3bb0de71-8bb2-4ea5-9bd4-c424ed91f081",
          "name": "returns-the-questions-owned-by-the-user-associated-with-the-given-access-token-that-have-no-answers-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/questions/no-answers?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the questions owned by the user associated with the given access_token that have no answers.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9bbf88cf-514c-42af-92f6-cef15c85d050"
            }
          ]
        },
        {
          "id": "fcca8e26-0bb6-481f-a160-b4bde8830146",
          "name": "returns-the-questions-owned-by-the-user-associated-with-the-given-access-token-that-have-no-accepted",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/questions/unaccepted?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the questions owned by the user associated with the given access_token that have no accepted answer.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "06932c1d-cf88-4789-adc6-89c603885dce"
            }
          ]
        },
        {
          "id": "eeeb6e2e-a245-4515-b033-4a09a8148664",
          "name": "returns-the-questions-owned-by-the-user-associated-with-the-given-access-token-that-are-not-consider",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/questions/unanswered?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the questions owned by the user associated with the given access_token that are not considered answered.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3fce3d17-41b8-455f-8bba-569c59ee6aa7"
            }
          ]
        },
        {
          "id": "225790f1-701d-41d2-9a9a-7ddb36771f5f",
          "name": "gets-all-the-questions-on-the-site-this-method-allows-you-make-fairly-flexible-queries-across-the-en",
          "request": {
            "url": "http://api.stackexchange.com/2.2/questions?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&tagged=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all the questions on the site.\n \nThis method allows you make fairly flexible queries across the entire corpus of questions on a site. For example, getting all questions asked in the the week of Jan 1st 2011 with scores of 10 or more is a single query with parameters sort=votes&min=10&fromdate=1293840000&todate=1294444800.\n \nTo constrain questions returned to those with a set of tags, use the tagged parameter with a semi-colon delimited list of tags. This is an and contraint, passing tagged=c;java will return only those questions with both tags. As such, passing more than 5 tags will always return zero results.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n - hot - by the formula ordering the hot tab Does not accept min or max\n - week - by the formula ordering the week tab Does not accept min or max\n - month - by the formula ordering the month tab Does not accept min or max\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f8714141-84f0-4716-ba4e-02f59dad9f41"
            }
          ]
        },
        {
          "id": "fdd72037-44a9-476d-8e36-38345f717195",
          "name": "returns-all-the-questions-with-active-bounties-in-the-system-the-sorts-accepted-by-this-method-opera",
          "request": {
            "url": "http://api.stackexchange.com/2.2/questions/featured?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&tagged=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all the questions with active bounties in the system.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "29326be4-2bb5-49a8-a923-c0e306d4210e"
            }
          ]
        },
        {
          "id": "147b9815-cd48-409d-95c3-94198ad9e5bb",
          "name": "returns-questions-which-have-received-no-answers-compare-with-questionsunanswered-which-mearly-retur",
          "request": {
            "url": "http://api.stackexchange.com/2.2/questions/no-answers?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&tagged=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns questions which have received no answers.\n \nCompare with /questions/unanswered which mearly returns questions that the sites consider insufficiently well answered.\n \nThis method corresponds roughly with the this site tab.\n \nTo constrain questions returned to those with a set of tags, use the tagged parameter with a semi-colon delimited list of tags. This is an and contraint, passing tagged=c;java will return only those questions with both tags. As such, passing more than 5 tags will always return zero results.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fca8430c-a5ef-47c0-9f8e-971dd0fba4b0"
            }
          ]
        },
        {
          "id": "d7f1dfda-3463-4f0f-a6ab-1575b1d4b55b",
          "name": "returns-questions-the-site-considers-to-be-unanswered-note-that-just-because-a-question-has-an-answe",
          "request": {
            "url": "http://api.stackexchange.com/2.2/questions/unanswered?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&tagged=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns questions the site considers to be unanswered.\n \nNote that just because a question has an answer, that does not mean it is considered answered. While the rules are subject to change, at this time a question must have at least one upvoted answer to be considered answered.\n \nTo constrain questions returned to those with a set of tags, use the tagged parameter with a semi-colon delimited list of tags. This is an and contraint, passing tagged=c;java will return only those questions with both tags. As such, passing more than 5 tags will always return zero results.\n \nCompare with /questions/no-answers.\n \nThis method corresponds roughly with the unanswered tab.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "323ddde4-8d4e-42a2-be1a-090ea43e3537"
            }
          ]
        },
        {
          "id": "2673741d-a9a0-4f38-a51d-156d7bf0a64e",
          "name": "returns-the-questions-identified-in-ids-this-is-most-useful-for-fetching-fresh-data-when-maintaining",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "questions/:ids"
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
            "description": "Returns the questions identified in {ids}.\n \nThis is most useful for fetching fresh data when maintaining a cache of question ids, or polling for changes.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for question_id on question objects.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b00da0b7-89a6-4ec3-ba81-ac64abfadfba"
            }
          ]
        },
        {
          "id": "9c2949d3-c5a3-47cd-baa3-0a38daa2cff1",
          "name": "gets-the-answers-to-a-set-of-questions-identified-in-id-this-method-is-most-useful-if-you-have-a-set",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "questions/:ids/answers"
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
            "description": "Gets the answers to a set of questions identified in id.\n \nThis method is most useful if you have a set of interesting questions, and you wish to obtain all of their answers at once or if you are polling for new or updates answers (in conjunction with sort=activity).\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for question_id on question objects.\n \nThe sorts accepted by this method operate on the follow fields of the answer object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of answers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b0a64d32-3c59-40eb-bf14-46e3d4148d74"
            }
          ]
        },
        {
          "id": "39873f5e-3d19-46e0-833b-601d58de6b20",
          "name": "gets-the-comments-on-a-question-if-you-know-that-you-have-an-question-id-and-need-the-comments-use-t",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "questions/:ids/comments"
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
            "description": "Gets the comments on a question.\n \nIf you know that you have an question id and need the comments, use this method. If you know you have a answer id, use /answers/{ids}/comments. If you are unsure, use /posts/{ids}/comments.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for question_id on question objects.\n \nThe sorts accepted by this method operate on the follow fields of the comment object:\n - creation - creation_date\n - votes - score\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "26788c2c-72b8-4e52-af2b-b25f042059f5"
            }
          ]
        },
        {
          "id": "fc6a5864-ea3a-4368-a92a-194f3dfdf1c7",
          "name": "gets-questions-which-link-to-those-questions-identified-in-ids-this-method-only-considers-questions-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "questions/:ids/linked"
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
            "description": "Gets questions which link to those questions identified in {ids}.\n \nThis method only considers questions that are linked within a site, and will never return questions from another Stack Exchange site.\n \nA question is considered \"linked\" when it explicitly includes a hyperlink to another question, there are no other heuristics.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for question_id on question objects.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n - rank - a priority sort by site applies, subject to change at any time Does not accept min or max\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e18f3f5c-247e-497b-8fd1-8fe1f046c8f9"
            }
          ]
        },
        {
          "id": "f3cc930f-1079-44d2-ac4a-3927e171e32f",
          "name": "returns-questions-that-the-site-considers-related-to-those-identified-in-ids-the-algorithm-for-deter",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "questions/:ids/related"
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
            "description": "Returns questions that the site considers related to those identified in {ids}.\n \nThe algorithm for determining if questions are related is not documented, and subject to change at any time. Futhermore, these values are very heavily cached, and may not update immediately after a question has been editted. It is also not guaranteed that a question will be considered related to any number (even non-zero) of questions, and a consumer should be able to handle a variable number of returned questions.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for question_id on question objects.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n - rank - a priority sort by site applies, subject to change at any time Does not accept min or max\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5f9780ee-b52a-4d81-83e6-bacf5361f096"
            }
          ]
        }
      ]
    },
    {
      "name": "Reputation",
      "item": [
        {
          "id": "71d4b4d8-de10-4065-8a11-c4da55ef09c7",
          "name": "returns-the-reputation-changed-for-the-user-associated-with-the-given-access-token-this-method-retur",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/reputation?callback=%7B%7D&filter=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the reputation changed for the user associated with the given access_token.\n \nThis method returns a list of reputation changes."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "337bafaa-df56-4fae-a4bd-34c2846af91a"
            }
          ]
        },
        {
          "id": "defcabc3-8d19-45f4-8b0a-42ad71a8f142",
          "name": "returns-users-public-reputation-history-this-method-returns-a-list-of-reputation-history",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/reputation-history?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns user's public reputation history.\n \nThis method returns a list of reputation_history."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3d809018-4217-406a-ae97-fee782ac4c9a"
            }
          ]
        },
        {
          "id": "95e1c1ea-7eed-4e3c-8be0-632f60ce0741",
          "name": "returns-users-full-reputation-history-including-private-events--this-method-requires-an-access-token",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/reputation-history/full?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns user's full reputation history, including private events.\n \n This method requires an access_token, with a scope containing \"private_info\".\n \nThis method returns a list of reputation_history."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "33ec0b82-1913-44ca-86ee-33656b5454f1"
            }
          ]
        }
      ]
    },
    {
      "name": "Suggested Edits",
      "item": [
        {
          "id": "d3d570df-3d67-4a51-81d8-8e6c94769738",
          "name": "returns-the-suggested-edits-the-user-identified-by-access-token-has-submitted-this-method-returns-a-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/suggested-edits?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the suggested edits the user identified by access_token has submitted.\n \nThis method returns a list of suggested-edits."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd058c3a-0479-4d93-a540-130a85198b8d"
            }
          ]
        }
      ]
    },
    {
      "name": "Tags",
      "item": [
        {
          "id": "e8c2d578-7671-4710-8181-9834d4b75086",
          "name": "returns-the-tags-the-user-identified-by-the-access-token-passed-is-active-in-this-method-returns-a-l",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/tags?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the tags the user identified by the access_token passed is active in.\n \nThis method returns a list of tags."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8332b220-4dd7-4195-8df8-6e96102ec059"
            }
          ]
        },
        {
          "id": "c2286653-6ce9-44dd-9b54-adae9304a18a",
          "name": "returns-the-top-30-answers-the-user-associated-with-the-given-access-token-has-posted-in-response-to",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "me/tags/:tags/top-answers"
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
            "description": "Returns the top 30 answers the user associated with the given access_token has posted in response to questions with the given tags.\n \nThis method returns a list of answers."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "12501e35-d2f2-4cb3-b5e6-a75e268f261e"
            }
          ]
        },
        {
          "id": "e8460933-a37e-4321-b125-c97035603e09",
          "name": "returns-the-top-30-questions-the-user-associated-with-the-given-access-token-has-posted-in-response-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "me/tags/:tags/top-questions"
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
            "description": "Returns the top 30 questions the user associated with the given access_token has posted in response to questions with the given tags.\n \nThis method returns a list of questions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eb11478b-0b01-4f6e-8c98-64e62c86c335"
            }
          ]
        },
        {
          "id": "3d809c4a-40c2-493f-92e4-046bd907a63e",
          "name": "returns-a-subset-of-the-actions-the-user-identified-by-the-passed-access-token-has-taken-on-the-site",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/timeline?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a subset of the actions the user identified by the passed access_token has taken on the site.\n \nThis method returns a list of user timeline objects."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "abafdf33-7b22-496d-abf4-b5ed683bde45"
            }
          ]
        },
        {
          "id": "cbf7facb-a37f-4ded-a6df-80de328197e7",
          "name": "returns-the-user-identified-by-access-tokens-top-30-tags-by-answer-score-this-method-returns-a-list-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/top-answer-tags?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the user identified by access_token's top 30 tags by answer score.\n \nThis method returns a list of top tag objects."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "13cea19d-f8a5-4088-83fe-60c6fff0c50f"
            }
          ]
        },
        {
          "id": "0496de68-f5f1-46d6-9739-f581f9997108",
          "name": "returns-the-user-identified-by-access-tokens-top-30-tags-by-question-score-this-method-returns-a-lis",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/top-question-tags?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the user identified by access_token's top 30 tags by question score.\n \nThis method returns a list of top tag objects."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "89ab703d-ec26-4fdc-8dc7-d69444644c61"
            }
          ]
        }
      ]
    },
    {
      "name": "Write Permissions",
      "item": [
        {
          "id": "91be9f93-5b23-4ac1-847c-2faf0d8ca0ca",
          "name": "returns-the-write-permissions-a-user-has-via-the-api-given-an-access-token-the-stack-exchange-api-gi",
          "request": {
            "url": "http://api.stackexchange.com/2.2/me/write-permissions?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the write permissions a user has via the api, given an access token.\n \nThe Stack Exchange API gives users the ability to create, edit, and delete certain types. This method returns whether the passed user is capable of performing those actions at all, as well as how many times a day they can.\n \nThis method does not consider the user's current quota (ie. if they've already exhausted it for today) nor any additional restrictions on write access, such as editing deleted comments.\n \nThis method returns a list of write_permissions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6cad3061-3302-4f66-92d8-2d64963f3e49"
            }
          ]
        }
      ]
    },
    {
      "name": "Posts",
      "item": [
        {
          "id": "779e5f1c-16f1-444e-a9b7-4c2237fd49ca",
          "name": "fetches-all-posts-questions-and-answers-on-the-site-in-many-ways-this-method-is-the-union-of-questio",
          "request": {
            "url": "http://api.stackexchange.com/2.2/posts?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches all posts (questions and answers) on the site.\n \nIn many ways this method is the union of /questions and /answers, returning both sets of data albeit only the common fields.\n \nMost applications should use the question or answer specific methods, but /posts is available for those rare cases where any activity is of intereset. Examples of such queries would be: \"all posts on Jan. 1st 2011\" or \"top 10 posts by score of all time\".\n \nThe sorts accepted by this method operate on the follow fields of the post object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of posts."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7c50815c-3955-466b-8ee7-072345550ae4"
            }
          ]
        },
        {
          "id": "a5364a64-978d-4db8-a604-8a395042aa08",
          "name": "fetches-a-set-of-posts-by-ids-this-method-is-meant-for-grabbing-an-object-when-unsure-whether-an-id-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "posts/:ids"
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
            "description": "Fetches a set of posts by ids.\n \nThis method is meant for grabbing an object when unsure whether an id identifies a question or an answer. This is most common with user entered data.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for post_id, answer_id, or question_id on post, answer, and question objects respectively.\n \nThe sorts accepted by this method operate on the follow fields of the post object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of posts."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0df945a2-c24d-4324-82d6-5872661fee89"
            }
          ]
        },
        {
          "id": "53bf142b-d2bf-4fbd-a558-7db59e0c5dd8",
          "name": "gets-the-comments-on-the-posts-identified-in-ids-regardless-of-the-type-of-the-posts-this-method-is-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "posts/:ids/comments"
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
            "description": "Gets the comments on the posts identified in ids, regardless of the type of the posts.\n \nThis method is meant for cases when you are unsure of the type of the post id provided. Generally, this would be due to obtaining the post id directly from a user.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for post_id, answer_id, or question_id on post, answer, and question objects respectively.\n \nThe sorts accepted by this method operate on the follow fields of the comment object:\n - creation - creation_date\n - votes - score\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of comments."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "38b295f6-a629-4bfe-b0d2-354aa50f7fca"
            }
          ]
        },
        {
          "id": "12c83f72-2e3f-48ba-b436-9e5f0168e615",
          "name": "returns-edit-revisions-for-the-posts-identified-in-ids-ids-can-contain-up-to-100-semicolon-delimited",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "posts/:ids/revisions"
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
            "description": "Returns edit revisions for the posts identified in ids.\n \n{ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for post_id, answer_id, or question_id on post, answer, and question objects respectively.\n \nThis method returns a list of revisions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a79973be-8ac6-4620-9960-44fa1664801c"
            }
          ]
        },
        {
          "id": "670cfc39-c942-4f0f-af33-763447332220",
          "name": "returns-suggsted-edits-on-the-posts-identified-in-ids---creation--creation-date--approval--approval-",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "posts/:ids/suggested-edits"
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
            "description": "Returns suggsted edits on the posts identified in ids.\n \n - creation - creation_date\n - approval - approval_date\n - rejection - rejection_date\n  creation is the default sort.\n \n {ids} can contain up to 100 semicolon delimited ids, to find ids programatically look for post_id, answer_id, or question_id on post, answer, and question objects respectively.\n \nThis method returns a list of suggested-edits."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fd277ebf-ae77-4724-91e1-18e2ac2446b2"
            }
          ]
        },
        {
          "id": "2a3b2091-2613-4e7b-b825-f5cfd7c53377",
          "name": "create-a-new-comment-use-an-access-token-with-write-access-to-create-a-new-comment-on-a-post-this-me",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "posts/:id/comments/add"
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
            "description": "Create a new comment.\n \nUse an access_token with write_access to create a new comment on a post.\n \nThis method returns the created comment."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "494d87f3-299c-428d-8e3f-faee7e61f770"
            }
          ]
        }
      ]
    }
  ]
}