---
title: "passwordCredential resource type"
description: "Contains a password credential associated with an application or a service principal. The **passwordCredentials** property of the servicePrincipal entity and of the application entity is a collection of **passwordCredential**."
localization_priority: Normal
doc_type: resourcePageType
ms.prod: "microsoft-identity-platform"
author: "davidmu1"
---

# passwordCredential resource type

Represents a password credential associated with an application or a service principal. The **passwordCredentials** property of the [application](application.md) <!--and [servicePrincipal](serviceprincipal.md) entitites--> entity is a collection of **passwordCredential** objects.

> [!IMPORTANT]
> Using POST or PATCH to set **passwordCredential** is not supported. Use the addPassword and removePassword methods to update the password for an application<!--or a servicePrincipal-->:
>
> - [application: addPassword](../api/application-addpassword.md)
> - [application: removePassword](../api/application-removepassword.md)
<!--
> - [servicePrincipal: addPassword](../api/serviceprincipal-addpassword.md)
> - [servicePrincipal: removePassword](../api/serviceprincipal-removepassword.md)
-->

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
| customKeyIdentifier | Binary | Do not use. |
| displayName | String | Friendly name for the password. Optional. |
| endDateTime | DateTimeOffset | The date and time at which the password expires represented using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Optional. |
| hint | String | Contains the first three characters of the password. Read-only. |
| keyId | Guid | The unique identifier for the password. |
| secretText | String | Read-only; Contains the strong passwords generated by Azure AD that are 16-64 characters in length. The generated password value is only returned during the initial POST request to [addPassword](../api/application-addpassword.md). There is no way to retrieve this password in the future. |
| startDateTime | DateTimeOffset | The date and time at which the password becomes valid. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Optional. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "passwordCredential resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.passwordCredential",
  "baseType": null
}-->

```json
{
  "customKeyIdentifier": "Binary",
  "displayName": "String",
  "endDateTime": "String (timestamp)",
  "hint": "String",
  "keyId": "Guid",
  "secretText": "String",
  "startDateTime": "String (timestamp)"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "passwordCredential resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->