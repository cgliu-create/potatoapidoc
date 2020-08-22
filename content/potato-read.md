---
weight: 13
title: Read Specific Product
---

## Read Specific Product

```go
package main

import "github.com/cgliu-create/potatoapi/lang/goapi"

func main() {
  api := goapi.Authorize("potatopotatopotato")
  id := 2
  response := api.ReadProduct(id) 
}
```


```python
from pybinding import potato

if __name__=="__main__":
  api = potato()
  api.authorize("potatopotatopotato")
  id = 2
  response = api.readProduct(id)
```

```shell
curl
    -H "Token: potatopotatopotato"
    -X GET "https://localhost:8000/api/products/2"
```

```javascript
const api = require("jsbinding");

api.authorize('potatopotatopotato');
let id = 2;
let response = api.readProduct(id);
```

> The above command returns JSON structured like this:

```json
{
    "ID": 2,
    "CreatedAt": "2020-08-18T14:01:03.439858-04:00",
    "UpdatedAt": "2020-08-18T14:01:03.439858-04:00",
    "DeletedAt": null,
    "Name": "FreshPotato",
    "Price": 100
}
or
"Product not found"
```

This endpoint retrieves a specific product.

### HTTP Request

`GET https://localhost:8000/api/products/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Product to retrieve

