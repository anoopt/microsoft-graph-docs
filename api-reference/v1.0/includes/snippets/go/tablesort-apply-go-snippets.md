---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-sdk-go/Drives/Item/Items/Item/Workbook/Tables/Item/Sort/Apply"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewApplyPostRequestBody()


workbookSortField := graphmodels.NewWorkbookSortField()
key := int32(99)
workbookSortField.SetKey(&key) 
sortOn := "sortOn-value"
workbookSortField.SetSortOn(&sortOn) 
ascending := true
workbookSortField.SetAscending(&ascending) 
color := "color-value"
workbookSortField.SetColor(&color) 
dataOption := "dataOption-value"
workbookSortField.SetDataOption(&dataOption) 
icon := graphmodels.NewWorkbookIcon()
set := "set-value"
icon.SetSet(&set) 
index := int32(99)
icon.SetIndex(&index) 
workbookSortField.SetIcon(icon)

fields := []graphmodels.WorkbookSortFieldable {
	workbookSortField,

}
requestBody.SetFields(fields)
matchCase := true
requestBody.SetMatchCase(&matchCase) 
method := "method-value"
requestBody.SetMethod(&method) 

graphClient.DrivesById("drive-id").ItemsById("driveItem-id").Workbook().TablesById("workbookTable-id").Sort().Apply().Post(context.Background(), requestBody, nil)


```