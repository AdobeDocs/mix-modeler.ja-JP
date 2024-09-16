---
title: モデルインサイト
description: 履歴の概要、モデルインサイト、Mix Modelerのモデル品質など、モデルに関する詳細を取得する方法を説明します。
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 09ec757a37725d4b41231076bd99432bffd6d555
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 0%

---

# モデルインサイト

モデルインサイトを表示するには、Mix Modelerの ![ モデル ](/help/assets/icons/FileData.svg)**[!UICONTROL Models]** ーザーインターフェイスで次の操作を行います。

1. **[!UICONTROL Models]** テーブルから、**[!UICONTROL Last run status]** が <span style="color:green">●</span> のモデルの名前を選択します。 **[!UICONTROL Success]**。

1. コンテキストメニューから「**[!UICONTROL Model Insights]**」を選択します。

![ モデルインサイトのタブバー ](/help/assets/model-insights-tabbar.png)

指定したモデルが最後に更新されると、[ モデルインサイト ](#model-insights)、[ アトリビューション ](#attribution)、[ 要因 ](#factors)、[ 診断 ](#diagnostics)、[ 履歴概要 ](#historical-overview) の 4 つのタブを使用してビジュアライゼーションが表示されます。

各タブのビジュアライゼーションの基になる期間を変更できます。 日付範囲を入力するか、「![ カレンダー ](/help/assets/icons/Calendar.svg)」を選択して日付範囲を選択します。

## [!UICONTROL Model insights]

モデルインサイト タブには、[ 日付およびベースメディア別の貢献度 ](#contribution-by-date-and-base-media)、[ チャネル別の貢献度 ](#contribution-by-channel)、[ マーケティングパフォーマンスの概要 ](#marketing-performance-summary)、および [ 限界応答曲線 ](#marginal-response-curves) のビジュアライゼーションが表示されます。

![ モデル – モデルインサイト ](/help/assets/model-insights-insights.png)

* 各ビジュアライゼーションの個々のグラフ要素にポインタを合わせると、詳細を含むポップオーバーが表示されます。

* ビジュアライゼーションのデータを含んだ CSV ファイルをダウンロードするには、「![ ダウンロード ](/help/assets/icons/Download.svg)」を選択します。

* Microsoft® Excel 形式で完全なモデルインサイトデータをダウンロードするには、「![ ダウンロード ](/help/assets/icons/Download.svg)**[!UICONTROL Download data]** を選択します。


### 貢献度（日付およびベースメディア別）

積み重ねグラフは順序が付けられており、下部にベース、中央に非支出チャネル、上部に支出チャネルが表示されます。

### 貢献度（チャネル別）

ドーナツビジュアライゼーションには、貢献度の分布がチャネル別に表示されます。

### マーケティング効果の概要。

チャネル別の ROI パフォーマンスを表示する横棒グラフ。

### 限界応答曲線。

折れ線グラフは、マーケティングチャネルでの投資によって生成された限界収益を視覚化し比較します。  そして、増分利益が増分費用よりも少ない損益分岐点を特定します。 その結果、このビジュアライゼーションは、マーケティング投資の影響が小さくなり始めたタイミングを理解するのに役立ちます。

選択したデータ範囲と選択したチャンネルに基づいて、カーブ、ブレークポイント、および対応する値が計算されます。

チャネルを変更するには：

* **[!UICONTROL Channel]** ドロップダウンメニューからチャネルを選択して、特定のチャネルのビジュアライゼーションを更新します。



## [!UICONTROL Attribution]

「[!UICONTROL Attribution]」タブを使用すると、イベントレベルのデータを持つタッチポイントとマーケティングキャンペーンの効果を把握できます。 次のアトリビューションモデルがサポートされています。

* Mix Modelerで選択したモデルに基づく：
   * アルゴリズム – 影響
   * アルゴリズム – 増分
* ルールベース：
   * 減衰単位
   * ファーストタッチ
   * ラストタッチ
   * 線形
   * U字型

Mix Modelerのマルチタッチアトリビューション機能の概要については、[ マルチタッチアトリビューション ](../get-started/about.md#multi-touch-attribution) を参照してください。

**[!UICONTROL Attribution Model]** ドロップダウンメニューから 1 つ以上のアトリビューションモデルを選択します。 選択したアトリビューションモデルは、「アトリビューション」タブのすべてのビジュアライゼーションに適用されます。

![アトリビューション](/help/assets/model-insights-attribution.png)

Mix Modelerのマルチタッチ アトリビューションのきめ細かいイベントスコアは、全体的なMix Modelerスコアと ROI に一致します。 これらのスコアは、Experience Platformのデータセットとしても使用できます。

「アトリビューション」タブは、次のビジュアライゼーションで構成されます。

### [!UICONTROL Overview]

[!UICONTROL Overview] のビジュアライゼーションには、選択したアトリビューションモデルに関して、コンバージョンの合計とパーセンテージが表示されます。 さらにモデルを選択すると、ビジュアライゼーションに円が追加され、凡例に対応する独自の色が付きます。

アトリビューションモデルの詳細を含むポップアップを表示するには、ビジュアライゼーションの任意の円にポインタを合わせます。

### [!UICONTROL Trends]

[!UICONTROL Daily trends]、[!UICONTROL Weekly trends] または [!UICONTROL Monthly trends] のビジュアライゼーションは、選択したアトリビューションモデルに関して、日別、週別または月別のコンバージョンのトレンドを表示します。

期間を選択するには、「**[!UICONTROL Daily trends]**」、「**[!UICONTROL Weekly trends]**」または「**[!UICONTROL Monthly trends]**」を ![ 詳細 ](/help/assets/icons/More.svg) から選択します。

詳細を確認するには、特定のアトリビューションモデルのデータラインにカーソルを合わせると、そのデータのコンバージョンの合計数を表示するポップオーバーが表示されます。

### [!UICONTROL Breakdown]

[!UICONTROL Breakdown] のビジュアライゼーションは、選択した各アトリビューションモデルのコンバージョンのチャネルまたはタッチポイントによる分類です。 このビジュアライゼーションは、各チャネルやタッチポイントの有効性を判断するのに役立ちます。

分類のタイプを選択するには、「**[!UICONTROL Breakdown by channel]**」または「**[!UICONTROL Breakdown by touchpoint]**」を ![ 詳細 ](/help/assets/icons/More.svg) から選択します。

詳細を表示するには、任意のグラフ要素にポインタを合わせます。

### [!UICONTROL Top campaigns]

上位キャンペーンのビジュアライゼーションには、キャンペーン名、チャネル、メディアタイプおよび増分コンバージョンの列を含む上位キャンペーンのテーブルが表示されます。 このビジュアライゼーションは、特定のチャネルに対する特定のキャンペーンの有効性をチームに知らせ、さらに投資する必要のあるキャンペーンに関するインサイトを提供するのに役立ちます。

チャネル、メディアタイプ、増分コンバージョンでテーブルを昇↑または降順に並べ替える↓合は、列ヘッダーを選択して並べ替えを切り替えます。

別のダイアログでテーブルを展開するには、「**[!UICONTROL Expand]** 細 ![」から「詳細 ](/help/assets/icons/More.svg) を選択します。

展開されたトップキャンペーン ダイアログには、と同じテーブルに対する追加列が表示されます

* 増分変換
* 影響コンバージョン
* ファーストタッチコンバージョン
* ラストタッチコンバージョン

  追加の各列ヘッダーを選択して、昇順または降順でテーブルを並べ替えることができます。

展開された「上位キャンペーン」ダイアログを閉じるには、「**[!UICONTROL Close]**」を選択します。


### [!UICONTROL Breakdown by touchpoint position]

[!UICONTROL Breakdown by touchpoint position] のビジュアライゼーションは、すべてのコンバージョンパスをまたいだタッチポイントとタッチポイントの位置別の、アトリビューションコンバージョンの分類です。 このグラフは、タッチポイントが任意の位置の残りの位置や他のタッチポイントよりも、その位置での寄与が良いかどうかを比較するのに役立ちます。

>[!NOTE]
>
>すべてのタッチポイントおよびポジションにわたる属性モデルの貢献率の合計は、100 に等しくする必要があります。


位置 [!UICONTROL Starter]、[!UICONTROL Player] および [!UICONTROL Closer] は、次のように定義されます。

| 位置 | 説明 |
|---|---|
| [!UICONTROL Starter] | この位置は、タッチポイントがコンバージョンパスのファーストタッチであるかどうかを示します。 |
| [!UICONTROL Player] | この位置は、タッチポイントがコンバージョンにつながるファーストタッチまたはラストタッチでないかどうかを示します。 |
| [!UICONTROL Closer] | この位置は、タッチポイントがコンバージョン前のラストタッチであるかどうかを示します。 |


### [!UICONTROL Top conversion paths]

[!UICONTROL Top conversion paths] のビジュアライゼーションには、選択したアトリビューションモデルに基づく上位 5 つのコンバージョンパスが表示されます。

各コンバージョンパスには、以下が表示されます。

* 影響を与えるチャネルの数、
* 合計アトリビューションパス
* 合計アトリビューションパスに対する、このコンバージョンパスのアトリビューションパスの割合、
* チャネルごとに、アトリビューションモデルの貢献度のパーセンテージ、
* これらのチャネルアトリビューションモデルのコントリビューションパーセンテージの合計。

## **[!UICONTROL Factors]**

「要因」タブには、外部要因関連のインサイトが表示されます。

![ 要因 ](/help/assets/factors.png)

このビジュアライゼーションは、様々な内部および外部の要因がコンバージョンのベースラインに与える増分的な影響を理解するのに役立ちます。 例えば、経済状況やプロモーション活動などです。


テーブルのデータを含む CSV ファイルをダウンロードするには、「![ ダウンロード ](/help/assets/icons/Download.svg)」を選択します。

使用できるデータがない場合は、メッセージ ![TableAndChart](/help/assets/icons/TableAndChart.svg) **[!UICONTROL No data is available, you may need to retrain your model, or change the date range to view insights]** が表示されます。

## [!UICONTROL Diagnostics]

「診断」タブには、次のビジュアライゼーションが表示されます。

* [!UICONTROL Model Assessment] のビジュアライゼーションは、実際のコンバージョンと予測コンバージョンまたは残差コンバージョンを分類できます。

  ビジュアライゼーションを分類するには、ビジュアライ **[!UICONTROL Breakdown]** ーションリストから「**[!UICONTROL Actual vs. Predicted]**」または「**[!UICONTROL Residuals]**」を選択します。

* 各コ [!UICONTROL Model fitting metrics] バージョン指標に関する次の列を示した表。

   * 実際の変換

   * モデル化された変換

   * 残差変換（実際の変換とモデル化された変換の差）

   * モデル品質スコア値：

      * R2 （R-2 乗）：回帰モデルに対するデータの適合度（適合度）を示します。

      * MAPE （平均絶対誤差率）：予測精度の測定に最も一般的に使用される KPI の 1 つで、予測誤差を実績値のパーセンテージで表します。

      * RMSE （二乗平均誤差）：誤差の二乗に従って重み付けされた、平均誤差を表示します。

  テーブルのデータを含む CSV ファイルをダウンロードするには、「![ ダウンロード ](/help/assets/icons/Download.svg)」を選択します。

* Attribution AIアルゴリズムモデルの結果を表す [!UICONTROL Touchpoint effectiveness] のテーブル。 このテーブルのデータは、特定の期間のみ生成されます。 詳細については、「**[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets/icons/InfoOutline.svg)」を選択してください。

  ビジュアライゼーションでは、タッチポイントご [!UICONTROL Efficiency measure] に降順 ![ 降順 ](/help/assets/icons/SortOrderDown.svg) で表示されます。

   * [!UICONTROL Paths touched]: コンバージョンを達成するパスの割合とコンバージョンを達成しないパスの割合を視覚化します。 タッチポイントの場合、アトリビューションコンバージョン率が高いと、より多くのアトリビューションコンバージョンが表示されます。 この比率では、コンバージョンにつながるパスの割合と、コンバージョンにつながる *つながらない* パスの割合が比較されます。
   * [!UICONTROL Efficiency measure]: アルゴリズムアトリビューションモデルによって生成される効率測定は、タッチポイント量に関係なく、コンバージョンに対するタッチポイントの相対的な重要度を示します。 効率は 1～5 のスケールで測定されます。 タッチポイント量が多いからといって、効率測定が高くなるとは限りません。
   * [!UICONTROL Total volume]：ユーザーがタッチポイントにタッチした合計回数。 この数は、コンバージョンを達成するパスと、コンバージョンに至るパス *ではない* に表示されるタッチポイントを含みます。

![ 診断 ](/help/assets/model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

履歴の概要タブには、次のビジュアライゼーションが表示されます。

* コンバージョンと支出（会計四半期および製品別）。

* チャネル別の支出。

* タッチポイント支出。

  このビジュアライゼーションに表示する別の費用ベースのチャネルを選択できます。 **[!UICONTROL Channels]** からチャネルを選択します。

* タッチポイント量。

  このビジュアライゼーションに表示する代替のボリュームベースのチャネルを選択できます。 **[!UICONTROL Channels]** からチャネルを選択します。

![ モデル – 履歴の概要 ](/help/assets/model-insights-historical-overview.png)
