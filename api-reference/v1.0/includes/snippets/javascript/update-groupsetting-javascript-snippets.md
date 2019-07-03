---
description: 自動的に生成されたファイル。 変更しない
ms.openlocfilehash: 3be4fd2cdfa23818879cf1597f9bbe1ca7f81279
ms.sourcegitcommit: 3f6a4eebe4b73ba848edbff74d51a2d5c81b7318
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2019
ms.locfileid: "35471684"
---
```javascript

const options = {
    authProvider,
};

const client = Client.init(options);

const groupSetting = {
  displayName: "displayName-value",
  templateId: "templateId-value",
  values: [
    {
      name: "CustomBlockedWordsList",
      value: ""
    },
    {
      name: "EnableMSStandardBlockedWords",
      value: "False"
    },
    {
      name: "ClassificationDescriptions",
      value: ""
    },
    {
      name: "DefaultClassification",
      value: ""
    },
    {
      name: "PrefixSuffixNamingRequirement",
      value: ""
    },
    {
      name: "AllowGuestsToBeGroupOwner",
      value: "False"
    },
    {
      name: "AllowGuestsToAccessGroups",
      value: "True"
    },
    {
      name: "GuestUsageGuidelinesUrl",
      value: ""
    },
    {
      name: "GroupCreationAllowedGroupId",
      value: "62e90394-69f5-4237-9190-012177145e10"
    },
    {
      name: "AllowToAddGuests",
      value: "True"
    },
    {
      name: "UsageGuidelinesUrl",
      value: ""
    },
    {
      name: "ClassificationList",
      value: ""
    },
    {
      name: "EnableGroupCreation",
      value: "True"
    }
  ]
};

let res = await client.api('/groupSettings/{id}')
    .update({groupSetting : groupSetting});

```