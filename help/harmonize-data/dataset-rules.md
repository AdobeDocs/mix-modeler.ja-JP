---
title: データセットルール
description: Mix Modelerのデータの調和の一部として使用するデータセットルールを定義する方法について説明します。
feature: Harmonized Data, Dataset Rules
exl-id: 57d7940a-2900-4814-a30d-bb02bff7615d
source-git-commit: d22bb8c9526821c28c9a59967e1be399957d3051
workflow-type: tm+mt
source-wordcount: '1628'
ht-degree: 1%

---

# データセットルール

データセットルールは、統一されたフィールドを、Mix Modelerに取り込んだデータのフィールドにマッピングする際に役立ちます。

* Adobe Experience Platformに取り込んだ集計データについて、1 つ以上の使用可能なデータセットフィールドを適切な統一されたフィールドにマッピングします。
* イベントデータの場合は、1 つ以上の統一されたフィールドを、直接または条件を使用して、データセットのフィールドに個別にマッピングできます。


## データセットルールの管理

Mix Modeler インターフェイスで、使用可能なデータセットルールのテーブルを表示するには、次の手順を実行します。

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
| ステータス | フィールドのステータス： <p><span style="color:gray">●</span> ドラフトまたは <p><span style="color:green">●</span> Active |
| 最終変更日 | データセットルールの最終変更日時。 |

{style="table-layout:auto"}

### データセットルールの作成

データセットルールを作成するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Dataset rules]** インターフェイスで、**[!UICONTROL Create a dataset rule]** ータセットウィザードの「**[!UICONTROL Dataset rules configuration]**」を選択します。

**[!UICONTROL Create]** 画面で、

1. **[!UICONTROL Dataset details]** では、**[!UICONTROL Select dataset]** からデータセットを選択して設定を開始します。 リストのデータセットは、**[!UICONTROL Consumer Experience Events]**、**[!UICONTROL Adobe Analytics]**、**[!UICONTROL Experience Event]**、**[!UICONTROL Summary]** に分類されています。

1. **[!UICONTROL Start of the week]** の日付を選択します。

1. **[!UICONTROL Daily]** に **[!UICONTROL Weekly]**、**[!UICONTROL Monthly]**、**[!UICONTROL Yearly]**、**[!UICONTROL Granularity]** のいずれかを選択します。

1. **[!UICONTROL Summary]** カテゴリのデータセットを選択した場合は、**[!UICONTROL Aggregation]** に **[!UICONTROL Replacement]** または **[!UICONTROL Data restatement is by]** を選択します。

   パブリッシャーとの連携は多くの場合、多額の費用を意味し、レポートデータの変更によりインサイトと投資プランが大きく異なる場合があるので、パブリッシャーからのレポートデータはマーケティングアナリストにとって非常に重要です。 さらに、マーケティングアナリストは、適切なインサイトを導き出し、関係者の信頼を得るために説得力のある提案を提示するために、正確なデータを必要としています。 ただし、Googleや Facebook などのパブリッシャーは、多くの場合、データを紐付ける際にレポートデータを再記述または削除します。 ほとんどの変更に対する時間枠は、レポートされたメディアパフォーマンスから 7 日以内です。 データの追加の変更は、30 日以内に可能です。 一般的に、30 日後、本は閉鎖され、データが完了したと見なされます。

   Mix Modelerは、データの再記述をサポートしています。 レポート、モデリングおよび計画に使用されるデータが正確であることを確認します。 また、データは、ブランドやマーケティングアナリストの期待やニーズをサポートできます。

   再表示された概要データ行をExperience Platform データセットの増分行として送信でき、調和サービスによって調和されたデータセットがその再表示されたデータで更新されます。 同様に、調和サービスに反映する必要がある概要データの行を削除することもできます。

1. **[!UICONTROL Map to harmonized fields]** のセクションで以下を実行します。

   1. **[!UICONTROL Standard harmonized field]** から統一フィールドを選択します。

   1. 選択した統一フィールドが指標タイプの場合：

      1. **[!UICONTROL Count]** から **[!UICONTROL Sum]** または **[!UICONTROL Mapping type]** を選択します。

      1. デフォルトで統一フィールドをマッピングする **[!UICONTROL *0&rbrace;AEP データセットフィールド &rbrace; を選択します。*]**

   1. 選択したフィールドのタイプがディメンションの場合：

      1. **[!UICONTROL Map Into]** から **[!UICONTROL Case]** または **[!UICONTROL Mapping type]** を選択します。

      1. **[!UICONTROL Map Into]** を選択した場合、**[!UICONTROL Field]** と **[!UICONTROL *AEP データセットフィールド&#x200B;*]**&#x200B;または&#x200B;**[!UICONTROL Value]**&#x200B;とデフォルト値を選択して、デフォルトで統一フィールドをデータセットフィールドまたは入力した値にマッピングします。

      1. **[!UICONTROL Case]** を選択する場合、**[!UICONTROL Field]** と **[!UICONTROL *AEP データセットフィールド&#x200B;*]**&#x200B;または&#x200B;**[!UICONTROL Value]**&#x200B;とデフォルト値を選択して、デフォルトで統一フィールドをデータセットフィールドまたは入力された値にマップします。

         1. 値を明示的に設定するには、1 つ以上の条件で構成される 1 つ以上のケースを定義します。 各条件は、特定の **[!UICONTROL *AEP データセットフィールドをチェックできます。フィールドの&#x200B;*]**&#x200B;または&#x200B;**[!UICONTROL Exists]**&#x200B;か&#x200B;**[!UICONTROL Not Exists]**&#x200B;**[!UICONTROL Contains]**、**[!UICONTROL Not Contains]**、**[!UICONTROL Equals]**、**[!UICONTROL Not Equals]**、**[!UICONTROL Starts With]**、または&#x200B;**[!UICONTROL Ends With]**&#x200B;入力値を入力&#x200B;**[!UICONTROL * で入力された値 *]** あるかをチェックします。

         1. 別のケースを追加するには、「![ 追加 ](/help/assets/icons/AddCircle.svg)」を選択します **[!UICONTROL Add case]**、別の条件を追加するには、「![ 追加 ](/help/assets/icons/AddCircle.svg)」 **[!UICONTROL Add condition]** を選択します。

         1. ケースまたは条件を削除するには、対応するコンテナで「![ 閉じる ](/help/assets/icons/Close.svg)」を選択します。

         1. 条件の一部または全部をケースに適用するかどうかを選択するには、「**[!UICONTROL Any of]**」または「**[!UICONTROL All of]**」を選択します。

         1. ケースの結果値を設定するには、値を **[!UICONTROL Then]** に入力します。

      以下の例

      * では、**[!UICONTROL Map Into]** **[!UICONTROL Mapping type]** を使用して、**[!UICONTROL Channel Type At Source]** 統一フィールドを **[!UICONTROL channel_type]** データセットの **[!DNL Luma Transactions]** フィールドにマッピングします。

      * では、**[!UICONTROL Case]** **[!UICONTROL Mapping type]** を使用して、**[!UICONTROL marketing.campaignName]** データセットの **[!DNL Luma Transactions]** フィールドの値を条件付きで **[!UICONTROL Campaign]** 統一フィールドにマッピングします。 Campaign 統一フィールドは次のように設定されます。

         * `Black Friday` が **[!UICONTROL marketing.campaignName]** または `_black_friday` の場合に `BlackFriday` します。
         * その他すべての場合、**[!UICONTROL marketing.campaignName]** の値に変換します。

        ![ データセットルールイベント ](/help/assets/dataset-create-event.png)

      概要データセットから標準統一フィールドをマッピングすると、Mix Modelerは対応するExperience Platform データセットフィールドの推測を試みます。 成功した場合：

      * フィールドのタイプがディメンションの場合は、**[!UICONTROL Map into]** が **[!UICONTROL Mapping type]** として選択されます。
      * フィールドのタイプが指標の場合は、**[!UICONTROL Sum]** として **[!UICONTROL Mapping type]** が選択されます。
      * **[!UICONTROL Field]** が **[!UICONTROL Default]** のマッピングタイプとして選択されます。
      * 対応するExperience Platform データセットフィールドが、*AEP データセットフィールド* に自動的に挿入されます。

      提案された値が正しくない場合や、特定のユースケースをサポートしていない場合は、値を変更できます。

1. ![ 追加 ](/help/assets/icons/AddCircle.svg)**[!UICONTROL Add field]** を選択して、追加のフィールドを定義します。

終了したら、「**[!UICONTROL Save as draft]**」を選択してルールのドラフトバージョンを保存するか、「**[!UICONTROL Save]**」を選択してルールを保存してアクティブにします。 「**[!UICONTROL Cancel]**」を選択して、ルール設定をキャンセルします。

>[!NOTE]
>
>概要データセットルール専用の **[!UICONTROL Map to harmonized fields]** エクスペリエンスは廃止されました。 データセットタイプに関係なく、すべてのデータセットルールが類似した **[!UICONTROL Map to harmonized fields]** エクスペリエンスを使用するようになりました。 非推奨の **[!UICONTROL Map to harmonized fields]** エクスペリエンスを使用してルールを定義した概要データセットの場合は、これらのルールを汎用の **[!UICONTROL Map to harmonized field]** エクスペリエンスに照らして検証することをお勧めします。
>



### データセットルールの編集

Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Dataset rules]** インターフェイスでデータセットルールを編集するには、次の手順を実行します。

1. 編集するデータセットルールの ![ 列で、「](/help/assets/icons/More.svg) 詳細 **[!UICONTROL Dataset]**」を選択します。
1. コンテキストメニューの「![ 編集 ](/help/assets/icons/Edit.svg)」を選択して、データセットルールの編集を開始します **[!UICONTROL Edit]**。 詳しくは [ データセットルールの作成 ](#create-a-dataset-rule) を参照してください。


### データセットルールの削除

データセットルールを削除するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Dataset rules]** インターフェイスで、次の手順を実行します。

1. 削除するデータセットルールの「![」列で、「](/help/assets/icons/More.svg) 詳細 **[!UICONTROL Dataset]**」を選択します。
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
>[!BADGE &#x200B; ベータ版 &#x200B;]{type=Informative} データ結合の環境設定はベータ版機能であり、その機能は変更される可能性があります。

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

1. **[!UICONTROL Data merge preferences]** [!BADGE &#x200B; ベータ版 &#x200B;]{type=Informative} ダイアログで、

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
