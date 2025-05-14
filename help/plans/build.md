---
title: プランの作成
description: Mix Modelerでプランを作成する方法を説明します。
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 3545a7045478108db4d9f6bb87df679bfede5a45
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%

---


# プランの作成

Mix Modelerでは、プランキャンバスを使用してプランを作成します。 プランキャンバスでは、プランの詳細と予算、およびプランに使用する基盤となるモデルを設定できます。 詳細、予算、モデルを指定したら、AI が推奨するプランを選択するか、チャネル別に費用を編集できます。

プランを作成するには、Mix Modelerの ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** インターフェイスで「**[!UICONTROL Create plan]**」を選択します。


1. **[!UICONTROL Plan creation]** 画面で、次の操作を行います。

   1. **[!UICONTROL Setup]** のセクションで以下を実行します。

      1. **[!UICONTROL Plan name]** （例：`Demo plan`）を入力します。 **[!UICONTROL Description]** （例：`Demo plan for Luma company`）を入力します。
      1. **[!UICONTROL _オプショ&#x200B;**[!UICONTROL Model]**を選択…_.]**
      1. ![ リンクアウト ](/help/assets/icons/LinkOut.svg)**[!UICONTROL Create model]** を選択して、プランの作成内から直接モデルを作成できます。 これにより、ブラウザーに新しいタブが開き、[ モデル ](../models/overview.md) インターフェイスが表示されます。

         ![ プラン設定 ](/help/assets/plan-setup.png)

   1. **[!UICONTROL Budget]** のセクションで以下を実行します。

      1. 日付を入力するか、![ カレンダー ](/help/assets/icons/Calendar.svg) を使用して日付範囲を選択して、日付範囲を指定します。
      1. 予算を入力します。

      日付範囲を追加するには、それぞれ予算と共に ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]** を選択します。

      日付範囲および関連する予算を削除するには、「![ クローズ ](/help/assets/icons/Close.svg)」を選択します。

      指定した最大予算を定義する手順は、次のとおりです。

      1. **[!UICONTROL Maximize budget]** をオンにします。
      1. 最大予算の金額を指定してください。 金額は、日付範囲に指定された予算の合計金額以上である必要があります。

         ![ 計画予算 ](/help/assets/plan-budget.png)

   1. **[!UICONTROL Next]** を選択します。

1. **[!UICONTROL Done with all required fields]** ダイアログで、次の手順を実行します。

   ![ 計画完了 ](/help/assets/plan-done-required-fields.png)

   * 予測 ROI を持つ AI 推奨プランを生成する場合は、「![ 新規プラン ](../assets/icons/NewPlan.svg)**[!UICONTROL Create plan now]**」を選択します。

     「**[!UICONTROL OK]**」を選択します。 プランが作成されます。


   * 予測 ROI を持つプランを作成する前にチャネル予算を編集して詳細設定を定義する場合は、「![ テーブル編集 ](/help/assets/icons/TableEdit.svg)」 **[!UICONTROL Edit channel budgets first]** を選択します。

     「**[!UICONTROL OK]**」を選択すると、次の手順で **[!UICONTROL Spend selection]** でのチャネル支出を定義できます。



1. **[!UICONTROL Spend selection]** セクションの各予算の日付範囲で、![ 山形 ](/help/assets/icons/ChevronRight.svg) の上部を使用して、そのデータ範囲のチャネル分布ビューを開きます。

   1. 各チャネルの予算を定義するには、**[!UICONTROL Min]** と **[!UICONTROL Max]** の値を入力するか、スライダーを使用します。

   1. 通貨またはパーセンテージの入力を切り替えるには、「**[!UICONTROL View spend by]**」で「**[!UICONTROL $]**」または「**[!UICONTROL %]**」を選択します。

      ![ 費用の選択 ](/help/assets/plan-spend-selection.png)

   1. **[!UICONTROL Next]** を選択します。


1. 「**[!UICONTROL Advanced configurations]**」セクションでは、オプションで詳細設定を入力できます。

   ![ 計画の概要 ](../assets/plan-advanced-configurations.png)

   * 計画名、モデル、日付範囲および予算合計が要約されます。

   * デフォルトでは、Mix Modelerは、最新の季節的な履歴データを使用して、コンバージョンあたりの平均売上高を自動計算します。 で **[!UICONTROL Average Revenue per conversion]**、コンバージョンごとの特定の平均売上高を定義できます。

      1. 予算の日付範囲ごとに、次の操作を行います。

         1. **[!UICONTROL Date range]** ドロップダウンメニューから日付範囲を選択します。
         1. **[!UICONTROL Average revenue]** 値を入力します。

      1. 「![AddCircle](/help/assets/icons/AddCircle.svg)」を選択し、コンバージョン単位あたりのカスタム平均売上高を追加して、日付範囲を追加します。
      1. ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) を選択して、日付範囲を削除します。

     >[!NOTE]
     >
     >モデルに収益履歴データが含まれていない場合は、予算に指定した日付範囲ごとに、コンバージョンごとの平均売上高を定義する必要があります。
     >

   * デフォルトでは、Mix Modelerは、最新の季節別の履歴データを使用してチャネルコストを自動計算します。 **[!UICONTROL Channel costs]** の中で、カスタムチャネルのコストを定義できます。

      1. モデルのチャネルごとに、カスタムチャネルコストを定義します。

         1. **[!UICONTROL Channel]** ドロップダウンメニューからチャネルを選択します。
         1. 予算の日付範囲ごとに、次の操作を行います。
            1. **[!UICONTROL Date range]** ドロップダウンメニューから日付範囲を選択します。
            1. **[!UICONTROL Average revenue]** 値を入力します。
         1. ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** を選択して、日付範囲を追加します。
         1. ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) を選択して、日付範囲を削除します。

      1. ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** を選択して、チャンネルを追加します。
      1. ![CrossSize400](/help/assets/icons/CrossSize400.svg) を選択して、カスタムチャネルを削除します。


   1. 終了したら「**[!UICONTROL Create]**」を選択します。

   1. **[!UICONTROL Create plan]** ダイアログで、「**[!UICONTROL Create plan]**」を選択してプランを作成します。 「**[!UICONTROL Cancel]**」を選択して、プランの作成をキャンセルします。 確認を求める **[!UICONTROL No work is saved]** ダイアログが表示されます。

