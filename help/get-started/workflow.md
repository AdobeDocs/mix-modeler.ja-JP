---
title: Mix Modelerワークフロー
description: Mix Modelerの一般的なワークフローを理解する。
feature: Ingest Data, Plans, Harmonized Data, Models
exl-id: 200ff846-5d78-4b25-a425-bfd558b88c88
source-git-commit: 512cc28a9fab81438d54e30bb6e20f05da5265d1
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# Mix Modelerワークフロー

Mix Modelerのユーザーワークフローの概要については、このビデオを参照してください。

>[!VIDEO](https://video.tv.adobe.com/v/3424854/?learn=on)


機能的な観点から、Mix Modelerの典型的なワークフローは、次のアクティビティで構成されます。

![代替テキスト](../assets/ApplicationWorkflow.svg)

|  | アクティビティ | 説明 |
|---|---|---|
| ![データ](../assets/icons/Data.svg){width="100"} | [**データの取得**](../ingest-data/overview.md) | Experience Platform( 例：Adobe Analytics、Web SDK、その他のソース ) からのイベントデータの取り込み、マーケティングチャネルからの集計データ（例：TV、ウォールガーデン、E メール、所有および操作済みのアクティビティ）、顧客からの外部要因データ（例：購読サービスの価格変更）。 |
| ![DataCheck](../assets/icons/DataCheck.svg){width="100"} | [**データを調和させる**](../harmonize-data/overview.md) | マッピングルールと競合解決ルールを設定し、Mix Modelerでキャンペーンのパフォーマンスを測定し計画するために必要な様々なマーケティングデータセットを結合します。 |
| ![FileConfig](../assets/icons/FileGear.svg){width="100"} | [**モデルの設定**](../models/create.md) | マーケティングタッチポイント（例：チャネル）とコンバージョンの定義を使用してモデルインスタンスを設定します。 |
| ![FileData](../assets/icons/FileData.svg){width="100"} | [**モデルのトレーニングとスコアリング**](../models/overview.md) | 機械学習のトレーニングとスコアリングを使用して、集計とイベントレベルのスコアを作成します。 |
| ![FileChart](../assets/icons/FileChart.svg){width="100"} | [**プランの作成**](../plans/overview.md) | Mix Modelerのモデルの出力を使用して、ビジネス目標を達成するためのマーケティング資金の最適な配分を決定します。 |
| ![ダッシュボード](../assets/icons/Dashboard.svg){width="100"} | [**概要ダッシュボード**](../dashboard/overview.md) | 様々な設定可能なウィジェットを使用して、調和されたデータ、モデル、プランに関するインサイトを得ます。 |

{style="table-layout:auto"}
