{
  "info": {
    "name": "Stack Exchange Get Badge Name",
    "_postman_id": "f9d9adf0-c162-4626-ae82-cf1aee2ff5f8",
    "description": "Gets all explicitly named badges in the system.\n \nA named badged stands in opposition to a tag-based badge. These are referred to as general badges on the sites themselves.\n \nFor the rank sort, bronze is greater than silver which is greater than gold. Along with sort=rank, set max=gold for just gold badges, max=silver&min=silver for just silver, and min=bronze for just bronze.\n \nrank is the default sort.\n \nThis method returns a list of badges.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "badges",
      "item": [
        {
          "id": "3a5fb07d-27ee-4ec1-ae82-6e6bb334f1a4",
          "name": "gets-all-explicitly-named-badges-in-the-system-a-named-badged-stands-in-opposition-to-a-tagbased-bad",
          "request": {
            "url": "http://api.stackexchange.com/2.2/badges/name?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&inname=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets all explicitly named badges in the system"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d17e8515-b636-484b-9ac4-929e5dc95e66"
            }
          ]
        }
      ]
    }
  ]
}