---
title: AdobeMix Modeler ワークフロー
description: Mix Modeler の一般的なAdobeを理解します。
feature: Datasets, Event Datasets, Plans, Harmonized Data, Models
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 4%

---


# AdobeMix Modeler ワークフロー

Mix Modeler の一般的なAdobeは次のようになります。

![代替テキスト](../assets/ApplicationWorkflow.svg)

|  | アクティビティ | 説明 |
|---|---|---|
| ![データ](../assets/icons/Data.svg){width="100"} | [**データの取得**](../ingest-data/overview.md) | Adobe Experience Platform( 例：Adobe Analytics、Web SDK、その他のソース ) からのイベントデータの取り込み、マーケティングチャネルからの集計データ（例：TV、ウォールガーデン、E メール、所有および操作されたアクティビティ）および顧客からの外部要因データ（例：購読サービスの価格変更）。 |
| ![DataCheck](../assets/icons/DataCheck.svg){width="100"} | [**データを調和させる**](../harmonize-data/overview.md) | マッピングルールと競合解決ルールを設定し、マッピングミックスモデラーでキャンペーンのパフォーマンスを測定および計画するために必要な様々なマーケティングデータセットをAdobeします。 |
| ![FileConfig](../assets/icons/FileGear.svg){width="100"} | [**モデルの設定**](../models/create.md) | マーケティングタッチポイント（例：チャネル）とコンバージョンの定義を使用してモデルインスタンスを設定します。 |
| ![FileData](../assets/icons/FileData.svg){width="100"} | [**モデルのトレーニングとスコアリング**](../models/overview.md) | 機械学習のトレーニングとスコアリングを使用して、集計とイベントレベルのスコアを作成します。 |
| ![FileChart](../assets/icons/FileChart.svg){width="100"} | [**プランの作成**](../plans/overview.md) | Adobeミックスモデラーのモデルの出力を使用して、ビジネス目標を達成するためのマーケティング資金の最適な配分を決定します。 |
| ![ダッシュボード](../assets/icons/Dashboard.svg){width="100"} | [**概要ダッシュボード**](../dashboard/overview.md) | 様々な設定可能なウィジェットを使用して、調和されたデータ、モデル、プランに関するインサイトを得ます。 |

{style="table-layout:auto"}

