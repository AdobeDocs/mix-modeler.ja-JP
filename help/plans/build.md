---
title: プランの作成
description: Mix Modelerでプランを作成する方法を説明します。
feature: Plans
exl-id: 6d61d0b2-5871-4d00-9a35-73fff0a1c3e5
source-git-commit: 20985d0f9e9d2990b881ab448f6475e4bb8244d1
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 1%

---


# プランの作成

Mix Modelerでは、プランウィザードを使用してプランを作成します。 プランウィザードでは、プランの詳細と予算またはターゲット指標、およびプランで使用する基になるモデルを設定できます。 詳細、予算、ターゲット指標およびモデルを指定したら、AI が推奨するプランを選択するか、チャネル別に費用を編集できます。 コンバージョンあたりの平均売上高とチャネルコストに関する高度な設定を定義するオプションがあります。

計画を最大化する目標を定義する必要があります。 この目標は、支出可能な予算または達成したいターゲットのいずれかです。 目標がターゲットの場合は、さらに、コンバージョン、売上高、CPA または ROI のターゲット指標の値を指定する必要があります。

プランを作成するには、Mix Modelerの ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** インターフェイスで「**[!UICONTROL Create plan]**」を選択します。


1. **[!UICONTROL Plan creation]** 画面で、次の操作を行います。

   1. **[!UICONTROL Setup]** のセクションで以下を実行します。

      1. **[!UICONTROL Plan name]** （例：`Goal based plan`）を入力します。 **[!UICONTROL Description]** （例：`A goal based plan`）を入力します。
      1. **[!UICONTROL Model]** オプショ **[!UICONTROL _を選択…_.]**

         ![&#x200B; プラン設定 &#x200B;](/help/assets/plan-setup.png)

   1. 「**[!UICONTROL Goal]**」セクションで、計画を最適化する目標を選択します。 以下から選択できます

      * **[!UICONTROL I have a budget to spend]**

        ![&#x200B; 計画予算 &#x200B;](../assets/plan-budget.png)

        このオプションを使用すると、1 つ以上の日付範囲の予算を入力できます。

         1. **[!UICONTROL Optimize]** コンテナで以下を実行します。
            1. コンバージョンをコンバージョ **[!UICONTROL Select conversion]** ドロップダウンメニューから選択します。
            1. **[!UICONTROL Select model]** ドロップダウンメニューからモデルを選択します。
         1. 日付を入力するか、**[!UICONTROL Date range]** カレン ![&#x200B; ー &#x200B;](/help/assets/icons/Calendar.svg) を使用して日付範囲を選択して、日付を指定します。
         1. **[!UICONTROL Budget]** を入力します。
日付範囲を追加するには、それぞれ予算と共に ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]** を選択します。
日付範囲および関連する予算を削除するには、「![&#x200B; クローズ &#x200B;](/help/assets/icons/Close.svg)」を選択します。
         1. オプションの最大予算を定義して計画を制約する手順は、次のとおりです。
            1. **[!UICONTROL Maximize budget]** をオンにします。
            1. 最大予算の金額を指定してください。 金額は、日付範囲に指定された予算の合計金額以上である必要があります。


      * **[!UICONTROL I have a target to achieve]** [!BADGE Beta]

        ![&#x200B; 目標を計画 &#x200B;](../assets/plan-target.png)

         1. **[!UICONTROL Optimize]** コンテナ内
            1. コンバージョンをコンバージョ **[!UICONTROL Select conversion]** ドロップダウンメニューから選択します。
            1. **[!UICONTROL Select target metric]** ドロップダウンメニューからターゲット指標を選択します。 **[!UICONTROL Conversion]**、**[!UICONTROL CPA]**、**[!UICONTROL Revenue]**、**[!UICONTROL ROI]** から選択できます。
            1. **[!UICONTROL Select model]** ドロップダウンメニューからモデルを選択します。
         1. 日付を入力するか、![&#x200B; カレンダー &#x200B;](/help/assets/icons/Calendar.svg) を使用して日付範囲を選択して、日付範囲を指定します。
         1. 選択したターゲット指標の値を入力します。 例えば、**[!UICONTROL Total Conversions]** の場合は数値、**[!UICONTROL Paid Marketing ROI]** の場合はパーセンテージ、**[!UICONTROL Paid Marketing CPA]** と **[!UICONTROL Total Revenue]** の場合は通貨値です。
日付範囲を追加するには、それぞれターゲット指標と共に ![CalendarAdd](/help/assets/icons/CalendarAdd.svg) **[!UICONTROL Add row]** を選択します。
日付範囲および関連するターゲット指標を削除するには、「![&#x200B; 閉じる &#x200B;](/help/assets/icons/Close.svg)」を選択します。
         1. オプションの最大予算を定義して計画を制約する手順は、次のとおりです。
            1. **[!UICONTROL Maximize budget]** をオンにします。
            1. 最大予算の金額を指定してください。


   1. **[!UICONTROL Next]** を選択します。

1. **[!UICONTROL Done with all required fields]** ダイアログで、次の手順を実行します。

   ![&#x200B; 計画完了 &#x200B;](/help/assets/plan-done-required-fields.png)

   * 予測 ROI を持つ AI 推奨プランを生成する場合は、「![&#x200B; 新規プラン &#x200B;](/help/assets/icons/NewPlan.svg)**[!UICONTROL Create plan now]**」を選択します。 「**[!UICONTROL OK]**」を選択します。 プランが作成されます。





   * 予測 ROI を持つプランを作成する前にチャネル予算を編集して詳細設定を定義する場合は、「![&#x200B; テーブル編集 &#x200B;](/help/assets/icons/TableEdit.svg)」 **[!UICONTROL Edit channel budgets first]** を選択します。  「**[!UICONTROL OK]**」を選択すると、次の手順で **[!UICONTROL Spend selection]** でのチャネル支出を定義できます。


     >[!IMPORTANT]
     >
     >以下の情報は、「![TableEdit](/help/assets/icons/TableEdit.svg)」を選択した場合にのみ関係し **[!UICONTROL Edit channel budgets first]** す。


1. **[!UICONTROL Spend selection]** セクションの各予算の日付範囲で、![&#x200B; 山形 &#x200B;](/help/assets/icons/ChevronRight.svg) を使用して、そのデータ範囲のチャネル配分表示を開きます。

   過去のマーケティング費用データとインサイトを使用する場合は、履歴参照データを使用できます。 次の履歴リファレンスデータを考慮します。

   * パフォーマンスの高いチャネルとパフォーマンスの低いチャネルを強調することで、予算割り当てを改善します。
   * トレンド分析をサポートします。
   * 効果的な戦略を特定し、計画の設定時にミスを避けます。

   過去の参照期間を選択した場合は、以前の支出パターンの環境設定に合わせて、Mix Modelerの計画機能で期待通りの計画を作成できます。 これらの計画は、最終的に関係者の信頼を高め、マーケティング計画が戦略的かつ効率的であり、これらの計画が実績データおよびビジネスニーズに基づいていることを確認する必要があります。

   ![&#x200B; 費用の選択 &#x200B;](/help/assets/plan-spend-selection.png)

   1. 「**[!UICONTROL Spend pattern]**」を選択します。

      * デフォルトのオプションは **[!UICONTROL Automatic]** です。
      * 「**[!UICONTROL Historical reference]**」を選択し、**[!UICONTROL Start date]** を入力して、Mix Modelerで既に使用可能な過去のマーケティング費用データを参照します。 **[!UICONTROL End date]** は、支出パターンを定義した日付範囲に基づいて自動的に決定されます。 提案された開始日は、利用可能な過去のマーケティング支出日のうち最初に利用できる日付です。 存在しない履歴参照期間または無効な履歴参照期間を選択したことを示すために、![AlertRed](/help/assets/icons/AlertRed.svg) が表示されます。

   1. 各チャネルの予算を定義するには、**[!UICONTROL Min]** と **[!UICONTROL Max]** の値を入力するか、スライダーを使用します。

   1. 通貨またはパーセンテージの入力を切り替えるには、「**[!UICONTROL $]**」で「**[!UICONTROL %]**」または「**[!UICONTROL View spend by]**」を選択します。 通貨ベースではないターゲット指標を選択した場合、この切替スイッチは無効になります。

   1. 終了したら「**[!UICONTROL Create]**」を選択します。
      ![&#x200B; 費用の選択 &#x200B;](/help/assets/plan-spend-selection.png)

   1. **[!UICONTROL Next]** を選択します。



1. 「**[!UICONTROL Advanced configurations]**」セクションでは、オプションで詳細設定を入力できます。

   ![&#x200B; 計画の概要 &#x200B;](../assets/plan-advanced-configurations.png)

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

