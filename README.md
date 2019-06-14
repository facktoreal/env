# Env loader

.env file loader

### Usage

Current release version of backend. Can be set in CI/CD using:

```go
package main

import "yn.ee/facktoreal/env"

func main()  {
    if err := env.Init(); err != nil {
        // handle error
    }
     
    // string or ""
    env.MayGetString("ENV_STRING_VAR")
    
    // string or panic
    env.MustGetString("ENV_STRING_VAR")
    
    // int or panic
    env.MustGetInt("ENV_INT")
    
    // must exist and not empty or panic
    env.MustPresent("ENV_BOOL")
}
```

