---
title: モデルの概要
description: Mix Modelerでモデルを作成して使用する方法を説明します。
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 39ea5ed145678d6ac7e5263b38255e725e488f8d
workflow-type: tm+mt
source-wordcount: '1090'
ht-degree: 1%

---

# モデルの概要

Mix Modelerのモデル機能を使用すると、ビジネス目標に固有のモデルを設定、トレーニング、スコアリングできます。 トレーニングとスコアリングは、マルチタッチアトリビューションとマーケティングミックスモデリングの間の AI 駆動の転送学習をサポートします。

モデルは、Mix Modeler アプリケーションワークフローの一部として作成する統一データに基づいています。

Mix Modelerのモデルは、マーケターの投資に基づいて指定された成果を測定し、予測するために使用される機械学習モデルです。 マーケティングタッチポイントおよび概要レベルデータを入力として使用できます。 Mix Modelerでは、売上高、販売数量、リードなど、変数、ディメンション、結果の様々なセットに基づいてモデルのバリアントを作成できます。

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


## モデルを作成

モデルを作成するには、「**[!UICONTROL Open model canvas]**」を選択すると使用できる、Mix Modeler ステップバイステップのガイド付きモデル設定フローを使用します。 詳しくは、[ モデルの作成 ](build.md) を参照してください。

## モデルの管理

Mix Modeler インターフェイスで現在のモデルのテーブルを表示するには、次の手順を実行します。

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. 現在のモデルのテーブルが表示されます。

   テーブルの列には、モデルに関する詳細が指定されます。

   | 列名 | 詳細 |
   |---|---|
   | 名前 | モデル名 |
   | 説明 | モデルの説明 |
   | コンバージョンイベント | モデルに対して選択した変換。 |
   | 実行頻度 | モデルをトレーニングする実行頻度。 |
   | 前回の実行 | モデルの最後のトレーニングの日時。 |
   | ステータス | モデルのステータス。 |

   {style="table-layout:auto"}

   モデルのレポートされたステータスは、モデルがライフサイクル内のどこにあるかによって異なります。 例えば、モデルが作成されたか、正常に（再）トレーニングされたか、正常に（再）スコアリングされたかなどです。

   次の表を参照してください。

   * ![ チェックマーク ](/help/assets/icons/Checkmark.svg) - モデルのライフサイクルでステップが正常に実行されたことを示します。
   * ![ クロック ](/help/assets/icons/Clock.svg) - モデルライフサイクルで現在ステップの進行中の実行を示します。
   * ![ 閉じる ](/help/assets/icons/Close.svg) - モデルのライフサイクルでのステップの実行失敗を示します。

   | ステータス |  の作成 | トレイン | スコア | 再トレーニング | 再スコア |
   |---|:---:|:---:|:---:|:---:|:---:|
   | 処理中 | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | | | | |
   | 処理中 | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ 時計 ](/help/assets/icons/Clock.svg) | | | |
   | 処理中 | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ 時計 ](/help/assets/icons/Clock.svg) | | |
   | 処理中 | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ 時計 ](/help/assets/icons/Clock.svg) | |
   | 処理中 | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ 時計 ](/help/assets/icons/Clock.svg) |
   | Training failed | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ 閉じる ](/help/assets/icons/Close.svg) | | | |
   | Training failed | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ 閉じる ](/help/assets/icons/Close.svg) | |
   | Training successful | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | | | |
   | Training successful | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | |
   | スコアリングに失敗しました | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ 閉じる ](/help/assets/icons/Close.svg) | | |
   | スコアリングに失敗しました | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ 閉じる ](/help/assets/icons/Close.svg) |
   | スコアリングに成功しました | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | | |
   | スコアリングに成功しました | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) |

1. リストに表示される列を変更するには、「![ 列設定 ](/help/assets/icons/ColumnSetting.svg) を選択し、列のオン ![ チェック ](/help/assets/icons/Checkmark.svg) とオフを切り替えます。

特定のモデルに対して次のアクションを実行できます。

### モデルインサイト

モデルインサイト機能は、正常にトレーニングされたモデルとスコアリングされたモデルでのみ使用できます。

モデルのインサイトを表示するには：

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデル名を選択します。

[ モデルインサイト ](insights.md) にリダイレクトされます。


### 詳細を表示

モデルの詳細を表示するには：

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 情報 ](/help/assets/icons/Info.svg) を選択して、詳細を含むポップアップを表示します。


### 複製

モデルをすばやく複製できます。

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Duplicate]**] を選択します。

新しいモデルを作成する手順にリダイレクトされ、提案された名前には元のモデルの名前に **[!UICONTROL (Copy)]（_n_）** が追加されます。

### 編集

モデルの名前、説明、およびトレーニングとスコアリングのスケジュールを編集できます。

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Edit]**] を選択します。

   **[!UICONTROL Edit model]** ダイアログで、次の手順を実行します。

   * 新しい **[!UICONTROL Name]** と **[!UICONTROL Description]** を入力します。

   * スケジュールを有効にするには、**[!UICONTROL Status]** を有効にします。 トレーニングおよびスコアリングされたモデルのスケジュールのみを有効にできます。

      1. **[!UICONTROL Scoring frequency]** を選択：

         * **[!UICONTROL Daily]**：有効な時間（例：`05:22 pm`）を入力するか、![Clock](/help/assets/icons/Clock.svg) を使用します。
         * **[!UICONTROL Weekly]**：曜日を選択して有効な時間（例：`05:22 pm`）を入力するか、![Clock](/help/assets/icons/Clock.svg) を使用します。
         * **[!UICONTROL Monthly]**: 「実行するタイミング」ドロップダウンメニューから日付を選択し、有効な時刻（例：`05:22 pm`）を入力するか、![ 時計 ](/help/assets/icons/Clock.svg) を使用します。

      1. ドロップダウンメニューから **[!UICONTROL Training frequency]** （**[!UICONTROL Monthly]**、**[!UICONTROL Quarterly]**、**[!UICONTROL Yearly]**、**[!UICONTROL None]** のいずれか）を選択します。

     ![ モデルを編集 ](../assets/model-edit.png)

1. **[!UICONTROL Save]** を選択します。



### 再トレーニング


モデルの再トレーニングは、正常にトレーニングされたモデルでのみ使用できます。

次のような場合に、モデルの再トレーニングを検討します。

* 新しい増分マーケティングおよび要因データを含めます。 例えば、前四半期の市場力学が変更されたり、マーケティングデータ配分が大幅に変更されたりしたとします。

モデルを再トレーニングするには：

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Train]**] を選択します。 または、青いアクションバーから ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** を選択します。

   **[!UICONTROL Train model]** ダイアログで、次の操作を実行するオプションを選択します。

   * **[!UICONTROL Train model with last 2 years of marketing data]**、または
   * **[!UICONTROL Train model using specific date range of data]**。
日付範囲を指定します。 ![ カレンダー ](/help/assets/icons/Calendar.svg) を使用して、日付範囲を選択できます。 最低 1 年のデータ範囲を選択する必要があります。

   ![ モデルの再トレーニング ](../assets/re-train-model.png)

1. **[!UICONTROL Train]** を選択してモデルを再トレーニングします。


### スコアまたは再スコア


新しいマーケティングデータに基づいてモデルに増分的にスコアを付けたり、特定の日付範囲でモデルを再スコア化したりできます。

以下が必要な場合は、モデルのスコアを変更することを検討します。

* 間違ったマーケティングデータを修正します。 例えば、モデルのトレーニングとスコアリングに含めた最近の有料検索データが、1 週間のデータを見逃したとします。
* 調和されたデータの一部として設定したデータセットの更新によって利用可能になった新しい増分マーケティングデータを使用します。

モデルにスコアを付ける、または再スコアを付ける手順は、次のとおりです。

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Score]**] を選択します。 または、青いアクションバーから ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** を選択します。

   **[!UICONTROL Score marketing data]** ダイアログで、次の操作を実行するオプションを選択します。

   * **[!UICONTROL Score new marketing data from *mm/dd/yyyy *]**：新しいマーケティングデータを使用してモデルに増分的にスコアを付ける
   * 特定の日付範囲に対して再スコア化する **[!UICONTROL Score specific date range of marketing data]** 要があります。
日付範囲を指定します。 ![ カレンダー ](/help/assets/icons/Calendar.svg) を使用して、日付範囲を選択できます。

   ![ モデルの再トレーニング ](../assets/re-score-model.png)

1. 「**[!UICONTROL Score]**」を選択します。 特定のデータ範囲を使用してモデルを再スコアリングすると、**[!UICONTROL Existing model is replaced]** のダイアログが表示され、選択した日付範囲の新しいスコアでモデルを置き換えるかどうかを確認するように求められます。 「**[!UICONTROL Replace model]**」を選択して確定します。


### モデルを削除

モデルを削除するには：

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。
1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Delete]**] を選択します。 または、青いアクションバーから ![ 削除 ](/help/assets/icons/Delete.svg)**[!UICONTROL Delete]** を選択します。
1. **[!UICONTROL Delete model]** の確認ダイアログで「**[!UICONTROL Delete]**」を選択して、モデルを削除します。 キャンセルする **[!UICONTROL Cancel]** を選択します。

複数のモデルを削除するには：

1. 複数のモデルを選択します。
1. 青いアクションバーから、「![ 削除 ](/help/assets/icons/Delete.svg)」 **[!UICONTROL Delete]** 選択してモデルを削除します。
1. **[!UICONTROL Delete *x *モデル]**確認ダイアログで「**[!UICONTROL Delete]**」を選択して、モデルを削除します。 キャンセルする&#x200B;**[!UICONTROL Cancel]**を選択します。

