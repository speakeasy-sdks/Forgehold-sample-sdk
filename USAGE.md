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
		Nickname:  "string",
		Password:  "TOXx1B29WwlhtAA",
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