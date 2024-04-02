---
title: データセットルール
description: Mix Modelerでのデータの調和の一環として使用するデータセットルールを定義する方法を説明します。
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: 4f4c7f05e90d73a0ab4865150b1ec4c2af88fc12
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 1%

---

# データセットルール

データセットルールは、調和されたフィールドを、Mix Modelerで取り込んだデータのフィールドとマッピングする際に役立ちます。

* Adobe Experience Platformで取り込んだ集計データについて、1 つ以上の使用可能なデータセットフィールドを、適切な調和されたフィールドにマッピングします。
* イベントデータの場合、1 つ以上の調和されたフィールドを、データセット内のフィールドに個別にマッピングしたり、直接または条件を使用してマッピングしたりできます。


## データセットルールの管理

使用可能なデータセットルールの表を確認するには、Mix Modelerインターフェイスで次の操作を実行します。

1. 選択 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** をクリックします。

1. 選択 **[!UICONTROL Dataset rules]** 上部のバーから。 データセットルールの表が表示されます。

テーブルの列には、データセットルールの詳細が示されます。

| 列名 | 詳細 |
| ---------------------- | ----------|
| データセット | データセットの名前。 |
| ソース | データセットのソース。Adobe Analytics、エクスペリエンスイベント、概要（集計）、消費者エクスペリエンスイベントのいずれかです。 |
| スキーマ | データセットが準拠するスキーマです。 スキーマ名をすばやく選択して、スキーマエディターの「Mix Modeler — スキーマ」で、新しいタブでスキーマを開くことができます。 |
| 精度 | データセット内のデータの精度。 指定できる値は、日別、週別、月別、年別です。 |
| 週の最初 | 特定のデータセットで新しい週の開始と見なされる曜日を指定します。 |
| ステータス | フィールドのステータス： <p><span style="color:gray">●</span> 下書きまたは <p><span style="color:green">●</span> アクティブ |
| 最終変更日 | データセットルールの最後の変更のデータと時刻。 |

{style="table-layout:auto"}

### データセットルールの作成

データセットルールを作成するには、 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** インタフェース (Mix Modeler): **[!UICONTROL Create Dataset rule]** （内） **[!UICONTROL Dataset rules configuration]** ウィザード。

Adobe Analytics の **[!UICONTROL Create]** 画面

1. In **[!UICONTROL Dataset details]**、次の中からデータセットを選択します。 **[!UICONTROL Select dataset]** をクリックして設定を開始します。 リストでは、データセットは **[!UICONTROL Consumer Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Experience Event]** そして **[!UICONTROL Summary]**.

1. 日付を選択 **[!UICONTROL Start of the week]**.

1. 選択 **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** または **[!UICONTROL Yearly]** 対象： **[!UICONTROL Granularity]**.

1. 次のデータセットを選択した場合： **[!UICONTROL Summary]** カテゴリ：

   1. データセットのデータを集計する必要があるか、既存のデータを置き換えるかを定義するには、 **[!UICONTROL Aggregation]** または **[!UICONTROL Replacement]** 対象： **[!UICONTROL Data restatement is by]**.

   1. 各 **[!UICONTROL Available dataset fields]** 対応する **[!UICONTROL Standard harmonized fields]** in **[!UICONTROL Map to harmonized fields]**. データセットフィールドを調整済みのフィールドにマッピングしない場合は、「 **[!UICONTROL -- None --]**.

   1. リストから利用できない、新しく調和されたフィールドが必要な場合は、「 」を選択します。 **[!UICONTROL Create New]** 新しく調和されたフィールドを作成します。 ダイアログが表示されます。詳しくは、 [新しい調整済みフィールドを追加](fields.md#add-a-harmonized-field) 新しい調和済みフィールドをすばやく追加できます。

   1. ルールのすべてのフィールドのマッピングが完了したら、 **[!UICONTROL Save as draft]** ルールのドラフトバージョンを保存するには、以下を実行します。 **[!UICONTROL Save]** ルールを保存してアクティブ化します。 選択 **[!UICONTROL Cancel]** をクリックして、ルール設定をキャンセルします。

      ![データセットルールの作成](../assets/dataset-create-summary.png)

1. イベントカテゴリデータセット (**[!UICONTROL Experience Events]**, **[!UICONTROL Adobe Analytics]**, **[!UICONTROL Consumer Experience Events]**)、の下のボックス **[!UICONTROL Map to harmonized fields]**:

   1. 次の中から調和されたフィールドを選択： **[!UICONTROL Standard harmonized field]**.

   1. 選択した調和済みフィールドのタイプが指標の場合：

      1. 選択 **[!UICONTROL Count]** または **[!UICONTROL Sum]** から **[!UICONTROL Mapping type]**.

      1. を選択します。 **[!UICONTROL *AEP データセットフィールド&#x200B;*]**調和されたフィールドをデフォルトでマッピングする

   1. 選択したフィールドのタイプが次の場合：

      1. 選択 **[!UICONTROL Map Into]** または **[!UICONTROL Case]** から **[!UICONTROL Mapping type]**.

      1. 次を選択した場合： **[!UICONTROL Map Into]**&#x200B;を選択します。 **[!UICONTROL Field]** および **[!UICONTROL *AEP データセットフィールド&#x200B;*]**または&#x200B;**[!UICONTROL Value]**「調和済み」フィールドのデフォルト値は、データセットフィールドまたは入力値に、デフォルトで調和済みフィールドをマッピングするデフォルト値です。

      1. 次の項目を選択した場合： **[!UICONTROL Case]**&#x200B;を選択します。 **[!UICONTROL Field]** および **[!UICONTROL *AEP データセットフィールド&#x200B;*]**または&#x200B;**[!UICONTROL Value]**「調和済み」フィールドのデフォルト値は、データセットフィールドまたは入力値に、デフォルトで調和済みフィールドをマッピングするデフォルト値です。

         1. また、値を明示的に設定する 1 つ以上の条件で構成される、1 つ以上のケースを定義します。 各条件は、特定の **[!UICONTROL *AEP データセットフィールド&#x200B;*]**どうか&#x200B;**[!UICONTROL Exists]**または&#x200B;**[!UICONTROL Not Exists]**または&#x200B;**[!UICONTROL Contains]**,**[!UICONTROL Not Contains]**,**[!UICONTROL Equals]**,**[!UICONTROL Not Equals]**,**[!UICONTROL Starts With]**または&#x200B;**[!UICONTROL Ends With]**次の場所に入力された値：**[!UICONTROL *&#x200B;入力値を入力&#x200B;*]**.

         1. 別のケースを追加するには、「 ![追加](../assets/icons/AddCircle.svg) **[!UICONTROL Add case]**、別の条件を追加するには、「 」を選択します。 ![追加](../assets/icons/AddCircle.svg) **[!UICONTROL Add condition]**.

         1. ケースまたは条件を削除する場合は、「 ![閉じる](../assets/icons/Close.svg) を指定します。

         1. 1 つのケースに対して、いずれかの条件を適用するかすべての条件を適用するかを選択するには、 **[!UICONTROL Any of]** または **[!UICONTROL All of]**.

         1. ケースの結果の値を設定するには、値を **[!UICONTROL Then]**.

      次の例

      * はを使用します **[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** 地図を作る **[!UICONTROL Channel Type At Source]** 調和された分野 **[!UICONTROL channel_type]** フィールド **[!DNL Luma Transactions]** データセット。

      * はを使用します **[!UICONTROL Case]** **[!UICONTROL Mapping type]** 条件付きでの **[!UICONTROL marketing.campaignName]** フィールド **[!DNL Luma Transactions]** データセットを **[!UICONTROL Campaign]** 調和されたフィールド。 「キャンペーンの調和済み」フィールドは次のように設定されます。

         * `Black Friday` 時に **[!UICONTROL marketing.campaignName]** 次に該当 `_black_friday` または `BlackFriday`.
         * を **[!UICONTROL marketing.campaignName]** 他のすべての場合には

        ![データセットルールイベント](../assets/dataset-create-event.png)

1. 選択 ![追加](../assets/icons/AddCircle.svg) **[!UICONTROL Add field]** をクリックして、追加のフィールドを定義します。

終了したら、「 」を選択します。 **[!UICONTROL Save as draft]** ルールのドラフトバージョンを保存するには、以下を実行します。 **[!UICONTROL Save]** ルールを保存してアクティブ化します。 選択 **[!UICONTROL Cancel]** をクリックして、ルール設定をキャンセルします。


### データセットルールの編集

データセットルールを編集するには、 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** インターフェイスのMix Modeler:

1. 選択 ![その他](../assets/icons/More.svg) （内） **[!UICONTROL Dataset]** 列を編集します。
1. コンテキストメニューから、「 」を選択します。 ![編集](../assets/icons/Edit.svg) **[!UICONTROL Edit]** 」をクリックして、データセットルールの編集を開始します。 参照： [データセットルールの作成](#create-a-dataset-rule) を参照してください。


### データセットルールの削除

データセットルールを削除するには、 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Dataset rules]** インターフェイスのMix Modeler:

1. 選択 ![その他](../assets/icons/More.svg) （内） **[!UICONTROL Dataset]** 」列に追加します。
1. コンテキストメニューから、「 」を選択します。 ![削除](../assets/icons/Delete.svg) **[!UICONTROL Delete]** をクリックして、データセットルールを削除します。 確認を求めるメッセージが表示されます。 選択 **[!UICONTROL Delete]** 選択したデータセットルールを完全に削除します。


## データを同期

調和したデータと概要データセット、またはイベントデータセット間でデータを同期するには、データセットルールのすべてのロジックに従います。

1. **[!UICONTROL Sync data]** を選択します。

1. 次から： **[!UICONTROL Sync data for dataset rules]** ダイアログで、次のいずれかを選択します。 **[!UICONTROL Refresh harmonized data for summary datasets]**, **[!UICONTROL Refresh harmonized data for event datasets]**&#x200B;または **[!UICONTROL Refresh harmonized data for both summary + event datasets]**.

1. データセット内のデータと調和したデータの定義済みデータセットルールに基づいて同期を開始するには、 **[!UICONTROL Sync]**. 同期をキャンセルする場合は、 **[!UICONTROL Cancel]**.

   ![データを同期](../assets/sync-data.png)


## データ結合環境設定

要約済みのデータとイベントソースが結合されたときの競合を解決する環境設定を定義できます。 その手順は次のとおりです。

1. 選択 ![データ結合環境設定](../assets/icons/Merge.svg) **データ結合環境設定**.

1. Adobe Analytics の **[!UICONTROL Data merge preferences]** ダイアログ：

   ![データ結合環境設定](../assets/data-merge-preferences.png)

   1. 以下からデフォルトの指標の環境設定を選択します。 **[!UICONTROL Default metric preference]** リスト。 <p>ハーモナイゼーション中に、複数のデータソースが特定のチャネルの指標フィールドを更新しようとすると、デフォルトの環境設定が適用されます。 この環境設定は、で定義された特定の指標の環境設定に対して上書きされない限り、サンドボックスレベルで適用されます。 **[!UICONTROL Metric based preference]**.

   1. 用途 ![プラス](../assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]**、以下に 1 つ以上の指標を追加します。 **[!UICONTROL Metric based preference]**.



      * 次から指標を選択： **[!UICONTROL _指標の選択_]** リスト、および
      * **[!UICONTROL Summary]** または **[!UICONTROL Event]** を選択します。

      用途 ![削除](../assets/icons/Close.svg) をクリックして、リストからエントリを削除します。

   1. 選択 **[!UICONTROL Save]** をクリックして、データ結合環境設定を保存します。 選択 **[!UICONTROL Cancel]** をクリックしてキャンセルします。
