---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/Drives/Item/Items/Item/Workbook/Worksheets/Item/Charts/Item"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewChart()
additionalData := map[string]interface{}{
	"index" : int32(8) , 
}
requestBody.SetAdditionalData(additionalData)

graphClient.DrivesById("drive-id").ItemsById("driveItem-id").Workbook().WorksheetsById("workbookWorksheet-id").ChartsById("workbookChart-id").Post(context.Background(), requestBody, nil)


```