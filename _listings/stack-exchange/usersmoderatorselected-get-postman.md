{
  "info": {
    "name": "Stack Exchange Get Users Moderators Elected",
    "_postman_id": "d8dbe88c-85bc-48da-8171-5ab5cc0062af",
    "description": "Returns those users on a site who both have moderator powers, and were actually elected.\n \nThis method excludes Stack Exchange Inc. employees, unless they were actually elected moderators on a site (which can only have happened prior to their employment).\n \nThe sorts accepted by this method operate on the follow fields of the user object:\n - reputation - reputation\n - creation - creation_date\n - name - display_name\n - modified - last_modified_date\n  reputation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of users.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "b3ff46bb-2a22-4231-9121-0dc5cea6cb1d",
          "name": "returns-those-users-on-a-site-who-both-have-moderator-powers-and-were-actually-elected-this-method-e",
          "request": {
            "url": "http://api.stackexchange.com/2.2/users/moderators/elected?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns those users on a site who both have moderator powers, and were actually elected"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "365bf38f-fa37-468e-bdc9-80bf5521fd9a"
            }
          ]
        }
      ]
    }
  ]
}