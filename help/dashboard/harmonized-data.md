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

ウィジェットに表示されるデータの日付範囲を変更するには、開始日と終了日を手動で入力するか、![ カレンダー ](/help/assets//icons/Calendar.svg) を使用して期間を選択します。

## データフィルター

![ フィルター ](/help/assets//icons/Filter.svg) データペインを使用して、すべてのウィジェットに表示される **[!UICONTROL Category Filters]** ータをフィルタリングできます。

各カテゴリに対して 1 つ以上のフィルターを選択します（**[!UICONTROL Brands]**、**[!UICONTROL Campaigns]**、**[!UICONTROL Cannels Type]**、**[!UICONTROL Conversion types]**、**[!UICONTROL Datasets]**、**[!UICONTROL Media types]**、**[!UICONTROL Source types]** および **[!UICONTROL Traffic Source]**）。

選択したフィルターは、**[!UICONTROL FILTERING BY:]** のウィジェットの上部に表示されます。

1. 個々のフィルターを削除するには、**[!UICONTROL FILTERING BY:]** に一覧表示されているフィルターで ![ 閉じる ](/help/assets//icons/Close.svg) を選択します。

1. **[!UICONTROL Clear All]** を使用すると、すべてのフィルターをすばやくクリアできます。

![ 統一データの概要 ](/help/assets//harmonized-data-overview.png)


## ウィジェットの設定

各ウィジェットを設定できます。

* KPI ステータスカードウィジェットで：

   1. コンテキストメニューから ![ 編集 ](/help/assets//icons/Edit.svg) および ![ 編集 ](/help/assets//icons/Edit.svg)**[!UICONTROL Edit data]** を選択します。

   1. **[!UICONTROL KPI status card]** ダイアログで、次の手順を実行します。

      1. リストから **[!UICONTROL KPI]** を選択します。

      1. 「**[!UICONTROL Apply]**」を選択すると、カードに変更が適用されます。 「**[!UICONTROL Cancel]**」を選択すると、変更がキャンセルされます。

* その他の設定可能なウィジェットでは、

   1. コンテキストメニューから ![ 編集 ](/help/assets//icons/Edit.svg) および ![ 編集 ](/help/assets//icons/Edit.svg)**[!UICONTROL Edit data]** を選択します。

   1. **[!UICONTROL Edit Data]** ダイアログで、次の手順を実行します。

      1. **[!UICONTROL Select a metric]** から指標（例：**[!UICONTROL Impressions]**）を選択します。
      1. **[!UICONTROL Select category]** からカテゴリ（例：**[!UICONTROL Media types]**）を選択します。
      1. （オプション） **[!UICONTROL Select second category (optional)]** から 2 番目のカテゴリ（例：**[!UICONTROL Traffic sources]**）を選択します。
      1. **[!UICONTROL Select analysis type]** で分析タイプとして ![Clock](/help/assets//icons/Clock.svg) **[!UICONTROL Time]** または ![Calculator](/help/assets//icons/Calculator.svg) **[!UICONTROL Total]** を選択します。

         ![Clock](/help/assets//icons/Clock.svg) **[!UICONTROL Time]** を選択すると、時間頻度を指定できます。 **[!UICONTROL Select time frequency]** から「**[!UICONTROL Daily]**」、「**[!UICONTROL Weekly]**」、「**[!UICONTROL Monthly]**」または「**[!UICONTROL Quarterly]**」を選択します。

         [!UICONTROL Preview Area] ージ内の現在の選択の更新されたプレビューと、[!UICONTROL Current] の下の現在のウィジェットが表示されます。

         ![ 統一データウィジェットを編集 ](/help/assets//edit-harmonized-data-widget.png)

         データが利用できないのでプレビューをレンダリングできない場合は、![ データエラー ](/help/assets//icons/DataUnavailable.svg) [!UICONTROL Insights Not Available] - [!UICONTROL Harmonized fields are not available] が表示されます。

      1. 「**[!UICONTROL Apply]**」を選択して、変更をウィジェットに適用します。 現在のウィジェットに加えられた変更をキャンセルするには、「**[!UICONTROL Cancel]**」を選択します。
