---
title: ポリシー
description: Mix Modelerからポリシーにアクセスする方法を説明します。
feature: Administration
exl-id: 4dba7c30-ad1e-4213-a2b0-afc55f2448a3
source-git-commit: 132dc18b84723358a7d65e2aaadd49cf1deb2dd8
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 11%

---

# ポリシー

ワークフローを実行してモデルを作成しモデルの設定を送信したら、違反がないかどうかを [&#x200B; ポリシーの適用 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/enforcement/overview#automatic-enforcement) が確認します。 ポリシー違反が発生した場合は、1 つ以上のポリシーに違反したことを示すポップオーバーが表示されます。 このチェックは、Experience Platform内のデータ操作とマーケティングアクションがデータ使用ポリシーに準拠していることを確認するためです。

デフォルトでは、Mix Modelerは次のラベルとマーケティングアクションに関連付けられたAdobe定義ポリシーの違反をチェックします。

| ポリシー名 | 関連するラベル | 関連するマーケティングアクション |
|---|---|---|
| 使用分析とユーザーベースの測定を制限 | C8 | Analytics |
| データサイエンスの制限 | C9 | データサイエンス |
| データの書き出しを制限 | C12 | データの書き出し |

また、自分自身で定義したポリシーや、上の表に示したマーケティングアクションを含むポリシーについても、違反がチェックされます。

データセットルールの構築中にポリシーに違反すると、ポリシー違反に関する情報を表示するポップオーバーが表示されます。

例：

- 関連するラベル [!UICONTROL C9] と関連するマーケティングアクション [!UICONTROL Data Science] に対して [!UICONTROL Restrict data science] ポリシーを有効にしました。
- [!UICONTROL C9] - [!UICONTROL No data science] ラベルをコンバージョンデータスキーマの `totalCost` フィールドに適用しました。
- コンバージョンデータスキーマの `totalCost` フィールドを、名前 `spend` （および表示名 `Spend`）の統一フィールドにマッピングするデータセットルールを設定します。

データセットルールを保存する場合は、違反したポリシーのリストを表示する **[!UICONTROL Data governance policy violation detected]** のポップアップが表示されます。 ポリシー名を選択すると、[!UICONTROL Violation summary] に [!UICONTROL Entity]、[!UICONTROL Type]、[!UICONTROL Field] および [!UICONTROL Government labels] を含む [!UICONTROL Active data governance labels] のリストが表示されます。

<!-- pending screenshot -->

統一されたデータで既に使用されているスキーマフィールドにデータ使用ラベルを適用すると、ポリシー違反に関する情報を表示するポップオーバーが表示されます。

例：

- コンバージョンデータスキーマの `totalCost` フィールドを、名前 `spend` （および表示名 `Spend`）の統一フィールドにマッピングするデータセットルールを設定しました。
- 統一されたデータを少なくとも 1 回正常に同期しました（[&#x200B; データセットルール – データの同期 &#x200B;](/help/harmonize-data/dataset-rules.md#sync-data) を参照）。
- [!UICONTROL Restrict data science] ポリシーは、関連するラベル [!UICONTROL C9] および関連するマーケティングアクション [!UICONTROL Data Science] に対して有効にします。
- [!UICONTROL C9] - [!UICONTROL No data science] ラベルをコンバージョンデータスキーマの `totalCost` フィールドに適用します。

スキーマの更新を保存する際に、違反したポリシーのリストを表示する **[!UICONTROL Data governance policy violation detected]** ポップアップが表示されます。 [!UICONTROL Violation summary] でポリシー名を選択すると、[!UICONTROL Data Lineage] のリストの詳細が表示されます。

<!-- pending screenshot -->

## 違反がポップオーバーを検出しました

検出されたデータガバナンスポリシー違反ポップオーバーは、違反に関する特定の情報を提供します。 これらの違反は、設定ワークフローに直接関係しないポリシー設定やその他の測定を通じて解決できます。 例えば、特定のフィールドをデータサイエンスの目的で使用できるようにラベルを変更できます。 または、モデル設定そのものを変更して、データ使用ラベルを持つオブジェクトをモデルが使用しないようにすることもできます。

左側のパネルの「![&#x200B; プライバシー &#x200B;](/help/assets/icons/Privacy.svg)」 **[!UICONTROL Policies]** 選択を使用すると、Experience Platformの [!UICONTROL Policies] インターフェイスにアクセスでき、ポリシー、ラベル、マーケティングアクションを管理できます。

<!--
Currently,  Mix Modeler does not support all of the data governance functionality offered by Experience Platform. Field level access control is supported. See [Field level access control](../harmonize-data/dataset-rules.md#field-level-access-control)
-->

>[!MORELIKETHIS]
>
>[データ使用ポリシーの概要](https://experienceleague.adobe.com/ja/docs/experience-platform/data-governance/policies/overview)
>
>

