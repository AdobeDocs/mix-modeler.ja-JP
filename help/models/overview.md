---
title: モデルの概要
description: Mix Modelerでモデルを作成して使用する方法を説明します。
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 2775c5a3779f6731f7f3143f6ed21db2993c0955
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

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

モデルを初めて作成すると、トレーニングとスコアリングのプロセスが直ちに開始されます。 最初のトレーニングおよびスコアリング実行が完了すると、モデルインサイトをレビューできます。 その後、モデルを再トレーニングしてもよい。 また、データがモデルに追加される場合もあり、その場合はモデルを手動で再コアする必要があります。 再トレーニングと再スコアリングは、新しい調査結果と情報が出てくると、ビジネス目標に最も適したモデルを取得するために調整が必要になるため、反復的なプロセスになります。


## モデルを作成

モデルを作成するには、「**[!UICONTROL Open model canvas]**」を選択すると使用できる、Mix Modeler ステップバイステップのガイド付きモデル設定フローを使用します。 詳しくは、[&#x200B; モデルの作成 &#x200B;](build.md) を参照してください。

## モデルの管理

Mix Modeler インターフェイスで現在のモデルのテーブルを表示するには、次の手順を実行します。

1. 左パネルから ![FileData](/help/assets/icons2/FileData.svg) **[!UICONTROL Models]** を選択します。

1. 現在のモデルのテーブルが表示されます。

   テーブルの列には、モデルに関する詳細が指定されます。

   | 列名 | 詳細 |
   |---|---|
   | **[!UICONTROL Name]** | モデル名 |
   | **[!UICONTROL Description]** | モデルの説明 |
   | **[!UICONTROL Conversion event]** | モデルに対して選択した変換。 |
   | **[!UICONTROL Run frequency]** | モデルをトレーニングする実行頻度。 |
   | **[!UICONTROL Last run]** | モデルの最後のトレーニングの日時。 |
   | **[!UICONTROL Status]** | モデルのステータス。 |

   任意の列のテーブルを昇順 ![ArrowMoveUp](/help/assets/icons2/ArrowMoveUp.svg) または降順 ![ArrowMoveDown](/help/assets/icons2/ArrowMoveDown.svg) で並べ替えるには、列のタイトルを選択します。

   **[!UICONTROL Name]** 列の並べ替えまたはサイズ変更を行うには、「**[!UICONTROL Name]** 山形 ![&#x200B; 下 &#x200B;](/help/assets/icons/ChevronDown.svg)」を選択します。 コンテキストメニューから「**[!UICONTROL Sort ascending]**」、「**[!UICONTROL Sort descending]**」、または「**[!UICONTROL Resize column]**」を選択します。 または、列区切り記号の上にマウスポインターを置いて、**[!UICONTROL Name]** の列のサイズを変更できます。

   モデルのレポートされたステータスは、モデルがライフサイクル内のどこにあるかによって異なります。 例えば、モデルが作成されたか、正常に（再）トレーニングされたか、正常に（再）スコアリングされたかなどです。

   次の表を参照してください。

   * ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) - モデルのライフサイクルでステップが正常に実行されたことを示します。
   * ![&#x200B; クロック &#x200B;](/help/assets/icons/Clock.svg) - モデルライフサイクルで現在ステップの進行中の実行を示します。
   * ![&#x200B; 閉じる &#x200B;](/help/assets/icons/Close.svg) - モデルのライフサイクルでのステップの実行失敗を示します。

   | ステータス | [&#x200B; ビルド &#x200B;](/help/models/build.md) | [&#x200B; トレイン &#x200B;](/help/models/train-score.md#train) | [スコア](/help/models/train-score.md#score) | [&#x200B; 再トレーニング &#x200B;](/help/models/train-score.md#train) | [Rescore](/help/models/train-score.md#score) |
   |---|:---:|:---:|:---:|:---:|:---:|
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | | | | |
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; 時計 &#x200B;](/help/assets/icons/Clock.svg) | | | |
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; 時計 &#x200B;](/help/assets/icons/Clock.svg) | | |
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; 時計 &#x200B;](/help/assets/icons/Clock.svg) | |
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; 時計 &#x200B;](/help/assets/icons/Clock.svg) |
   | Training failed | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; 閉じる &#x200B;](/help/assets/icons/Close.svg) | | | |
   | Training failed | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; 閉じる &#x200B;](/help/assets/icons/Close.svg) | |
   | Training successful | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | | | |
   | Training successful | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | |
   | スコアリングに失敗しました | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; 閉じる &#x200B;](/help/assets/icons/Close.svg) | | |
   | スコアリングに失敗しました | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; 閉じる &#x200B;](/help/assets/icons/Close.svg) |
   | スコアリングに成功しました | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | | |
   | スコアリングに成功しました | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) |

   {style="table-layout:fixed"}

1. リストに表示される列を変更するには、「![&#x200B; 列設定 &#x200B;](/help/assets/icons/ColumnSetting.svg) を選択し、列のオン ![&#x200B; チェック &#x200B;](/help/assets/icons/Checkmark.svg) とオフを切り替えます。

特定のモデルに対して次のアクションを実行できます。

### モデルインサイト

モデルインサイト機能は、正常にトレーニングされたモデルとスコアリングされたモデルでのみ使用できます。

モデルのインサイトを表示するには：

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデル名を選択します。

[&#x200B; モデルインサイト &#x200B;](insights.md) にリダイレクトされます。


### 詳細を表示

モデルの詳細を表示するには：

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![&#x200B; 情報 &#x200B;](/help/assets/icons/Info.svg) を選択して、詳細を含むポップアップを表示します。


### 複製

モデルをすばやく複製できます。

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![&#x200B; 詳細 &#x200B;](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Duplicate]**] を選択します。

新しいモデルを作成する手順にリダイレクトされ、提案された名前には元のモデルの名前に **[!UICONTROL (Copy)]（_n_）** が追加されます。

### 編集

モデルの名前、説明、およびトレーニングとスコアリングのスケジュールを編集できます。

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![&#x200B; 詳細 &#x200B;](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Edit]**] を選択します。

   **[!UICONTROL Edit model]** ダイアログで、次の手順を実行します。

   * 新しい **[!UICONTROL Name]** と **[!UICONTROL Description]** を入力します。

   * スケジュールを有効にするには、**[!UICONTROL Status]** を有効にします。 トレーニングおよびスコアリングされたモデルのスケジュールのみを有効にできます。

      1. **[!UICONTROL Scoring frequency]** を選択：

         * **[!UICONTROL Daily]**：有効な時間（例：`05:22 pm`）を入力するか、![Clock](/help/assets/icons/Clock.svg) を使用します。
         * **[!UICONTROL Weekly]**：曜日を選択して有効な時間（例：`05:22 pm`）を入力するか、![Clock](/help/assets/icons/Clock.svg) を使用します。
         * **[!UICONTROL Monthly]**: 「実行するタイミング」ドロップダウンメニューから日付を選択し、有効な時刻（例：`05:22 pm`）を入力するか、![&#x200B; 時計 &#x200B;](/help/assets/icons/Clock.svg) を使用します。

      1. ドロップダウンメニューから **[!UICONTROL Training frequency]** （**[!UICONTROL Monthly]**、**[!UICONTROL Quarterly]**、**[!UICONTROL Yearly]**、**[!UICONTROL None]** のいずれか）を選択します。

     ![&#x200B; モデルを編集 &#x200B;](../assets/model-edit.png)

1. **[!UICONTROL Save]** を選択します。



### トレイン

新しい増分マーケティングと要因データを含める場合は、モデルの再トレーニングを検討してください。 詳しくは、[&#x200B; モデルのトレーニングとスコアリング &#x200B;](train-score.md#train) を参照してください。


### スコア

新しいマーケティングデータに基づいてモデルを増分的にスコアリングしたり、特定の日付範囲でモデルを再コア化したりできます。 詳しくは、[&#x200B; モデルのトレーニングとスコアリング &#x200B;](train-score.md#score) を参照してください。


### モデルを削除

モデルを削除するには：

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。
1. モデルの ![&#x200B; 詳細 &#x200B;](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Delete]**] を選択します。 または、青いアクションバーから ![&#x200B; 削除 &#x200B;](/help/assets/icons/Delete.svg)**[!UICONTROL Delete]** を選択します。
1. **[!UICONTROL Delete]** の確認ダイアログで「**[!UICONTROL Delete model]**」を選択して、モデルを削除します。 キャンセルする **[!UICONTROL Cancel]** を選択します。

複数のモデルを削除するには：

1. 複数のモデルを選択します。
1. 青いアクションバーから、「![&#x200B; 削除 &#x200B;](/help/assets/icons/Delete.svg)」 **[!UICONTROL Delete]** 選択してモデルを削除します。
1. **[!UICONTROL Delete]** x **[!UICONTROL Delete *モデル *確認ダイアログで「]**」を選択して、モデルを削除します。 キャンセルする&#x200B;**[!UICONTROL Cancel]**&#x200B;を選択します。

