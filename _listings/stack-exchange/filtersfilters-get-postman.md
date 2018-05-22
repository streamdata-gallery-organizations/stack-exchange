{
  "info": {
    "name": "Stack Exchange Get Filters",
    "_postman_id": "d238ca24-2ad1-4369-be48-4c43f26a63bb",
    "description": "Returns the fields included by the given filters, and the \"safeness\" of those filters.\n \nIt is not expected that this method will be consumed by many applications at runtime, it is provided to aid in debugging.\n \n{filters} can contain up to 20 semicolon delimited filters. Filters are obtained via calls to /filters/create, or by using a built-in filter.\n \nThis method returns a list of filters.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "files",
      "item": [
        {
          "id": "dd033753-c8cb-4f48-bd66-374f0c97b7f5",
          "name": "returns-the-fields-included-by-the-given-filters-and-the-safeness-of-those-filters-it-is-not-expecte",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.stackexchange.com",
              "path": [
                "2.2",
                "filters/:filters"
              ],
              "variable": [
                {
                  "id": "filters",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the fields included by the given filters, and the \"safeness\" of those filters"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0caa9681-2ce7-477d-83e6-245a5275fdb5"
            }
          ]
        }
      ]
    }
  ]
}