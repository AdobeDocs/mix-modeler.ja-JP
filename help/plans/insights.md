---
title: プランインサイト
description: Mix Modelerでプランのインサイトを確認し、プランを編集する方法を説明します。
feature: Plans
exl-id: 91385595-284f-4fcb-b54b-9539905e552b
source-git-commit: f0871834ec665c907caf0af3edeeed4fb2549a58
workflow-type: tm+mt
source-wordcount: '1134'
ht-degree: 0%

---

# プランインサイト


[!UICONTROL Plan insights] では、プランのインサイトが作成され、プランのベースとなる [!UICONTROL Model]、[!UICONTROL Data range] および [!UICONTROL Plan target] が表示されます。


インサイトが作成されると、次の要素で構成されるプランの概要が表示されます。

- プランのベースとなる [!UICONTROL Model]、[!UICONTROL Data range] および [!UICONTROL Plan target] を表示するヘッダー。
   - 目標ベースのプランを定義した場合、バッジにターゲットのステータスが示されます。可能なオプションは次のとおりです。

      - [!BADGE Target 達成可能 &#x200B;]{type=Positive}
      - [!BADGE Target 実現不可能 &#x200B;]{type=Negative}

   - ![ChevronDown](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Show more]** を選択すると、詳細が表示されます。

- [[!UICONTROL Forecasted paid channel ROI] ビジュアライゼーション](#forecasted-paid-channel-spend-and-roi)
- [[!UICONTROL Forecasted revenue] ビジュアライゼーション](#forecasted-revenue)
- [[!UICONTROL Forecasted conversion] ビジュアライゼーション](#forecasted-conversions)
- [[!UICONTROL Marginal channel return] ビジュアライゼーション](#marginal-channel-return)
- 計画 [[!UICONTROL Data range breakdown] 表 ](#date-range-breakdown)、次の列を表示

   - チャネル
   - ROI
   - 公認会計士
   - 収益
   - コンバージョン目標
   - 費用

インターフェイスを閉じるには、「**[!UICONTROL Close]**」を選択します。

プランの ROI の表示方法を変更するには、**[!UICONTROL View ROI]** で **[!UICONTROL X]** または **[!UICONTROL &#x200B; %]** を選択します。

## 予測された有料チャネル支出と ROI

このビジュアライゼーションでは、モデル、日付範囲、予算に基づいて、有料チャネルの予測支出と投資回収率の散布図が表示されます。

![ 予測された有料チャネル支出と ROI ビジュアライゼーション ](../assets/overview-plan-forecasted-paid-channel-send-roi.png)


## 予測収益

この棒グラフビジュアライゼーションには、モデル、日付範囲、予算に基づいて、チャネルの予測収益が表示されます。

![ 予測収益ビジュアライゼーション ](../assets/overview-plan-forecasted-revenue.png)


## 予測コンバージョン

この棒グラフビジュアライゼーションは、モデル、日付範囲および予算に基づいて、チャネルの予測コンバージョンを表示します。

![ 予測コンバージョンビジュアライゼーション ](../assets/overview-plan-forecasted-conversions.png)


## マージナルチャネル再来訪

この折れ線グラフビジュアライゼーションには、選択したチャネルのマージナル帰還曲線と、**[!UICONTROL Marginal break-even]** と **[!UICONTROL Return point]** のインジケーターが表示されます。 このビジュアライゼーションは、チャネルの支出が限界損益分岐点に到達するまでにどの程度推移しているかを理解するのに役立ちます。 そして、チャネルの費用を増やす余地があるかどうか、またはチャネルの費用効率を向上させるためにチャネルへの費用を減らす必要があるかどうか。

![ マージナルチャネル再来訪の視覚化 ](../assets/overview-plan-marginal-channel-return.png)

ビジュアライゼーションの特定のチャネルを選択するには、チャネル ドロップダウ **[!UICONTROL View]** メニューからチャネルを選択します。


## 日付範囲の分類

[!UICONTROL Date range breakdown] の表には、[!UICONTROL ROI]、[!UICONTROL Revenue]、[!UICONTROL CPA]、[!UICONTROL Conversions] および [!UICONTROL Spend] のチャネルごとの詳細な詳細データが表示されます。

![ 日付範囲の分類テーブル ](../assets/overview-plan-date-range-breakdown.png)

1. 日付範囲の分類のデータを含んだ CSV ファイルをダウンロードするには、「![ ダウンロード ](/help/assets/icons/Download.svg)」 **[!UICONTROL Download CSV]** 選択します。 コンテキストメニューから、次の操作を行います。

   - CSV 形式の詳細なデータについては、「![ ダウンロード ](/help/assets/icons/Download.svg)」 **[!UICONTROL Detailed CSV]** を選択してください。
   - CSV 形式の概要データの場合は、「![ ダウンロード ](/help/assets/icons/Download.svg)」 **[!UICONTROL Summary CSV]** を選択します。

   詳細データは、週別にキー設定された粒度の高いデータです。 概要データは、モデルが指定した日付範囲でキー設定されたデータです。

1. チャネルのカテゴリ別に日付範囲の分類を表示するには、「**[!UICONTROL View]**」の選択から「**[!UICONTROL All channels]**」、「**[!UICONTROL Paid channels]**」または「**[!UICONTROL Non-paid channels]**」を選択します。


## プランを編集

プランを編集するには、「![ 編集 ](/help/assets/icons/Edit.svg)」を選択 **[!UICONTROL Edit plan]** ます。

1. **[!UICONTROL Spend selection]** セクションの各予算の日付範囲で、![ 山形 ](/help/assets/icons/ChevronRight.svg) を使用して、そのデータ範囲のチャネル配分表示を開きます。

   過去のマーケティング費用データとインサイトを使用する場合は、履歴参照データを使用できます。 次の履歴リファレンスデータを考慮します。

   - パフォーマンスの高いチャネルとパフォーマンスの低いチャネルを強調することで、予算割り当てを改善します。
   - トレンド分析をサポートします。
   - 効果的な戦略を特定し、計画の設定時にミスを避けます。

   過去の参照期間を選択した場合は、以前の支出パターンの環境設定に合わせて、Mix Modelerの計画機能で期待通りの計画を作成できます。 これらの計画は、最終的に関係者の信頼を高め、マーケティング計画が戦略的かつ効率的であり、これらの計画が実績データおよびビジネスニーズに基づいていることを確認する必要があります。

   ![ 費用の選択 ](/help/assets/plan-spend-selection.png)

   1. 「**[!UICONTROL Spend pattern]**」を選択します。

      - デフォルトオプションは **[!UICONTROL Automatic]** です。
      - 「**[!UICONTROL Historical reference]**」を選択し、**[!UICONTROL Start date]** を入力して、Mix Modelerで既に使用可能な過去のマーケティング費用データを参照します。 選択したデータ範囲に基づいて、**[!UICONTROL End date]** が自動的に決定されます。 提案された開始日は、利用可能な過去のマーケティング費用データのうち最初に利用できるものです。 存在しない履歴参照期間を選択したことを示すために、![AlertRed](/help/assets/icons/AlertRed.svg) が表示されます。


   1. 各チャネルの予算を変更するには、「**[!UICONTROL Min]**」と「**[!UICONTROL Max]**」の値を変更するか、スライダーを使用します。

   1. 通貨またはパーセンテージの入力を切り替えるには、「**[!UICONTROL View spend by]**」で「**[!UICONTROL $]**」または「**[!UICONTROL %]**」を選択します。

   1. プランの詳細を編集するには、**[!UICONTROL Edit details]** を選択します。

      1. **[!UICONTROL Setup]** のセクションで以下を実行します。

         1. **[!UICONTROL Plan name]** （例：`Demo plan`）を入力します。 **[!UICONTROL Description]** （例：`Demo plan for Luma company`）を入力します。
         1. **[!UICONTROL _オプショ&#x200B;**&#x200B;[!UICONTROL Model]&#x200B;**を選択…_.]**

            ![ プラン設定 ](/help/assets/plan-setup.png)

      1. 「**[!UICONTROL Goal]**」セクションで、計画を最適化する目標を選択します。 以下から選択できます
         - **[!UICONTROL I have a budget to spend]**

           ![ 計画予算 ](../assets/plan-budget.png)

           このオプションを使用すると、1 つ以上の日付範囲の予算を入力できます。

            1. **[!UICONTROL Optimize]** コンテナで以下を実行します。
               1. コンバージョンをコンバージョ **[!UICONTROL Select conversion]** ドロップダウンメニューから選択します。
               1. **[!UICONTROL Select model]** ドロップダウンメニューからモデルを選択します。
            1. 日付を入力するか、![ カレン **[!UICONTROL Date range]** ー ](/help/assets/icons/Calendar.svg) を使用して日付範囲を選択して、日付を指定します。
            1. **[!UICONTROL Budget]** を入力します。
日付範囲を追加するには、それぞれ予算と共に ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]** を選択します。
日付範囲および関連する予算を削除するには、「![ クローズ ](/help/assets/icons/Close.svg)」を選択します。
            1. オプションの最大予算を定義して計画を制約する手順は、次のとおりです。
               1. **[!UICONTROL Maximize budget]** をオンにします。
               1. 最大予算の金額を指定してください。 金額は、日付範囲に指定された予算の合計金額以上である必要があります。


         - **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

           ![ 目標を計画 ](../assets/plan-target.png)

            1. **[!UICONTROL Optimize]** コンテナ内
               1. コンバージョンをコンバージョ **[!UICONTROL Select conversion]** ドロップダウンメニューから選択します。
               1. **[!UICONTROL Select target metric]** ドロップダウンメニューからターゲット指標を選択します。 **[!UICONTROL Conversion]**、**[!UICONTROL CPA]**、**[!UICONTROL Revenue]**、**[!UICONTROL ROI]** から選択できます。
               1. **[!UICONTROL Select model]** ドロップダウンメニューからモデルを選択します。
            1. 日付を入力するか、![ カレンダー ](/help/assets/icons/Calendar.svg) を使用して日付範囲を選択して、日付範囲を指定します。
            1. 選択したターゲット指標の値を入力します。 例えば、**[!UICONTROL Conversion]** の場合は数値、**[!UICONTROL ROI]** の場合はパーセンテージ、**[!UICONTROL CPA]** と **[!UICONTROL Revenue]** の場合は通貨値です。
日付範囲を追加するには、それぞれターゲット指標と共に ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]** を選択します。
日付範囲および関連するターゲット指標を削除するには、「![ 閉じる ](/help/assets/icons/Close.svg)」を選択します。
            1. オプションの最大予算を定義して計画を制約する手順は、次のとおりです。
               1. **[!UICONTROL Maximize budget]** をオンにします。
               1. 最大予算の金額を指定してください。

         1. 「**[!UICONTROL Next]**」を選択すると、「**[!UICONTROL Spend selection]**」セクションに戻ります。

1. **[!UICONTROL Advanced configuration]** のセクションで以下を実行します。

   ![ 詳細設定を編集 ](../assets/edit-plan-advanced-configuration.png)

   - 計画名、モデル、日付範囲および予算合計が要約されます。

   - デフォルトでは、Mix Modelerは、最新の季節的な履歴データを使用して、コンバージョンあたりの平均売上高を自動計算します。 で **[!UICONTROL Average Revenue per conversion]**、コンバージョンごとの特定の平均売上高を定義できます。

   1. 予算の日付範囲ごとに、次の操作を行います。
      1. **[!UICONTROL Date range]** ドロップダウンメニューから日付範囲を選択します。
      1. **[!UICONTROL Average revenue]** 値を入力します。
   1. 「![AddCircle](/help/assets/icons/AddCircle.svg)」を選択し、コンバージョン単位あたりのカスタム平均売上高を追加して、日付範囲を追加します。
   1. ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) を選択して、日付範囲を削除します。

   >[!NOTE]
   >
   >モデルに収益履歴データが含まれていない場合は、予算に指定した日付範囲ごとに、コンバージョンごとの平均売上高を定義する必要があります。
   >

   - デフォルトでは、Mix Modelerは、最新の季節別の履歴データを使用してチャネルコストを自動計算します。 **[!UICONTROL Channel costs]** の中で、カスタムチャネルのコストを定義できます。

   1. モデルのチャネルごとに、カスタムチャネルコストを定義します。
      1. **[!UICONTROL Channel]** ドロップダウンメニューからチャネルを選択します。
      1. 予算の日付範囲ごとに、次の操作を行います。
         1. **[!UICONTROL Date range]** ドロップダウンメニューから日付範囲を選択します。
         1. **[!UICONTROL Average revenue]** 値を入力します。
      1. ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom average revenue per conversion unit]** を選択して、日付範囲を追加します。
      1. ![RemoveCircle](/help/assets/icons/RemoveCircle.svg) を選択して、日付範囲を削除します。

   1. ![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add custom channel cost]** を選択して、チャンネルを追加します。
   1. ![CrossSize400](/help/assets/icons/CrossSize400.svg) を選択して、カスタムチャネルを削除します。


1. プランの編集が終了したら、「**[!UICONTROL Edit]**」を選択します。

   **[!UICONTROL All changes are final]** ダイアログで、「**[!UICONTROL OK]**」を選択して、プランの現在の支出配分と ROI および収益予測を更新します。 「**[!UICONTROL Cancel]**」を選択して、プランの更新をキャンセルします。


- プランの更新をいつでもキャンセルするには、[**[!UICONTROL Cancel]**] を選択します。 **[!UICONTROL No work will be saved]** ダイアログで、「**[!UICONTROL Cancel]**」を選択してプランの作業を続行するか、「**[!UICONTROL OK]**」を選択してプランインターフェイスに戻ります。
- ウィザードに戻るには、「**[!UICONTROL Back]**」を選択します。
