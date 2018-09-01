{
  "info": {
    "name": "Stack Exchange Get User Moderators",
    "_postman_id": "66f90546-cedf-482e-ba91-a8a36ba20bed",
    "description": "Gets those users on a site who can exercise moderation powers.\n \nNote, employees of Stack Exchange Inc. will be returned if they have been granted moderation powers on a site even if they have never been appointed or elected explicitly. This method checks abilities, not the manner in which they were obtained.\n \nThe sorts accepted by this method operate on the follow fields of the user object:\n - reputation - reputation\n - creation - creation_date\n - name - display_name\n - modified - last_modified_date\n  reputation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis method returns a list of users.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "74f19aa8-36d6-4d7e-92bd-5a2307e3bde9",
          "name": "gets-those-users-on-a-site-who-can-exercise-moderation-powers-note-employees-of-stack-exchange-inc-w",
          "request": {
            "url": "http://api.stackexchange.com/2.2/users/moderators?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets those users on a site who can exercise moderation powers"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a52fe444-8109-4bba-b1f1-0362e243354d"
            }
          ]
        }
      ]
    }
  ]
}