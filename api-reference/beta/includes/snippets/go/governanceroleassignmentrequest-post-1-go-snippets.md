---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter);

requestBody := msgraphsdk.NewGovernanceRoleAssignmentRequest()
roleDefinitionId := "ea48ad5e-e3b0-4d10-af54-39a45bbfe68d"
requestBody.SetRoleDefinitionId(&roleDefinitionId)
resourceId := "e5e7d29d-5465-45ac-885f-4716a5ee74b5"
requestBody.SetResourceId(&resourceId)
subjectId := "918e54be-12c4-4f4c-a6d3-2ee0e3661c51"
requestBody.SetSubjectId(&subjectId)
assignmentState := "Eligible"
requestBody.SetAssignmentState(&assignmentState)
type := "AdminAdd"
requestBody.SetType(&type)
reason := "Assign an eligible role"
requestBody.SetReason(&reason)
schedule := msgraphsdk.NewGovernanceSchedule()
requestBody.SetSchedule(schedule)
startDateTime, err := time.Parse(time.RFC3339, "2018-05-12T23:37:43.356Z")
schedule.SetStartDateTime(&startDateTime)
endDateTime, err := time.Parse(time.RFC3339, "2018-11-08T23:37:43.356Z")
schedule.SetEndDateTime(&endDateTime)
type := "Once"
schedule.SetType(&type)
options := &msgraphsdk.RoleAssignmentRequestsRequestBuilderPostOptions{
	Body: requestBody,
}
privilegedAccessId := "privilegedAccess-id"
result, err := graphClient.PrivilegedAccessById(&privilegedAccessId).RoleAssignmentRequests().Post(options)


```