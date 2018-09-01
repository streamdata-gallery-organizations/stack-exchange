{
  "info": {
    "name": "Stack Exchange Advanced Search",
    "_postman_id": "f4354d54-0720-438b-9a2a-7c45ba739142",
    "description": "Searches a site for any questions which fit the given criteria.\n \nSearch criteria are expressed using the following parameters:\n  - q - a free form text parameter, will match all question properties based on an undocumented algorithm.\n - accepted - true to return only questions with accepted answers, false to return only those without. Omit to elide constraint.\n - answers - the minimum number of answers returned questions must have.\n - body - text which must appear in returned questions' bodies.\n - closed - true to return only closed questions, false to return only open ones. Omit to elide constraint.\n - migrated - true to return only questions migrated away from a site, false to return only those not. Omit to elide constraint.\n - notice - true to return only questions with post notices, false to return only those without. Omit to elide constraint.\n - nottagged - a semicolon delimited list of tags, none of which will be present on returned questions.\n - tagged - a semicolon delimited list of tags, of which at least one will be present on all returned questions.\n - title - text which must appear in returned questions' titles.\n - user - the id of the user who must own the questions returned.\n - url - a url which must be contained in a post, may include a wildcard.\n - views - the minimum number of views returned questions must have.\n - wiki - true to return only community wiki questions, false to return only non-community wiki ones. Omit to elide constraint.\n  \nAt least one additional parameter must be set if nottagged is set, for performance reasons.\n \nThe sorts accepted by this method operate on the follow fields of the question object:\n - activity - last_activity_date\n - creation - creation_date\n - votes - score\n - relevance - matches the relevance tab on the site itself Does not accept min or max\n  activity is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of questions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "search",
      "item": [
        {
          "id": "4d9ef601-31b2-4a5e-9294-f33e72451bac",
          "name": "searches-a-site-for-any-questions-which-fit-the-given-criteria-search-criteria-are-expressed-using-t",
          "request": {
            "url": "http://api.stackexchange.com/2.2/search/advanced?accepted=%7B%7D&answers=%7B%7D&body=%7B%7D&callback=%7B%7D&closed=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&migrated=%7B%7D&min=%7B%7D&notice=%7B%7D&nottagged=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&q=%7B%7D&site=%7B%7D&sort=%7B%7D&tagged=%7B%7D&title=%7B%7D&todate=%7B%7D&url=%7B%7D&user=%7B%7D&views=%7B%7D&wiki=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Searches a site for any questions which fit the given criteria"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8cc7da43-b439-4d99-a43f-3908bedcf24c"
            }
          ]
        }
      ]
    }
  ]
}