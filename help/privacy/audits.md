---
title: 監査
description: Mix Modelerから監査にアクセスする方法を説明します。
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: c45f4e4412258f959726c49129c6b9b6fff48f4a
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 6%

---

# 監査

Mix ModelerUI に組み込まれたExperience Platformの一部である監査インターフェイスを使用して、ユーザーがMix Modelerで何をしているかを監査します。

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

