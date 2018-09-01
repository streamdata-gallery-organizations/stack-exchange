{
  "info": {
    "name": "Stack Exchange Create Filter",
    "_postman_id": "9e0d9393-3ff3-4cf1-a98d-020909c10756",
    "description": "Creates a new filter given a list of includes, excludes, a base filter, and whether or not this filter should be \"unsafe\".\n \nFilter \"safety\" is defined as follows. Any string returned as a result of an API call with a safe filter will be inline-able into HTML without script-injection concerns. That is to say, no additional sanitizing (encoding, HTML tag stripping, etc.) will be necessary on returned strings. Applications that wish to handle sanitizing themselves should create an unsafe filter. All filters are safe by default, under the assumption that double-encoding bugs are more desirable than script injections.\n \nIf no base filter is specified, the default filter is assumed. When building a filter from scratch, the none built-in filter is useful.\n \nWhen the size of the parameters being sent to this method grows to large, problems can occur. This method will accept POST requests to mitigate this.\n \nIt is not expected that many applications will call this method at runtime, filters should be pre-calculated and \"baked in\" in the common cases. Furthermore, there are a number of built-in filters which cover common use cases.\n \nThis method returns a single filter.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "files",
      "item": [
        {
          "id": "5eb032b2-1b9a-412e-957b-68a586112877",
          "name": "creates-a-new-filter-given-a-list-of-includes-excludes-a-base-filter-and-whether-or-not-this-filter-",
          "request": {
            "url": "http://api.stackexchange.com/2.2/filters/create?base=%7B%7D&exclude=%7B%7D&include=%7B%7D&unsafe=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new filter given a list of includes, excludes, a base filter, and whether or not this filter should be \"unsafe\""
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "31417d87-b657-4fce-9462-84ccff496206"
            }
          ]
        }
      ]
    }
  ]
}