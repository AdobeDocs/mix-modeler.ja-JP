---
title: プランを編集
description: Mix Modelerでプランを編集する方法を説明します。
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: 3e2330ffe0337c4ac9ef09fda3cd611656179d29
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# プランを編集

プランを編集するには、で ![プラン](../assets/icons/FileChart.svg) **[!UICONTROL Plans]** インターフェイス Mix Modelerで、名前でプランを選択します。

対象： [!UICONTROL Plan insights]をクリックすると、計画インサイトが作成され、以下が表示されます [!UICONTROL Model], [!UICONTROL Data range]、および [!UICONTROL Total budget] プランのベース。

取得が完了すると、プランの概要が次の内容で表示されます。

- [!UICONTROL Forecasted paid channel ROI] 可視化
- [!UICONTROL Forecasted revenue] 可視化
- [!UICONTROL Data range breakdown] 計画のテーブル、次の列を表示

   - チャネル
   - ROI
   - 公認会計士
   - 収益
   - コンバージョン目標
   - 費用

![プランの概要](../assets/overview-plan.png)

1. を選択 **[!UICONTROL Close]** をクリックして、計画インターフェイスに戻ります。

1. を選択 **[!UICONTROL X]** または **[!UICONTROL  %]** ～する方法について **[!UICONTROL View ROI]**.

1. 日付範囲の分類のデータを含んだ CSV ファイルをダウンロードするには、次を選択します。 ![Download](../assets/icons/Download.svg) **[!UICONTROL Download CSV]**. コンテキストメニューから、次の操作を行います。

   - を選択 ![Download](../assets/icons/Download.svg) **[!UICONTROL Detailed CSV]** 詳細なデータを CSV 形式で表示する場合、または
   - を選択 ![Download](../assets/icons/Download.svg) **[!UICONTROL Summary CSV]** （CSV 形式の概要データ用）。

   詳細データは、週別にキー設定された粒度の高いデータです。 概要データは、モデルが指定した日付範囲でキー設定されたデータです。

1. チャネルのカテゴリ別に日付範囲の分類を表示するには、次を選択します。 **[!UICONTROL All channels]**, **[!UICONTROL Paid channels]**、または **[!UICONTROL Non-paid channels]** から **[!UICONTROL View]** 選択。

1. プランを編集するには、を選択します **[!UICONTROL Edit plan]**:

   1. が含まれる **[!UICONTROL Spend selection]** セクションでは、予算の日付範囲ごとに次を使用します ![山形](../assets/icons/ChevronRight.svg) をクリックして、そのデータ範囲のチャネル配信ビューを開きます。

   1. 各チャネルの予算を変更するには、の値を変更します **[!UICONTROL Min]** および **[!UICONTROL Max]** または、スライダーを使用します。

   1. 通貨またはパーセンテージの入力を切り替えるには、 **[!UICONTROL $]** または **[!UICONTROL %]** （用） **[!UICONTROL View spend by]**.

      ![費用の選択](../assets/spend-selection.png)

   1. プランの詳細を編集するには、次を選択します **[!UICONTROL Edit details]**:

      1. が含まれる **[!UICONTROL Setup]** セクションを変更する場合は、 **[!UICONTROL Plan name]** および **[!UICONTROL Description]**.

      1. が含まれる **[!UICONTROL Budget]** セクション：

         1. を変更する **[!UICONTROL Date range]** 日付を入力するか、を使用して日付範囲を選択して、プランの 1 つ以上の日付範囲に対して ![カレンダー](../assets/icons/Calendar.svg).

         1. を変更する **[!UICONTROL Budget]** プランの 1 つ以上の日付範囲。

         日付範囲を追加するには、日付範囲と予算を選択します。 ![CalendarAdd](../assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

         日付範囲および関連する予算を削除するには、 ![閉じる](../assets/icons/Close.svg).

         最大予算を定義する手順は、次のとおりです。

         1. 切り替え **[!UICONTROL Maximize budget]** オン。
         1. 最大予算の金額を指定してください。 金額は、日付範囲に指定された予算の合計金額以上である必要があります。

      1. を選択 **[!UICONTROL Next]** に戻る **[!UICONTROL Spend]** セクション。 を選択 **[!UICONTROL Cancel]** 計画の概要に戻る

         ![プランの詳細](../assets/plan-details.png)


1. プランの編集が終了したら、 **[!UICONTROL Edit]**.

   が含まれる **[!UICONTROL All changes are final]** ダイアログ、選択 **[!UICONTROL OK]** 計画の現在の支出配分と ROI および収益予測を更新します。 を選択 **[!UICONTROL Cancel]** ：計画の更新をキャンセルします。

1. プランの更新をキャンセルするには、次を選択します： **[!UICONTROL Cancel]**.

   が含まれる **[!UICONTROL No work will be saved]** ダイアログ、選択 **[!UICONTROL Cancel]** プランの作業を続行するには、を選択するか、 **[!UICONTROL OK]** をクリックして、計画インターフェイスに戻ります。
