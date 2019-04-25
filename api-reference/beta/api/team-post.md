---
title: チームの作成
description: 新しいチームを作成します。
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
ms.openlocfilehash: 394fa92f6ef97d6bc7a8dff0d4ddfe10c677bf99
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32536841"
---
# <a name="create-team"></a><span data-ttu-id="4320e-103">チームを作成する</span><span class="sxs-lookup"><span data-stu-id="4320e-103">Create team</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="4320e-104">新しい[チーム](../resources/team.md)を作成します。</span><span class="sxs-lookup"><span data-stu-id="4320e-104">Create a new [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="4320e-105">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="4320e-105">Permissions</span></span>

<span data-ttu-id="4320e-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4320e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="4320e-108">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="4320e-108">Permission type</span></span>                        | <span data-ttu-id="4320e-109">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="4320e-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="4320e-110">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="4320e-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="4320e-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4320e-111">Group.ReadWrite.All</span></span>                         |
| <span data-ttu-id="4320e-112">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="4320e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4320e-113">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4320e-113">Not supported.</span></span>                              |
| <span data-ttu-id="4320e-114">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4320e-114">Application</span></span>                            | <span data-ttu-id="4320e-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4320e-115">Group.ReadWrite.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="4320e-116">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="4320e-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /teams
```

## <a name="request-headers"></a><span data-ttu-id="4320e-117">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="4320e-117">Request headers</span></span>

| <span data-ttu-id="4320e-118">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="4320e-118">Header</span></span>        | <span data-ttu-id="4320e-119">値</span><span class="sxs-lookup"><span data-stu-id="4320e-119">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="4320e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="4320e-120">Authorization</span></span> | <span data-ttu-id="4320e-p102">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="4320e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4320e-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4320e-123">Content-Type</span></span>  | <span data-ttu-id="4320e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4320e-124">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="4320e-125">要求本文</span><span class="sxs-lookup"><span data-stu-id="4320e-125">Request body</span></span>

<span data-ttu-id="4320e-126">要求本文で、[team](../resources/team.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="4320e-126">In the request body, supply a JSON representation of a [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="4320e-127">応答</span><span class="sxs-lookup"><span data-stu-id="4320e-127">Response</span></span>

<span data-ttu-id="4320e-128">成功すると、この API は [teamsAsyncOperation](../resources/teamsasyncoperation.md) へのリンクを含む `202 Accepted` 応答を返します。</span><span class="sxs-lookup"><span data-stu-id="4320e-128">If successful, this API returns a `202 Accepted` response containing a link to the [teamsAsyncOperation](../resources/teamsasyncoperation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4320e-129">例</span><span class="sxs-lookup"><span data-stu-id="4320e-129">Examples</span></span>

### <a name="example-1-delegated-permissions"></a><span data-ttu-id="4320e-130">例 1: 委任されたアクセス許可</span><span class="sxs-lookup"><span data-stu-id="4320e-130">Example 1: Delegated permissions</span></span>

<span data-ttu-id="4320e-131">最低限の要求の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4320e-131">The following is an example of a minimal request.</span></span> <span data-ttu-id="4320e-132">他のプロパティを省略することにより、クライアントは `template` で表される事前に定義されたテンプレートから暗黙的に既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4320e-132">By omitting other properties, the client is implicitly taking defaults from the pre-defined template represented by `template`.</span></span>

#### <a name="request"></a><span data-ttu-id="4320e-133">要求</span><span class="sxs-lookup"><span data-stu-id="4320e-133">Request</span></span>

```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json
{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('standard')",
  "displayName": "My Sample Team",
  "description": "My Sample Team’s Description"
}
```

##### <a name="response"></a><span data-ttu-id="4320e-134">応答</span><span class="sxs-lookup"><span data-stu-id="4320e-134">Response</span></span>

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

### <a name="example-2-application-permissions"></a><span data-ttu-id="4320e-135">例 2:アプリケーションのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="4320e-135">Example 2: Application permissions</span></span>

<span data-ttu-id="4320e-136">アプリケーションのアクセス許可を使用した最小限の要求の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4320e-136">The following is an example of a minimal request using application permissions.</span></span> <span data-ttu-id="4320e-137">他のプロパティを省略することにより、クライアントは `template` で表される事前に定義されたテンプレートから暗黙的に既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4320e-137">By omitting other properties, the client is implicitly taking defaults from the predefined template represented by `template`.</span></span> <span data-ttu-id="4320e-138">アプリケーションのアクセス許可で要求を発行する際には、[ユーザー](../resources/user.md)が `owners` コレクションで指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4320e-138">When issuing a request with application permissions, a [user](../resources/user.md) must be specified in the `owners` collection.</span></span>

#### <a name="request"></a><span data-ttu-id="4320e-139">要求</span><span class="sxs-lookup"><span data-stu-id="4320e-139">Request</span></span>

```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json
{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('standard')",
  "displayName": "My Sample Team",
  "description": "My Sample Team’s Description",
  "owners@odata.bind": [
    "https://graph.microsoft.com/beta/users('abc123')"
  ]
}
```

#### <a name="response"></a><span data-ttu-id="4320e-140">応答</span><span class="sxs-lookup"><span data-stu-id="4320e-140">Response</span></span>

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

### <a name="example-3-create-a-team-with-an-app-installed-multiple-channels-with-pinned-tabs-using-delegated-permissions"></a><span data-ttu-id="4320e-141">例 3: 委任されたアクセス許可を使用して、インストールされたアプリと固定されたタブによる複数のチャネルを持つチームを作成する</span><span class="sxs-lookup"><span data-stu-id="4320e-141">Example 3: Create a team with an app installed, multiple channels with pinned tabs using delegated permissions</span></span>

<span data-ttu-id="4320e-142">完全なペイロードの要求を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4320e-142">The following is a request with a full payload.</span></span> <span data-ttu-id="4320e-143">クライアントは基本テンプレートの値を上書きして、`specialization` の検証規則で許容される範囲に配列値のアイテムを追加できます。</span><span class="sxs-lookup"><span data-stu-id="4320e-143">The client can override values in the base template and add to array-valued items to the extent allowed by validation rules for the `specialization`.</span></span> 

#### <a name="request"></a><span data-ttu-id="4320e-144">要求</span><span class="sxs-lookup"><span data-stu-id="4320e-144">Request</span></span>

```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json
{
    "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('standard')",
    "visibility": "Private",
    "displayName": "Sample Engineering Team",
    "description": "This is a sample engineering team, used to showcase the range of properties supported by this API",
    "channels": [
        {
            "displayName": "Announcements 📢",
            "isFavoriteByDefault": true,
            "description": "This is a sample announcements channel that is favorited by default. Use this channel to make important team, product, and service announcements."
        },
        {
            "displayName": "Training 🏋️",
            "isFavoriteByDefault": true,
            "description": "This is a sample training channel, that is favorited by default, and contains an example of pinned website and YouTube tabs.",
            "tabs": [
                {
                    "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.web')",
                    "name": "A Pinned Website",
                    "configuration": {
                        "contentUrl": "https://docs.microsoft.com/en-us/microsoftteams/microsoft-teams"
                    }
                },
                {
                    "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.youtube')",
                    "name": "A Pinned YouTube Video",
                    "configuration": {
                        "contentUrl": "https://tabs.teams.microsoft.com/Youtube/Home/YoutubeTab?videoId=X8krAMdGvCQ",
                        "websiteUrl": "https://www.youtube.com/watch?v=X8krAMdGvCQ"
                    }
                }
            ]
        },
        {
            "displayName": "Planning 📅 ",
            "description": "This is a sample of a channel that is not favorited by default, these channels will appear in the more channels overflow menu.",
            "isFavoriteByDefault": false
        },
        {
            "displayName": "Issues and Feedback 🐞",
            "description": "This is a sample of a channel that is not favorited by default, these channels will appear in the more channels overflow menu."
        }
    ],
    "memberSettings": {
        "allowCreateUpdateChannels": true,
        "allowDeleteChannels": true,
        "allowAddRemoveApps": true,
        "allowCreateUpdateRemoveTabs": true,
        "allowCreateUpdateRemoveConnectors": true
    },
    "guestSettings": {
        "allowCreateUpdateChannels": false,
        "allowDeleteChannels": false
    },
    "funSettings": {
        "allowGiphy": true,
        "giphyContentRating": "Moderate",
        "allowStickersAndMemes": true,
        "allowCustomMemes": true
    },
    "messagingSettings": {
        "allowUserEditMessages": true,
        "allowUserDeleteMessages": true,
        "allowOwnerDeleteMessages": true,
        "allowTeamMentions": true,
        "allowChannelMentions": true
    },
    "installedApps": [
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.vsts')"
        },
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('1542629c-01b3-4a6d-8f76-1938b779e48d')"
        }
    ]
}
```

#### <a name="response"></a><span data-ttu-id="4320e-145">応答</span><span class="sxs-lookup"><span data-stu-id="4320e-145">Response</span></span>

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

### <a name="example-4-create-a-team-with-a-non-standard-base-template-type"></a><span data-ttu-id="4320e-146">例 4: 非標準のベース テンプレート タイプを使用してチームを作成する</span><span class="sxs-lookup"><span data-stu-id="4320e-146">Example 4: Create a team with a non-standard base template type</span></span>

<span data-ttu-id="4320e-147">ベース テンプレート タイプとは、Microsoft が特定の業界向けに作成した特別なテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="4320e-147">Base template types are special templates that Microsoft created for specific industries.</span></span> <span data-ttu-id="4320e-148">多くの場合、これらのベース テンプレートにはストアでは入手できない独自のアプリおよび Microsoft Teams のテンプレートでまだ個別にサポートされていないチームのプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4320e-148">These base templates often contain proprietary apps that aren't available in the store and team properties that are not yet supported individually in Microsoft Teams templates.</span></span>

<span data-ttu-id="4320e-149">非標準のベース テンプレートからチームを作成するには、要求本文で `template@odata.bind` プロパティを `standard` から使用する特定のベース テンプレートへのポイントに変更します。</span><span class="sxs-lookup"><span data-stu-id="4320e-149">To create a team from a non-standard base template, you’ll want to change the `template@odata.bind` property in the request body from `standard` to point to the specific base template you’d like to create.</span></span>

<span data-ttu-id="4320e-150">サポートされているベース テンプレートの詳細については、「[Teams テンプレートの使用を開始する](https://docs.microsoft.com/ja-JP/MicrosoftTeams/get-started-with-teams-templates)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4320e-150">To learn more about supported base template types, see [Get started with Teams templates](https://docs.microsoft.com/ja-JP/MicrosoftTeams/get-started-with-teams-templates).</span></span>

#### <a name="request"></a><span data-ttu-id="4320e-151">要求</span><span class="sxs-lookup"><span data-stu-id="4320e-151">Request</span></span>

```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json
{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('educationClass')",
  "displayName": "My Class Team",
  "description": "My Class Team’s Description"
}
```

#### <a name="response"></a><span data-ttu-id="4320e-152">応答</span><span class="sxs-lookup"><span data-stu-id="4320e-152">Response</span></span>

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

### <a name="example-5-create-a-team-with-a-non-standard-base-template-type-with-extended-properties"></a><span data-ttu-id="4320e-153">例 5: 拡張プロパティを含んだ非標準のベース テンプレート タイプを使用してチームを作成する</span><span class="sxs-lookup"><span data-stu-id="4320e-153">Example 5: Create a team with a non-standard base template type with extended properties</span></span>

<span data-ttu-id="4320e-154">ベース テンプレート タイプは追加のプロパティを使用して拡張することができ、既存のベース テンプレートを元にチームの追加の設定、チャンネル、アプリ、またはタブを設定してベース テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="4320e-154">Base template types can be extended with additional properties, enabling you to build on an existing base template with additional team settings, channels, apps, or tabs.</span></span>

<span data-ttu-id="4320e-155">サポートされているベース テンプレートとサポートされているプロパティの詳細については、「[Teams テンプレートの使用を開始する](https://docs.microsoft.com/ja-JP/MicrosoftTeams/get-started-with-teams-templates)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4320e-155">To learn more about supported base template types and supported properties, see [Get started with Teams templates](https://docs.microsoft.com/ja-JP/MicrosoftTeams/get-started-with-teams-templates).</span></span>

#### <a name="request"></a><span data-ttu-id="4320e-156">要求</span><span class="sxs-lookup"><span data-stu-id="4320e-156">Request</span></span>

```http
POST https://graph.microsoft.com/beta/teams
Content-Type: application/json
{
  "template@odata.bind": "https://graph.microsoft.com/beta/teamsTemplates('educationClass')",
  "displayName": "My Class Team",
  "description": "My Class Team’s Description",
  "channels": [
        {
            "displayName": "Class Announcements 📢",
            "isFavoriteByDefault": true
        },
        {
            "displayName": "Homework 🏋️",
            "isFavoriteByDefault": true,
        }
    ],
    "memberSettings": {
        "allowCreateUpdateChannels": false,
        "allowDeleteChannels": false,
        "allowAddRemoveApps": false,
        "allowCreateUpdateRemoveTabs": false,
        "allowCreateUpdateRemoveConnectors": false
    },
    "installedApps": [
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('com.microsoft.teamspace.tab.vsts')"
        },
        {
            "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps('1542629c-01b3-4a6d-8f76-1938b779e48d')"
        }
    ]
}
```

#### <a name="response"></a><span data-ttu-id="4320e-157">応答</span><span class="sxs-lookup"><span data-stu-id="4320e-157">Response</span></span>

```http
HTTP/1.1 202 Accepted
Content-Type: application/json
Location: /teams/{teamId}/operations/{operationId}
Content-Location: /teams/{teamId}
{
}
```

## <a name="see-also"></a><span data-ttu-id="4320e-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="4320e-158">See also</span></span>

- [<span data-ttu-id="4320e-159">使用可能なテンプレート</span><span class="sxs-lookup"><span data-stu-id="4320e-159">Available templates</span></span>](https://docs.microsoft.com/ja-JP/MicrosoftTeams/get-started-with-teams-templates)
- [<span data-ttu-id="4320e-160">Retail Teams テンプレートの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="4320e-160">Getting started with Retail Teams templates</span></span>](https://docs.microsoft.com/MicrosoftTeams/get-started-with-retail-teams-templates)
- [<span data-ttu-id="4320e-161">Healthcare Teams テンプレートの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="4320e-161">Getting started with Healthcare Teams templates</span></span>](https://docs.microsoft.com/MicrosoftTeams/healthcare/healthcare-templates)
- [<span data-ttu-id="4320e-162">チームを使用してグループを作成する</span><span class="sxs-lookup"><span data-stu-id="4320e-162">Creating a group with a team</span></span>](/graph/teams-create-group-and-team)

<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Error:{/api-reference/beta/api/team-post.md}:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
}-->
