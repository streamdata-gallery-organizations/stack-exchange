{
  "info": {
    "name": "Stack Exchange Get Tags Requred",
    "_postman_id": "0b0e92c9-a784-49cc-88a7-0740c26fc445",
    "description": "Returns the tags found on a site that fulfill required tag constraints on questions.\n \nThe inname parameter lets a consumer filter down to tags that contain a certain substring. For example, inname=own would return both \"download\" and \"owner\" amongst others.\n \nThis method returns a list of tags.\n \nThe sorts accepted by this method operate on the follow fields of the tag object:\n - popular - count\n - activity - the creation_date of the last question asked with the tag\n - name - name\n  popular is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tags",
      "item": [
        {
          "id": "321f6b7d-cfe3-4c0c-b866-4f667314e107",
          "name": "returns-the-tags-found-on-a-site-that-fulfill-required-tag-constraints-on-questions-the-inname-param",
          "request": {
            "url": "http://api.stackexchange.com/2.2/tags/required?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the tags found on a site that fulfill required tag constraints on questions"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "facad21f-45a2-4399-8e7b-51141b722238"
            }
          ]
        }
      ]
    }
  ]
}