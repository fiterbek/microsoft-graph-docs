---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter);

outlookTaskId := "outlookTask-id"
result, err := graphClient.Me().Outlook().TasksById(&outlookTaskId).Get(options)


```