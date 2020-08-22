---
weight: 10
title: API Reference
---

# Introduction

Welcome to the Potato API! A simple API that holds product information: name and price.

Language bindings are in Shell, Go, Python, and Javascript! 


# Authentication

> To authorize, use this code:

```go
package main

import "github.com/cgliu-create/potatoapi/lang/goapi"

func main() {
  api := goapi.Authorize("potatopotato")
}
```

```python
from pybinding import potato

if __name__=="__main__":
  api = potato()
  api.authorize("potatopotato")
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Token: potatopotato"
```

```javascript
const api = require("jsbinding");

api.authorize('potatopotato');
```

> Make sure to replace `potatopotato` with your API key.

Potato API uses API keys to allow access to the API. You can register a new API key with the [developer portal](http://example.com/developers).

Potato API expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Token: potatopotato`

<aside class="notice">
Replace <code>potatopotato</code> with your personal API key.
</aside>
