---
title: "group: checkMemberGroups"
description: "Check for membership in the specified list of groups."
author: "Jordanndahl"
ms.localizationpriority: high
ms.prod: "groups"
doc_type: apiPageType
---

# group: checkMemberGroups

Namespace: microsoft.graph

Check for membership in the specified list of groups. Returns from the list those groups of which
the specified group has a direct or transitive membership.

You can check up to a maximum of 20 groups per request. This function supports Microsoft 365 and other
types of groups provisioned in Azure AD. Note that Microsoft 365 groups cannot contain groups. So membership
in a Microsoft 365 group is always direct.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged)                                                 |
| :------------------------------------- | :------------------------------------------------------------------------------------------ |
| Delegated (work or school account)     | GroupMember.Read.All, Group.Read.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All |
| Delegated (personal Microsoft account) | Not supported.                                                                              |
| Application                            | GroupMember.Read.All, Group.Read.All, Directory.Read.All, Directory.ReadWrite.All                               |



## HTTP request

<!-- { "blockType": "ignored" } -->

```http
POST /groups/{id}/checkMemberGroups
```

## Request headers

| Name          | Type   | Description               |
| :------------ | :----- | :------------------------ |
| Authorization | string | Bearer {token}. Required. |

## Request body

In the request body, provide a JSON object with the following parameters.

| Parameter | Type              | Description           |
| :-------- | :---------------- | :-------------------- |
| groupIds  | String collection | An array of group ids |

## Response

If successful, this method returns `200 OK` response code and String collection object in the response body.

## Example

Here is an example of how to call this API.

##### Request

Here is an example of the request.


# [HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "group_checkmembergroups"
}-->

```http
POST https://graph.microsoft.com/v1.0/groups/{id}/checkMemberGroups
Content-type: application/json

{
  "groupIds": [
    "groupIds-value"
  ]
}
```
# [C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/group-checkmembergroups-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/group-checkmembergroups-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/group-checkmembergroups-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/group-checkmembergroups-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# [Go](#tab/go)
[!INCLUDE [sample-code](../includes/snippets/go/group-checkmembergroups-go-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### Response

Here is an example of the response. Note: The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "group: checkMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->

