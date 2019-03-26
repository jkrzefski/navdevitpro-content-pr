---
title: Update customerPaymentsJournals | Microsoft Docs
description: Updates a customer payments journal in Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen

ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2019
ms.author: solsen
---

# Update customerPaymentsJournals
Update the properties of a customer payments journal object for [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)].

## HTTP request

```
PATCH /businesscentral/companies({id})/customerPaymentsJournals({id})
```

## Request headers

|Header|Value|
|------|-----|
|Authorization |Bearer {token}. Required.|
|Content-Type  |application/json|
|If-Match      |Required. When this request header is included and the eTag provided does not match the current tag on the **customerPaymentsJournals**, the **customerPaymentsJournals** will not be updated. |

## Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

## Response
If successful, this method returns a ```200 OK``` response code and an updated **customerPaymentsJournals** object in the response body.

## Example

**Request**

Here is an example of the request.

```json
PATCH https://api.businesscentral.dynamics.com/v1.0/api/v1.0/companies({id})/customerPaymentsJournals({id})
Content-type: application/json

{
  "code": "EXPENSE",
  "displayName": "Expense Batch"
}
```

**Response**

Here is an example of the response. 

> [!NOTE]  
>   The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "id-value",
  "code": "EXPENSE",
  "displayName": "Expense Batch",
  "lastModifiedDateTime": "2017-05-17T11:30:01.313Z"
}
```

## See also
[Microsoft Graph Reference](../api/dynamics_graph_reference.md)  



[Error Codes](../dynamics_error_codes.md)  
[Customer Payments Journal](../resources/dynamics_customerpaymentsjournal.md)  
[Get Customer Payment Journal](dynamics_customerpaymentsjournal_get.md)  
[Post Customer Payments Journal](dynamics_create_customerpaymentsjournal.md)  
[Delete Customer Payments Journal](dynamics_customerpaymentsjournal_delete.md)  