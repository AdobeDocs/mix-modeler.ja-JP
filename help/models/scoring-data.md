---
title: スコアリングデータ
description: Mix Modelerでのモデルのスコアリングデータの保持方法を説明します。
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 8%

---

# スコアリングデータ

モデルのスコアリングの一環として、スコアリングデータはExperience Platformのデータセット内に保持されます。 このデータセットは、Mix Modelerインスタンスの各モデル用に作成されたスキーマに準拠しています。

スコアリングデータのスキーマには、`AMM AI Schema - <name of model> <id>` のような名前が付けられます。 例：`AMM AI Schema - Model for Online Conversion 10120`。

モデルのスコアリングデータを保持するデータセットには、`AMM AI Aggregrate Scores - <id>` のような名前が付けられます（例：`AMM AI Aggregrate Scores - 10120`）。


## スキーマ

スキーマには、スコアに関する詳細を含むオブジェクトを持つフィールドグループが含まれています。 オブジェクトは、次のフィールドで構成されます。

| フィールド名 | タイプ | 定義 |
|---|---|---|
| **campaignGroup** | 文字列 | キャンペーングループの名前。 |
| **campaignName** | 文字列 | キャンペーンの名前。 |
| **投稿** | Double | 特定のタッチポイントに対してこのコンバージョンに起因する貢献度。 |
| **conversionEndDate** | 日付 | コンバージョンウィンドウの終了日。 |
| **conversionName** | 文字列 | コンバージョン定義の設定手順で作成されたコンバージョンの名前。 |
| **conversionStartDate** | 日付 | コンバージョンウィンドウの開始日。 |
| **geo** | 文字列 | コンバージョンが発生した地理的位置。 |
| **mediaChannel** | 文字列 | タッチポイントの設定手順で使用されたチャネルの名前。 |
| **mediaSubChannel** | 文字列 | サブチャネルの名前。 |
| **売上高** | Double | 特定のタッチポイントに対してこのコンバージョンに起因する収益。 |
| **scoreCreatedTime** | 日時 | このスコアレコードが作成された時間。 |
| **touchpointEndDate** | 日付 | タッチポイントウィンドウの終了日。 |
| **touchpointName** | 文字列 | タッチポイント定義の設定手順で作成されたタッチポイントの名前。 現在、タッチポイントはメディアチャネルで定義されています。 |
| **touchpointStartDate** | 日付 | タッチポイントウィンドウの開始日。 |

詳しくは、[ スキーマ ](../ingest-data/schemas.md) を参照してください。
