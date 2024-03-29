# UserAPIForSpeakeasyTemplateService SDK


## Overview

User API for Speakeasy template service: The Rest Template API is an API used for instrucitonal purposes.

### Available Operations

* [CreateUserv1](#createuserv1) - Create user
* [DeleteUserv1](#deleteuserv1) - Delete a user by ID
* [GetHealth](#gethealth) - Healthcheck
* [GetUserv1](#getuserv1) - Get a user by ID
* [SearchUsersv1](#searchusersv1) - Search users
* [UpdateUserv1](#updateuserv1)

## CreateUserv1

Create user

### Example Usage

```go
package main

import(
	forgeholdsamplesdk "github.com/speakeasy-sdks/Forgehold-sample-sdk"
	"context"
	"github.com/speakeasy-sdks/Forgehold-sample-sdk/pkg/models/shared"
	"log"
)

func main() {
    s := forgeholdsamplesdk.New()

    ctx := context.Background()
    res, err := s.CreateUserv1(ctx, shared.UserInput{
        Country: "Benin",
        Email: "Della67@yahoo.com",
        Firstname: "Enrique",
        Lastname: "Ernser",
        Nickname: "<value>",
        Password: "TOXx1B29WwlhtAA",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.User != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ctx`                                                    | [context.Context](https://pkg.go.dev/context#Context)    | :heavy_check_mark:                                       | The context to use for the request.                      |
| `request`                                                | [shared.UserInput](../../pkg/models/shared/userinput.md) | :heavy_check_mark:                                       | The request object to use for the request.               |


### Response

**[*operations.CreateUserv1Response](../../pkg/models/operations/createuserv1response.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

## DeleteUserv1

Delete a user by ID

### Example Usage

```go
package main

import(
	forgeholdsamplesdk "github.com/speakeasy-sdks/Forgehold-sample-sdk"
	"context"
	"github.com/speakeasy-sdks/Forgehold-sample-sdk/pkg/models/operations"
	"log"
)

func main() {
    s := forgeholdsamplesdk.New()

    ctx := context.Background()
    res, err := s.DeleteUserv1(ctx, operations.DeleteUserv1Request{
        ID: "<id>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.Success != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |
| `request`                                                                            | [operations.DeleteUserv1Request](../../pkg/models/operations/deleteuserv1request.md) | :heavy_check_mark:                                                                   | The request object to use for the request.                                           |


### Response

**[*operations.DeleteUserv1Response](../../pkg/models/operations/deleteuserv1response.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

## GetHealth

Healthcheck

### Example Usage

```go
package main

import(
	forgeholdsamplesdk "github.com/speakeasy-sdks/Forgehold-sample-sdk"
	"context"
	"log"
)

func main() {
    s := forgeholdsamplesdk.New()

    ctx := context.Background()
    res, err := s.GetHealth(ctx)
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |


### Response

**[*operations.GetHealthResponse](../../pkg/models/operations/gethealthresponse.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

## GetUserv1

Get a user by ID

### Example Usage

```go
package main

import(
	forgeholdsamplesdk "github.com/speakeasy-sdks/Forgehold-sample-sdk"
	"context"
	"github.com/speakeasy-sdks/Forgehold-sample-sdk/pkg/models/operations"
	"log"
)

func main() {
    s := forgeholdsamplesdk.New()

    ctx := context.Background()
    res, err := s.GetUserv1(ctx, operations.GetUserv1Request{
        ID: "<id>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.User != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                      | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `ctx`                                                                          | [context.Context](https://pkg.go.dev/context#Context)                          | :heavy_check_mark:                                                             | The context to use for the request.                                            |
| `request`                                                                      | [operations.GetUserv1Request](../../pkg/models/operations/getuserv1request.md) | :heavy_check_mark:                                                             | The request object to use for the request.                                     |


### Response

**[*operations.GetUserv1Response](../../pkg/models/operations/getuserv1response.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

## SearchUsersv1

Search users

### Example Usage

```go
package main

import(
	forgeholdsamplesdk "github.com/speakeasy-sdks/Forgehold-sample-sdk"
	"context"
	"github.com/speakeasy-sdks/Forgehold-sample-sdk/pkg/models/shared"
	"log"
)

func main() {
    s := forgeholdsamplesdk.New()

    ctx := context.Background()
    res, err := s.SearchUsersv1(ctx, shared.Filters{
        Filters: []shared.Filter{
            shared.Filter{
                Field: "<value>",
                Matchtype: "<value>",
                Value: "<value>",
            },
        },
        Limit: 230189,
        Offset: 260836,
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.Users != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `request`                                             | [shared.Filters](../../pkg/models/shared/filters.md)  | :heavy_check_mark:                                    | The request object to use for the request.            |


### Response

**[*operations.SearchUsersv1Response](../../pkg/models/operations/searchusersv1response.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |

## UpdateUserv1

### Example Usage

```go
package main

import(
	forgeholdsamplesdk "github.com/speakeasy-sdks/Forgehold-sample-sdk"
	"context"
	"github.com/speakeasy-sdks/Forgehold-sample-sdk/pkg/models/shared"
	"github.com/speakeasy-sdks/Forgehold-sample-sdk/pkg/models/operations"
	"log"
)

func main() {
    s := forgeholdsamplesdk.New()

    ctx := context.Background()
    res, err := s.UpdateUserv1(ctx, operations.UpdateUserv1Request{
        User: shared.UserInput{
            Country: "Reunion",
            Email: "Anjali_Mann@gmail.com",
            Firstname: "Miracle",
            Lastname: "Bosco",
            Nickname: "<value>",
            Password: "_rsrQvhIQt3Jjvn",
        },
        ID: "<id>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res.User != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                            | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `ctx`                                                                                | [context.Context](https://pkg.go.dev/context#Context)                                | :heavy_check_mark:                                                                   | The context to use for the request.                                                  |
| `request`                                                                            | [operations.UpdateUserv1Request](../../pkg/models/operations/updateuserv1request.md) | :heavy_check_mark:                                                                   | The request object to use for the request.                                           |


### Response

**[*operations.UpdateUserv1Response](../../pkg/models/operations/updateuserv1response.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |
