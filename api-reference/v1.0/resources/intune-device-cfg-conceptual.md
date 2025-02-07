---
title: Microsoft Intune でのデバイス構成
description: Microsoft Intune のデバイス構成のワークロードを使用して、管理するすべてのデバイスの設定と機能を管理します。
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: eda3d25b712b10feba3aac76135861acbc5a2f86
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32575220"
---
# <a name="device-configuration-in-microsoft-intune"></a>Microsoft Intune でのデバイス構成

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune-pricing)を持っている必要があります。

Microsoft Intune のデバイス構成のワークロードを使用して、管理するすべてのデバイスの設定と機能を管理します。

次の Graph リソースを使用して、Intune でのデバイスの設定と機能を管理できます。

- [Android コンプライアンス ポリシー](intune-deviceconfig-androidcompliancepolicy.md)
- [Android カスタム構成](intune-deviceconfig-androidcustomconfiguration.md)
- [Android 一般デバイス構成](intune-deviceconfig-androidgeneraldeviceconfiguration.md)
- [Android に必要なパスワードの種類](intune-deviceconfig-androidrequiredpasswordtype.md)
- [Android 作業プロファイル コンプライアンス ポリシー](intune-deviceconfig-androidworkprofilecompliancepolicy.md)
- [Android 仕事用プロファイルのクロス プロファイル データ共有タイプ](intune-deviceconfig-androidworkprofilecrossprofiledatasharingtype.md)
- [Android 仕事用プロファイルのカスタム構成](intune-deviceconfig-androidworkprofilecustomconfiguration.md)
- [Android 仕事用プロファイル既定アプリのアクセス許可ポリシーのタイプ](intune-deviceconfig-androidworkprofiledefaultapppermissionpolicytype.md)
- [Android 仕事用プロファイル一般デバイス構成](intune-deviceconfig-androidworkprofilegeneraldeviceconfiguration.md)
- [Android 仕事用プロファイルに必要なパスワードの種類](intune-deviceconfig-androidworkprofilerequiredpasswordtype.md)
- [アプリ リストの項目](intune-deviceconfig-applistitem.md)
- [アプリ リストの種類](intune-deviceconfig-applisttype.md)
- [App locker アプリケーションのコントロールの種類](intune-deviceconfig-applockerapplicationcontroltype.md)
- [Apple デバイス機能構成ベース](intune-deviceconfig-appledevicefeaturesconfigurationbase.md)
- [アプリケーション ガード ブロックのクリップボード共有タイプ](intune-deviceconfig-applicationguardblockclipboardsharingtype.md)
- [アプリケーション ガード ブロックのファイル転送タイプ](intune-deviceconfig-applicationguardblockfiletransfertype.md)
- [自動更新モード](intune-deviceconfig-automaticupdatemode.md)
- [BitLocker 暗号化方法](intune-deviceconfig-bitlockerencryptionmethod.md)
- [BitLocker リムーバブル ドライブ ポリシー](intune-deviceconfig-bitlockerremovabledrivepolicy.md)
- [曜日](intune-deviceconfig-dayofweek.md)
- [Defender クラウド ブロックレベルの種類](intune-deviceconfig-defendercloudblockleveltype.md)
- [Defender によって検出されたマルウェア アクション](intune-deviceconfig-defenderdetectedmalwareactions.md)
- [Defender ファイル アクティビティの監視](intune-deviceconfig-defendermonitorfileactivity.md)
- [Defender サンプルの送信を促す](intune-deviceconfig-defenderpromptforsamplesubmission.md)
- [Defender スキャンの種類](intune-deviceconfig-defenderscantype.md)
- [Defender 脅威アクション](intune-deviceconfig-defenderthreataction.md)
- [デバイス コンプライアンス アクションの項目](intune-deviceconfig-devicecomplianceactionitem.md)
- [デバイス コンプライアンス アクションの種類](intune-deviceconfig-devicecomplianceactiontype.md)
- [デバイス コンプライアンスのデバイスの概要](intune-deviceconfig-devicecompliancedeviceoverview.md)
- [デバイス コンプライアンスのデバイスの状態](intune-deviceconfig-devicecompliancedevicestatus.md)
- [デバイス コンプライアンス ポリシー](intune-deviceconfig-devicecompliancepolicy.md)
- [デバイス コンプライアンス ポリシーの割り当て](intune-deviceconfig-devicecompliancepolicyassignment.md)
- [デバイス コンプライアンス ポリシーのデバイス状態の要約](intune-deviceconfig-devicecompliancepolicydevicestatesummary.md)
- [デバイス コンプライアンス ポリシーの設定状態](intune-deviceconfig-devicecompliancepolicysettingstate.md)
- [デバイス コンプライアンス ポリシーの設定状態の要約](intune-deviceconfig-devicecompliancepolicysettingstatesummary.md)
- [デバイス コンプライアンスのルールに関するスケジュール済みアクション](intune-deviceconfig-devicecompliancescheduledactionforrule.md)
- [デバイス コンプライアンスの設定状態](intune-deviceconfig-devicecompliancesettingstate.md)
- [デバイス コンプライアンスのユーザーの概要](intune-deviceconfig-devicecomplianceuseroverview.md)
- [デバイス コンプライアンスのユーザーの状態](intune-deviceconfig-devicecomplianceuserstatus.md)
- [デバイス構成](intune-deviceconfig-deviceconfiguration.md)
- [デバイス構成の割り当て](intune-deviceconfig-deviceconfigurationassignment.md)
- [デバイス構成のデバイスの概要](intune-deviceconfig-deviceconfigurationdeviceoverview.md)
- [デバイス構成のデバイス状態の要約](intune-deviceconfig-deviceconfigurationdevicestatesummary.md)
- [デバイス構成のデバイスの状態](intune-deviceconfig-deviceconfigurationdevicestatus.md)
- [デバイス構成の設定状態](intune-deviceconfig-deviceconfigurationsettingstate.md)
- [デバイス構成のユーザーの概要](intune-deviceconfig-deviceconfigurationuseroverview.md)
- [デバイス構成のユーザーの状態](intune-deviceconfig-deviceconfigurationuserstatus.md)
- [デバイス管理設定](intune-deviceconfig-devicemanagementsettings.md)
- [デバイスの脅威保護レベル](intune-deviceconfig-devicethreatprotectionlevel.md)
- [診断データの送信モード](intune-deviceconfig-diagnosticdatasubmissionmode.md)
- [Edge cookie ポリシー](intune-deviceconfig-edgecookiepolicy.md)
- [Edge の検索エンジン](intune-deviceconfig-edgesearchengine.md)
- [Edge の検索エンジン ベース](intune-deviceconfig-edgesearchenginebase.md)
- [Edge の検索エンジンのユーザー設定](intune-deviceconfig-edgesearchenginecustom.md)
- [Edge の検索エンジンの種類](intune-deviceconfig-edgesearchenginetype.md)
- [エディション アップグレード構成](intune-deviceconfig-editionupgradeconfiguration.md)
- [エディション アップグレード ライセンスの種類](intune-deviceconfig-editionupgradelicensetype.md)
- [ファイアウォール証明書失効リスト確認方法の種類](intune-deviceconfig-firewallcertificaterevocationlistcheckmethodtype.md)
- [ファイアウォール パケット キュー メソッドの種類](intune-deviceconfig-firewallpacketqueueingmethodtype.md)
- [ファイアウォール事前共有キー エンコーディング方法の種類](intune-deviceconfig-firewallpresharedkeyencodingmethodtype.md)
- [インターネット サイトのセキュリティ レベル](intune-deviceconfig-internetsitesecuritylevel.md)
- [iOS 証明書のプロファイル](intune-deviceconfig-ioscertificateprofile.md)
- [iOS コンプライアンス ポリシー](intune-deviceconfig-ioscompliancepolicy.md)
- [iOS カスタム構成](intune-deviceconfig-ioscustomconfiguration.md)
- [iOS デバイス機能構成](intune-deviceconfig-iosdevicefeaturesconfiguration.md)
- [iOS 一般デバイス構成](intune-deviceconfig-iosgeneraldeviceconfiguration.md)
- [iOS ホーム画面のアプリ](intune-deviceconfig-ioshomescreenapp.md)
- [iOS ホーム画面のフォルダー](intune-deviceconfig-ioshomescreenfolder.md)
- [iOS ホーム画面のフォルダーのページ](intune-deviceconfig-ioshomescreenfolderpage.md)
- [iOS ホーム画面のアイテム](intune-deviceconfig-ioshomescreenitem.md)
- [iOS ホーム画面のページ](intune-deviceconfig-ioshomescreenpage.md)
- [iOS ネットワークの使用規則](intune-deviceconfig-iosnetworkusagerule.md)
- [iOS の通知アラートの種類](intune-deviceconfig-iosnotificationalerttype.md)
- [iOS の通知設定](intune-deviceconfig-iosnotificationsettings.md)
- [iOS 更新構成](intune-deviceconfig-iosupdateconfiguration.md)
- [iOS 更新デバイスの状態](intune-deviceconfig-iosupdatedevicestatus.md)
- [iOS の更新プログラムのインストール状態](intune-deviceconfig-iosupdatesinstallstatus.md)
- [macOS コンプライアンス ポリシー](intune-deviceconfig-macoscompliancepolicy.md)
- [macOS カスタム構成](intune-deviceconfig-macoscustomconfiguration.md)
- [macOS デバイス機能構成](intune-deviceconfig-macosdevicefeaturesconfiguration.md)
- [macOS 一般デバイス構成](intune-deviceconfig-macosgeneraldeviceconfiguration.md)
- [メディア コンテンツのレーティング、オーストラリア](intune-deviceconfig-mediacontentratingaustralia.md)
- [メディア コンテンツのレーティング、カナダ](intune-deviceconfig-mediacontentratingcanada.md)
- [メディア コンテンツのレーティング、フランス](intune-deviceconfig-mediacontentratingfrance.md)
- [メディア コンテンツのレーティング、ドイツ](intune-deviceconfig-mediacontentratinggermany.md)
- [メディア コンテンツのレーティング、アイルランド](intune-deviceconfig-mediacontentratingireland.md)
- [メディア コンテンツのレーティング、日本](intune-deviceconfig-mediacontentratingjapan.md)
- [メディア コンテンツのレーティング、ニュージーランド](intune-deviceconfig-mediacontentratingnewzealand.md)
- [メディア コンテンツのレーティング、英国](intune-deviceconfig-mediacontentratingunitedkingdom.md)
- [メディア コンテンツのレーティング、米国](intune-deviceconfig-mediacontentratingunitedstates.md)
- [Miracast チャネル](intune-deviceconfig-miracastchannel.md)
- [OMA 設定](intune-deviceconfig-omasetting.md)
- [OMA 設定、base 64](intune-deviceconfig-omasettingbase64.md)
- [OMA 設定、ブール型 (Boolean)](intune-deviceconfig-omasettingboolean.md)
- [OMA 設定、日時](intune-deviceconfig-omasettingdatetime.md)
- [OMA 設定、浮動小数点数](intune-deviceconfig-omasettingfloatingpoint.md)
- [OMA 設定、整数](intune-deviceconfig-omasettinginteger.md)
- [OMA 設定、文字列](intune-deviceconfig-omasettingstring.md)
- [OMA 設定、xml 文字列](intune-deviceconfig-omasettingstringxml.md)
- [ポリシー プラットフォームの種類](intune-deviceconfig-policyplatformtype.md)
- [プレリリース機能](intune-deviceconfig-prereleasefeatures.md)
- [アプリの種類の評価](intune-deviceconfig-ratingappstype.md)
- [オーストラリアの映画の種類の評価](intune-deviceconfig-ratingaustraliamoviestype.md)
- [オーストラリアのテレビの種類の評価](intune-deviceconfig-ratingaustraliatelevisiontype.md)
- [カナダの映画の種類の評価](intune-deviceconfig-ratingcanadamoviestype.md)
- [カナダのテレビの種類の評価](intune-deviceconfig-ratingcanadatelevisiontype.md)
- [フランスの映画の種類の評価](intune-deviceconfig-ratingfrancemoviestype.md)
- [フランスのテレビの種類の評価](intune-deviceconfig-ratingfrancetelevisiontype.md)
- [ドイツの映画の種類の評価](intune-deviceconfig-ratinggermanymoviestype.md)
- [ドイツのテレビの種類の評価](intune-deviceconfig-ratinggermanytelevisiontype.md)
- [アイルランドの映画の種類の評価](intune-deviceconfig-ratingirelandmoviestype.md)
- [アイルランドのテレビの種類の評価](intune-deviceconfig-ratingirelandtelevisiontype.md)
- [日本の映画の種類の評価](intune-deviceconfig-ratingjapanmoviestype.md)
- [日本のテレビの種類の評価](intune-deviceconfig-ratingjapantelevisiontype.md)
- [ニュージーランド ムービーの種類の評価](intune-deviceconfig-ratingnewzealandmoviestype.md)
- [ニュージーランド テレビの種類の評価](intune-deviceconfig-ratingnewzealandtelevisiontype.md)
- [英国ムービーの種類の評価](intune-deviceconfig-ratingunitedkingdommoviestype.md)
- [英国のテレビの種類の評価](intune-deviceconfig-ratingunitedkingdomtelevisiontype.md)
- [アメリカ合衆国ムービーの種類の評価](intune-deviceconfig-ratingunitedstatesmoviestype.md)
- [アメリカ合衆国テレビの種類の評価](intune-deviceconfig-ratingunitedstatestelevisiontype.md)
- [パスワードの入力が必要](intune-deviceconfig-requiredpasswordtype.md)
- [セーフ サーチのフィルターのタイプ](intune-deviceconfig-safesearchfiltertype.md)
- [ソースの設定](intune-deviceconfig-settingsource.md)
- [設定状態とデバイスの要約](intune-deviceconfig-settingstatedevicesummary.md)
- [共有 PC アカウントの削除ポリシーの種類](intune-deviceconfig-sharedpcaccountdeletionpolicytype.md)
- [共有 PC アカウント マネージャー ポリシー](intune-deviceconfig-sharedpcaccountmanagerpolicy.md)
- [共有 PC が許可するアカウント タイプ](intune-deviceconfig-sharedpcallowedaccounttype.md)
- [共有 PC 構成](intune-deviceconfig-sharedpcconfiguration.md)
- [サイトのセキュリティ レベル](intune-deviceconfig-sitesecuritylevel.md)
- [ソフトウェア更新状態の要約](intune-deviceconfig-softwareupdatestatussummary.md)
- [状態管理の設定](intune-deviceconfig-statemanagementsetting.md)
- [表示設定](intune-deviceconfig-visibilitysetting.md)
- [Web ブラウザーの cookie の設定](intune-deviceconfig-webbrowsercookiesettings.md)
- [週単位のスケジュール](intune-deviceconfig-weeklyschedule.md)
- [ようこそ画面の会議情報](intune-deviceconfig-welcomescreenmeetinginformation.md)
- [Windows 10 コンプライアンス ポリシー](intune-deviceconfig-windows10compliancepolicy.md)
- [Windows 10 カスタム構成](intune-deviceconfig-windows10customconfiguration.md)
- [Windows 10 エディションの種類](intune-deviceconfig-windows10editiontype.md)
- [Windows 10 Endpoint Protection 構成](intune-deviceconfig-windows10endpointprotectionconfiguration.md)
- [Windows 10 Enterprise モダン アプリの管理構成](intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md)
- [Windows 10 一般構成](intune-deviceconfig-windows10generalconfiguration.md)
- [Windows 10 モバイル コンプライアンス ポリシー](intune-deviceconfig-windows10mobilecompliancepolicy.md)
- [Windows 10 ネットワーク プロキシ サーバー](intune-deviceconfig-windows10networkproxyserver.md)
- [Windows 10 の安全評価の構成](intune-deviceconfig-windows10secureassessmentconfiguration.md)
- [Windows 10 Team 一般構成](intune-deviceconfig-windows10teamgeneralconfiguration.md)
- [Windows 8.1 コンプライアンス ポリシー](intune-deviceconfig-windows81compliancepolicy.md)
- [Windows 8.1 一般構成](intune-deviceconfig-windows81generalconfiguration.md)
- [Windows Defender Advanced Threat Protection 構成](intune-deviceconfig-windowsdefenderadvancedthreatprotectionconfiguration.md)
- [Windows 配信最適化モード](intune-deviceconfig-windowsdeliveryoptimizationmode.md)
- [Windows ファイアウォール ネットワーク プロファイル](intune-deviceconfig-windowsfirewallnetworkprofile.md)
- [Windows Phone 8.1 コンプライアンス ポリシー](intune-deviceconfig-windowsphone81compliancepolicy.md)
- [Windows Phone 8.1 カスタム構成](intune-deviceconfig-windowsphone81customconfiguration.md)
- [Windows Phone 8.1 一般構成](intune-deviceconfig-windowsphone81generalconfiguration.md)
- [Windows スポットライト有効化設定](intune-deviceconfig-windowsspotlightenablementsettings.md)
- [Windows スタート メニュー アプリ リストの表示タイプ](intune-deviceconfig-windowsstartmenuapplistvisibilitytype.md)
- [Windows スタート メニューのモード タイプ](intune-deviceconfig-windowsstartmenumodetype.md)
- [Windows Update アクティブ期間インストール](intune-deviceconfig-windowsupdateactivehoursinstall.md)
- [Windows Update for Business 構成](intune-deviceconfig-windowsupdateforbusinessconfiguration.md)
- [Windows Update インストール スケジュールのタイプ](intune-deviceconfig-windowsupdateinstallscheduletype.md)
- [Windows Update のスケジュール済みインストール](intune-deviceconfig-windowsupdatescheduledinstall.md)
- [Windows Update の種類](intune-deviceconfig-windowsupdatetype.md)
- [Windows ユーザー アカウント制御の設定](intune-deviceconfig-windowsuseraccountcontrolsettings.md)
