---
title: iosGeneralDeviceConfiguration リソース タイプ
description: このトピックでは、iosGeneralDeviceConfiguration リソースによって公開された、宣言されたメソッド、プロパティ、リレーションシップについて説明します。
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: d3ede1a887fcac80b4645d771719f89124932ea8
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/24/2019
ms.locfileid: "32554619"
---
# <a name="iosgeneraldeviceconfiguration-resource-type"></a>iosGeneralDeviceConfiguration リソース タイプ

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

このトピックでは、iosGeneralDeviceConfiguration リソースによって公開された、宣言されたメソッド、プロパティ、リレーションシップについて説明します。


[deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List iosGeneralDeviceConfigurations](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-list.md)|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) コレクション|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get iosGeneralDeviceConfiguration](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-get.md)|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md)|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create iosGeneralDeviceConfiguration](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-create.md)|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md)|新しい [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) オブジェクトを作成します。|
|[Delete iosGeneralDeviceConfiguration](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-delete.md)|なし|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) を削除します。|
|[Update iosGeneralDeviceConfiguration](../api/intune-deviceconfig-iosgeneraldeviceconfiguration-update.md)|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md)|[iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列型 (String)|エンティティのキー。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|オブジェクトの最終更新の DateTime。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|createdDateTime|DateTimeOffset|オブジェクトが作成された DateTime。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|description|String|管理者が指定した、デバイス構成についての説明。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|displayName|String|管理者が指定した、デバイス構成の名前。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|version|Int32|デバイス構成のバージョン。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|accountBlockModification|ブール値|デバイスが監視モードのときに、アカウントの変更を許可するかどうかを示します。|
|activationLockAllowWhenSupervised|ブール値|デバイスが監視モードのときに、アクティベーション ロックを許可するかどうかを示します。|
|airDropBlocked|ブール値|デバイスが監視モードのときに、AirDrop を許可するかどうかを示します。|
|airDropForceUnmanagedDropTarget|ブール値|AirDrop を管理対象外のドロップ ターゲットと見なすかどうかを示します (iOS 9.0 以降)。|
|airPlayForcePairingPasswordForOutgoingRequests|ブール値|ペアリング パスワードを使用するために、このデバイスからの AirPlay 要求を受信するすべてのデバイスを適用するかどうかを示します。|
|appleWatchBlockPairing|ブール値|デバイスが監視モードのときに、Apple Watch のペアリングを許可するかどうかを示します (iOS 9.0 以降)。|
|appleWatchForceWristDetection|ブール値|ペアリングされている Apple Watch に手首検出機能を強制的に使用させるかどうかを示します (iOS 8.2 以降)。|
|appleNewsBlocked|ブール値|デバイスが監視モードのときに、ユーザーによる News の使用を禁止するかどうかを示します (iOS 9.0 以降)。|
|appsSingleAppModeList|[appListItem](../resources/intune-deviceconfig-applistitem.md) コレクション|単一アプリ モードに自律的に入ることが許可されている iOS アプリのリストを取得または設定します。 監視モードのみ。 iOS 7.0 以降。 このコレクションには、最大で 500 個の要素を含めることができます。|
|appsVisibilityList|[appListItem](../resources/intune-deviceconfig-applistitem.md) コレクション|可視性リストにあるアプリのリスト (iOS 9.3 以降で、AppVisibilityListType によって制御される、表示可能/起動可能なアプリのリスト、または非表示/起動できないアプリのリスト)。 このコレクションには、最大で 10000 個の要素を含めることができます。|
|appsVisibilityListType|[アプライアンスの種類](../resources/intune-deviceconfig-applisttype.md)|AppsVisibilityList 内にあるリストの種類です。 可能な値は、`none`、`appsInListCompliant`、`appsNotInListCompliant` です。|
|appStoreBlockAutomaticDownloads|ブール値|デバイスが監視モードのときに、他のデバイスで購入したアプリの自動ダウンロードをブロックするかどうかを示します (iOS 9.0 以降)。|
|appStoreBlocked|ブール値|ユーザーによる App Store の使用を禁止するかどうかを示します。|
|appStoreBlockInAppPurchases|ブール値|ユーザーによるアプリの購入を禁止するかどうかを示します。|
|appStoreBlockUIAppInstallation|ブール値|ホスト アプリによるインストールを制限せずに、App Store アプリをブロックするかどうかを示します。 監視モードのみに適用されます (iOS 9.0 以降)。|
|appStoreRequirePassword|ブール値|App Store 使用時に、パスワードを要求するかどうかを指定します。|
|bluetoothBlockModification|Boolean|デバイスが監視モードのときに、Bluetooth の設定の変更を許可するかどうかを示します (iOS 10.0 以降)。|
|cameraBlocked|Boolean|ユーザーによるデバイスのカメラへのアクセスを禁止するかどうかを示します。|
|cellularBlockDataRoaming|ブール値|データ ローミングをブロックするかどうかを示します。|
|cellularBlockGlobalBackgroundFetchWhileRoaming|ブール値|ローミング中に、グローバルなバックグラウンド フェッチをブロックするかどうかを示します。|
|cellularBlockPerAppDataModification|ブール値|デバイスが監視モードのときに、携帯ネットワーク アプリのデータの使用設定の変更を許可するかどうかを示します。|
|cellularBlockPersonalHotspot|ブール値|個人用ホットスポットをブロックするかどうかを示します。|
|cellularBlockVoiceRoaming|ブール値|音声通話ローミングをブロックするかどうかを示します。|
|certificatesBlockUntrustedTlsCertificates|ブール値|信頼されていない TLS の証明書をブロックするかどうかを示します。|
|classroomAppBlockRemoteScreenObservation|ブール値|デバイスが監視モードのときに、Classroom アプリによるリモート画面の監視を許可するかどうかを示します (iOS 9.3 以降)。|
|classroomAppForceUnpromptedScreenObservation|ブール値|デバイスが監視モードになっているときに、Classroom アプリでの管理対象コースの教師に、メッセージを表示せずに学生の画面を表示する許可を自動的に与えるかどうかを示します。|
|compliantAppsList|[appListItem](../resources/intune-deviceconfig-applistitem.md) コレクション|コンプライアンス内のアプリのリスト (CompliantAppListType によって制御される、許可リストまたは禁止リスト)。 このコレクションには、最大で 10000 個の要素を含めることができます。|
|compliantAppListType|[アプライアンスの種類](../resources/intune-deviceconfig-applisttype.md)|AppComplianceList 内にあるリスト。 可能な値は、`none`、`appsInListCompliant`、`appsNotInListCompliant` です。|
|configurationProfileBlockChanges|ブール値|デバイスが監視モードのときに、ユーザーが構成プロファイルと証明書を対話形式でインストールするのをブロックするかどうかを示します。|
|definitionLookupBlocked|ブール値|デバイスが監視モードのときに、定義の検索を禁止するかどうかを示します (iOS 8.1.3 以降)。|
|deviceBlockEnableRestrictions|ブール値|デバイスが監視モードのときに、ユーザーがデバイス設定の制限を有効にできるようにするかどうかを示します。|
|deviceBlockEraseContentAndSettings|ブール値|デバイスが監視モードのときに、デバイスの [すべてのコンテンツと設定を消去] オプションの使用を許可するかどうかを示します。|
|deviceBlockNameModification|ブール値|デバイスが監視モードのときに、デバイス名の変更を許可するかどうかを示します (iOS 9.0 以降)。|
|diagnosticDataBlockSubmission|ブール値|診断データの送信をブロックするかどうかを示します。|
|diagnosticDataBlockSubmissionModification|ブール値|デバイスが監視モードのときに、診断の送信の設定変更を許可するかどうかを示します (iOS 9.3.2 以降)。|
|documentsBlockManagedDocumentsInUnmanagedApps|ブール値|ユーザーによる非管理対象アプリでの管理対象ドキュメントの表示を禁止するかどうかを示します。|
|documentsBlockUnmanagedDocumentsInManagedApps|ブール値|ユーザーによる管理対象アプリでの非管理対象ドキュメントの表示を禁止するかどうかを示します。|
|emailInDomainSuffixes|String コレクション|これらの文字列のいずれかに一致するサフィックスがないメール アドレスは、ドメイン外と見なされます。|
|enterpriseAppBlockTrust|ブール値|ユーザーによるエンタープライズ アプリの信頼を禁止するかどうかを示します。|
|enterpriseAppBlockTrustModification|ブール値|ユーザーによるエンタープライズ アプリの信頼の設定の変更を禁止するかどうかを示します。|
|faceTimeBlocked|ブール値|ユーザーによる FaceTime の使用を禁止するかどうかを示します。|
|findMyFriendsBlocked|ブール値|デバイスが監視モードのときに、"友達を探す" をブロックするかどうかを示します。|
|gamingBlockGameCenterFriends|ブール値|ユーザーによる Game Center での友達の追加を禁止するかどうかを示します。|
|gamingBlockMultiplayer|ブール値|ユーザーによるマルチプレイヤー ゲームの使用を禁止するかどうかを示します。|
|gameCenterBlocked|ブール値|デバイスが監視モードのときに、ユーザーによる Game Center の使用を禁止するかどうかを示します。|
|hostPairingBlocked|ブール値|iOS デバイスが監視モードのときに、iOS デバイスがペアリングできるデバイスをホスト ペアリングで制御できるようにするかどうかを示します。|
|iBooksStoreBlocked|ブール値|デバイスが監視モードのときに、ユーザーによる iBooks Store の使用を禁止するかどうかを示します。|
|iBooksStoreBlockErotica|ブール値|アダルトのフラグが付いている iBookstore からのメディアのダウンロードをブロックするかどうかを示します。|
|iCloudBlockActivityContinuation|ブール型|ユーザーが ios デバイスで開始された作業を別の ios デバイスまたは macOS デバイスに継続して実行することを禁止するかどうかを示します。|
|iCloudBlockBackup|ブール値|iCloud バックアップを禁止するかどうかを示します。|
|iCloudBlockDocumentSync|Boolean|iCloud のドキュメントの同期を禁止するかどうかを示します。|
|iCloudBlockManagedAppsSync|ブール値|管理対象アプリのクラウドの同期を禁止するかどうかを示します。|
|iCloudBlockPhotoLibrary|ブール値|iCloud フォト ライブラリを禁止するかどうかを示します。|
|iCloudBlockPhotoStreamSync|ブール値|iCloud フォトのストリームの同期を禁止するかどうかを示します。|
|iCloudBlockSharedPhotoStream|ブール値|共有フォト ストリームの同期を禁止するかどうかを示します。|
|iCloudRequireEncryptedBackup|ブール値|iCloud のバックアップを暗号化する必要があるかどうかを示します。|
|iTunesBlockExplicitContent|ブール値|ユーザーによる iTunes および App Store の過激な描写のコンテンツへのアクセスをブロックするかどうかを指定します。|
|iTunesBlockMusicService|ブール値|デバイスが監視モードのときに、Music サービスをブロックして Music アプリをクラシック モードに戻すかどうかを示します (iOS 9.3 以降および macOS 10.12 以降)。|
|iTunesBlockRadio|ブール値|デバイスが監視モードのときに、ユーザーによる iTunes Radio の使用を禁止するかどうかを示します (iOS 9.3 以降)。|
|keyboardBlockAutoCorrect|ブール値|デバイスが監視モードのときに、キーボードの自動修正を禁止するかどうかを示します (iOS 8.13 以降)。|
|keyboardBlockDictation|ブール値|デバイスが監視モードのときに、ユーザーによるディクテーション入力の使用を禁止するかどうかを示します。|
|keyboardBlockPredictive|ブール値|デバイスが監視モードのときに、予測キーボードを禁止するかどうかを示します (iOS 8.1.3 以降)。|
|keyboardBlockShortcuts|ブール値|デバイスが監視モードのときに、キーボード ショートカットを禁止するかどうかを示します (iOS 9.0 以降)。|
|keyboardBlockSpellCheck|ブール値|デバイスが監視モードのときに、キーボードのスペル チェックを禁止するかどうかを示します (iOS 8.13 以降)。|
|kioskModeAllowAssistiveSpeak|ブール値|キオスク モード時の補助音声を許可するかどうかを示します。|
|kioskModeAllowAssistiveTouchSettings|ブール値|キオスク モード時の Assistive Touch の設定へのアクセスを許可するかどうかを示します。|
|kioskModeAllowAutoLock|ブール値|キオスク モード時のデバイスの自動ロックを許可するかどうかを示します。|
|kioskModeAllowColorInversionSettings|ブール値|キオスク モード時の色反転の設定へのアクセスを許可するかどうかを示します。|
|kioskModeAllowRingerSwitch|ブール値|キオスク モード時の着信音スイッチの使用を許可するかどうかを示します。|
|kioskModeAllowScreenRotation|ブール値|キオスク モード時の画面の回転を許可するかどうかを示します。|
|kioskModeAllowSleepButton|ブール値|キオスク モード時のスリープ ボタンの使用を許可するかどうかを示します。|
|kioskModeAllowTouchscreen|ブール値|キオスク モード時のタッチスクリーンの使用を許可するかどうかを示します。|
|kioskModeAllowVoiceOverSettings|ブール値|キオスク モード時のボイス オーバーの設定へのアクセスを許可するかどうかを示します。|
|kioskModeAllowVolumeButtons|ブール値|キオスク モード時のボリューム ボタンの使用を許可するかどうかを示します。|
|kioskModeAllowZoomSettings|ブール値|キオスク モード時のズーム設定へのアクセスを許可するかどうかを示します。|
|kioskModeAppStoreUrl|String|キオスク モード用に使用するアプリへの、App Store 内の URL。 KioskModeManagedAppId が不明な場合に使用します。|
|kioskModeBuiltInAppId|String|キオスクモード用に使用する組み込みアプリの ID。 KioskModeManagedAppId および KioskModeAppStoreUrl が設定されていない場合に使用します。|
|kioskModeRequireAssistiveTouch|ブール値|キオスク モード時に Assistive Touch が必要かどうかを示します。|
|kioskModeRequireColorInversion|ブール値|キオスク モード時に色反転が必要かどうかを示します。|
|kioskModeRequireMonoAudio|ブール値|キオスク モード時にモノラル オーディオが必要かどうかを示します。|
|kioskModeRequireVoiceOver|ブール値|キオスク モード時にボイス オーバーが必要かどうかを示します。|
|kioskModeRequireZoom|ブール値|キオスク モード時にズームが必要かどうかを示します。|
|kioskModeManagedAppId|String|キオスク モード用に使用するアプリの管理対象アプリ ID。 KioskModeManagedAppId が指定されている場合は、KioskModeAppStoreUrl は無視されます。|
|lockScreenBlockControlCenter|Boolean|ユーザーによるロック画面でのコントロール センターの使用を禁止するかどうかを示します。|
|lockScreenBlockNotificationView|ブール値|ユーザーによるロック画面での通知ビューの使用を禁止するかどうかを示します。|
|lockScreenBlockPassbook|ブール値|デバイスがロックされているときに、ユーザーによる Passbook の使用を禁止するかどうかを示します。|
|lockScreenBlockTodayView|ブール値|ユーザーによるロック画面での本日のビューの使用を禁止するかどうかを示します。|
|mediaContentRatingAustralia|[mediaContentRatingAustralia](../resources/intune-deviceconfig-mediacontentratingaustralia.md)|メディア コンテンツの評価の設定 (オーストラリア向け)|
|mediaContentRatingCanada|[mediaContentRatingCanada](../resources/intune-deviceconfig-mediacontentratingcanada.md)|メディア コンテンツの評価の設定 (カナダ向け)|
|mediaContentRatingFrance|[mediaContentRatingFrance](../resources/intune-deviceconfig-mediacontentratingfrance.md)|メディア コンテンツの評価の設定 (フランス向け)|
|mediaContentRatingGermany|[mediaContentRatingGermany](../resources/intune-deviceconfig-mediacontentratinggermany.md)|メディア コンテンツの評価の設定 (ドイツ向け)|
|mediaContentRatingIreland|[mediaContentRatingIreland](../resources/intune-deviceconfig-mediacontentratingireland.md)|メディア コンテンツの評価の設定 (アイルランド向け)|
|mediaContentRatingJapan|[mediaContentRatingJapan](../resources/intune-deviceconfig-mediacontentratingjapan.md)|メディア コンテンツの評価の設定 (日本向け)|
|mediaContentRatingNewZealand|[mediaContentRatingNewZealand](../resources/intune-deviceconfig-mediacontentratingnewzealand.md)|メディア コンテンツの評価の設定 (ニュージーランド向け)|
|mediaContentRatingUnitedKingdom|[mediaContentRatingUnitedKingdom](../resources/intune-deviceconfig-mediacontentratingunitedkingdom.md)|メディア コンテンツの評価の設定 (英国向け)|
|mediaContentRatingUnitedStates|[mediaContentRatingUnitedStates](../resources/intune-deviceconfig-mediacontentratingunitedstates.md)|メディア コンテンツの評価の設定 (米国向け)|
|networkUsageRules|[iosNetworkUsageRule](../resources/intune-deviceconfig-iosnetworkusagerule.md) コレクション|管理対象アプリと、それらに適用されるネットワーク ルールのリストです。 このコレクションには、最大で 1000 個の要素を含めることができます。|
|mediaContentRatingApps|[ratingAppsType](../resources/intune-deviceconfig-ratingappstype.md)|アプリのメディアコンテンツの評価の設定。 可能な値は `allAllowed`、`allBlocked`、`agesAbove4`、`agesAbove9`、`agesAbove12`、`agesAbove17` です。|
|messagesBlocked|ブール値|ユーザーによる監視対象デバイスでのメッセージ アプリの使用を禁止するかどうかを示します。|
|notificationsBlockSettingsModification|ブール値|通知の設定の変更を許可するかどうかを示します (iOS 9.3 以降)。|
|passcodeBlockFingerprintUnlock|ブール値|指紋によるロック解除を禁止するかどうかを示します。|
|passcodeBlockFingerprintModification|ブール値|監視モードの際の、登録済みの Touch ID の指紋認証の修正を禁止します。|
|passcodeBlockModification|ブール値|監視対象デバイスでのパスコードの変更を許可するかどうかを示します (iOS 9.0 以降)。|
|passcodeBlockSimple|ブール値|単純なパスコードを禁止するかどうかを示します。|
|passcodeExpirationDays|Int32|パスコードの有効期限が切れるまでの日数。 有効な値は 1 から 65535 までです|
|passcodeMinimumLength|Int32|パスコードの最小の長さ。 有効な値は 4 から 14 までです|
|passcodeMinutesOfInactivityBeforeLock|Int32|パスコードが要求されるまでの非アクティブ時間 (分)。|
|passcodeMinutesOfInactivityBeforeScreenTimeout|Int32|画面がタイムアウトになるまでの非アクティブ時間 (分)。|
|passcodeMinimumCharacterSetCount|Int32|パスコードが含まなければならない文字セットの数。 有効な値は 0 から 4 までです|
|passcodePreviousPasscodeBlockCount|Int32|ブロックする、以前のパスコードの数。 有効な値は 1 から 24 までです|
|passcodeSignInFailureCountBeforeWipe|Int32|デバイスをワイプするまでの、失敗が許可されるサインインの回数。 有効な値は 4 から 11 までです|
|passcodeRequiredType|[requiredpasswordtype](../resources/intune-deviceconfig-requiredpasswordtype.md)|必要なパスコードの種類。 可能な値は、`deviceDefault`、`alphanumeric`、`numeric` です。|
|passcodeRequired|ブール値|パスコードを要求するかどうかを指定します。|
|podcastsBlocked|Boolean|ユーザーによる監視対象デバイスでのポッドキャストの使用を禁止するかどうかを示します (iOS 8.0 以降)。|
|safariBlockAutofill|ブール値|ユーザーによる Safari での自動入力の使用を禁止するかどうかを示します。|
|safariBlockJavaScript|ブール値|Safari 内で JavaScript をブロックするかどうかを示します。|
|safariBlockPopups|ブール値|Safari 内でポップアップをブロックするかどうかを示します。|
|safariBlocked|ブール値|ユーザーによる Safari の使用を禁止するかどうかを示します。|
|safariCookieSettings|[webBrowserCookieSettings](../resources/intune-deviceconfig-webbrowsercookiesettings.md)|Safari の Cookie の設定。 可能な値は、`browserDefault`、`blockAlways`、`allowCurrentWebSite`、`allowFromWebsitesVisited`、`allowAlways` です。|
|safariManagedDomains|String collection|ここに記載されているパターンに一致する URL は管理対象と見なされます。|
|safariPasswordAutoFillDomains|String コレクション|ユーザーは、ここに記載されているパターンに一致する URL からのみ、パスワードを Safari に保存できます。 監視モードのデバイスに適用されます (iOS 9.3 以降)。|
|safariRequireFraudWarning|ブール値|Safari での不正行為の警告を必要とするかどうかを示します。|
|screenCaptureBlocked|ブール値|ユーザーがスクリーンショットを撮ることを禁止するかどうかを示します。|
|siriBlocked|ブール値|ユーザーによる Siri の使用を禁止するかどうかを示します。|
|siriBlockedWhenLocked|ブール値|ロックされている場合に、ユーザーによる Siri の使用を禁止するかどうかを示します。|
|siriBlockUserGeneratedContent|ブール値|監視対象デバイスでの使用時に、Siri による、ユーザー生成コンテンツに対するクエリの実行をブロックするかどうかを示します。|
|siriRequireProfanityFilter|ブール値|Siri が監視対象デバイスで不適切な言葉をディクテーションまたは読み上げないようにするかどうかを示します。|
|spotlightBlockInternetResults|ブール値|監視対象デバイスで Spotlight 検索がインターネットでの結果を返すのをブロックするかどうかを示します。|
|voiceDialingBlocked|ブール値|音声ダイヤルをブロックするかどうかを示します。|
|wallpaperBlockModification|ブール値|監視対象デバイスでの壁紙の変更を許可するかどうかを示します (iOS 9.0 以降)。|
|wiFiConnectOnlyToConfiguredNetworks|Boolean|デバイスが監視モードのときに、構成プロファイルからの Wi-Fi ネットワークのみを使用するようデバイスに強制するかどうかを示します。|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|assignments|[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) コレクション|デバイスの構成プロファイルの割り当てのリスト。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|deviceStatuses|[deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) コレクション|デバイスごとのデバイス構成のインストール状況。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|userStatuses|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) コレクション|ユーザーごとのデバイス構成のインストール状態。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|デバイス構成のデバイス状態の概要 ([deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|デバイス構成のユーザー状態の概要 ([deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承)|
|deviceSettingStateSummaries|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) コレクション|デバイス構成設定状態のデバイスの要約 ([deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承)|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosGeneralDeviceConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosGeneralDeviceConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "accountBlockModification": true,
  "activationLockAllowWhenSupervised": true,
  "airDropBlocked": true,
  "airDropForceUnmanagedDropTarget": true,
  "airPlayForcePairingPasswordForOutgoingRequests": true,
  "appleWatchBlockPairing": true,
  "appleWatchForceWristDetection": true,
  "appleNewsBlocked": true,
  "appsSingleAppModeList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "appsVisibilityList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "appsVisibilityListType": "String",
  "appStoreBlockAutomaticDownloads": true,
  "appStoreBlocked": true,
  "appStoreBlockInAppPurchases": true,
  "appStoreBlockUIAppInstallation": true,
  "appStoreRequirePassword": true,
  "bluetoothBlockModification": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockGlobalBackgroundFetchWhileRoaming": true,
  "cellularBlockPerAppDataModification": true,
  "cellularBlockPersonalHotspot": true,
  "cellularBlockVoiceRoaming": true,
  "certificatesBlockUntrustedTlsCertificates": true,
  "classroomAppBlockRemoteScreenObservation": true,
  "classroomAppForceUnpromptedScreenObservation": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "compliantAppListType": "String",
  "configurationProfileBlockChanges": true,
  "definitionLookupBlocked": true,
  "deviceBlockEnableRestrictions": true,
  "deviceBlockEraseContentAndSettings": true,
  "deviceBlockNameModification": true,
  "diagnosticDataBlockSubmission": true,
  "diagnosticDataBlockSubmissionModification": true,
  "documentsBlockManagedDocumentsInUnmanagedApps": true,
  "documentsBlockUnmanagedDocumentsInManagedApps": true,
  "emailInDomainSuffixes": [
    "String"
  ],
  "enterpriseAppBlockTrust": true,
  "enterpriseAppBlockTrustModification": true,
  "faceTimeBlocked": true,
  "findMyFriendsBlocked": true,
  "gamingBlockGameCenterFriends": true,
  "gamingBlockMultiplayer": true,
  "gameCenterBlocked": true,
  "hostPairingBlocked": true,
  "iBooksStoreBlocked": true,
  "iBooksStoreBlockErotica": true,
  "iCloudBlockActivityContinuation": true,
  "iCloudBlockBackup": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockManagedAppsSync": true,
  "iCloudBlockPhotoLibrary": true,
  "iCloudBlockPhotoStreamSync": true,
  "iCloudBlockSharedPhotoStream": true,
  "iCloudRequireEncryptedBackup": true,
  "iTunesBlockExplicitContent": true,
  "iTunesBlockMusicService": true,
  "iTunesBlockRadio": true,
  "keyboardBlockAutoCorrect": true,
  "keyboardBlockDictation": true,
  "keyboardBlockPredictive": true,
  "keyboardBlockShortcuts": true,
  "keyboardBlockSpellCheck": true,
  "kioskModeAllowAssistiveSpeak": true,
  "kioskModeAllowAssistiveTouchSettings": true,
  "kioskModeAllowAutoLock": true,
  "kioskModeAllowColorInversionSettings": true,
  "kioskModeAllowRingerSwitch": true,
  "kioskModeAllowScreenRotation": true,
  "kioskModeAllowSleepButton": true,
  "kioskModeAllowTouchscreen": true,
  "kioskModeAllowVoiceOverSettings": true,
  "kioskModeAllowVolumeButtons": true,
  "kioskModeAllowZoomSettings": true,
  "kioskModeAppStoreUrl": "String",
  "kioskModeBuiltInAppId": "String",
  "kioskModeRequireAssistiveTouch": true,
  "kioskModeRequireColorInversion": true,
  "kioskModeRequireMonoAudio": true,
  "kioskModeRequireVoiceOver": true,
  "kioskModeRequireZoom": true,
  "kioskModeManagedAppId": "String",
  "lockScreenBlockControlCenter": true,
  "lockScreenBlockNotificationView": true,
  "lockScreenBlockPassbook": true,
  "lockScreenBlockTodayView": true,
  "mediaContentRatingAustralia": {
    "@odata.type": "microsoft.graph.mediaContentRatingAustralia",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingCanada": {
    "@odata.type": "microsoft.graph.mediaContentRatingCanada",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingFrance": {
    "@odata.type": "microsoft.graph.mediaContentRatingFrance",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingGermany": {
    "@odata.type": "microsoft.graph.mediaContentRatingGermany",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingIreland": {
    "@odata.type": "microsoft.graph.mediaContentRatingIreland",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingJapan": {
    "@odata.type": "microsoft.graph.mediaContentRatingJapan",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingNewZealand": {
    "@odata.type": "microsoft.graph.mediaContentRatingNewZealand",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingUnitedKingdom": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom",
    "movieRating": "String",
    "tvRating": "String"
  },
  "mediaContentRatingUnitedStates": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates",
    "movieRating": "String",
    "tvRating": "String"
  },
  "networkUsageRules": [
    {
      "@odata.type": "microsoft.graph.iosNetworkUsageRule",
      "managedApps": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "String",
          "publisher": "String",
          "appStoreUrl": "String",
          "appId": "String"
        }
      ],
      "cellularDataBlockWhenRoaming": true,
      "cellularDataBlocked": true
    }
  ],
  "mediaContentRatingApps": "String",
  "messagesBlocked": true,
  "notificationsBlockSettingsModification": true,
  "passcodeBlockFingerprintUnlock": true,
  "passcodeBlockFingerprintModification": true,
  "passcodeBlockModification": true,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 1024,
  "passcodeMinimumLength": 1024,
  "passcodeMinutesOfInactivityBeforeLock": 1024,
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 1024,
  "passcodeMinimumCharacterSetCount": 1024,
  "passcodePreviousPasscodeBlockCount": 1024,
  "passcodeSignInFailureCountBeforeWipe": 1024,
  "passcodeRequiredType": "String",
  "passcodeRequired": true,
  "podcastsBlocked": true,
  "safariBlockAutofill": true,
  "safariBlockJavaScript": true,
  "safariBlockPopups": true,
  "safariBlocked": true,
  "safariCookieSettings": "String",
  "safariManagedDomains": [
    "String"
  ],
  "safariPasswordAutoFillDomains": [
    "String"
  ],
  "safariRequireFraudWarning": true,
  "screenCaptureBlocked": true,
  "siriBlocked": true,
  "siriBlockedWhenLocked": true,
  "siriBlockUserGeneratedContent": true,
  "siriRequireProfanityFilter": true,
  "spotlightBlockInternetResults": true,
  "voiceDialingBlocked": true,
  "wallpaperBlockModification": true,
  "wiFiConnectOnlyToConfiguredNetworks": true
}
```



