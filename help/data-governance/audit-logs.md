---
title: 監査ログ
description: Mix Modelerから監査ログにアクセスする方法を説明します。
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: 77a338ae568c854b99069b849a18661d413c501c
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 12%

---

# 監査ログ

システムで実行されるアクティビティの透明性と可視性を高めるために、Mix Modelerワークフロー内のユーザーアクティビティがExperience Platform監査ログに取り込まれ、Mix Modelerカテゴリに対するユーザー主導の変更を理解します。 これらのログは、問題のトラブルシューティングに役立つ監査証跡を形成し、企業のデータ管理ポリシーおよび規制要件に効果的に準拠するのに役立ちます。

<!-- DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

監査ログは、誰がどのアクションを、いつ実行したかを通知します。 ログに記録される各アクションには、アクションのタイプ、日時、アクションを実行したユーザーの電子メール ID、アクションのタイプに関連する追加の属性を示すメタデータが含まれます。これにより、Mix Modeler内のユーザーが実行した作成、更新、削除アクションをトラッキングします。

監査ログを調べるには、Mix Modelerインターフェイスで次を実行します。

1. **[!UICONTROL PRIVACY]** から ![ タスクリスト ](/help/assets/icons/TaskList.svg)**[!UICONTROL Audits]** を選択します。

1. **[!UICONTROL Audits]** では、**[!UICONTROL Activity log]** を見つけることができます。 アクティビティログには、次のMix Modelerカテゴリ、アクション、およびステータスのエントリが表示されます。

   | カテゴリ | アクション | ステータス |
   |---|---|---|
   | Mix Modelerデータセットルール |  の作成 | 許可または拒否 |
   | Mix Modelerデータセットルール | 更新 | 許可または拒否 |
   | Mix Modelerデータセットルール | 削除 | 許可または拒否 |
   | Mix Modelerフィールド |  の作成 | 許可または拒否 |
   | Mix Modelerフィールド | 更新 | 許可または拒否 |
   | Mix Modelerフィールド | 削除 | 許可または拒否 |
   | Mix Modelerマーケティングタッチポイント |  の作成 | 許可または拒否 |
   | Mix Modelerマーケティングタッチポイント | 更新 | 許可または拒否 |
   | Mix Modelerマーケティングタッチポイント | 削除 | 許可または拒否 |
   | Mix Modeler変換 |  の作成 | 許可または拒否 |
   | Mix Modeler変換 | 更新 | 許可または拒否 |
   | Mix Modeler変換 | 削除 | 許可または拒否 |
   | Mix Modelerモデル |  の作成 | 許可または拒否 |
   | Mix Modelerモデル | 更新 | 許可または拒否 |
   | Mix Modelerモデル | 削除 | 許可または拒否 |
   | Mix Modelerモデル | 再スコア | 許可または拒否 |
   | Mix Modelerモデル | クローン | 許可または拒否 |
   | Mix Modelerモデル | トレーニング/再トレーニング | 許可または拒否 |
   | Mix Modelerモデル | メタデータのダウンロード/保存 | 許可または拒否 |
   | Mix Modelerプラン |  の作成 | 許可または拒否 |
   | Mix Modelerプラン | 更新 | 許可または拒否 |
   | Mix Modelerプラン | 関連モデルを変更 | 許可または拒否 |
   | Mix Modelerデータの調和 | トリガー同期 | 許可または拒否 |


1. アクティビティログでエントリを選択すると、パネルが開いて詳細を確認できます。

   ![Mix Modeler監査 ](/help/assets/mix-modeler-audit.png)

1. **[!UICONTROL Category]**、**[!UICONTROL Action]**、**[!UICONTROL Request ID]**、**[!UICONTROL User]**、**[!UICONTROL Status]** または **[!UICONTROL Date]** の範囲に対してフィルターを適用するには、「![ フィルター ](/help/assets/icons/Filter.svg)」を選択します。

1. アクティビティログに表示されている列を変更するには、「![ 列 ](/help/assets/icons/ColumnSetting.svg)」を選択し、**[!UICONTROL Customize table]** ダイアログで表示する列を選択します。 **[!UICONTROL Apply]** を選択して選択を適用するか、**[!UICONTROL Cancel]** を選択して選択をキャンセルします。

1. 監査ログをダウンロードするには、「![ ダウンロード ](/help/assets/icons/Download.svg)」 **[!UICONTROL Download log]** を選択します。 **[!UICONTROL Download log]** ダイアログで、形式として **[!UICONTROL CSV]** または **[!UICONTROL JSON]** を選択し、「**[!UICONTROL Download]**」を選択します。

## 監査ログへのアクセス

組織に対してこの機能が有効になっている場合、アクティビティが発生すると監査ログが自動的に収集されます。 監査ログの収集を手動で有効にする必要はありません。

監査ログを表示および書き出すには、監査ログのアクセスアクセス制御権限を付与されている必要があります。 Mix Modeler機能の個々の権限を管理する方法については、[ アクセス制御ドキュメント ](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/home) を参照してください。
