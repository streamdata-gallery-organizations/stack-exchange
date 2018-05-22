{
  "info": {
    "name": "Stack Exchange Get Badge Tags",
    "_postman_id": "08c259fa-9ca1-41f2-9ce9-65984384b899",
    "description": "Returns the badges that are awarded for participation in specific tags.\n \nFor the rank sort, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \nThis method returns a list of badges.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "badges",
      "item": [
        {
          "id": "35e305ed-799c-4de0-8410-66c801fcb7cf",
          "name": "returns-the-badges-that-are-awarded-for-participation-in-specific-tags-for-the-rank-sort-bronze-is-g",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges/tags?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the badges that are awarded for participation in specific tags"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "97a2d04a-4735-4d8a-b3b6-1739b14a5ed5"
            }
          ]
        }
      ]
    }
  ]
}