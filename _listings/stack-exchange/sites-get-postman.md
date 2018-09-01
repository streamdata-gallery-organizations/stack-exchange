{
  "info": {
    "name": "Stack Exchange Get Sites",
    "_postman_id": "1f275017-dfa7-4f76-9183-3b7634f349c4",
    "description": "Returns all sites in the network.\n \nThis method allows for discovery of new sites, and changes to existing ones. Be aware that unlike normal API methods, this method should be fetched very infrequently, it is very unusual for these values to change more than once on any given day. It is suggested that you cache its return for at least one day, unless your app encounters evidence that it has changed (such as from the /info method).\n \nThe pagesize parameter for this method is unbounded, in acknowledgement that for many applications repeatedly fetching from /sites would complicate start-up tasks needlessly.\n \nThis method returns a list of sites.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "sites",
      "item": [
        {
          "id": "5703d6e3-c0a6-4feb-b212-5f02172f4296",
          "name": "returns-all-sites-in-the-network-this-method-allows-for-discovery-of-new-sites-and-changes-to-existi",
          "request": {
            "url": "http://api.stackexchange.com/2.2/sites?callback=%7B%7D&filter=%7B%7D&page=%7B%7D&pagesize=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all sites in the network"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee2702a8-3c46-4aa7-b7a8-a83c00b855fd"
            }
          ]
        }
      ]
    }
  ]
}