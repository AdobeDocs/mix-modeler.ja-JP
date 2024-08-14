---
title: モデル
description: Mix Modelerでモデルを設定および使用する方法を説明します。
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: d5d9ec6b7b1222b3da9dcecaf3fa1cf2b2198881
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 1%

---

# モデル

Mix Modelerのモデル機能を使用すると、ビジネス目標に固有の AI/ML モデルを設定、トレーニング、スコアリングできます。 トレーニングとスコアリングは、マルチタッチアトリビューションとマーケティングミックスモデリングの間の AI 駆動の転送学習をサポートします。

モデルは、Mix Modelerアプリケーションワークフローの一部として作成する統一データに基づいています。

Mix Modelerのモデルは、マーケターの投資に基づいて指定された成果を測定および/または予測するために使用される機械学習モデルです。 マーケティングタッチポイントおよび概要レベルデータを入力として使用できます。 Mix Modelerを使用すると、売上高、販売数量、リードなど、変数、ディメンション、結果の様々なセットに基づいてモデルのバリアントを作成できます。

モデルには次の要件があります。

* 1 つのコンバージョン。
* 概要レベルデータ、マーケティングタッチポイントデータ（イベントデータ）またはその両方で構成された 1 つ以上のマーケティングタッチポイント（チャネル）です。
* 設定可能なルックバックウィンドウ。
* 設定可能なトレーニングウィンドウ。

モデルには、オプションで次の項目を含めることができます。

* 外部要因。
* 内部要因。
* 過去の関係者エクスペリエンス、増分的テスト、その他のモデルなど、他のソースからのマーケティング投稿に関する予備知識。
* 費用共有：マーケティングデータが疎な場合に、相対的な費用共有をプロキシとして使用します。


## モデルの作成

モデルを作成するには、「**[!UICONTROL Open model canvas]**」を選択すると使用できるMix Modelerステップバイステップのガイド付きモデル設定フローを使用します。 詳しくは、[ モデルの作成 ](create.md) を参照してください。

## モデルの管理

Mix Modelerインターフェイスで現在のモデルのテーブルを表示するには：

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. 現在のモデルのテーブルが表示されます。

   テーブルの列には、モデルに関する詳細が指定されます。

   | 列名 | 詳細 |
   |---|---|
   | 名前 | モデル名 |
   | 説明 | モデルの説明 |
   | コンバージョンイベント | モデルに対して選択した変換。 |
   | 実行頻度 | モデルをトレーニングする実行頻度。 |
   | 前回の実行 | モデルの最後のトレーニングの日時。 |
   | ステータス | モデルのトレーニングの前回の実行ステータス。 <br/>![StatusGreen](/help/assets/icons/StatusGreen.svg)Success<br/>![StatusOrange](/help/assets/icons/StatusOrange.svg) トレーニングの問題 <br/> ![StatusOrange](/help/assets/icons/StatusOrange.svg) トレーニングを待機中 <br/>![StatusRed](/help/assets/icons/StatusRed.svg) 失敗 <br/>![StatusGreen](/help/assets/icons/StatusGray.svg)_（前回の実行が処理中） |

   {style="table-layout:auto"}

1. リストに表示される列を変更するには、「![ 列設定 ](/help/assets//icons/ColumnSetting.svg) を選択し、列のオン ![ チェック ](/help/assets//icons/Checkmark.svg) とオフを切り替えます。

特定のモデルに対して次のアクションを実行できます。

### 詳細を表示

モデルの詳細を表示するには：

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 情報 ](/help/assets//icons/Info.svg) を選択して、詳細を含むポップアップを表示します。



### 複製

モデルをすばやく複製できます。

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Duplicate]**] を選択します。


### モデルインサイト

モデルインサイト機能は、正常にトレーニングされたモデルとスコアリングされたモデルでのみ使用できます。 モデルのインサイトを表示するには：

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデル名を選択します。

[ モデルインサイト ](insights.md) にリダイレクトされます。


### 再トレーニング

モデルの再トレーニングは、正常にトレーニングされたモデルでのみ使用できます。 モデルを再トレーニングするには：

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Train]**] を選択します。 または、青いアクションバーから ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** を選択します。

   **[!UICONTROL Train model]** ダイアログで、次の操作を実行するオプションを選択します。

   * **[!UICONTROL Train model with last 2 years of marketing data]**、または
   * **[!UICONTROL Train model using specific date range of data]**。
日付範囲を指定します。 ![ カレンダー ](/help/assets/icons/Calendar.svg) を使用して、日付範囲を選択できます。 最低 1 年のデータ範囲を選択する必要があります。

   ![ モデルの再トレーニング ](../assets/re-train-model.png)

1. **[!UICONTROL Train]** を選択してモデルを再トレーニングします。


### スコアまたは再スコア


新しいマーケティングデータに基づいてモデルに増分的にスコアを付けたり、特定の日付範囲でモデルを再スコア化したりできます。 モデルにスコアを付ける、または再スコアを付ける手順は、次のとおりです。

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Score]**] を選択します。 または、青いアクションバーから ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** を選択します。

   **[!UICONTROL Score marketing data]** ダイアログで、次の操作を実行するオプションを選択します。

   * **[!UICONTROL Score new marketing data from *mm/dd/yyyy *]**：新しいマーケティングデータを使用してモデルに増分的にスコアを付ける
   * 特定の日付範囲に対して再スコア化する **[!UICONTROL Score specific date range of marketing data]** 要があります。
日付範囲を指定します。 ![ カレンダー ](/help/assets/icons/Calendar.svg) を使用して、日付範囲を選択できます。

   ![ モデルの再トレーニング ](../assets/re-score-model.png)

1. 「**[!UICONTROL Score]**」を選択します。 特定のデータ範囲を使用してモデルを再スコアリングすると、**[!UICONTROL Existing model is replaced]** のダイアログが表示され、選択した日付範囲の新しいスコアでモデルを置き換えるかどうかを確認するように求められます。 「**[!UICONTROL Replace model]**」を選択して確定します。


### モデルの削除

モデルを削除するには：

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Delete]**] を選択します。 または、青いアクションバーから ![ 削除 ](/help/assets/icons/Delete.svg)**[!UICONTROL Delete]** を選択します。

複数のモデルを削除するには：

1. 複数のモデルを選択します。

1. 青いアクションバーから、「![ 削除 ](/help/assets/icons/Delete.svg)」 **[!UICONTROL Delete]** 選択してモデルを削除します。

   >[!WARNING]
   >
   >モデルはすぐに削除されます。


