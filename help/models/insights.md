---
title: モデルインサイト
description: 履歴の概要、モデルのインサイト、Mix Modelerのモデルの品質など、モデルに関する詳細を取得する方法を説明します。
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 4f4c7f05e90d73a0ab4865150b1ec4c2af88fc12
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# モデルインサイト

モデルのインサイトを表示するには、 ![モデル](../assets/icons/FileData.svg) **[!UICONTROL Models]** インターフェイスのMix Modeler:

1. モデルの名前を **[!UICONTROL Last run status]** / <span style="color:green">●</span> **[!UICONTROL Success]** から **[!UICONTROL Models]** 表。

1. コンテキストメニューから、「 」を選択します。 **[!UICONTROL Model Insights]**.

指定したモデルが最後に更新された日時が表示され、3 つのタブ（履歴の概要、モデルのインサイト、モデルの品質）を使用してウィジェットが表示されます。

各タブのウィジェットのベースとなる日付期間を変更できます。 期間を入力するか、 ![カレンダー](../assets/icons/Calendar.svg) をクリックして、日付期間を選択します。


## 履歴の概要

「履歴の概要」タブには、以下のウィジェットが表示されます。

* 会計四半期および製品別の換算および支出。

* チャネル別の支出。

* タッチポイント費用。

  このウィジェットに表示する別の支出ベースのチャネルを選択できます。 チャネルの選択元 **[!UICONTROL Channels]**.

* タッチポイントボリューム。

  このウィジェットに表示する別のボリュームベースのチャネルを選択できます。 チャネルの選択元 **[!UICONTROL Channels]**.

![モデル — 履歴の概要](../assets/model-historical-overview.png)

## モデルインサイト

「モデルインサイト」タブには、以下のウィジェットが表示されます。

* 日付別およびベースメディア別の貢献度。 積み重ねグラフは順番に並べられます。下部に基づくチャネル、中央に支出なしチャネル、上部に支出チャネルがあります。

* チャネル別の貢献度。

* マーケティングパフォーマンスの概要。

* 限界応答曲線。

![モデル — モデルインサイト](../assets/model-model-insights.png)

各ウィジェットの個々のグラフ要素の上にマウスポインターを置くと、ポップオーバーに詳細情報を表示できます。

ウィジェットのデータを含む CSV ファイルをダウンロードするには、「 」を選択します。 ![ダウンロード](../assets/icons/Download.svg).

完全なモデルインサイトデータをMicrosoft® Excel 形式でダウンロードするには、「 ![ダウンロード](../assets/icons/Download.svg) **[!UICONTROL Download data]**.


## モデルの品質

![モデル品質評価](/help/assets/model-quality-assessment.png)
「モデル品質」タブには、

* [!UICONTROL Model Assessment] ビジュアライゼーション：実際のコンバージョンと予測コンバージョンまたは残差コンバージョンの内訳を表示できます。

  ビジュアライゼーションを分類するには、「 **[!UICONTROL Actual vs. Predicted]** または **[!UICONTROL Residuals]** から **[!UICONTROL Breakdown]** リスト。

* [!UICONTROL Model fitting metrics] 表に、各コンバージョン指標の次の列を表示します。

   * 実際のコンバージョン

   * モデル化された変換

   * 残差コンバージョン（実際のコンバージョンとモデル化されたコンバージョンの違い）

   * モデル品質スコア値：

      * R2 （R-2 乗）：データが回帰モデル（適合度）にどの程度適合するかを示します。

      * MAPE（平均絶対率誤差）：予測精度を測定するために最もよく使用される KPI の 1 つで、予測誤差を実際の値に対する割合で表します。

      * RMSE(Root Mean Square Error)：平均「エラー」を、エラーの平方に従って重み付けした値として示します。

  テーブルのデータを含む CSV ファイルをダウンロードするには、「 ![ダウンロード](../assets/icons/Download.svg).
