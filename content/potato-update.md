---
weight: 14
title: Update Specific Product 
---

## Update Specific Product

```go
package main

import "github.com/cgliu-create/potatoapi/lang/goapi"

func main() {
  api := goapi.Authorize("potatopotato")
  Name := "abc"
  Price := 123
  id := 2
  response := api.UpdateProduct(id, Name, Price)
}
```


```python
from pybinding import potato

if __name__=="__main__":
  api = potato()
  api.authorize("potatopotato")
  name = "abc"
  price = 123
  id = 2
  response = api.updateProduct(id, name, price)
```

```shell
   curl -d '{"Name":"abcd", "Price":4321}'
    -H "Content-Type: application/json" -H "Token: potatopotato"
    -X PUT "https://localhost:8000/api/products/2"
```

```javascript
const api = require("jsbinding");

api.authorize('potatopotato');
let name = "abc";
let price = 123;
let id = 2;
let response = api.updateProduct(id, name, price);
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
"Product not changed"
or
"Product not found"
```

This endpoint replaces a specific product.

### HTTP Request

`PUT https://localhost:8000/api/products/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Product to retrieve

