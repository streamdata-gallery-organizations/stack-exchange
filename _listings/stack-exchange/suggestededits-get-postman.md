{
  "info": {
    "name": "Stack Exchange Get Suggested Edits",
    "_postman_id": "0e5d9475-5fc8-47db-bd38-a0015b70b84c",
    "description": "Returns all the suggested edits in the systems.\n \nThis method returns a list of suggested-edits.\n \nThe sorts accepted by this method operate on the follow fields of the suggested_edit object:\n - creation - creation_date\n - approval - approval_date Does not return unapproved suggested_edits\n - rejection - rejection_date Does not return unrejected suggested_edits\n  creation is the default sort.\n \n It is possible to create moderately complex queries using sort, min, max, fromdate, and todate.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "suggested edits",
      "item": [
        {
          "id": "180ffd97-1769-4519-bb3b-b8ff80170a62",
          "name": "returns-all-the-suggested-edits-in-the-systems-this-method-returns-a-list-of-suggestededits-the-sort",
          "request": {
            "url": "http://api.stackexchange.com/2.2/suggested-edits?callback=%7B%7D&filter=%7B%7D&fromdate=%7B%7D&max=%7B%7D&min=%7B%7D&order=%7B%7D&page=%7B%7D&pagesize=%7B%7D&site=%7B%7D&sort=%7B%7D&todate=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all the suggested edits in the systems"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2e47dce2-7618-4591-90d3-0ae325402d0f"
            }
          ]
        }
      ]
    }
  ]
}