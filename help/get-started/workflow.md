---
title: Mix Modelerワークフロー
description: Mix Modelerの一般的なワークフローを理解する。
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Mix Modelerワークフロー

Mix Modelerのユーザーワークフローの概要については、このビデオを参照してください。

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


Mix Modelerの一般的なワークフローは、次のアクティビティで構成されます。

![ 代替テキスト ](/help/assets/ApplicationWorkflow.svg)

|  | Activity | 説明 |
|---|---|---|
| ![データ](/help/assets/icons/Data.svg){width="100"} | [**データの取り込み**](../ingest-data/overview.md) | Experience Platform（Adobe Analytics、Web SDK、その他のソースなど）からのイベントデータ、マーケティングチャネル（テレビ、壁庭、メール、所有および運営アクティビティなど）からの集計データ、顧客からの外部要因データ（購読サービスの価格変化など）および内部要因データ（休暇プランなど）を取り込みます。 |
| ![ データチェック ](/help/assets/icons/DataCheck.svg){width="100"} | [**データのハーモナイズ**](../harmonize-data/overview.md) | マッピングルールと競合解決ルールを設定して、Mix Modelerでキャンペーンのパフォーマンスを測定および計画するために必要な様々なマーケティングデータセットを結合します。 |
| ![FileConfig](/help/assets/icons/FileGear.svg){width="100"} | [**モデルの設定**](../models/create.md) | マーケティングタッチポイント（チャネルなど）、コンバージョン定義、内部要因および外部要因を持つモデルインスタンスを設定します。 |
| ![FileData](/help/assets/icons/FileData.svg){width="100"} | [**モデルのトレーニングとスコアリング**](../models/overview.md) | 機械学習のトレーニングとスコアリングを使用して、集計レベルとイベントレベルのスコアを作成します。 |
| ![FileChart](/help/assets/icons/FileChart.svg){width="100"} | [**プランの作成**](../plans/overview.md) | Mix Modelerのモデルの出力を使用して、ビジネス目標を達成するためのマーケティング資金の最適な配分を決定します。 |
| ![ ダッシュボード ](/help/assets/icons/Dashboard.svg){width="100"} | [**概要ダッシュボード**](../dashboard/overview.md) | 様々な設定可能なビジュアライゼーションを使用して、統一されたデータ、モデルおよびプランに関するインサイトを取得します。 |

{style="table-layout:auto"}

以下の詳細なデータ指向フローチャートで、その方法を説明します。

* 統一されたデータは以下に基づきます。

   * エクスペリエンスイベントデータ（Analytics ソースコネクタから発生し、Experience Platform SDK および API を通じて収集され、ソースコネクタを通じて取り込まれるか、ストリーミング取り込みを使用します）、
   * ウォールガーデン（Facebook、YouTubeなど）、トラフィックソース、オフライン広告データからの集計または概要データ
   * 統一フィールドとデータセットルールの定義。

* モデルのベースは次のとおりです。

   * 統一されたデータから生成されたコンバージョンおよびマーケティングタッチポイント定義および
   * 内部または外部要因を含む非マーケティングの集計または概要データ。

* マルチタッチのアトリビューションイベントスコアは、後続のモデル設定、トレーニングおよびスコアリングで使用するために、Experience Platformデータレイクにフィードバックされる可能性があります。

![ 包括的なワークフロー ](/help/assets/comprehensive-workflow.svg)
