---
title: データセットルール
description: Mix Modeler内のデータの調和の一部として使用するデータセットルールを定義する方法について説明します。
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: a8590d604f79268bc8d1f012f2c19271a3b38668
workflow-type: tm+mt
source-wordcount: '1407'
ht-degree: 1%

---

# データセットルール

データセットルールは、統一されたフィールドを、Mix Modelerに取り込んだデータのフィールドとマッピングする際に役立ちます。

* Adobe Experience Platformに取り込んだ集計データについて、1 つ以上の使用可能なデータセットフィールドを適切な統一されたフィールドにマッピングします。
* イベントデータの場合は、1 つ以上の統一されたフィールドを、直接または条件を使用して、データセットのフィールドに個別にマッピングできます。


## データセットルールの管理

Mix Modelerインターフェイスで使用可能なデータセットルールのテーブルを表示するには、次の手順を実行します。

1. 左パネルから ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** を選択します。

1. 上部バーの「**[!UICONTROL Dataset rules]**」を選択します。 データセットルールのテーブルが表示されます。

テーブルの列には、データセットルールの詳細が表示されます。

| 列名 | 詳細 |
| ---------------------- | ----------|
| データセット | データセットの名前。 |
| ソース | データセットのソース：Adobe Analytics、エクスペリエンスイベント、概要（集計）またはコンシューマーエクスペリエンスイベント。 |
| スキーマ | データセットが準拠するスキーマ。 スキーマ名をすばやく選択して、![ スキーマ ](/help/assets/icons/Schemas.svg) [ スキーマ ](../ingest-data/schemas.md) のスキーマエディターの新しいタブでスキーマを開くことができます。 |
| 精度 | データセット内のデータの精度。 指定可能な値は、Daily、Weekly、Monthly、Yearly です。 |
| 週の開始日 | 特定のデータセットについて、新しい週の開始日と見なされる曜日を指定します。 |
| ステータス | フィールドのステータス： <p><span style="color:gray">●</span> ドラフトまたは <p><span style="color:green">●</span> アクティブ |
| 最終変更日 | データセットルールの最終変更日時。 |

{style="table-layout:auto"}

### データセットルールの作成

データセットルールを作成するには、ウィザードの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Dataset rules]** インターフェイスで、**[!UICONTROL Dataset rules configuration]** Mix Modelerの **[!UICONTROL Create a dataset rule]** を選択します。

**[!UICONTROL Create]** 画面で、

1. **[!UICONTROL Dataset details]** では、**[!UICONTROL Select dataset]** からデータセットを選択して設定を開始します。 リストのデータセットは、**[!UICONTROL Consumer Experience Events]**、**[!UICONTROL Adobe Analytics]**、**[!UICONTROL Experience Event]**、**[!UICONTROL Summary]** に分類されています。

1. **[!UICONTROL Start of the week]** の日付を選択します。

1. **[!UICONTROL Granularity]** に **[!UICONTROL Daily]**、**[!UICONTROL Weekly]**、**[!UICONTROL Monthly]**、**[!UICONTROL Yearly]** のいずれかを選択します。

1. **[!UICONTROL Summary]** カテゴリのデータセットを選択した場合：

   1. データセットのデータを集計するか、既存のデータを置き換えるかを定義するには、「**[!UICONTROL Aggregation]**」または「**[!UICONTROL Replacement]**」を選択し **[!UICONTROL Data restatement is by]** す。

   1. 各 **[!UICONTROL Available dataset fields]** を対応する **[!UICONTROL Standard harmonized fields]** に **[!UICONTROL Map to harmonized fields]** でマッピングします。 データセットフィールドを統一フィールドにマッピングしない場合は、「**[!UICONTROL -- None --]**」を明示的に選択します。

   1. リストにない新しい統一フィールドが必要な場合は、「**[!UICONTROL Create New]**」を選択して新しい統一フィールドを作成します。 [ 新しい統一フィールドの追加 ](fields.md#add-a-harmonized-field) の説明に従ってダイアログが表示されます。

   1. ルールのすべてのフィールドのマッピングが完了したら、「**[!UICONTROL Save as draft]**」を選択してルールのドラフトバージョンを保存するか、「**[!UICONTROL Save]**」を選択してルールを保存してアクティブ化します。 「**[!UICONTROL Cancel]**」を選択して、ルール設定をキャンセルします。

      ![ データセットルールの作成 ](/help/assets/dataset-create-summary.png)

1. **[!UICONTROL Map to harmonized fields]** の下のボックスでイベントカテゴリデータセット（**[!UICONTROL Experience Events]**、**[!UICONTROL Adobe Analytics]**、**[!UICONTROL Consumer Experience Events]**）を選択した場合：

   1. **[!UICONTROL Standard harmonized field]** から統一フィールドを選択します。

   1. 選択した統一フィールドが指標タイプの場合：

      1. **[!UICONTROL Mapping type]** から **[!UICONTROL Count]** または **[!UICONTROL Sum]** を選択します。

      1. デフォルトで統一フィールドをマッピングする **[!UICONTROL *AEP データセットフィールド&#x200B;*]**&#x200B;を選択します。

   1. 選択したフィールドのタイプがディメンションの場合：

      1. **[!UICONTROL Mapping type]** から **[!UICONTROL Map Into]** または **[!UICONTROL Case]** を選択します。

      1. **[!UICONTROL Map Into]** を選択した場合、**[!UICONTROL Field]** と **[!UICONTROL *AEP データセットフィールド&#x200B;*]**&#x200B;または&#x200B;**[!UICONTROL Value]**&#x200B;とデフォルト値を選択して、デフォルトで統一フィールドをデータセットフィールドまたは入力した値にマッピングします。

      1. **[!UICONTROL Case]** を選択する場合、「**[!UICONTROL Field]** と **[!UICONTROL *AEP データセットフィールド&#x200B;*]**&#x200B;または&#x200B;**[!UICONTROL Value]**&#x200B;とデフォルト値を選択して、デフォルトで統一フィールドをデータセットフィールドまたは入力した値にマッピングします。

         1. 値を明示的に設定するには、1 つ以上の条件で構成される 1 つ以上のケースを定義します。 各条件では、特定の **[!UICONTROL *AEP データセットフィールド&#x200B;*]**&#x200B;**[!UICONTROL Exists]**&#x200B;または&#x200B;**[!UICONTROL Not Exists]**、**[!UICONTROL Contains]**、**[!UICONTROL Not Contains]**、**[!UICONTROL Equals]**、**[!UICONTROL Not Equals]**、**[!UICONTROL Starts With]**、または&#x200B;**[!UICONTROL * 入力値を入力 *]** で入力された値を **[!UICONTROL Ends With]** るかどうかを確認できます。

         1. 別のケースを追加するには、「![ 追加 ](/help/assets/icons/AddCircle.svg)」を選択します **[!UICONTROL Add case]**、別の条件を追加するには、「![ 追加 ](/help/assets/icons/AddCircle.svg)」 **[!UICONTROL Add condition]** を選択します。

         1. ケースまたは条件を削除するには、対応するコンテナで「![ 閉じる ](/help/assets/icons/Close.svg)」を選択します。

         1. 条件の一部または全部をケースに適用するかどうかを選択するには、「**[!UICONTROL Any of]**」または「**[!UICONTROL All of]**」を選択します。

         1. ケースの結果値を設定するには、値を **[!UICONTROL Then]** に入力します。

      以下の例

      * では、**[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** を使用して、**[!UICONTROL Channel Type At Source]** 統一フィールドを **[!DNL Luma Transactions]** データセットの **[!UICONTROL channel_type]** フィールドにマッピングします。

      * では、**[!UICONTROL Case]** **[!UICONTROL Mapping type]** を使用して、**[!DNL Luma Transactions]** データセットの **[!UICONTROL marketing.campaignName]** フィールドの値を条件付きで **[!UICONTROL Campaign]** 統一フィールドにマッピングします。 Campaign 統一フィールドは次のように設定されます。

         * **[!UICONTROL marketing.campaignName]** が `_black_friday` または `BlackFriday` の場合に `Black Friday` します。
         * その他すべての場合、**[!UICONTROL marketing.campaignName]** の値に変換します。

        ![ データセットルールイベント ](/help/assets/dataset-create-event.png)

1. ![ 追加 ](/help/assets/icons/AddCircle.svg)**[!UICONTROL Add field]** を選択して、追加のフィールドを定義します。

終了したら、「**[!UICONTROL Save as draft]**」を選択してルールのドラフトバージョンを保存するか、「**[!UICONTROL Save]**」を選択してルールを保存してアクティブにします。 「**[!UICONTROL Cancel]**」を選択して、ルール設定をキャンセルします。


### データセットルールの編集

データセットルールを編集するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Dataset rules]** インターフェイスで、次の手順を実行します。

1. 編集するデータセットルールの **[!UICONTROL Dataset]** 列で、「![ 詳細 ](/help/assets/icons/More.svg)」を選択します。
1. コンテキストメニューの「![ 編集 ](/help/assets/icons/Edit.svg)」を選択して、データセットルールの編集を開始します **[!UICONTROL Edit]**。 詳しくは [ データセットルールの作成 ](#create-a-dataset-rule) を参照してください。


### データセットルールの削除

データセットルールを削除するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Dataset rules]** インターフェイスで、次の手順を実行します。

1. 削除するデータセットルールの「**[!UICONTROL Dataset]**」列で、「![ 詳細 ](/help/assets/icons/More.svg)」を選択します。
1. コンテキストメニューの「![ 削除 ](/help/assets/icons/Delete.svg)」を選択して、データセットルール **[!UICONTROL Delete]** 削除します。 確認を求めるプロンプトが表示されます。 選択したデータセットルールを完全に削除するには、「**[!UICONTROL Delete]**」を選択します。


## データを同期

データセットルールでロジックを適用する際に、統一データと概要データセットやイベントデータセットの間でデータを同期するには：

1. **[!UICONTROL Sync data]** を選択します。

1. **[!UICONTROL Sync data for dataset rules]** ダイアログで、次のいずれかを選択します。
   * **[!UICONTROL Refresh harmonized data for summary datasets]**,
   * **[!UICONTROL Refresh harmonized data for event datasets]**、または
   * **[!UICONTROL Refresh harmonized data for both summary + event datasets]**。

1. 統一データとデータセット内のデータの間に定義されたデータセットルールに基づいて同期を開始するには、「**[!UICONTROL Sync]**」を選択します。 同期をキャンセルするには、[**[!UICONTROL Cancel]**] を選択します。

   ![ データを同期 ](/help/assets/sync-data.png)


## データ結合環境設定

>[!NOTE]
>
>[!BADGE &#x200B; ベータ版 &#x200B;]{type=Informative}

モデルを正確に予測するには、データの結合の環境設定を定義します。 この機能を使用すると、ユーザーは概要レベルとイベントレベルのデータを結合した後に競合を解決できます。

更新が競合する場合に適用されるデフォルトの指標環境設定を設定できます。 このデフォルトの指標は、次の 3 つのオプションのいずれかになります。

* **[!UICONTROL Summary data]**
* **[!UICONTROL Sum of summary and event data]**
* **[!UICONTROL Event data]**

ハーモナイゼーション中に複数のデータソースが特定のチャネルの指標フィールドを更新しようとすると、ユーザーが設定したデフォルトの環境設定が適用されます。 この環境設定は、追加設定された特定の指標ベースの環境設定で上書きされない限り、サンドボックスレベルで適用されます。

**[!UICONTROL Metric based preferences]** では、特定の指標の特定のソース（**[!UICONTROL Summary]** または **[!UICONTROL Event]**）と、その指標に対応するコンバージョンタイプを設定できます。

典型的なユースケースを次に示します。

* 同じ広告指標が複数のデータセットで測定およびレポートされる
* 一部のデータセットでは指標の測定が不完全な場合がありますが、別のデータセットは特定の指標のスーパーセットである場合があり、二重カウントが発生する可能性があります。

### 設定

データの結合の環境設定を指定するには：


1. ![ データ結合環境設定 ](/help/assets/icons/Merge.svg) [!BADGE &#x200B; ベータ版 &#x200B;] を選択します。

1. **[!UICONTROL Data merge preferences]**&#x200B;[!BADGE &#x200B; ベータ版 &#x200B;]{type=Informative}

   ![ データ結合環境設定 ](/help/assets/data-merge-preferences.png)

   * **[!UICONTROL Default metric preference]** を選択します。 選択したデフォルトの指標の環境設定は、ハーモナイゼーション中に、複数のデータソースが特定のチャネルの指標フィールドを更新すると適用されます。 特定の指標ベースの環境設定で上書きされない限り、環境設定はサンドボックスレベルで適用されます。 **[!UICONTROL Summary data]**、**[!UICONTROL Event data]**、**[!UICONTROL Sum of summary and event data]** から選択できます。

   * 特定の指標ベースの環境設定を追加するには：

      1. ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a metric]** を選択します。
         1. **[!UICONTROL *指標選択&#x200B;*]**&#x200B;リストから指標を選択します。
         1. **[!UICONTROL CHANNELS]** または **[!UICONTROL CONVERSION TYPES]** を選択します。リストから、**[!UICONTROL All]** または特定のチャネルやコンバージョンのタイプを選択します。
         1. **[!UICONTROL Summary]** または **[!UICONTROL Event]** を選択して、データを結合する際に、指標（およびすべてのチャネルまたは選択したチャネル）に対して概要データまたはイベントデータを優先するかどうかを指定します。

         1 つ以上のチャネルまたはコンバージョンタイプを追加するには：

         1. ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a channel]** または ![Plus](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion type]** を選択します。
         1. **[!UICONTROL Summary]** または **[!UICONTROL Event]** を選択します。

         チャネルまたはコンバージョンタイプを削除するには、「![ クロス ](/help/assets/icons/Close.svg)」を選択します。

      1. 指標に基づいた環境設定をさらに具体的に追加するには、前の手順を繰り返します。

   * 既存の特定の指標ベースの環境設定を削除するには、「![ 削除 ](/help/assets/icons/Delete.svg)」を選択します。

1. 「**[!UICONTROL Save]**」を選択して、データ結合の環境設定を保存します。 データの再同期が開始されます。 <br/> キャンセルする **[!UICONTROL Cancel]** を選択します。

## ソースデータセットの削除

調和されたデータで使用されているソースデータセットを削除すると、そのソースデータセットに対する基になるエントリが [[!UICONTROL Harmonized data]](/help/harmonize-data/overview.md) から削除されます。 ただし、削除されたソースデータセットを含むデータセットルールは、ソースデータセットが削除されたことを示すアイコン ![DataRemove](/help/assets/icons/DataRemove.svg) とともに、データセットルール設定リストに残ります。 詳細情報を取得するには：

* コンテキストメニューから ![ その他 ](/help/assets/icons/More.svg) および ![ プレビュー ](/help/assets/icons/Preview.svg)**[!UICONTROL View]** を選択します。
**[!UICONTROL Dataset rule mapping - Fields]** ダイアログには、削除されたソースデータセットと、データセットルール設定で使用されているフィールドに関する情報が表示されます。

**[!UICONTROL Dataset rules]** 設定に戻ると、1 つ以上のソースデータセットが削除されたことを説明するダイアログが表示されます。 統一されたデータは、次のアドホック同期またはスケジュールされた同期で影響を受けます。 データセットルールの設定を確認します。

調和されたデータは、次のアドホック同期時またはスケジュール同期時に、削除されたソースデータなしで更新される。 ただし、削除されたソースデータセットに基づいてデータセットルールを削除するように求めるアラートダイアログが引き続き表示されます。 このアラートを使用すると、ユーザーは、削除されたデータセット内の影響を受けたフィールドを表示および評価できます。 任意のモデルで使用できるマーケティングタッチポイントまたはコンバージョンへの影響を判断する場合もあります。 この影響を確認し、軽減したら、データセットルール設定リストからデータセットルールを削除する必要があります。
