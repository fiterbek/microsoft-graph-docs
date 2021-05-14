---
title: "serviceHealthIssue resource type"
description: "**TODO: Add Description**"
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: resourcePageType
---

# serviceHealthIssue resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

**TODO: Add Description**


Inherits from [serviceAnnouncementBase](../resources/serviceannouncementbase.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List serviceHealthIssues](../api/servicehealthissue-list.md)|[serviceHealthIssue](../resources/servicehealthissue.md) collection|Get a list of the [serviceHealthIssue](../resources/servicehealthissue.md) objects and their properties.|
|[Create serviceHealthIssue](../api/servicehealthissue-create.md)|[serviceHealthIssue](../resources/servicehealthissue.md)|Create a new [serviceHealthIssue](../resources/servicehealthissue.md) object.|
|[Get serviceHealthIssue](../api/servicehealthissue-get.md)|[serviceHealthIssue](../resources/servicehealthissue.md)|Read the properties and relationships of a [serviceHealthIssue](../resources/servicehealthissue.md) object.|
|[Update serviceHealthIssue](../api/servicehealthissue-update.md)|[serviceHealthIssue](../resources/servicehealthissue.md)|Update the properties of a [serviceHealthIssue](../resources/servicehealthissue.md) object.|
|[Delete serviceHealthIssue](../api/servicehealthissue-delete.md)|None|Deletes a [serviceHealthIssue](../resources/servicehealthissue.md) object.|
|[incidentReport](../api/servicehealthissue-incidentreport.md)|Stream|**TODO: Add Description**|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|classification|serviceHealthClassificationType|**TODO: Add Description**. Possible values are: `advisory`, `incident`, `unknownFutureValue`.|
|details|[keyValuePair](../resources/synchronization-keyvaluepair.md) collection|**TODO: Add Description** Inherited from [serviceAnnouncementBase](../resources/serviceannouncementbase.md).|
|endDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [serviceAnnouncementBase](../resources/serviceannouncementbase.md).|
|feature|String|**TODO: Add Description**|
|featureGroup|String|**TODO: Add Description**|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md).|
|impactDescription|String|**TODO: Add Description**|
|isResolved|Boolean|**TODO: Add Description**|
|lastModifiedDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [serviceAnnouncementBase](../resources/serviceannouncementbase.md).|
|origin|serviceHealthOrigin|**TODO: Add Description**. Possible values are: `microsoft`, `thirdParty`, `customer`, `unknownFutureValue`.|
|posts|[serviceHealthIssuePost](../resources/servicehealthissuepost.md) collection|**TODO: Add Description**|
|service|String|**TODO: Add Description**|
|startDateTime|DateTimeOffset|**TODO: Add Description** Inherited from [serviceAnnouncementBase](../resources/serviceannouncementbase.md).|
|status|serviceHealthStatus|**TODO: Add Description**. Possible values are: `serviceOperational`, `investigating`, `restoringService`, `verifyingService`, `serviceRestored`, `postIncidentReviewPublished`, `serviceDegradation`, `serviceInterruption`, `extendedRecovery`, `falsePositive`, `investigationSuspended`, `resolved`, `mitigatedExternal`, `mitigated`, `resolvedExternal`, `confirmed`, `reported`, `unknownFutureValue`.|
|title|String|**TODO: Add Description** Inherited from [serviceAnnouncementBase](../resources/serviceannouncementbase.md).|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.serviceHealthIssue",
  "baseType": "microsoft.graph.serviceAnnouncementBase",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.serviceHealthIssue",
  "id": "String (identifier)",
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "title": "String",
  "details": [
    {
      "@odata.type": "microsoft.graph.keyValuePair"
    }
  ],
  "impactDescription": "String",
  "classification": "String",
  "origin": "String",
  "posts": [
    {
      "@odata.type": "microsoft.graph.serviceHealthIssuePost"
    }
  ],
  "status": "String",
  "service": "String",
  "feature": "String",
  "featureGroup": "String",
  "isResolved": "Boolean"
}
```
