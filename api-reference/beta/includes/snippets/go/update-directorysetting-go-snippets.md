---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/models"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewDirectorySetting()


settingValue := graphmodels.NewSettingValue()
name := "CustomBlockedWordsList"
settingValue.SetName(&name) 
value := "Contoso"
settingValue.SetValue(&value) 

values := []graphmodels.SettingValueable {
	settingValue,

}
requestBody.SetValues(values)

result, err := graphClient.Settings().BySettingId("directorySetting-id").Patch(context.Background(), requestBody, nil)


```