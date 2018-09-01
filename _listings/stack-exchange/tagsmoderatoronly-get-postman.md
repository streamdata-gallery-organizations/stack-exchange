{
  "info": {
    "name": "Stack Exchange Get Tags Moderator Only",
    "_postman_id": "a2f86cf3-9f6f-42fe-80d7-2db6f1257b26",
    "description": "Returns the tags found on a site that only moderators can use.\n \nThe inname parameter lets a consumer filter down to tags that contain a certain substring. For example, inname=own would return both \"download\" and \"owner\" amongst others.\n \nThis method returns a list of tags.\n \nThe sorts accepted by this method operate on the follow fields of the tag object:\n - popular - count\n - activity - the creation_date of the last question asked with the tag\n - name - name\n  popular is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "bd05d308-58ce-4ef2-80b7-5eaf9a38a59e",
          "name": "returns-the-tags-found-on-a-site-that-only-moderators-can-use-the-inname-parameter-lets-a-consumer-f",
          "request": {
            "url": "http://api.stackexchange.com/2.2/tags/moderator-only?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the tags found on a site that only moderators can use"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6997fe61-2d52-4a9c-a289-40ab4c6b46d0"
            }
          ]
        }
      ]
    }
  ]
}