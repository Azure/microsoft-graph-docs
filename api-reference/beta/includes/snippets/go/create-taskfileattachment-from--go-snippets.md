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


requestBody := graphmodels.NewAttachmentBase()
name := "smile"
requestBody.SetName(&name) 
contentType := "image/gif"
requestBody.SetContentType(&contentType) 
additionalData := map[string]interface{}{
	"contentBytes" : "a0b1c76de9f7=", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Me().Todo().Lists().ByListId("todoTaskList-id").Tasks().ByTaskId("todoTask-id").Attachments().Post(context.Background(), requestBody, nil)


```