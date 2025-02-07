---
title: Office 365 アカウントを Azure AD と関連付けてアプリを作成および管理する
description: 'Microsoft Azure Active Directory (Azure AD) を使用してアプリケーションを認証するには、Azure AD にアプリケーションを登録する必要があります。ここに Office 365 のユーザー アカウントとアプリケーション情報が保存されています。Azure ポータルから Azure AD を管理するには、Microsoft Azure サブスクリプションが必要です。Microsoft Azure のポータルを使用して、ユーザー、ロール、アプリを管理できます。 '
localization_priority: Normal
ms.openlocfilehash: af77e9bbe87ba3a7c92c91967c8df87a16224d99
ms.sourcegitcommit: 94aaf594c881c02f353c6a417460cdf783a0bfe0
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2019
ms.locfileid: "33951212"
---
# <a name="associate-your-office-365-account-with-azure-ad-to-create-and-manage-apps"></a>Office 365 アカウントを Azure AD と関連付けてアプリを作成および管理する

Microsoft Azure Active Directory (Azure AD) を使用してアプリケーションを認証するには、Azure AD にアプリケーションを登録する必要があります。ここに Office 365 のユーザー アカウントとアプリケーション情報が保存されています。Azure ポータルから Azure AD を管理するには、Microsoft Azure サブスクリプションが必要です。Microsoft Azure のポータルを使用して、ユーザー、ロール、アプリを管理できます。

この記事では、Office 365 アカウントを Azure AD と関連付けてアプリを作成および管理する方法を説明します。

 >**注:** この記事では、アプリの認証プロバイダーとして Azure AD を使用します。Azure AD v2.0 エンドポイントを使用する場合、この手順を実行する必要はありません。詳細については、「[Microsoft Graph を使ったアプリ認証](/graph/auth)」をご覧ください。

## <a name="prerequisites"></a>前提条件

**ビジネス向けの Office 365 アカウント**

既存のビジネス向けの Office 365 アカウントがない場合は、次の操作を実行できます。

- 上記のいずれかの[ビジネス向けの Office 365 プラン](https://products.office.com/en-us/business/compare-office-365-for-business-plans)にサインアップする、または
- [Join the Office 365 Developer Program and get a free 1 year subscription to Office 365](https://aka.ms/devprogramsignup).

**Microsoft Azure サブスクリプション**

- 既存の Microsoft Azure サブスクリプションをお持ちの場合は、ビジネス向けの Office 365 サブスクリプションとそのサブスクリプションを関連付けることができます。

- それ以外の場合は、アプリを登録および管理するために、新しい Azure サブスクリプションを作成して、Office 365 アカウントに関連付ける必要があります。


<!---<a name="bk_AssociateExistingAzureSubscription"> </a>-->

## <a name="to-associate-an-existing-azure-subscription-with-your-office-365-account"></a>既存の Azure サブスクリプションと Office 365 アカウントを関連付けるには


1. 既存の Azure 資格情報 (例: user@live.com などの Microsoft ID) を使用して、[Microsoft Azure のポータル](https://portal.azure.com)にログオンします。

2. **[Active Directory]** ノードを選択し、**[ディレクトリ]** タブを選択し、画面下の **[新規]** を選択します。

4. **[新規]** メニュー上で、**[Active Directory]**  >  **[ディレクトリ]**  >  **[カスタム作成]** を選びます。

5. **[ディレクトリの追加]** の **[ディレクトリ]** ドロップダウン ボックスで、**[既存のディレクトリの使用]** を選びます。**[サインアウトする準備ができました]** のチェックボックスをオンにして、右下隅にあるチェック マークを選びます。

    これで、Azure のポータルに戻ります。

3. Office 365 のアカウント情報を使ってログインします。

    ディレクトリを Azure で使用するかどうかを指定するよう、ダイアログが表示されます。

    >**重要:** Office 365 アカウントと Azure AD を関連付けるには、グローバル管理者特権を持つ Office 365 ビジネス アカウントが必要です。


4. **[続行]**、**[今すぐサインアウトする]** の順に選択します。

5. ブラウザーを閉じて、もう一度[ポータル](https://manage.windowsazure.com)を開きます。それ以外の場合は、アクセス拒否エラーを受け取ります。


6. 既存の Azure 資格情報 (例: user@live.com などの Microsoft ID) を使用して、もう一度ログオンします。**[Active Directory]** ノードに移動すると、**[ディレクトリ]** の一覧にお客様の Office 365 アカウントが表示されます。


<!--<a name="bk_AssociateNewAzureSubscription"> </a>-->

## <a name="to-create-a-new-azure-subscription-and-associate-it-with-your-office-365-account"></a>新しい Azure サブスクリプションを作成して Office 365 アカウントを関連付けるには


1. Office 365 にログオンします。[**ホーム**] ページから [**管理**] アイコンを選択して、Office 365 管理センターを開きます。
2. ページの左側にあるメニュー ページで **[管理]** までスクロール ダウンして、**[Azure AD]** を選びます。

    >**重要:** Office 365 管理センターを開いて Azure AD にアクセスするには、グローバル管理者特権を持つ Office 365 ビジネス アカウントが必要です。

3. 新しいサブスクリプションを作成します。

    If you're using a trial version of Office 365, you'll see a message telling you that Azure AD is limited to customers with paid services. You can still create a trial 30-day Azure subscription at no charge, but you'll need to perform a few extra steps:

    1. 国または地域を選択して、**[Azure サブスクリプション]** を選択します。
    2. 個人情報を入力します。確認のために連絡可能な電話番号を入力して、テキスト メッセージの送信または通話のいずれかを指定します。
    3. 認証コードを受信したら、そのコードを入力して **[コードの確認]** を選びます。
    4. 支払い情報を入力して、承諾のチェック ボックスをオンにし、**[サインアップ]** を選びます。

        Your credit card will not be charged.

        Azure サブスクリプションの作成中は、ブラウザーを閉じたり更新したりしないでください。

4. Azure サブスクリプションが作成されたら、**[ポータル]** を選びます。

5. Azure Tour が表示されます。表示するか、**[X]** をクリックしてツアーを閉じます。

    You should now see all items in your Azure subscription. It lists a directory with the name of your Office 365 tenant.

## <a name="see-also"></a>関連項目
- [Azure AD でのアプリケーションの登録の基本](https://azure.microsoft.com/en-us/documentation/articles/active-directory-authentication-scenarios/#basics-of-registering-an-application-in-azure-ad)
- [Azure AD でアプリケーションを追加、更新、削除する](https://azure.microsoft.com/en-us/documentation/articles/active-directory-integrating-applications/)
