---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/Drives/Item/Items/Item/Workbook/Tables/Add"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewAddPostRequestBody()
address := "Sheet1!A1:D5"
requestBody.SetAddress(&address) 
hasHeaders := true
requestBody.SetHasHeaders(&hasHeaders) 

result, err := graphClient.DrivesById("drive-id").ItemsById("driveItem-id").Workbook().Tables().Add().Post(context.Background(), requestBody, nil)


```