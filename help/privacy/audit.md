---
title: 監査
description: Mix Modelerの監査方法を説明します。
feature: Administration
source-git-commit: 44e37f385241d90da87e1fd85fb4ce9024b67250
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 6%

---

# 監査

>[!AVAILABILITY]
>
>この記事で説明している機能は、リリースの限定的テスト段階にあり、お使いの環境ではまだ使用できない可能性があります。 機能が一般入手可能になったら、このメモは削除されます。 最新のMix Modelerリリースについて詳しくは、を参照してください。 [Mix Modelerリリース](/help/releases/latest.md).

Mix Modelerの監査インターフェイスの一部やExperience PlatformUI に組み込まれている機能を使用して、Mix Modelerでのユーザーの作業状況を監査できます。

監査ログを調べるには、Mix Modelerインターフェイスで次を実行します。

1. を選択 ![タスクリスト](../assets/icons/TaskList.svg) **[!UICONTROL Audits]** から **[!UICONTROL PRIVACY]**.

1. 対象： **[!UICONTROL Audits]** 次を見つけることができます **[!UICONTROL Activity log]**. アクティビティログには、次のMix Modelerカテゴリ、アクション、ステータスのエントリが表示されます。

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

1. アクティビティログでエントリを選択すると、パネルが開いて詳細を確認できます。

   ![Mix Modeler監査](../assets/mix-modeler-audit.png)

1. フィルタリング対象 **[!UICONTROL Category]**, **[!UICONTROL Action]**, **[!UICONTROL Request ID]**, **[!UICONTROL User]**, **[!UICONTROL Status]** または **[!UICONTROL Date]** 範囲、選択 ![フィルター](../assets/icons/Filter.svg).

1. アクティビティ・ログに表示される列を変更するには、 ![列](../assets/icons/ColumnSetting.svg) および **[!UICONTROL Customize table]** ダイアログ表示する列を選択します。 を選択 **[!UICONTROL Apply]** 選択を適用するには、 **[!UICONTROL Cancel]** をクリックして選択をキャンセルします。

1. 監査ログをダウンロードするには、次を選択します ![Download](../assets/icons/Download.svg) **[!UICONTROL Download log]**. が含まれる **[!UICONTROL Download log]** ダイアログ次のいずれかを選択 **[!UICONTROL CSV]** または **[!UICONTROL JSON]** 形式として、を選択します。 **[!UICONTROL Download]**.
