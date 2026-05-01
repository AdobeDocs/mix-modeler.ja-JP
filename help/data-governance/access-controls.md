---
title: アクセス制御
description: Mix Modelerでアクセス制御を設定する方法について説明します。
feature: Administration
exl-id: c9ec97d9-b9a2-41f5-8626-1cf967d5d7fe
TQID: https://experienceleague.adobe.com/EoiF5ui2Bqq0Oxuv-s5E5pQclj9gnjoKgZ1bOzRK-vY
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2: id: abe9e290-7d2f-4131-b71e-ef9900865044
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
autotag-review: '2026-05-01T09:20:37.287Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 25%

---

# アクセス制御

Mix Modelerのアクセス制御は、[Adobe Admin Console](https://adminconsole.adobe.com/)のExperience PlatformおよびExperience Platformの[権限](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home#platform-permissions)を通じて提供されます。 この機能は、権限とサンドボックスをユーザーにリンクさせるAdmin Consoleの製品プロファイルを活用します。

アクセス制御について詳しくは、[ アクセス制御の概要](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/home)を参照してください。

## 役割ベースのアクセス制御

Experience PlatformでMix Modeler ユーザーとユーザーグループに対するロールベースのアクセス権限を設定する方法については、[管理](../main-guide/administration.md)を参照してください。

## 属性ベースのアクセス制御

[属性ベースのアクセス制御](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview)は、管理者が属性に基づいて特定のオブジェクトや機能へのアクセスを制御できるようにするExperience Platformの機能です。 属性は、スキーマフィールドやセグメントに追加されるラベルなど、オブジェクトに追加されるメタデータであることがあります。 管理者は、ユーザーアクセス権限を管理する属性を含めた、アクセスポリシーを定義します。

この機能を使用すると、エクスペリエンスデータモデル（XDM）スキーマフィールドに、組織またはデータの使用範囲を定義するラベルを付けることができます。 また、管理者は、ユーザーと役割の管理インターフェイスを使用して、XDM スキーマフィールドに対するアクセスポリシーを定義できます。 ユーザーまたはユーザーグループ（内部、外部、またはサードパーティユーザー）に与えられるアクセスをより適切に管理します。 また、属性ベースのアクセス制御により、管理者は特定のセグメントへのアクセスを管理できます。

管理者は、属性ベースのアクセス制御を通じて、Adobe Experience Platformのあらゆるワークフローとリソースをまたいで、機密性の高い個人データ（SPD）と個人を特定できる情報（PII）の両方へのユーザーのアクセスを制御できます。 管理者は、特定のフィールドと、それらのフィールドに対応するデータにのみアクセスできるユーザーの役割を定義できます。

統一されたデータセットのデータセットルールを設定する場合、Experience Platformの[属性ベースのアクセス制御](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/overview)はフィールドレベルで適用されます。 ラベルがスキーマフィールドに添付されている場合、フィールドは制限されます。 そのフィールドへのアクセスを拒否するアクティブなポリシーが有効になっています。 これにより、

* データセットルールの作成時に制限されているスキーマフィールドが表示されません，
* 自分に制限されている1つ以上のスキーマフィールドのマッピングを表示または編集できません。 このような制限付きフィールドを含むデータセットルールを編集または表示すると、次の画面が表示されます。
  ![ アクションは許可されていません](/help/assets/action-not-permitted.png)
