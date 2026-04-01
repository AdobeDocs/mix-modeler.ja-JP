---
title: モデルの概要
description: Mix Modelerでマシンラーニングモデルを構築、トレーニング、スコアリング、管理し、マーケティング成果を測定、予測する方法を紹介します。
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 7836e378a0f9068fc868dcede0ab8b3e2803776a
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 0%

---

# モデルの概要

Mix Modelerのモデル機能を使用すると、ビジネス目標に合わせてモデルを設定、トレーニング、スコアリングできます。 トレーニングとスコアリングは、マルチタッチアトリビューションとマーケティングミックスモデリング間の、AIを活用した転送学習をサポートします。

モデルは、アプリケーションワークフローの一部として作成した調整済みデータに基づいています。

Mix Modelerのモデルは、マーケターの投資にもとづいて、特定の結果を測定および予測するために使用されるマシンラーニングモデルです。 マーケティングのタッチポイントや概要レベルのデータを入力として利用できます。 Mix Modelerを活用すれば、様々な変数、ディメンション、結果（収益、販売個数、リードなど）のセットにもとづいてモデルのバリエーションを作成できます。

モデルには次のものが必要です。

* コンバージョンをひとつ。
* サマリーレベルのデータ、マーケティング顧客接点データ（イベントデータ）またはその両方で構成される1つ以上のマーケティング顧客接点（チャネル）。
* 設定可能なルックバックウィンドウ。
* 設定可能なトレーニングウィンドウ。

モデルには、オプションで次の項目を含めることができます。

* 外部要因：
* 内部要因：
* 過去のステークホルダーの経験、段階的テスト、その他のモデルなど、他のソースからのマーケティング貢献度に関する事前知識。
* 支出分担：マーケティングデータがスパースの場合、相対的な支出分担をプロキシとして使用します

モデルが最初に作成されると、すぐにトレーニングとスコアリングのプロセスが開始されます。 最初のトレーニングとスコアリングの実行が完了すると、モデルインサイトをレビューできます。 モデルは後で再訓練される可能性があります。 また、データがモデルに追加される場合があり、モデルを手動で再分割する必要があります。 リトレーニングとリスコアリングは、新たな知見や情報の獲得につながる反復的なプロセスです。ビジネス目標に最も適したモデルフィットを得るためには、調整が必要です。

## モデルを構築

モデルを構築するには、**[!UICONTROL Open model canvas]**&#x200B;を選択するときに利用できるMix Modelerのステップバイステップのガイド付きモデル設定フローを使用します。 詳しくは、[&#x200B; モデルの構築](build.md)を参照してください。

## モデルの管理

現在のモデルのテーブルを表示するには、Mix Modeler インターフェイスで次の操作を行います。

1. 左側のパネルから![FileDataS2](/help/assets/icons2/FileData.svg) **[!UICONTROL Models]**&#x200B;を選択します。

1. 現在のモデルのテーブルが表示されます。

   表の列には、モデルに関する詳細が指定されます。

   | 列の名前 | 詳細 |
   |---|---|
   | **[!UICONTROL Name]** | モデルの名前 |
   | **[!UICONTROL Description]** | モデルの説明 |
   | **[!UICONTROL Conversion event]** | モデルに対して選択した変換。 |
   | **[!UICONTROL Run frequency]** | モデルのトレーニング実施頻度。 |
   | **[!UICONTROL Last run]** | モデルの最後のトレーニングの日時。 |
   | **[!UICONTROL Status]** | モデルのステータス。 |

   昇順![ArrowMoveUpS2](/help/assets/icons2/ArrowMoveUp.svg)または降順![ArrowMoveDownS2](/help/assets/icons2/ArrowMoveDown.svg)の任意の列でテーブルを並べ替えるには、列のタイトルを選択します。

   **[!UICONTROL Name]**&#x200B;列を並べ替えたり、サイズを変更したりするには、**[!UICONTROL Name]** ![ChevronDown](/help/assets/icons/ChevronDown.svg)を選択します。 コンテキストメニューから、**[!UICONTROL Sort ascending]**、**[!UICONTROL Sort descending]**、または&#x200B;**[!UICONTROL Resize column]**&#x200B;を選択します。 または、列区切り記号にカーソルを合わせて&#x200B;**[!UICONTROL Name]**&#x200B;列のサイズを変更することもできます。

   レポートされるモデルのステータスは、モデルがライフサイクル内のどの段階にあるかによって異なります。 例えば、モデルが作成されたか、（再）トレーニングが成功したか否か、または（再）スコアリングが成功したかどうかを示します。

   次の表に示します。

   * ![Checkmark](/help/assets/icons/Checkmark.svg) - モデル ライフサイクルのステップが正常に実行されたことを示します。
   * ![時計](/help/assets/icons/Clock.svg) - モデル ライフサイクルのステップの現在の進行中の実行を示します。
   * ![閉じる](/help/assets/icons/Close.svg) - モデル ライフサイクルのステップの実行に失敗したことを示します。

   | ステータス | [&#x200B; ビルド &#x200B;](/help/models/build.md) | [&#x200B; トレーニング &#x200B;](/help/models/train-score.md#train) | [スコア](/help/models/train-score.md#score) | [再トレーニング &#x200B;](/help/models/train-score.md#train) | [Rescore](/help/models/train-score.md#score) |
   |---|:---:|:---:|:---:|:---:|:---:|
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | | | | |
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![時計](/help/assets/icons/Clock.svg) | | | |
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![時計](/help/assets/icons/Clock.svg) | | |
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![時計](/help/assets/icons/Clock.svg) | |
   | 処理中 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![時計](/help/assets/icons/Clock.svg) |
   | トレーニングに失敗しました | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![閉じる](/help/assets/icons/Close.svg) | | | |
   | トレーニングに失敗しました | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![閉じる](/help/assets/icons/Close.svg) | |
   | トレーニングの成功 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | | | |
   | トレーニングの成功 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | |
   | スコアリング失敗 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![閉じる](/help/assets/icons/Close.svg) | | |
   | スコアリング失敗 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![閉じる](/help/assets/icons/Close.svg) |
   | スコアリングに成功しました | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | | |
   | スコアリングに成功しました | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) |

   {style="table-layout:fixed"}

1. リストに表示される列を変更するには、![列設定](/help/assets/icons/ColumnSetting.svg)を選択し、![&#x200B; チェック &#x200B;](/help/assets/icons/Checkmark.svg)またはオフで列を切り替えます。

特定のモデルに対して次のアクションを実行できます。

### モデルインサイト

モデルインサイト機能は、正常にトレーニングおよびスコアリングされたモデルでのみ使用できます。

モデルのインサイトを表示するには：

1. 左側のパネルから「![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]**」を選択します。
1. モデル名を選択します。

「[&#x200B; モデルインサイト &#x200B;](insights.md)」にリダイレクトされます。

### 詳細を表示

モデルの詳細を表示するには：

1. 左側のパネルから「![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]**」を選択します。

1. モデルの![情報](/help/assets/icons/Info.svg)を選択して、詳細を含むポップアップを表示します。


### 複製

モデルをすばやく複製できます。

1. 左側のパネルから「![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]**」を選択します。

1. モデルの![詳細](/help/assets/icons/More.svg)を選択し、コンテキストメニューから&#x200B;**[!UICONTROL Duplicate]**&#x200B;を選択します。

新しいモデルを作成する手順にリダイレクトされ、元のモデルの名前で構成された提案名に&#x200B;**[!UICONTROL (Copy)]（_n_）**&#x200B;が追加されます。

### 編集

モデルの名前、説明、トレーニングとスコアリングのスケジュールを編集できます。

1. 左側のパネルから「![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]**」を選択します。

1. モデルの![詳細](/help/assets/icons/More.svg)を選択し、コンテキストメニューから&#x200B;**[!UICONTROL Edit]**&#x200B;を選択します。

   **[!UICONTROL Edit model]** ダイアログで、次の操作を行います。

   ![&#x200B; モデルの編集](../assets/model-edit.png)

   * 新しい&#x200B;**[!UICONTROL Name]**&#x200B;と&#x200B;**[!UICONTROL Description]**&#x200B;を入力してください。

   * スケジュールを有効にするには、**[!UICONTROL Enable schedule model training and scoring]**&#x200B;を有効にします。 トレーニングおよびスコアリングされたモデルに対してのみスケジュールを有効にできます。

      1. **[!UICONTROL Scoring frequency]**&#x200B;を選択：

         * **[!UICONTROL Daily]**：有効な時間（例：`10:00 am`）を入力するか、![時計](/help/assets/icons/Clock.svg)を使用して時間を定義します。
         * **[!UICONTROL Weekly]**：曜日を選択し、有効な時間（例：`10:00 am`）を入力するか、![時計](/help/assets/icons/Clock.svg)を使用して時間を定義します。
         * **[!UICONTROL Monthly]**：毎回の実行メニューから月の日を選択し、有効な時間（例：`10:00 am`）を入力するか、![時計](/help/assets/icons/Clock.svg)を使用して時間を定義します。

      1. ドロップダウンメニューから&#x200B;**[!UICONTROL Training frequency]**&#x200B;を選択します：**[!UICONTROL Monthly]**、**[!UICONTROL Quarterly]**、**[!UICONTROL Yearly]**、または&#x200B;**[!UICONTROL None]**。

   * **[!UICONTROL Granular Insights Reporting Fields]** セクションの[詳細インサイト レポート フィールド &#x200B;](/help/models/build.md#granular-insights-reporting-fields)を更新するには：
      1. **[!UICONTROL Includes]**&#x200B;の下の&#x200B;**[!UICONTROL _調和フィールド_]**&#x200B;から1つ以上の調和フィールドを選択します。 選択した調和フィールドがパネルに追加されます。
      1. **[!UICONTROL *調和フィールド&#x200B;*]**![CrossSize100](/help/assets/icons/CrossSize100.svg)を選択して、選択した調和フィールドを含む調和フィールドをコンテナから削除します。
      1. 選択したすべての調和フィールドを削除するには、**[!UICONTROL Clear all]**&#x200B;を選択します。

     >[!IMPORTANT]
     >2026年2月18日&#x200B;**より前に**&#x200B;作成されたモデルに詳細なインサイト レポート フィールドを追加する場合は、モデルのリスコアリングが必要です。 このリスコアリングにより、モデルの基礎となるスキーマが、詳細なインサイトのレポートフィールドで更新されます。
     >
     >このようなモデルを複製することをお勧めします。 複製モデルの作成に、詳細なインサイトのレポートフィールドを含めることができます。
     >

1. **[!UICONTROL Save]** を選択します。

### トレーニング

新しい増分マーケティングや要因データを含める場合に、モデルを保持する。 詳しくは、[&#x200B; モデルのトレーニングとスコアモデル &#x200B;](train-score.md#train)を参照してください。

### Score

新しいマーケティングデータにもとづいてモデルを段階的にスコアリングしたり、特定の日付範囲に合わせてモデルをスコアリングしたりできます。 詳しくは、[&#x200B; モデルのトレーニングとスコアモデル &#x200B;](train-score.md#score)を参照してください。

### モデルの削除

モデルを削除するには：

1. 左側のパネルから「![FileData](/help/assets/icons/FileData.svg) **[!UICONTROL Models]**」を選択します。
1. モデルの![詳細](/help/assets/icons/More.svg)を選択し、コンテキストメニューから&#x200B;**[!UICONTROL Delete]**&#x200B;を選択します。 または、青いアクションバーから「![削除](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]**」を選択します。
1. **[!UICONTROL Delete model]**&#x200B;確認ダイアログで「**[!UICONTROL Delete]**」を選択して、モデルを削除します。 キャンセルする場合は&#x200B;**[!UICONTROL Cancel]**&#x200B;を選択してください。

複数のモデルを削除するには：

1. 複数のモデルを選択。
1. 青いアクションバーから、![削除](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]**&#x200B;を選択して、モデルを削除します。
1. **[!UICONTROL Delete *x *モデル]**&#x200B;の確認ダイアログで&#x200B;**[!UICONTROL Delete]**&#x200B;を選択して、モデルを削除します。 キャンセルする場合は&#x200B;**[!UICONTROL Cancel]**&#x200B;を選択してください。

