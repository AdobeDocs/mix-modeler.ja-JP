---
title: モデルインサイト
description: 履歴の概要、モデルインサイト、Mix Modelerのモデル品質など、モデルに関する詳細を取得する方法を説明します。
feature: Models
exl-id: d99852f9-ba0d-4a2e-b5f3-ca0efe6002fd
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# モデルインサイト

モデルインサイトを表示するには、Mix Modelerの ![ モデル ](/help/assets//icons/FileData.svg)**[!UICONTROL Models]** ーザーインターフェイスで次の操作を行います。

1. **[!UICONTROL Models]** テーブルから、**[!UICONTROL Last run status]** が <span style="color:green">●</span> のモデルの名前を選択します。 **[!UICONTROL Success]**。

1. コンテキストメニューから「**[!UICONTROL Model Insights]**」を選択します。

![ モデルインサイトのタブバー ](/help/assets//model-insights-tabbar.png)

指定したモデルが最後に更新された日時を確認できます。また、次の 4 つのタブを使用してウィジェットが表示されます。[ モデルインサイト ](#model-insights)、[ アトリビューション ](#attribution)、[ 診断 ](#diagnostics)、[ 概要の履歴 ](#historical-overview)。

各タブのウィジェットの基になる期間を変更できます。 日付範囲を入力するか、「![ カレンダー ](/help/assets//icons/Calendar.svg)」を選択して日付範囲を選択します。

## [!UICONTROL Model insights]

「モデルインサイト」タブには、次のウィジェットが表示されます。

* 貢献度（日付およびベースメディア別） 積み重ねグラフは順序が付けられており、下部にベース、中央に非支出チャネル、上部に支出チャネルが表示されます。

* 貢献度（チャネル別）。

* マーケティング効果の概要。

* 限界応答曲線。
  <br/> 「チャネル」ドロップダウンリストから **[!UICONTROL Channel]** ャネルを選択して、特定のチャネルのウィジェットを更新します。

![ モデル – モデルインサイト ](/help/assets//model-insights-insights.png)

各ウィジェットの個々のグラフ要素にポインタを合わせると、詳細を含むポップオーバーが表示されます。

ウィジェットのデータを含んだ CSV ファイルをダウンロードするには、「![ ダウンロード ](/help/assets//icons/Download.svg)」を選択します。

Microsoft® Excel 形式で完全なモデルインサイトデータをダウンロードするには、「![ ダウンロード ](/help/assets//icons/Download.svg)**[!UICONTROL Download data]** を選択します。

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

**[!UICONTROL Attribution Model]** ドロップダウンリストから 1 つ以上のアトリビューションモデルを選択します。 選択したアトリビューションモデルは、「アトリビューション」タブのすべてのウィジェットに適用されます。

![アトリビューション](/help/assets//model-insights-attribution.png)

Mix Modelerのマルチタッチ アトリビューションのきめ細かいイベントスコアは、全体的なMix Modelerスコアと ROI に一致します。 これらのスコアは、Experience Platformのデータセットとしても使用できます。

「アトリビューション」タブは、次のウィジェットで構成されます。

### [!UICONTROL Overview]

[!UICONTROL Overview] ウィジェットには、選択したアトリビューションモデルに関して、コンバージョンの合計とパーセンテージが表示されます。 さらにモデルを選択すると、ビジュアライゼーションに円が追加され、凡例に対応する独自の色が付きます。

アトリビューションモデルの詳細を含むポップアップを表示するには、ビジュアライゼーションの任意の円にポインタを合わせます。

### [!UICONTROL Trends]

[!UICONTROL Daily trends]、[!UICONTROL Weekly trends]、[!UICONTROL Monthly trends] のウィジェットは、選択したアトリビューションモデルに関して、日別、週別、月別のコンバージョントレンドを表示します。

期間を選択するには、「**[!UICONTROL Daily trends]**」、「**[!UICONTROL Weekly trends]**」または「**[!UICONTROL Monthly trends]**」を ![ 詳細 ](/help/assets//icons/More.svg) から選択します。

詳細を確認するには、特定のアトリビューションモデルのデータラインにカーソルを合わせると、そのデータのコンバージョンの合計数を表示するポップオーバーが表示されます。

### [!UICONTROL Breakdown]

[!UICONTROL Breakdown] ウィジェットは、選択した各アトリビューションモデルのコンバージョンのチャネルまたはタッチポイントごとの分類です。 このウィジェットは、各チャネルまたはタッチポイントの有効性を決定するのに役立ちます。

分類のタイプを選択するには、「**[!UICONTROL Breakdown by channel]**」または「**[!UICONTROL Breakdown by touchpoint]**」を ![ 詳細 ](/help/assets//icons/More.svg) から選択します。

詳細を表示するには、任意のグラフ要素にポインタを合わせます。

### [!UICONTROL Top campaigns]

上位キャンペーン ウィジェットには、キャンペーン名、チャネル、メディアタイプおよび増分コンバージョン用の列を含んだ上位キャンペーンのテーブルが表示されます。 このウィジェットは、特定のチャネルに対する特定のキャンペーンの有効性をチームに伝え、さらに投資する必要があるキャンペーンに関するインサイトを提供するのに役立ちます。

チャネル、メディアタイプ、増分コンバージョンでテーブルを昇↑または降順に並べ替える↓合は、列ヘッダーを選択して並べ替えを切り替えます。

別のダイアログでテーブルを展開するには、「**[!UICONTROL Expand]** 細 ![」から「詳細 ](/help/assets//icons/More.svg) を選択します。

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


## [!UICONTROL Diagnostics]

「診断」タブには、次のウィジェットが表示されます。

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

  テーブルのデータを含む CSV ファイルをダウンロードするには、「![ ダウンロード ](/help/assets//icons/Download.svg)」を選択します。

* Attribution AIアルゴリズムモデルの結果を表す [!UICONTROL Touchpoint effectiveness] のテーブル。 このテーブルのデータは、特定の期間のみ生成されます。 詳細については、「**[!UICONTROL As of *xx/xx/xx, xx:xx TZ *]**![Info](/help/assets//icons/InfoOutline.svg)」を選択してください。

  ビジュアライゼーションでは、タッチポイントご [!UICONTROL Efficiency measure] に降順 ![ 降順 ](/help/assets//icons/SortOrderDown.svg) で表示されます。

   * [!UICONTROL Paths touched]: コンバージョンを達成するパスの割合とコンバージョンを達成しないパスの割合を視覚化します。 タッチポイントの場合、アトリビューションコンバージョン率が高いと、より多くのアトリビューションコンバージョンが表示されます。 この比率では、コンバージョンにつながるパスの割合と、コンバージョンにつながる *つながらない* パスの割合が比較されます。
   * [!UICONTROL Efficiency measure]: アルゴリズムアトリビューションモデルによって生成される効率測定は、タッチポイント量に関係なく、コンバージョンに対するタッチポイントの相対的な重要度を示します。 効率は 1～5 のスケールで測定されます。 タッチポイント量が多いからといって、効率測定が高くなるとは限りません。
   * [!UICONTROL Total volume]：ユーザーがタッチポイントにタッチした合計回数。 この数は、コンバージョンを達成するパスと、コンバージョンに至るパス *ではない* に表示されるタッチポイントを含みます。

![ 診断 ](/help/assets//model-insights-diagnostics.png)


## [!UICONTROL Historical overview]

「履歴の概要」タブには、次のウィジェットが表示されます。

* コンバージョンと支出（会計四半期および製品別）。

* チャネル別の支出。

* タッチポイント支出。

  このウィジェットに表示する別の費用ベースのチャネルを選択できます。 **[!UICONTROL Channels]** からチャネルを選択します。

* タッチポイント量。

  このウィジェットに表示する別のボリュームベースのチャネルを選択できます。 **[!UICONTROL Channels]** からチャネルを選択します。

![ モデル – 履歴の概要 ](/help/assets//model-insights-historical-overview.png)
