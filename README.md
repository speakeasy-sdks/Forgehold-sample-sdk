# github.com/speakeasy-sdks/Forgehold-sample-sdk

<div align="left">
    <a href="https://speakeasyapi.dev/"><img src="https://custom-icon-badges.demolab.com/badge/-Built%20By%20Speakeasy-212015?style=for-the-badge&logoColor=FBE331&logo=speakeasy&labelColor=545454" /></a>
    <a href="https://github.com/speakeasy-sdks/Forgehold-sample-sdk.git/actions"><img src="https://img.shields.io/github/actions/workflow/status/speakeasy-sdks/Forgehold-sample-sdk/speakeasy_sdk_generation.yml?style=for-the-badge" /></a>
    
</div>

<!-- Start SDK Installation -->
# SDK Installation

```bash
go get github.com/speakeasy-sdks/Forgehold-sample-sdk
```
<!-- End SDK Installation -->

## SDK Example Usage
<!-- Start SDK Example Usage -->


```go
package main

import (
	"context"
	forgeholdsamplesdk "github.com/speakeasy-sdks/Forgehold-sample-sdk"
	"github.com/speakeasy-sdks/Forgehold-sample-sdk/pkg/models/shared"
	"log"
)

func main() {
	s := forgeholdsamplesdk.New()

	ctx := context.Background()
	res, err := s.UserAPIForSpeakeasyTemplateService.CreateUserv1(ctx, shared.UserInput{
		Country:   "Benin",
		Email:     "Della67@yahoo.com",
		Firstname: "Enrique",
		Lastname:  "Ernser",
		Nickname:  "panel",
		Password:  "OXx1B29WwlhtAAe",
	})
	if err != nil {
		log.Fatal(err)
	}

	if res.User != nil {
		// handle response
	}
}

```
<!-- End SDK Example Usage -->

<!-- Start SDK Available Operations -->
# Available Resources and Operations

## [UserAPIForSpeakeasyTemplateService SDK](docs/sdks/userapiforspeakeasytemplateservice/README.md)

* [CreateUserv1](docs/sdks/userapiforspeakeasytemplateservice/README.md#createuserv1) - Create user
* [DeleteUserv1](docs/sdks/userapiforspeakeasytemplateservice/README.md#deleteuserv1) - Delete a user by ID
* [GetHealth](docs/sdks/userapiforspeakeasytemplateservice/README.md#gethealth) - Healthcheck
* [GetUserv1](docs/sdks/userapiforspeakeasytemplateservice/README.md#getuserv1) - Get a user by ID
* [SearchUsersv1](docs/sdks/userapiforspeakeasytemplateservice/README.md#searchusersv1) - Search users
* [UpdateUserv1](docs/sdks/userapiforspeakeasytemplateservice/README.md#updateuserv1)
<!-- End SDK Available Operations -->

<!-- Start Dev Containers -->



<!-- End Dev Containers -->

<!-- Start Go Types -->

<!-- End Go Types -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically.
Feel free to open a PR or a Github issue as a proof of concept and we'll do our best to include it in a future release!

### SDK Created by [Speakeasy](https://docs.speakeasyapi.dev/docs/using-speakeasy/client-sdks)
