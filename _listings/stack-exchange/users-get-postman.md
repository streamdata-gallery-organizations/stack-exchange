{
  "info": {
    "name": "Stack Exchange Get Users",
    "_postman_id": "985ba0f7-97f4-49c2-b933-1e7955b644ed",
    "description": "Returns all users on a site.\n \nThis method returns a list of users.\n \nThe sorts accepted by this method operate on the follow fields of the user object:\n - reputation - reputation\n - creation - creation_date\n - name - display_name\n - modified - last_modified_date\n  reputation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThe inname parameter lets consumers filter the results down to just those users with a certain substring in their display name. For example, inname=kevin will return all users with both users named simply \"Kevin\" or those with Kevin as one of (or part of) their names; such as \"Kevin Montrose\".",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "52e5e042-6dc9-496a-9707-f8f116698574",
          "name": "returns-all-users-on-a-site-this-method-returns-a-list-of-users-the-sorts-accepted-by-this-method-op",
          "request": {
            "url": "http://api.stackexchange.com/2.2/users?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all users on a site"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c04f489-cbdc-4af1-97a9-3f704a02625e"
            }
          ]
        }
      ]
    }
  ]
}