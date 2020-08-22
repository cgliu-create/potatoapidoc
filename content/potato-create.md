---
weight: 11
title: Product
---

# Product

## Create Product

```go
package main

import "github.com/cgliu-create/potatoapi/lang/goapi"

func main() {
  api := goapi.Authorize("potatopotato")
  Name := "abc"
  Price := 123
  response := api.CreateProduct(Name, Price)
}
```

```python
from pybinding import potato

if __name__=="__main__":
  api = potato()
  api.authorize("potatopotato")
  name = "abc"
  price = 123
  response = api.createProduct(name, price)
```

```shell
curl -d '{"Name":"abcd", "Price":1234}'
  -H "Content-Type: application/json" -H "Token: potatopotato"
  -X POST "https://localhost:8000/api/products"
```

```javascript
const api = require("jsbinding");

api.authorize('potatopotato');
let name = "abc";
let price = 123;
let response = api.createProduct(name, price);
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
"Product not created"
```

This endpoint adds a new product.

### HTTP Request

`POST https://localhost:8000/api/products`

