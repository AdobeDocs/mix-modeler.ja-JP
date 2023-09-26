---
title: モデルインサイト
description: 履歴の概要、モデルのインサイト、モデルの品質など、モデルの詳細をAdobeMix モデラーで取得する方法を説明します。
feature: Models
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# モデルインサイト

モデルのインサイトを表示するには、 ![モデル](../assets/icons/FileData.svg) **[!UICONTROL Models]** AdobeMix Modeler のインタフェース：

1. モデルの名前を **[!UICONTROL Last run status]** / <span style="color:green">●</span> **[!UICONTROL Success]** から **[!UICONTROL Models]** 表。

1. コンテキストメニューから、「 」を選択します。 **[!UICONTROL Model Insights]**.

指定したモデルが最後に更新された日時が表示され、3 つのタブ（履歴の概要、モデルのインサイト、モデルの品質）を使用してウィジェットが表示されます。

各タブのウィジェットのベースとなる日付期間を変更できます。 期間を入力するか、 ![カレンダー](../assets/icons/Calendar.svg) をクリックして、日付期間を選択します。


## 履歴の概要

「履歴の概要」タブには、以下のウィジェットが表示されます。

* 会計四半期および製品別の換算および支出

* チャネル別支出

* タッチポイント費用

  このウィジェットに表示する別の支出ベースのチャネルを選択できます。 チャネルの選択元 **[!UICONTROL Channels]**.

* タッチポイントボリューム

  このウィジェットに表示する別のボリュームベースのチャネルを選択できます。 チャネルの選択元 **[!UICONTROL Channels]**.



![モデル — 履歴の概要](../assets/model-historical-overview.png)


## モデルインサイト

「モデルインサイト」タブには、以下のウィジェットが表示されます。

* 日付別貢献度およびベースメディア別貢献度

* チャネル別の貢献度

* マーケティングパフォーマンスの概要

各ウィジェットの個々のグラフ要素の上にマウスポインターを置くと、ポップオーバーに詳細を表示できます。

![モデル — モデルインサイト](../assets/model-model-insights.png)


## モデルの品質

「モデル品質」タブには、以下の測定用のウィジェットが表示されます。

* R2 （R-2 乗）：データが回帰モデル（適合度）にどの程度適合するかを示します。

* MAPE（平均絶対率誤差）：予測精度を測定するために最もよく使用される KPI の 1 つで、予測誤差を実際の値に対する割合で表します。

* RMSE(Root Mean Square Error)：平均「エラー」を、エラーの平方に従って重み付けした値として示します。


