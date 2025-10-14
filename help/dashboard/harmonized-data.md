---
title: 統一データダッシュボード
description: Mix Modelerの統一データ概要ダッシュボードの使用方法について説明します。
feature: Dashboard, Harmonized Data
exl-id: fbb01613-d648-4db1-a782-a7720b7a03ad
source-git-commit: 9776b79cfc4a8eaebecd4bce85cfc9d85329c910
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# 統一データ

Mix Modeler![&#x200B; ホーム &#x200B;](/help/assets/icons/Home.svg) の「**[!UICONTROL Harmonized data]**」タブには、取り込んだデータ **[!UICONTROL Overview]** 統一データの一部として使用するように設定した統一データに関するインサイトが表示されます。

この概要には、4 つの KPI ステータスカードのビジュアライゼーション （一番上の行）と、その他 6 つの設定可能なビジュアライゼーションが表示されます。

ビジュアライゼーションに表示するデータの日付範囲を変更するには、開始日と終了日を手動で入力するか、![&#x200B; カレンダー &#x200B;](/help/assets/icons/Calendar.svg) を使用して期間を選択します。

## データフィルター

![&#x200B; フィルター &#x200B;](/help/assets/icons/Filter.svg) データペインを使用して、すべてのビジュアライゼーションで表示される **[!UICONTROL Category Filters]** ータをフィルタリングできます。

各カテゴリに対して 1 つ以上のフィルターを選択します（**[!UICONTROL Brands]**、**[!UICONTROL Campaigns]**、**[!UICONTROL Channels Type]**、**[!UICONTROL Conversion types]**、**[!UICONTROL Datasets]**、**[!UICONTROL Media types]**、**[!UICONTROL Source types]** および **[!UICONTROL Traffic Source]**）。

選択したフィルターは、**[!UICONTROL FILTERING BY:]** のビジュアライゼーションの上部に表示されます。

1. 個々のフィルターを削除するには、**[!UICONTROL FILTERING BY:]** に一覧表示されているフィルターで ![&#x200B; 閉じる &#x200B;](/help/assets/icons/Close.svg) を選択します。

1. **[!UICONTROL Clear All]** を使用すると、すべてのフィルターをすばやくクリアできます。

![&#x200B; 統一データの概要 &#x200B;](/help/assets/harmonized-data-overview.png)


## ビジュアライゼーションの設定

各ビジュアライゼーションを設定できます。

* KPI ステータスカードのビジュアライゼーションで、次の操作を行います。

   1. コンテキストメニューから ![&#x200B; 編集 &#x200B;](/help/assets/icons/Edit.svg) および ![&#x200B; 編集 &#x200B;](/help/assets/icons/Edit.svg)**[!UICONTROL Edit data]** を選択します。

   1. **[!UICONTROL KPI status card]** ダイアログで、次の手順を実行します。

      1. リストから **[!UICONTROL KPI]** を選択します。

      1. 「**[!UICONTROL Apply]**」を選択すると、カードに変更が適用されます。 「**[!UICONTROL Cancel]**」を選択すると、変更がキャンセルされます。

* その他の設定可能なビジュアライゼーションでは、次の操作を行います。

   1. コンテキストメニューから ![&#x200B; 編集 &#x200B;](/help/assets/icons/Edit.svg) および ![&#x200B; 編集 &#x200B;](/help/assets/icons/Edit.svg)**[!UICONTROL Edit data]** を選択します。

   1. **[!UICONTROL Edit Data]** ダイアログで、次の手順を実行します。

      1. **[!UICONTROL Select a metric]** から指標（例：**[!UICONTROL Impressions]**）を選択します。
      1. **[!UICONTROL Select category]** からカテゴリ（例：**[!UICONTROL Media types]**）を選択します。
      1. （オプション） **[!UICONTROL Select second category (optional)]** から 2 番目のカテゴリ（例：**[!UICONTROL Traffic sources]**）を選択します。
      1. **[!UICONTROL Select analysis type]** で分析タイプとして ![Clock](/help/assets/icons/Clock.svg) **[!UICONTROL Time]** または ![Calculator](/help/assets/icons/Calculator.svg) **[!UICONTROL Total]** を選択します。

         ![Clock](/help/assets/icons/Clock.svg) **[!UICONTROL Time]** を選択すると、時間頻度を指定できます。 **[!UICONTROL Select time frequency]** から「**[!UICONTROL Daily]**」、「**[!UICONTROL Weekly]**」、「**[!UICONTROL Monthly]**」または「**[!UICONTROL Quarterly]**」を選択します。

         [!UICONTROL Preview Area] ージ内の現在の選択の更新されたプレビューと、[!UICONTROL Current] の下の現在のビジュアライゼーションが表示されます。

         ![&#x200B; 統一データウィジェットを編集 &#x200B;](/help/assets/edit-harmonized-data-widget.png)

         データが利用できないのでプレビューをレンダリングできない場合は、![&#x200B; データエラー &#x200B;](/help/assets/icons/DataUnavailable.svg) [!UICONTROL Insights Not Available] - [!UICONTROL Harmonized fields are not available] が表示されます。

      1. 「**[!UICONTROL Apply]**」を選択して、ビジュアライゼーションに変更を適用します。 現在のビジュアライゼーションに対して行われた変更をキャンセルするには、「**[!UICONTROL Cancel]**」を選択します。
