---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/Drives/Item/Items/Item/Workbook/CreateSession"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewCreateSessionPostRequestBody()
persistChanges := true
requestBody.SetPersistChanges(&persistChanges) 

result, err := graphClient.DrivesById("drive-id").ItemsById("driveItem-id").Workbook().CreateSession().Post(context.Background(), requestBody, nil)


```