---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter);

requestBody := msgraphsdk.NewUnifiedRoleAssignment()
principalId := "6b937a9d-c731-465b-a844-2d5b5368c161"
requestBody.SetPrincipalId(&principalId)
roleDefinitionId := "9b895d92-2cd3-44c7-9d02-a6ac2d5ea5c3"
requestBody.SetRoleDefinitionId(&roleDefinitionId)
directoryScopeId := "/661e1310-bd76-4795-89a7-8f3c8f855bfc"
requestBody.SetDirectoryScopeId(&directoryScopeId)
requestBody.SetAdditionalData(map[string]interface{}{
	"@odata.type": "#microsoft.graph.unifiedRoleAssignment",
}
options := &msgraphsdk.RoleAssignmentsRequestBuilderPostOptions{
	Body: requestBody,
}
result, err := graphClient.RoleManagement().Directory().RoleAssignments().Post(options)


```