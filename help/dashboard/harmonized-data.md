---
title: 統一データ概要ダッシュボード
description: Mix Modelerでの統一データ概要ダッシュボードの使用方法を説明します。
feature: Dashboard, Harmonized Data
exl-id: fbb01613-d648-4db1-a782-a7720b7a03ad
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# 統一データの概要

Mix Modelerの概要の「統一データ」タブには、取り込まれたデータおよび統一データ設定の一部として使用するように設定した統一データに関するインサイトが表示されます。

この概要には、4 つの KPI ステータスカードウィジェット（一番上の行）と 6 つの他の設定可能なウィジェットが表示されます。

ウィジェットに表示されるデータの日付範囲を変更するには、開始日と終了日を手動で入力するか、を使用して期間を選択します ![カレンダー](/help/assets//icons/Calendar.svg).

## データフィルター

を使用して、すべてのウィジェットに表示されるデータをフィルタリングできます ![フィルター](/help/assets//icons/Filter.svg) **[!UICONTROL Category Filters]** ペイン。

各カテゴリに 1 つ以上のフィルターを選択します（**[!UICONTROL Brands]**, **[!UICONTROL Campaigns]**, **[!UICONTROL Cannels Type]**, **[!UICONTROL Conversion types]**, **[!UICONTROL Datasets]**, **[!UICONTROL Media types]**, **[!UICONTROL Source types]**、および **[!UICONTROL Traffic Source]**）に設定します。

選択したフィルターは、ウィジェットの上部にある **[!UICONTROL FILTERING BY:]**.

1. 個々のフィルターを削除するには、 ![閉じる](/help/assets//icons/Close.svg) フィルターで、にリストされています **[!UICONTROL FILTERING BY:]**.

1. を使用して、すべてのフィルターをすばやくクリアできます **[!UICONTROL Clear All]**.

![統一データの概要](/help/assets//harmonized-data-overview.png)


## ウィジェットの設定

各ウィジェットを設定できます。

* KPI ステータスカードウィジェットで：

   1. を選択 ![編集](/help/assets//icons/Edit.svg) および ![編集](/help/assets//icons/Edit.svg) **[!UICONTROL Edit data]** コンテキストメニューから。

   1. が含まれる **[!UICONTROL KPI status card]** ダイアログ：

      1. を選択 **[!UICONTROL KPI]** リストから。

      1. を選択 **[!UICONTROL Apply]** 変更をカードに適用します。 を選択 **[!UICONTROL Cancel]** 変更をキャンセルします。

* その他の設定可能なウィジェットでは、

   1. を選択 ![編集](/help/assets//icons/Edit.svg) および ![編集](/help/assets//icons/Edit.svg) **[!UICONTROL Edit data]** コンテキストメニューから。

   1. が含まれる **[!UICONTROL Edit Data]** ダイアログ：

      1. から指標を選択 **[!UICONTROL Select a metric]**、例： **[!UICONTROL Impressions]**.
      1. からカテゴリを選択 **[!UICONTROL Select category]**、例： **[!UICONTROL Media types]**.
      1. （オプション） 2 つ目のカテゴリを次から選択します **[!UICONTROL Select second category (optional)]**、例： **[!UICONTROL Traffic sources]**.
      1. を選択 ![時計](/help/assets//icons/Clock.svg) **[!UICONTROL Time]** または ![計算機](/help/assets//icons/Calculator.svg) **[!UICONTROL Total]** 分析タイプとしてを使用します **[!UICONTROL Select analysis type]**.

         を選択する場合 ![時計](/help/assets//icons/Clock.svg) **[!UICONTROL Time]**&#x200B;の場合、時間頻度を指定できます。 を選択 **[!UICONTROL Daily]**, **[!UICONTROL Weekly]**, **[!UICONTROL Monthly]** または **[!UICONTROL Quarterly]** から **[!UICONTROL Select time frequency]**.

         現在の選択の更新されたプレビューが [!UICONTROL Preview Area] とその下にある現在のウィジェット [!UICONTROL Current].

         ![統一データウィジェットを編集](/help/assets//edit-harmonized-data-widget.png)

         データが使用できないのでプレビューをレンダリングできない場合は、次のように表示されます ![データエラー](/help/assets//icons/DataUnavailable.svg) [!UICONTROL Insights Not Available] - [!UICONTROL Harmonized fields are not available].

      1. を選択 **[!UICONTROL Apply]** 変更をウィジェットに適用します。 を選択 **[!UICONTROL Cancel]** 現在のウィジェットに加えられた変更をキャンセルします。
