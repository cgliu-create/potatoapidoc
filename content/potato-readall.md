---
weight: 12
title: Read All Products
--- 

## Read All Products

```go
package main

import "github.com/cgliu-create/potatoapi/lang/goapi"

func main() {
  api := goapi.Authorize("potatopotatopotato")
  response := api.ReadAllProduct()
}
```

```python
from pybinding import potato

if __name__=="__main__":
  api = potato()
  api.authorize("potatopotatopotato")
  response = api.readAllProduct()
```

```shell
curl
    -H "Token: potatopotatopotato"
    -X GET "https://localhost:8000/api/products"
```

```javascript
const api = require("jsbinding");

api.authorize('potatopotatopotato');
let response = api.readAllProduct();
```

> The above command returns JSON structured like this:

```json
[
  {
    "ID": 1,
    "CreatedAt": "2020-08-18T14:01:03.439858-04:00",
    "UpdatedAt": "2020-08-18T14:01:03.439858-04:00",
    "DeletedAt": null,
    "Name": "MoldyPotato",
    "Price": 10
  },
  {
    "ID": 2,
    "CreatedAt": "2020-08-18T14:01:03.439858-04:00",
    "UpdatedAt": "2020-08-18T14:01:03.439858-04:00",
    "DeletedAt": null,
    "Name": "FreshPotato",
    "Price": 100
  }
]
or
"Product not found"
```

This endpoint retrieves all products.

### HTTP Request

`GET https://localhost:8000/api/products`

<aside class="success">
Remember — all requests require authentication!
</aside>
