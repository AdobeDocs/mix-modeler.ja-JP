---
title: Mix Modeler ワークフロー
description: Mix Modelerの一般的なワークフローを理解する
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: bdb5992ba1e6a4e5aa546b6ffb8e9673ed69be22
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Mix Modeler ワークフロー

Mix Modelerのユーザーワークフローの概要については、このビデオを参照してください。

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Mix Modelerの一般的なワークフローは、次のアクティビティで構成されます。

![ 代替テキスト ](/help/assets/ApplicationWorkflow.svg)

|  | Activity | 説明 |
|---|---|---|
| ![データ](/help/assets/icons/Data.svg){width="100"} | [**データの取り込み**](../ingest-data/overview.md) | Experience Platformからのイベントデータ（Adobe Analytics、Web SDK、その他のソースなど）、マーケティングチャネルからの集計データ（テレビ、壁庭、メール、所有および運営アクティビティなど）、顧客からの外部要因データ（購読サービスの価格変化など）、内部要因データ（休暇プランなど）を取り込みます。 |
| ![ データチェック ](/help/assets/icons/DataCheck.svg){width="100"} | [**データのハーモナイズ**](../harmonize-data/overview.md) | マッピングルールと競合解決ルールを設定して、Mix Modelerでキャンペーンのパフォーマンスを測定および計画するために必要な様々なマーケティングデータセットを結合します。 |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**モデルの作成**](../models/overview.md) | マーケティングタッチポイント（チャネルなど）、コンバージョン定義、内部要因および外部要因を持つモデルインスタンスを作成します。 |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**モデルのトレーニングとスコアリング**](../models/overview.md) | 機械学習のトレーニングとスコアリングを使用して、集計レベルとイベントレベルのスコアを作成します。 |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**プランの作成**](../plans/overview.md) | プランを作成および作成します。 Mix Modeler モデルの出力を使用して、ビジネス目標を達成するためのマーケティング資金の最適な配分を決定します。 |
| ![ ダッシュボード ](/help/assets/icons/Dashboard.svg){width="100"} | [**概要ダッシュボード**](../dashboard/overview.md) | 様々な設定可能なビジュアライゼーションを使用して、統一されたデータ、モデルおよびプランに関するインサイトを取得します。 |

{style="table-layout:auto"}

入力データがMix Modelerにどのように流れ込むか、およびMix Modelerが独自のインターフェイスだけでなく、Customer Journey Analyticsなどの他のソリューションの出力データを生成する方法の概要を以下に示します。

![Mix Modeler入出力データフロー ](../assets/mm-input-output.png)
<!---
The detailed data-oriented flowchart below illustrates how:

* harmonized data is based on:

  * experience event data (originating from Analytics source connector, collected through Experience Platform SDKs and APIs, ingested through source connectors, or using streaming ingestion),
  * aggregate or summary data from walled gardens (like Facebook, YouTube), traffic sources, or offline advertising data, and 
  * definitions of harmonized fields and dataset rules.

* a model is based on:

  * the conversion and marketing touchpoint definitions resulting from the harmonized data and 
  * non-marketing aggregate or summary data containing internal or external factors.

* mult-touch attribution event scores can potentially be fed back into Experience Platform data lake for use in subsequent model configuration, training and scoring.

![Comprehensive workflow](/help/assets/comprehensive-workflow.svg)

-->
