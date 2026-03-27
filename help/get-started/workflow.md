---
title: Mix Modeler workflow
description: Mix Modelerの一般的なワークフローを理解する。
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: e6f24c96e873804b37011a1afafb7012d999fc1b
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---

# Mix Modeler workflow

Mix Modelerのユーザーワークフローの概要については、このビデオを参照してください。

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Mix Modelerの一般的なワークフローは、次のアクティビティで構成されます。

![代替テキスト &#x200B;](/help/assets/ApplicationWorkflow.svg)

|  | アクティビティ | 説明 |
|---|---|---|
| ![データ](/help/assets/icons/Data.svg){width="100"} | [**データの取り込み**](../ingest-data/overview.md) | Experience Platformからイベントデータ（Adobe Analytics、Web SDK、その他のソースなど）、マーケティングチャネルから集約データ（TV、ウォールドガーデン、電子メール、所有および運営アクティビティなど）、顧客からの外部要因データ（サブスクリプションサービスの価格変更など）、内部要因データ（ホリデープランなど）を取り込みます。 |
| ![DataCheck](/help/assets/icons/DataCheck.svg){width="100"} | [**データの調和**](../harmonize-data/overview.md) | マッピングルールと競合解決ルールを設定して、Adobe Mix Modelerでキャンペーンのパフォーマンスを測定および計画するために必要なさまざまなマーケティングデータセットを統合できます。 |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**モデルを作成**](../models/overview.md) | マーケティングのタッチポイント（チャネルなど）、コンバージョンの定義、社内外の要因を使用してモデルインスタンスを構築します。 |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**モデルのトレーニングとスコアリング**](../models/overview.md) | マシンラーニングとスコアリングを利用して、集計レベルおよびイベントレベルのスコアを作成できます。 |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**プランの作成**](../plans/overview.md) | 計画の策定： Mix Modelerのモデルから得られるアウトプットを活用して、ビジネス目標を達成するために必要なマーケティング資金の配分を決定します。 |
| ![&#x200B; ダッシュボード &#x200B;](/help/assets/icons/Dashboard.svg){width="100"} | [**概要ダッシュボード**](../dashboard/overview.md) | 設定可能なさまざまなビジュアライゼーションを使用して、調和されたデータ、モデル、計画に関するインサイトを得ることができます。 |

{style="table-layout:auto"}

入力データをMix Modelerに流し込む方法と、Mix Modelerが独自のインターフェイス用だけでなく、Customer Journey Analyticsなどの他のソリューション用に出力データを生成する方法の概要を以下に示します。

![Mix Modeler入力出力データフロー](../assets/mm-input-output.png)

<!--
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
