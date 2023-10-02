---
title: プランの作成
description: プランを作成する方法については、Mix Modelerを参照してください。
feature: Plans
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 1%

---


# プランの作成

Mix Modelerで、プランキャンバスを使用してプランを作成します。 「計画」キャンバスで、計画および計画に使用する基になるモデルの詳細と予算を設定できます。 詳細、予算、モデルを指定したら、AI 推奨プランを実行するか、チャネル別に支出を編集できます。

プランを作成するには、 ![PLan](../assets/icons/FileChart.svg) **[!UICONTROL Plans]** インタフェース (Mix Modeler): **[!UICONTROL Open plan canvas]**.

1. プラン作成画面で、次の操作をおこないます。

   1. Adobe Analytics の **[!UICONTROL Setup]** セクション

      1. を入力します。 **[!UICONTROL Plan name]**&#x200B;例： `Demo plan`. を入力します。 **[!UICONTROL Description]**&#x200B;例： `Demo plan for Luma company`.
      1. を選択します。 **[!UICONTROL Model]** から **[!UICONTROL _オプションを選択…_.]**.
      1. 次の項目を選択できます。 ![LinkOut](../assets/icons/LinkOut.svg) **[!UICONTROL Create model]** をクリックして、プラン作成内から直接モデルを作成します。

         ![プラン設定](../assets/plan-setup.png)

   1. Adobe Analytics の **[!UICONTROL Budget]** セクション：

      1. 日付を入力するか、 ![カレンダー](../assets/icons/Calendar.svg).
      1. 予算を入力します。

      予算を含む日付範囲をさらに追加するには、「 ![CalendarAdd](../assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]**.

      日付範囲と関連予算を削除するには、 ![閉じる](../assets/icons/Close.svg).

      指定した最大予算を定義する手順は、次のとおりです。

      1. 切り替え **[!UICONTROL Maximize budget]** オン。
      1. 最大予算額を指定します。 金額は、日付範囲に指定された予算の合計金額以上にする必要があります。

         ![予算の計画](../assets/plan-budget.png)

   1. **[!UICONTROL Next]** を選択します。

1. Adobe Analytics の **[!UICONTROL Done with all required fields]** ダイアログ：

   ![計画完了](../assets/plan-done-required-fields.png)

   * 選択 <img src="../assets/icons/NewPlan.svg" width="25" /> **[!UICONTROL Create plan now]** 予測された ROI を含む AI 推奨プランを生成する場合。

     **[!UICONTROL OK]** を選択します。プランが作成されました。


   * 選択 ![TableEdit](../assets/icons/TableEdit.svg) **[!UICONTROL Edit channel budgets first]** 予測された ROI を使用して計画を作成する前にチャネル予算を編集する場合。

     選択 **[!UICONTROL OK]**&#x200B;を使用して、 **[!UICONTROL Spend selection]** 次の手順で使用します。



1. Adobe Analytics の **[!UICONTROL Spend selection]** セクションで、予算の日付範囲ごとに、 ![シェブロン](../assets/icons/ChevronRight.svg) 上部で、そのデータ範囲のチャネル配分表示を開きます。

   1. 各チャネルの予算を定義するには、次の値を入力します： **[!UICONTROL Min]** および **[!UICONTROL Max]** または、スライダを使用します。

   1. 通貨入力と割合入力を切り替えるには、「 **[!UICONTROL $]** または **[!UICONTROL %]** 対象： **[!UICONTROL View spend by]**.

      ![支出の選択](../assets/plan-spend-selection.png)

   1. 終了したら「**[!UICONTROL Create]**」を選択します。

   1. Adobe Analytics の **[!UICONTROL Create plan]** ダイアログ、選択 **[!UICONTROL Create plan]** をクリックして、プランを作成します。 選択 **[!UICONTROL Cancel]** ：プランの作成をキャンセルします。



