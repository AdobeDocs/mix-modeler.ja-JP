---
title: プランを作成
description: Mix Modelerでプランを作成する方法を説明します。
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# プランを作成

Mix Modelerでは、プランキャンバスを使用してプランを作成します。 プランキャンバスでは、プランの詳細と予算、およびプランに使用する基盤となるモデルを設定できます。 詳細、予算、モデルを指定したら、AI が推奨するプランを選択するか、チャネル別に費用を編集できます。

プランを作成するには、で ![プラン](/help/assets//icons/FileChart.svg) **[!UICONTROL Plans]** Mix Modelerのインターフェイスで、を選択します **[!UICONTROL Open plan canvas]**.

1. プラン作成画面で、次の操作を行います。

   1. が含まれる **[!UICONTROL Setup]** セクション

      1. を入力 **[!UICONTROL Plan name]**、例： `Demo plan`. を入力 **[!UICONTROL Description]**、例： `Demo plan for Luma company`.
      1. を選択 **[!UICONTROL Model]** から **[!UICONTROL _オプションを選択…_.]**.
      1. 以下を選択できます。 ![LinkOut](/help/assets//icons/LinkOut.svg) **[!UICONTROL Create model]** を使用して、プラン作成内から直接モデルを作成できます。 ブラウザーに新しいタブが開き、 [モデル](../models/overview.md) インターフェイス。

         ![プラン設定](/help/assets//plan-setup.png)

   1. が含まれる **[!UICONTROL Budget]** セクション：

      1. 日付を入力するか、を使用して日付範囲を選択して、日付範囲を指定します。 ![カレンダー](/help/assets//icons/Calendar.svg).
      1. 予算を入力します。

      日付範囲を追加するには、日付範囲と予算を選択します。 ![CalendarAdd](/help/assets//icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      日付範囲および関連する予算を削除するには、 ![閉じる](/help/assets//icons/Close.svg).

      指定した最大予算を定義する手順は、次のとおりです。

      1. 切り替え **[!UICONTROL Maximize budget]** オン。
      1. 最大予算の金額を指定してください。 金額は、日付範囲に指定された予算の合計金額以上である必要があります。

         ![計画予算](/help/assets//plan-budget.png)

   1. **[!UICONTROL Next]** を選択します。

1. が含まれる **[!UICONTROL Done with all required fields]** ダイアログ：

   ![計画が完了しました](/help/assets//plan-done-required-fields.png)

   * 選択 <img src="/help/assets//icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** 予測 ROI を持つ AI 推奨プランを生成する場合。

     を選択 **[!UICONTROL OK]**. プランが作成されます。


   * を選択 ![TableEdit](/help/assets//icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** 予測 ROI を持つプランを作成する前にチャネル予算を編集する場合。

     を選択 **[!UICONTROL OK]**&#x200B;でチャネル支出を定義できるようにします。 **[!UICONTROL Spend selection]** 次の手順で行います。



1. が含まれる **[!UICONTROL Spend selection]** セクションでは、予算の日付範囲ごとに次を使用します ![山形](/help/assets//icons/ChevronRight.svg) トップそのデータ範囲のチャネル配信ビューを開きます。

   1. 各チャネルの予算を定義するには、次の値を入力します **[!UICONTROL Min]** および **[!UICONTROL Max]** または、スライダーを使用します。

   1. 通貨またはパーセンテージの入力を切り替えるには、 **[!UICONTROL $]** または **[!UICONTROL %]** （用） **[!UICONTROL View spend by]**.

      ![費用の選択](/help/assets//plan-spend-selection.png)

   1. 終了したら「**[!UICONTROL Create]**」を選択します。

   1. が含まれる **[!UICONTROL Create plan]** ダイアログ、選択 **[!UICONTROL Create plan]** をクリックしてプランを作成します。 を選択 **[!UICONTROL Cancel]** ：プランの作成をキャンセルします。 A **[!UICONTROL No work is saved]** 確認のダイアログが表示されます。
