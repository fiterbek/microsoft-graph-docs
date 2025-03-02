---
title: "broadcastMeetingSettings resource type"
description: "Settings related to a Teams live event"
author: "mkhribech"
ms.localizationpriority: medium
ms.prod: "cloud-communications"
doc_type: resourcePageType
---

# broadcastMeetingSettings resource type

Namespace: microsoft.graph

Settings related to a [Microsoft Teams live event](/microsoftteams/teams-live-events/what-are-teams-live-events).

## Properties

| Property                   | Type                                                         | Description                                                                                 |
|----------------------------|--------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| allowedAudience            | [broadcastMeetingAudience](#broadcastmeetingaudience-values) | Defines who can join the Teams live event. Possible values are listed in the following table.     |
| isRecordingEnabled         | Boolean                                                      | Indicates whether recording is enabled for this Teams live event. Default value is `false`.       |
| isAttendeeReportEnabled    | Boolean                                                      | Indicates whether attendee report is enabled for this Teams live event. Default value is `false`. |
| isQuestionAndAnswerEnabled | Boolean                                                      | Indicates whether Q&A is enabled for this Teams live event. Default value is `false`.             |
| isVideoOnDemandEnabled     | Boolean                                                      | Indicates whether video on demand is enabled for this Teams live event. Default value is `false`. |

### broadcastMeetingAudience values

| Value              | Description                                                       |
| ------------------ | ----------------------------------------------------------------- |
| everyone           | This Teams live event will be open to anyone. This is the default value. |
| organization       | Everyone in your org can join this Teams live event.                     |
| roleIsAttendee     | Only the specified people can join this Teams live event.                |
| unknownFutureValue | Evolvable enumeration sentinel value. Do not use.  |

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [],
  "@odata.type": "microsoft.graph.broadcastMeetingSettings"
}-->
```json
{
  "allowedAudience": "everyone | organization | roleIsAttendee | unknownFutureValue",
  "isRecordingEnabled": "Boolean",
  "isAttendeeReportEnabled": "Boolean",
  "isQuestionAndAnswerEnabled": "Boolean",
  "isVideoOnDemandEnabled": "Boolean"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "broadcastSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
