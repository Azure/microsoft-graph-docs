---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphapplications "github.com/microsoftgraph/msgraph-beta-sdk-go/applications"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphapplications.NewAcquireAccessTokenPostRequestBody()


synchronizationSecretKeyStringValuePair := graphmodels.NewSynchronizationSecretKeyStringValuePair()

credentials := []graphapplications.SynchronizationSecretKeyStringValuePairable {
	synchronizationSecretKeyStringValuePair,

}
requestBody.SetCredentials(credentials)

graphClient.Applications().ByApplicationId("application-id").Synchronization().AcquireAccessToken().Post(context.Background(), requestBody, nil)


```