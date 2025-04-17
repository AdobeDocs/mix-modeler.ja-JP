---
title: 監査ログ
description: Mix Modelerから監査ログにアクセスする方法を説明します。
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 85f9b42a775006cd3566447b2bb9d0a806fa3e73
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 12%

---

# 監査ログ

システムで実行されるアクティビティの透明性と可視性を高めるために、Mix Modeler ワークフロー内のユーザーアクティビティはExperience Platform監査ログに取り込まれ、Mix Modeler カテゴリに対するユーザー主導の変更を理解します。 これらのログは、問題のトラブルシューティングに役立つ監査証跡を形成し、企業のデータ管理ポリシーおよび規制要件に効果的に準拠するのに役立ちます。

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

監査ログは、誰がどのアクションを、いつ実行したかを通知します。 ログに記録される各アクションには、アクションのタイプ、日時、アクションを実行したユーザーの電子メール ID、アクションのタイプに関連する追加の属性を示すメタデータが含まれます。これにより、Mix Modelerでユーザーが実行した作成、更新、削除アクションをトラッキングします。

Mix Modeler インターフェイスで監査ログを調べるには、次の手順を実行します。

1. **[!UICONTROL PRIVACY]** から ![ タスクリスト ](/help/assets/icons/TaskList.svg)**[!UICONTROL Audits]** を選択します。

1. **[!UICONTROL Audits]** では、**[!UICONTROL Activity log]** を見つけることができます。 アクティビティログには、次のMix Modeler カテゴリ、アクション、ステータスのエントリが表示されます。

   | カテゴリ | アクション | ステータス |
   |---|---|---|
   | Mix Modeler データセットルール |  の作成 | 許可または拒否 |
   | Mix Modeler データセットルール | 更新 | 許可または拒否 |
   | Mix Modeler データセットルール | 削除 | 許可または拒否 |
   | Mix Modeler フィールド |  の作成 | 許可または拒否 |
   | Mix Modeler フィールド | 更新 | 許可または拒否 |
   | Mix Modeler フィールド | 削除 | 許可または拒否 |
   | Mix Modeler マーケティングタッチポイント |  の作成 | 許可または拒否 |
   | Mix Modeler マーケティングタッチポイント | 更新 | 許可または拒否 |
   | Mix Modeler マーケティングタッチポイント | 削除 | 許可または拒否 |
   | Mix Modeler変換 |  の作成 | 許可または拒否 |
   | Mix Modeler変換 | 更新 | 許可または拒否 |
   | Mix Modeler変換 | 削除 | 許可または拒否 |
   | Mix Modeler モデル |  の作成 | 許可または拒否 |
   | Mix Modeler モデル | 更新 | 許可または拒否 |
   | Mix Modeler モデル | 削除 | 許可または拒否 |
   | Mix Modeler モデル | Rescore | 許可または拒否 |
   | Mix Modeler モデル | クローン | 許可または拒否 |
   | Mix Modeler モデル | トレーニング/再トレーニング | 許可または拒否 |
   | Mix Modeler モデル | メタデータのダウンロード/保存 | 許可または拒否 |
   | Mix Modelerプラン |  の作成 | 許可または拒否 |
   | Mix Modelerプラン | 更新 | 許可または拒否 |
   | Mix Modelerプラン | 関連モデルを変更 | 許可または拒否 |
   | Mix Modeler Data Harmonization | トリガー同期 | 許可または拒否 |


1. アクティビティログでエントリを選択すると、パネルが開いて詳細を確認できます。

   ![Mix Modeler監査 ](/help/assets/mix-modeler-audit.png)

1. **[!UICONTROL Category]**、**[!UICONTROL Action]**、**[!UICONTROL Request ID]**、**[!UICONTROL User]**、**[!UICONTROL Status]** または **[!UICONTROL Date]** の範囲に対してフィルターを適用するには、「![ フィルター ](/help/assets/icons/Filter.svg)」を選択します。

1. アクティビティログに表示されている列を変更するには、「![ 列 ](/help/assets/icons/ColumnSetting.svg)」を選択し、**[!UICONTROL Customize table]** ダイアログで表示する列を選択します。 **[!UICONTROL Apply]** を選択して選択を適用するか、**[!UICONTROL Cancel]** を選択して選択をキャンセルします。

1. 監査ログをダウンロードするには、「![ ダウンロード ](/help/assets/icons/Download.svg)」 **[!UICONTROL Download log]** を選択します。 **[!UICONTROL Download log]** ダイアログで、形式として **[!UICONTROL CSV]** または **[!UICONTROL JSON]** を選択し、「**[!UICONTROL Download]**」を選択します。

## 監査ログへのアクセス

組織に対してこの機能が有効になっている場合、アクティビティが発生すると監査ログが自動的に収集されます。 監査ログの収集を手動で有効にする必要はありません。

監査ログを表示および書き出すには、監査ログのアクセスアクセス制御権限を付与されている必要があります。 Mix Modeler機能の個々の権限を管理する方法については、[ アクセス制御ドキュメント ](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/home) を参照してください。
