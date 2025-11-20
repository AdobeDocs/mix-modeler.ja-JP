---
title: 計画するパフォーマンス
description: Mix Modelerの Performance to Plan の概要を使用する方法を説明します。
feature: Dashboard, Plans, Models
exl-id: 930fc1d5-8e28-4610-af7b-c4ec91f86a8a
source-git-commit: 89def3d6f5a1415d8f7a91b05d68d70ca881bdf4
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# 計画するパフォーマンス

>[!NOTE]
>
>Mix Modeler **[!UICONTROL Performance to plan]** ホーム [!BADGE  の「]{type=Informative} ![Beta](/help/assets/icons/Home.svg)」タブはベータ版機能であり、**[!UICONTROL Overview]** の機能は変更される場合があります。 この機能を使用できるのは、限られた数のお客様です。

Mix Modeler **[!UICONTROL Plans]** ホーム [!BADGE  ]{type=Informative} の ![ ](/help/assets/icons/Home.svg)Beta **[!UICONTROL Overview]** タブには、マーケティングがプランに対してどの程度効果を発揮しているかを監視するトラッキングダッシュボードが表示されます。 ステータスカードとビジュアライゼーションを使用して、実際のパフォーマンスと予定パフォーマンスを追跡できます。

このダッシュボードを使用すると、ギャップを特定し、リスクや機会を見つけ出して、計画や予算をタイムリーに調整できます。

KPI ステータス・カードおよびビジュアライゼーションに表示するデータを選択するには、次の手順を実行します。

* **[!UICONTROL Plan name]** ドロップダウンメニューから **[!UICONTROL _オプションを選択…_]** を使用して、プランを選択します。

* 期間を指定します。 日付範囲を変更するには、開始日と終了日を手動で入力するか、![ カレンダー ](/help/assets/icons/Calendar.svg) を使用して日付範囲を選択します。

「**[!UICONTROL Plans]** [!BADGE Beta]{type=Informative}」タブには、次の情報が表示されます。

* [KPI ステータス カード ](#kpi-status-cards):

   * [予算](#budget)
   * [収益](#revenue)
   * [ROI](#roi)
   * [KPI](#kpi)

* [ ビジュアライゼーション ](#visualizations):
   * [*指標*](#metric-actual-vs-planned)
   * [*指標*](#metric-actual-vs-planned-by-granularity)
   * [チャネル ](#channel-metric-by-granularity)
   * [*指標*](#metric-vs-metric-by-channel)
   * [*指標*](#metric-by-granularity)
   * [*指標*](#metric-by-channel)

## KPI ステータスカード

![KPI ステータスカード ](../assets/performance-to-plan-kpi-cards.png)


### 予算

マーケティング費用とプランの予算との比較を期間ごとに表示する、円形の進捗ビジュアライゼーション。

### 収益

日付範囲での実収益と予定ターゲット収益の比較方法を表示する、循環的な進捗ビジュアライゼーション。


### ROI

期間の ROI を表示する線のビジュアライゼーション。


### KPI

期間の KPI を表示する折れ線グラフ ビジュアライゼーション。

別の KPI を選択する手順は、次のとおりです。

1. 「![編集](/help/assets/icons/Edit.svg)」を選択します。
1. **[!UICONTROL KPI status card]** ダイアログで、**[!UICONTROL KPI]** ドロップダウンメニューから KPI を選択します。 使用可能なオプションは、[!UICONTROL Conversions]、[!UICONTROL CPA]、[!UICONTROL Revenue]、[!UICONTROL ROI] および [!UICONTROL Spend] です。


## ビジュアライゼーション

6 つのビジュアライゼーションを使用でき、6 つのビジュアライゼーションをそれぞれ編集できます。

ビジュアライゼーションのサイズを変更するには、右下隅にある ┛ ハンドルを使用します。 ビジュアライゼーションを移動するには、ビジュアライゼーションを希望の位置にドラッグ&amp;ドロップします。

ビジュアライゼーション内の線、棒グラフまたは散布図の要素の上にマウスポインターを置くと、追加情報を含むポップアップが表示されます。

![ 表示 ](../assets/performance-to-plan-visualizations.png)

### *指標*：実際と予定

選択した指標の値を累計、予定から累計および合計で比較する、積み重ね棒グラフのビジュアライゼーション。


### *指標*：実績対予定比 *精度*

選択した指標の実際の値と予定値、および選択した精度を表示する折れ線グラフ ビジュアライゼーション。


### チャネル *指標**精度*

選択した指標のチャネルと選択した精度を表示する積み重ね棒グラフを表示する積み重ね棒グラフのビジュアライゼーション。


### チャネル別の *指標* 対 *指標*

選択した指標全体のチャネルの散布図を表示する散布図ビジュアライゼーション。


### *指標* by *精度*

選択した指標の実際の値と予定値を示す棒グラフ ビジュアライゼーション。


### *指標* チャネル別

選択した精度で選択した指標を表示する複数行のビジュアライゼーション。


### ビジュアライゼーションの編集

ビジュアライゼーションを編集するには：

1. 「![ 編集 ](/help/assets/icons/Edit.svg)」を選択して、**[!UICONTROL Edit data]** ダイアログを開きます。
1. ビジュアライゼーションに応じて、次を変更できます。

   * 1 つまたは 2 つの指標：**[!UICONTROL Select metric]** ドロップダウンメニューから指標を選択します。

      * ROI ベースプランの場合、オプションは [!UICONTROL Conversions]、[!UICONTROL CPA]、[!UICONTROL Revenue]、[!UICONTROL ROI]、[!UICONTROL Spend]、[!UICONTROL Volume] です。
      * CPA ベースのプランの場合、オプションは [!UICONTROL Conversions]、[!UICONTROL CPA]、[!UICONTROL Spend] および [!UICONTROL Volume] です。
   * **[!UICONTROL Granularity]**: **[!UICONTROL date ranges]** ドロップダウンメニューから **[!UICONTROL week]** または **[!UICONTROL Granularity]** を選択します。

   **[!UICONTROL Preview]** のビジュアライゼーションと **[!UICONTROL Current]** 変化の違いがわかります。

1. 「**[!UICONTROL Apply]**」を選択して、変更を適用します。 「**[!UICONTROL Cancel]**」を選択して、ビジュアライゼーションに対する変更をキャンセルします。
