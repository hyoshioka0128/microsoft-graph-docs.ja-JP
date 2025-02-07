---
title: managementAgentType 列挙型
description: 管理エージェントの種類。
author: rolyon
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: e3b9fd469a787e0afdacb26dc5a07ee114d72bbe
ms.sourcegitcommit: 0a62bc5849f27a55d83efce9b3eb01b9711bbe1d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/14/2019
ms.locfileid: "34986124"
---
# <a name="managementagenttype-enum-type"></a>managementAgentType 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

管理エージェントの種類。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|eas|1-d|デバイスは、Exchange server によって管理されています。|
|mdm.exe|pbm-2|デバイスは Intune MDM によって管理されます。|
|easMdm|1/3|デバイスは、Exchange server と Intune MDM の両方によって管理されます。|
|Intアンの場合|2/4|Intune クライアント管理。|
|Easintアンの場合|5|デバイスは EAS で、Intune クライアントはデュアル管理されています。|
|configurationManagerClient|8 |デバイスは構成マネージャーによって管理されています。|
|configurationManagerClientMdm|10 |デバイスは、構成マネージャーおよび MDM によって管理されます。|
|configurationManagerClientMdmEas|#|デバイスは、構成マネージャー、MDM、Eas によって管理されます。|
|不明|16|管理エージェントの種類が不明です。|
|jamf|32|デバイス属性は、Jamf から取得されます。|
|googleCloudDevicePolicyController|64|デバイスは Google の CloudDPC によって管理されています。|
|microsoft365ManagedMdm|258|このデバイスは、Microsoft 365 によって Intune によって管理されます。|





