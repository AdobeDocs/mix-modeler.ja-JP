---
title: ポリシー
description: Mix Modelerからポリシーにアクセスする方法を説明します。
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
TQID: https://experienceleague.adobe.com/fk6qAZS7Uymx2dzptcazBieXIJ3mGF2pjG-EDhm-Kh4
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: f6633d1c-3d2d-4f48-95d4-4bbc9913db52
subfeature_v2:
  - id: fd80ec6b-9b9e-448a-a6d0-b0c9a15da6b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: '2026-05-01T09:17:02.907Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 507
ht-degree: 9%

---

# ポリシー

ワークフローを実行してモデルを作成し、モデルの設定を送信すると、[&#x200B; ポリシーの適用](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement)が違反がないか確認します。 ポリシー違反が発生した場合は、1 つ以上のポリシーに違反したことを示すポップオーバーが表示されます。 このチェックは、Experience Platform内のデータ運用とマーケティングアクションがデータ使用ポリシーに準拠していることを確認するためのものです。

デフォルトでは、Mix Modelerは、次のラベルとマーケティングアクションに関連付けられたAdobe定義ポリシーの違反をチェックします。

| ポリシー名 | 関連ラベル | 関連するマーケティングアクション |
|---|---|---|
| 利用状況分析とユーザーベースの測定を制限 | C8 | Analytics |
| データサイエンス制限 | C9 | データサイエンス |
| データ書き出し制限 | C12 | データの書き出し |

違反は、自分で定義したポリシーについてもチェックされます。このポリシーには、上記の表に記載されているマーケティングアクションが含まれています。

データセットルールの構築中にポリシーに違反すると、ポリシー違反に関する情報を表示するポップオーバーが表示されます。

例：

- 関連するラベル [!UICONTROL C9]と関連するマーケティングアクション [!UICONTROL Data Science]で[!UICONTROL Restrict data science] ポリシーを有効にしました。
- コンバージョンデータスキーマの`totalCost` フィールドに[!UICONTROL C9] - [!UICONTROL No data science] ラベルを適用しました。
- コンバージョンデータスキーマの`totalCost` フィールドを、名前`spend` （および表示名`Spend`）の調和フィールドにマッピングするデータセットルールを設定します。

データセットルールを保存すると、**[!UICONTROL Data governance policy violation detected]** ポップアップが表示され、違反したポリシーのリストが表示されます。 ポリシー名を選択すると、[!UICONTROL Violation summary]に、[!UICONTROL Entity]、[!UICONTROL Type]、[!UICONTROL Field]および[!UICONTROL Government labels]が適用された[!UICONTROL Active data governance labels]のリストが表示されます。

<!-- pending screenshot -->

既に調和データで使用されているスキーマフィールドにデータ使用ラベルを適用すると、ポリシー違反に関する情報を表示するポップオーバーが表示されます。

例：

- コンバージョンデータスキーマの`totalCost` フィールドを、名前`spend` （および表示名`Spend`）の調和フィールドにマッピングするデータセットルールを設定しました。
- 調整されたデータを少なくとも1回は正常に同期しました（[&#x200B; データセットルール – データの同期](/help/harmonize-data/dataset-rules.md#sync-data)を参照）。
- 関連するラベル [!UICONTROL C9]と関連するマーケティングアクション [!UICONTROL Data Science]で[!UICONTROL Restrict data science] ポリシーを有効にします。
- コンバージョンデータスキーマの`totalCost` フィールドに[!UICONTROL C9] - [!UICONTROL No data science] ラベルを適用します。

スキーマの更新を保存すると、**[!UICONTROL Data governance policy violation detected]** ポップアップが表示され、違反したポリシーのリストが表示されます。 [!UICONTROL Violation summary]でポリシー名を選択して、[!UICONTROL Data Lineage] リストの詳細を確認します。

<!-- pending screenshot -->

## 違反が検出されたポップオーバー

検出されたデータガバナンスポリシー違反ポップオーバーは、違反に関する具体的な情報を提供します。 これらの違反は、設定ワークフローに直接関係しないポリシー設定やその他の測定を通じて解決できます。 例えば、特定のフィールドをデータサイエンス目的で使用できるように、ラベルを変更できます。 または、モデル設定そのものを変更して、モデルがデータ使用ラベル付きのオブジェクトを使用しないようにすることもできます。

左側のパネルの![&#x200B; プライバシー](/help/assets/icons/Privacy.svg) **[!UICONTROL Policies]**&#x200B;の選択範囲では、Experience Platformの[!UICONTROL Policies] インターフェイスにアクセスし、ポリシー、ラベル、マーケティングアクションを管理できます。

<!--
Currently,  Mix Modeler does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[&#x200B; データ使用ポリシーの概要](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/policies/overview)
>
>

