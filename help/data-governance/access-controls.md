---
title: アクセス制御
description: Mix Modelerでアクセス制御を設定する方法を説明します。
feature: Administration
source-git-commit: 6776a91563f120db1341adef923aab4b0f582c9d
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 32%

---

# アクセス制御

Mix Modelerのアクセス制御は、[Adobe Admin ConsoleのExperience Platformを通じて提供され ](https://adminconsole.adobe.com/) す。また、Experience Platformの [ 権限 ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions) を通じて提供されます。 この機能は、Admin Consoleの製品プロファイルを利用して、ユーザーを権限およびサンドボックスにリンクします。

アクセス制御について詳しくは、「[ アクセス制御の概要 ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home)」を参照してください。

## 役割ベースのアクセス制御

Experience PlatformのMix Modelerユーザーおよびユーザーグループに対する役割ベースのアクセス権限を設定する方法については、[ 管理 ](../main-guide/administration.md) を参照してください。

## 属性ベースのアクセス制御

[ 属性ベースのアクセス制御 ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) は、Experience Platform者が属性に基づいて特定のオブジェクトや機能へのアクセスを制御できるようにする管理機能です。 属性は、スキーマフィールドやセグメントに追加されるラベルなど、オブジェクトに追加されるメタデータであることがあります。 管理者は、ユーザーアクセス権限を管理する属性を含めた、アクセスポリシーを定義します。

この機能を使用すると、エクスペリエンスデータモデル（XDM）スキーマフィールドに、組織またはデータの使用範囲を定義するラベルを付けることができます。同時に、管理者は、ユーザーと役割の管理インターフェイスを使用して、XDM スキーマフィールドに対するアクセスポリシーを定義できます。 また、ユーザーまたはユーザーのグループ（内部、外部、またはサードパーティのユーザー）に付与するアクセス権をより適切に管理できます。 また、属性ベースのアクセス制御により、管理者は特定のセグメントへのアクセスを管理できます。

属性ベースのアクセス制御により、管理者は、すべてのプラットフォームワークフローとリソースにわたって、機密性の高い個人データ（SPD）と個人を特定できる情報（PII）の両方へのユーザーのアクセスを制御できます。管理者は、特定のフィールドと、それらのフィールドに対応するデータにのみアクセスできるユーザーの役割を定義できます。

統一データセットのデータセットルールを設定する場合、Experience Platformの [ 属性ベースのアクセス制御 ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview) がフィールドレベルで適用されます。 ラベルがスキーマフィールドに添付されている場合、フィールドは制限されます。 アクティブなポリシーが有効になり、そのフィールドへのアクセスが拒否されます。 その結果、次のようになります。

* データセットルールを作成する際に、制限されているスキーマフィールドが表示されません。
* 自身に対して制限されている 1 つ以上のスキーマフィールドのマッピングを表示または編集できません。 このような制限されたフィールドを含むデータセットルールを編集または表示すると、次の画面が表示されます。
  ![ アクションが許可されていません ](/help/assets//action-not-permitted.png)

