{
  "info": {
    "name": "Stack Exchange Get Tags Synonyms",
    "_postman_id": "fa5fefc6-0aa8-4098-b21f-dbb726796b8d",
    "description": "Returns all tag synonyms found a site.\n \nWhen searching for synonyms of specific tags, it is better to use /tags/{tags}/synonyms over this method.\n \nThe sorts accepted by this method operate on the follow fields of the tag_synonym object:\n - creation - creation_date\n - applied - applied_count\n - activity - last_applied_date\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of tag_synonyms.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "1471c400-3800-4fea-b9c2-4ce7c9c8eafa",
          "name": "returns-all-tag-synonyms-found-a-site-when-searching-for-synonyms-of-specific-tags-it-is-better-to-u",
          "request": {
            "url": "http://api.stackexchange.com/2.2/tags/synonyms?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all tag synonyms found a site"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "92b46777-7081-4076-8094-112f9e926fa6"
            }
          ]
        }
      ]
    }
  ]
}