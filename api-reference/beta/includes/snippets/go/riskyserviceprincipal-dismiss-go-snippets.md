---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphidentityprotection "github.com/microsoftgraph/msgraph-beta-sdk-go/identityprotection"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphidentityprotection.NewDismissPostRequestBody()
servicePrincipalIds := []string {
	"9089a539-a539-9089-39a5-899039a58990",

}
requestBody.SetServicePrincipalIds(servicePrincipalIds)

graphClient.IdentityProtection().RiskyServicePrincipals().Dismiss().Post(context.Background(), requestBody, nil)


```