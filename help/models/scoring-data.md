---
title: スコアリングデータ
description: Mix Modelerでのモデルのスコアリングデータの保持方法を説明します。
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
source-git-commit: b6045176e82b97f848113f4e0ffbbb995c48b3d4
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 25%

---

# スコアリングデータ

モデルのスコアリングの一環として、スコアリングデータはExperience Platformのデータセット内に保持されます。 モデルの作成時にマルチタッチアトリビューションを有効にした場合、追加のイベントスコアデータはExperience Platformのデータセット内に保持されます。

これらの各データセットは、スキーマに準拠しています。 この記事では、これらのスキーマについて説明します。


## スコアリングデータスキーマを集計

スコアリングデータのスキーマには、`AMM AI Schema - <name of model> <id>` のような名前が付けられます。 例：`AMM AI Schema - Model for Online Conversion 10120`。

モデルのスコアリングデータを保持するデータセットには、`AMM AI Aggregrate Scores - <id>` のような名前が付けられます（例：`AMM AI Aggregrate Scores - 10120`）。

スキーマには、スコアに関する詳細を含むオブジェクトを持つフィールドグループが含まれています。 オブジェクトは、次のフィールドで構成されます。

| フィールド名 | タイプ | 定義 |
|---|---|---|
| `campaignGroup` | 文字列 | キャンペーングループの名前。 |
| `campaignName` | 文字列 | キャンペーンの名前。 |
| `contribution` | Double | 特定のタッチポイントに対してこのコンバージョンに起因する貢献度。 |
| `conversionEndDate` | 日付 | コンバージョンウィンドウの終了日。 |
| `conversionName` | 文字列 | コンバージョン定義の設定手順で作成されたコンバージョンの名前。 |
| `conversionStartDate` | 日付 | コンバージョンウィンドウの開始日。 |
| `geo` | 文字列 | コンバージョンが発生した地理的位置。 |
| `mediaChannel` | 文字列 | タッチポイントの設定手順で使用されたチャネルの名前。 |
| `mediaSubChannel` | 文字列 | サブチャネルの名前。 |
| `revenue` | Double | 特定のタッチポイントに対してこのコンバージョンに起因する収益。 |
| `scoreCreatedTime` | 日時 | このスコアレコードが作成されたときのタイムスタンプ。 |
| `touchpointEndDate` | 日付 | タッチポイントウィンドウの終了日。 |
| `touchpointName` | 文字列 | タッチポイント定義の設定手順で作成されたタッチポイントの名前。 現在、タッチポイントはメディアチャネルで定義されています。 |
| `touchpointStartDate` | 日付 | タッチポイントウィンドウの開始日。 |


## イベントスコアリングデータスキーマ

スコアリングデータのスキーマには、`Attribution AI Scores - <name of model> <id> - Schema` のような名前が付けられます。 例：`Attribution AI Scores - Model for Online Conversion 10120 - Schema`。

モデルのスコアリングデータを保持するデータセットには、`Attribution AI Scores - <name of model> <id>` のような名前が付けられます（例：`Attribution AI Scores - Model for Online Conversion 10120 `）。

スキーマには、コアの詳細を含むオブジェクトを含むフィールドグループが含まれています。 オブジェクトの名前は `attibution_AI_scores__<name of model> id` のようになります。

フィールドグループには、次のフィールドが含まれます。

| フィールド名 | タイプ | 説明 |
|---|---|---|
| `conversion` | オブジェクト | 変換メタデータ列。 |
|     `passThrough` | オブジェクト |  |
|         `eventType` | 文字列 | |
|         `channel_typeAtSource` | 文字列 | |
|      `dataSource` | 文字列 | データソースのグローバルに一意の ID。<br> **例：** `Adobe Analytics` |
|      `eventSource` | 文字列 | 実際のイベントが発生したソース。<br> **例：** `Adobe.com` |
|      `eventType` | 文字列 | この時系列レコードの主なイベントタイプ。<br> **例：** `Order` |
|      `geo` | 文字列 | コンバージョンが配信された地理的 `placeContext.geo.countryCode` 場所。<br> **例：** `US` |
|      `path` | 文字列 | |
|      `priceTotal` | Double | コンバージョン <br> を通じて得られた収益 **例：** `99.9` |
|      `product` | 文字列 | 製品自体の XDM 識別子。<br> **例：** `RX 1080 ti` |
|      `productType` | 文字列 | この商品表示でユーザーに提示される商品の表示名。<br> **例：** `Gpus` |
|      `quantity` | 整数 | コンバージョン中に購入された数量。<br> **例：** `1` |
|      `receivedTimeStamp` | 日時 | コンバージョンのタイムスタンプを受信しました。<br> **例：** `2020-06-09T00:01:51.000Z` |
|      `skuId` | 文字列 | 最小在庫管理単位（SKU）。ベンダーによって定義された商品の一意の ID。<br> **例：** `MJ-03-XS-Black` |
|      `timestamp` | 日時 | コンバージョンのタイムスタンプ。<br> **例：** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | 整数 |  |
|      `totalTouchpointCount` | 整数 | |
| `customerProfile` | オブジェクト | モデルの構築に使用されるユーザーの ID の詳細。 |
|      `identity` | オブジェクト | |
|           `id` | 文字列 | |
|           `namespace` | 文字列 | `id` や `namespace` など、モデルの構築に使用されるユーザーの詳細が含まれます。 |
| `touchpointsDetail` | オブジェクト [] | コンバージョンに至るタッチポイントの詳細のリスト （タッチポイント発生またはタイムスタンプ順）。 |
|      `scores` | オブジェクト | このコンバージョンに対するタッチポイントの貢献度（スコア）。 |
|           `algorithmicInfluenced` | Double | 影響スコアは、各マーケティングタッチポイントがコンバージョンに寄与している割合です。 |
|           `algorithmicSourced` | Double | 増分スコアは、マーケティングタッチポイントで直接引き起こされたわずかな影響の量です。 |
|           `decayUnits` | Double | コンバージョンに近いタッチポイントが、コンバージョンから遠いタッチポイントよりも多くのクレジットを受け取るルールベースのアトリビューションスコアです。 |
|           `firstTouch` | Double | コンバージョンパスの最初のタッチポイントにすべてのクレジットを割り当てるルールベースのアトリビューションスコアです。 |
|           `lastTouch` | Double | コンバージョンに最も近いタッチポイントにすべてのクレジットを割り当てるルールベースのアトリビューションスコアです。 |
|           `linear` | Double | コンバージョンパスの各タッチポイントに同等のクレジットを割り当てるルールベースのアトリビューションスコアです。 |
|           `uShape` | Double | 最初のタッチポイントにクレジットの 40%、最後のタッチポイントにクレジットの 40% を割り当てるルールベースのアトリビューションスコア。 他のタッチポイントは残りの 20% を均等に分割します。 |
|      `touchPoint` | オブジェクト | タッチポイントメタデータ。 |
|           `passThrough` | オブジェクト | |
|                `eventType` | 文字列 | |
|           `campaignGroup` | 文字列 |  |
|           `campaignName` | 文字列 | |
|           `campaignTag` | 文字列 | |
|           `eventId` | 文字列 | |
|           `geo` | 文字列 | |
|           `mediaAction` | 文字列 | |
|           `mediaChannel` | 文字列 | |
|           `receivedTimeStamp` | 日時 | |
|           `timestamp` | 日時 | |
|      `isFirstInThePosition` | 整数 | |
|      `lag` | 整数 | |
|      `position` | 文字列 | |
|      `touchpointCountToConversion` | 整数 | |
|      `touchpointName` | 文字列 | 設定時に設定されたタッチポイントの名前。<br> **例：** `PAID_SEARCH_CLICK` |
| `conversionName` | 文字列 | セットアップ時に設定されたコンバージョンの名前。<br> **例：** `Order`、`Lead`、`Visit` |
| `scoreCreatedTime` | 日時 | |
| `segmentation` | 文字列 | モデルの基になるコンバージョンセグメント（地理セグメント化など）。 セグメントが存在しない場合、`segmentation` は `conversionName` と同じです。<br> **例：** `ORDER_US` |





詳しくは、[ スキーマ ](../ingest-data/schemas.md) を参照してください。
