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
  api := goapi.Authorize("potatopotatopotato")
}
```

```python
from pybinding import potato

if __name__=="__main__":
  api = potato()
  api.authorize("potatopotatopotato")
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Token: potatopotatopotato"
```

```javascript
const api = require("jsbinding");

api.authorize('potatopotatopotato');
```

> Make sure to replace `potatopotatopotato` with your API key.

Potato API uses API keys to allow access to the API. You can register a new API key with the [developer portal](http://example.com/developers).

Potato API expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Token: potatopotatopotato`

<aside class="notice">
Replace <code>potatopotatopotato</code> with your personal API key.
</aside>
