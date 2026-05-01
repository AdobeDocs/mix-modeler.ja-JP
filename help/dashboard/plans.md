---
title: パフォーマンスからプランへ
description: Mix ModelerでPerformance to Planの概要を使用する方法を説明します。
feature: Dashboard, Plans, Models
exl-id: 930fc1d5-8e28-4610-af7b-c4ec91f86a8a
TQID: https://experienceleague.adobe.com/iRFbGXoCx5jzg6ATId2tNLTfyigoTzD4JQIqlPU5isU
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: d822825b-9821-40d5-9b0d-42a9e3f317c5
subfeature_v2: id: d7b067e6-4f39-41e9-a081-7650346a84cdid: b2520ae7-8f6c-4952-935e-aacc2c10256fid: e6c284e0-b6e6-4f82-bf96-e96bb5157b90
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:20:18.412Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 537
ht-degree: 0%

---

# パフォーマンスからプランへ

>[!NOTE]
>
>Mix Modeler ![ ホーム ](/help/assets/icons/Home.svg) **[!UICONTROL Overview]**&#x200B;の「**[!UICONTROL Performance to plan]** [!BADGE Beta]{type=Informative}」タブはベータ機能であり、その機能は変更される可能性があります。 この機能は、限られた数のお客様にご利用いただけます。

Mix Modeler ![ ホーム ](/help/assets/icons/Home.svg) **[!UICONTROL Overview]**&#x200B;の&#x200B;**[!UICONTROL Plans]** [!BADGE Beta]{type=Informative} タブには、計画に対するマーケティングのパフォーマンスを監視するためのトラッキングダッシュボードが用意されています。 ステータスカードとビジュアライゼーション機能を利用して、実際のパフォーマンスと計画されたパフォーマンスを追跡することができます。

ダッシュボードは、ギャップを特定し、リスクや機会を特定し、計画や予算をタイムリーに調整するのに役立ちます。

KPI ステータス カードとビジュアライゼーションに表示されるデータを選択するには：

* **[!UICONTROL _オプションを選択…_]**&#x200B;を使用して、**[!UICONTROL Plan name]** ドロップダウンメニューからプランを選択します。

* 日付期間を指定します。 日付期間を変更するには、開始日と終了日を手動で入力するか、![ カレンダー](/help/assets/icons/Calendar.svg)を使用して日付期間を選択します。

「**[!UICONTROL Plans]** [!BADGE Beta]{type=Informative}」タブには、次の情報が表示されます。

* [KPI ステータスカード ](#kpi-status-cards):

   * [予算](#budget)
   * [売上高](#revenue)
   * [ROI](#roi)
   * [KPI](#kpi)

* [ ビジュアライゼーション ](#visualizations):
   * [*指標*：実際の指標と計画された指標の比較](#metric-actual-vs-planned)
   * [*指標*：実際の指標と&#x200B;*精度*&#x200B;で計画された指標の比較](#metric-actual-vs-planned-by-granularity)
   * [チャネル *指標* by *精度*](#channel-metric-by-granularity)
   * [チャネル別&#x200B;*指標*&#x200B;対&#x200B;*指標*](#metric-vs-metric-by-channel)
   * [*粒度*&#x200B;による&#x200B;*指標*](#metric-by-granularity)
   * [チャネル別&#x200B;*指標*](#metric-by-channel)

## KPI ステータスカード

![KPI ステータスカード ](../assets/performance-to-plan-kpi-cards.png)


### 予算

マーケティング費用と日付期間の計画の予算との比較を表示する、循環進行状況のビジュアライゼーション。

### 売上高

日付期間の計画された目標収益と実際の収益の比較を表示する循環進行状況のビジュアライゼーション。


### ROI

日付期間のROIを表示する行の可視化。


### KPI

日付期間のKPIを表示する行の可視化。

別のKPIを選択するには：

1. ![編集](/help/assets/icons/Edit.svg)を選択します。
1. **[!UICONTROL KPI status card]** ダイアログで、**[!UICONTROL KPI]** ドロップダウンメニューからKPIを選択します。 利用できるオプションは、[!UICONTROL Conversions]、[!UICONTROL CPA]、[!UICONTROL Revenue]、[!UICONTROL ROI]および[!UICONTROL Spend]です。


## ビジュアライゼーション

6つのビジュアライゼーションを使用でき、6つのビジュアライゼーションのそれぞれを編集できます。

ビジュアライゼーションのサイズを変更するには、右下隅の┛ ハンドルを使用します。 ビジュアライゼーションを移動するには、ビジュアライゼーションを目的の位置にドラッグ&amp;ドロップするだけです。

ビジュアライゼーションの任意の行、棒グラフまたは散布要素にカーソルを合わせると、追加情報を含むポップアップが表示されます。

![ ビジュアライゼーション ](../assets/performance-to-plan-visualizations.png)

### *指標*：実際の指標と計画された指標の比較

選択した指標の値を日付、予定日、合計と比較する積み上げ棒グラフのビジュアライゼーション。


### *指標*：実際の指標と&#x200B;*精度*&#x200B;で計画された指標の比較

選択した指標と選択した粒度の実際の値と計画された値を表示する折れ線ビジュアライゼーション。


### チャネル *指標* by *精度*

選択した指標と選択した粒度のチャネルを表示する積み重ね棒を表示する積み重ね棒ビジュアライゼーション。


### チャネル別&#x200B;*指標*&#x200B;対&#x200B;*指標*

選択した指標のチャネルの散布図を表示する散布図のビジュアライゼーション。


### *粒度*&#x200B;による&#x200B;*指標*

選択した指標の実際の値と計画された値を表示する棒グラフのビジュアライゼーション。


### チャネル別&#x200B;*指標*

選択した粒度に対して選択した指標を表示する複数行のビジュアライゼーション。


### ビジュアライゼーションの編集

ビジュアライゼーションを編集するには：

1. 「![編集](/help/assets/icons/Edit.svg)」を選択して、**[!UICONTROL Edit data]** ダイアログを開きます。
1. ビジュアライゼーションに応じて、以下を変更できます。

   * 1つまたは2つの指標：**[!UICONTROL Select metric]** ドロップダウンメニューから指標を選択します。

      * ROI ベースのプランの場合、オプションは[!UICONTROL Conversions]、[!UICONTROL CPA]、[!UICONTROL Revenue]、[!UICONTROL ROI]、[!UICONTROL Spend]および[!UICONTROL Volume]です。
      * CPA ベースのプランの場合、オプションは[!UICONTROL Conversions]、[!UICONTROL CPA]、[!UICONTROL Spend]、および[!UICONTROL Volume]です。
   * **[!UICONTROL Granularity]**: **[!UICONTROL Granularity]** ドロップダウンメニューから&#x200B;**[!UICONTROL date ranges]**&#x200B;または&#x200B;**[!UICONTROL week]**&#x200B;のいずれかを選択します。

   **[!UICONTROL Preview]**&#x200B;で、変更が&#x200B;**[!UICONTROL Current]** ビジュアライゼーションとどのように異なるかがわかります。

1. **[!UICONTROL Apply]**&#x200B;を選択して変更を適用します。 ビジュアライゼーションの変更をキャンセルするには、**[!UICONTROL Cancel]**&#x200B;を選択します。
