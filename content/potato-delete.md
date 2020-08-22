---
weight: 15
title: Delete Specific Product
---

## Delete Specific Product

```go
package main

import "github.com/cgliu-create/potatoapi/lang/goapi"

func main() {
  api := goapi.Authorize("potatopotatopotato")
  id := 2
  response := api.DeleteProduct(id) 
}
```


```python
from pybinding import potato

if __name__=="__main__":
  api = potato()
  api.authorize("potatopotatopotato")
  id = 2
  response = api.deleteProduct(id)
```

```shell
curl
    -H "Token: potatopotatopotato"
    -X DELETE "https://localhost:8000/api/products/2"
```

```javascript
const api = require("jsbinding");

api.authorize('potatopotatopotato');
let id = 2;
let response = api.updateProduct(id, name, price);
```

> The above command returns a status message:

```json
"Product removed"
or
"Product not found"
```

This endpoint removes a specific product.

### HTTP Request

`DELETE https://localhost:8000/api/products/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Product to retrieve

