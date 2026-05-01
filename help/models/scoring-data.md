---
title: スコアリングデータの活用
description: Mix Modelerのモデルのスコアリングデータがどのように保持されるかを説明します。
feature: Models
exl-id: 2f2c3d20-7b14-41cc-a11a-03e8ad9e5d7a
TQID: https://experienceleague.adobe.com/6eMg5Azsb-rdyG5g-hIkiyJrVbgOOul5V-0TvxzCTyo
autotag-review: '2026-05-01T08:58:54.964Z'
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: f40f1683-8300-4054-aab8-77da06ad63ff
subfeature_v2: id: cb40363e-1205-4921-971c-9ee6bdb18329
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 684
ht-degree: 25%

---

# スコアリングデータの活用

モデルのスコアリングの一部として、スコアリングデータはExperience Platformのデータセット内に保持されます。 モデル作成中にマルチタッチアトリビューションを有効にすると、追加のイベントスコアデータがExperience Platformのデータセット内に保持されます。

これらのデータセットはそれぞれスキーマに準拠しています。 この記事では、これらのスキーマについて説明します。


## 集計スコアリングデータスキーマ

データをスコアリングするためのスキーマの名前は`AMM AI Schema - <name of model> <id>`のようになっています。 例：`AMM AI Schema - Model for Online Conversion 10120`。

モデルのスコアリングデータを保持するデータセットは、例えば`AMM AI Aggregrate Scores - 10120`のように`AMM AI Aggregrate Scores - <id>`という名前になります。

スキーマには、スコアに関する詳細を含むオブジェクトを含むフィールドグループが含まれます。 オブジェクトは次のフィールドで構成されます。

| フィールド名 | タイプ | 定義 |
|---|---|---|
| `campaignGroup` | 文字列 | キャンペーングループの名前。 |
| `campaignName` | 文字列 | キャンペーンの名前。 |
| `contribution` | Double | 特定のタッチポイントに対するこのコンバージョンに起因する貢献度。 |
| `conversionEndDate` | 日付 | コンバージョンウィンドウの終了日。 |
| `conversionName` | 文字列 | コンバージョン定義設定手順で作成されたコンバージョンの名前。 |
| `conversionStartDate` | 日付 | コンバージョンウィンドウの開始日。 |
| `geo` | 文字列 | コンバージョンが発生した地理的な場所。 |
| `mediaChannel` | 文字列 | タッチポイントの設定手順で使用されたチャネルの名前。 |
| `mediaSubChannel` | 文字列 | サブチャネルの名前。 |
| `revenue` | Double | 特定のタッチポイントに対するこのコンバージョンに起因する売上。 |
| `scoreCreatedTime` | 日時 | このスコアレコードが作成されるタイミング。 |
| `touchpointEndDate` | 日付 | タッチポイントウィンドウの終了日。 |
| `touchpointName` | 文字列 | タッチポイント定義設定手順で作成されたタッチポイントの名前。 現在、タッチポイントはメディアチャネルで定義されています。 |
| `touchpointStartDate` | 日付 | タッチポイントウィンドウの開始日。 |


## イベントスコアリングデータスキーマ

データをスコアリングするためのスキーマの名前は`Attribution AI Scores - <name of model> <id> - Schema`のようになっています。 例：`Attribution AI Scores - Model for Online Conversion 10120 - Schema`。

モデルのスコアリングデータを保持するデータセットは、例えば`Attribution AI Scores - Model for Online Conversion 10120 `のように`Attribution AI Scores - <name of model> <id>`という名前になります。

スキーマは、コアに関する詳細を含むオブジェクトを含むフィールドグループを含む。 オブジェクトの名前は`attibution_AI_scores__<name of model> id`のようです。

フィールドグループには、次のフィールドが含まれます。

| フィールド名 | タイプ | 説明 |
|---|---|---|
| `conversion` | オブジェクト | コンバージョンメタデータ列： |
|     `passThrough` | オブジェクト |  |
|         `eventType` | 文字列 | |
|         `channel_typeAtSource` | 文字列 | |
|      `dataSource` | 文字列 | データソースのグローバルに一意のID。<br> **例：** `Adobe Analytics` |
|      `eventSource` | 文字列 | 実際のイベントが発生したソース。<br> **例：** `Adobe.com` |
|      `eventType` | 文字列 | この時系列レコードのプライマリイベントタイプ。<br> **例：** `Order` |
|      `geo` | 文字列 | コンバージョンが配信された地理的な場所`placeContext.geo.countryCode`。<br> **例：** `US` |
|      `path` | 文字列 | |
|      `priceTotal` | Double | コンバージョン <br>を通じて獲得した収益 **例：** `99.9` |
|      `product` | 文字列 | 製品自体のXDM ID。<br> **例：** `RX 1080 ti` |
|      `productType` | 文字列 | この製品ビューのユーザーに表示される製品の表示名。<br> **例：** `Gpus` |
|      `quantity` | 整数 | コンバージョン時に購入した数量。<br> **例：** `1` |
|      `receivedTimeStamp` | 日時 | コンバージョンの受信タイムスタンプ。<br> **例：** `2020-06-09T00:01:51.000Z` |
|      `skuId` | 文字列 | SKU （在庫保管単位）：ベンダーが定義した商品の一意のID。<br> **例：** `MJ-03-XS-Black` |
|      `timestamp` | 日時 | コンバージョンのタイムスタンプ。<br> **例：** `2020-06-09T00:01:51.000Z` |
|      `totalDaysToConversion` | 整数 |  |
|      `totalTouchpointCount` | 整数 | |
| `customerProfile` | オブジェクト | モデルの構築に使用したユーザーのIDの詳細。 |
|      `identity` | オブジェクト | |
|           `id` | 文字列 | |
|           `namespace` | 文字列 | `id`や`namespace`など、モデルの構築に使用されるユーザーの詳細が含まれます。 |
| `touchpointsDetail` | オブジェクト [] | コンバージョンに至るタッチポイントの詳細のリスト。タッチポイントの発生またはタイムスタンプで並べ替えられます。 |
|      `scores` | オブジェクト | このコンバージョンへのタッチポイントの貢献度をスコアとして求めます。 |
|           `algorithmicInfluenced` | Double | 影響スコアは、各マーケティングタッチポイントがコンバージョンに寄与している割合です。 |
|           `algorithmicSourced` | Double | 増分スコアは、マーケティングタッチポイントで直接引き起こされたわずかな影響の量です。 |
|           `decayUnits` | Double | コンバージョンに近いタッチポイントが、コンバージョンから遠いタッチポイントよりも多くのクレジットを受け取るルールベースのアトリビューションスコアです。 |
|           `firstTouch` | Double | コンバージョンパスの最初のタッチポイントにすべてのクレジットを割り当てるルールベースのアトリビューションスコアです。 |
|           `lastTouch` | Double | コンバージョンに最も近いタッチポイントにすべてのクレジットを割り当てるルールベースのアトリビューションスコアです。 |
|           `linear` | Double | コンバージョンパスの各タッチポイントに同等のクレジットを割り当てるルールベースのアトリビューションスコアです。 |
|           `uShape` | Double | ルールベースのアトリビューションスコアにより、最初のタッチポイントに40%、最後のタッチポイントに40%のクレジットが割り当てられます。 残りの20%を均等に分配するほかのタッチポイントも同様です。 |
|      `touchPoint` | オブジェクト | タッチポイントメタデータ： |
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
|      `touchpointName` | 文字列 | 設定中に設定されたタッチポイントの名前。<br> **例：** `PAID_SEARCH_CLICK` |
| `conversionName` | 文字列 | 設定中に設定されたコンバージョンの名前。<br> **例：** `Order`、`Lead`、`Visit` |
| `scoreCreatedTime` | 日時 | |
| `segmentation` | 文字列 | ジオセグメンテーションなどのコンバージョンセグメントを作成します。 セグメントが存在しない場合、`segmentation`は`conversionName`と同じです。<br> **例：** `ORDER_US` |





詳しくは、[ スキーマ ](../ingest-data/schemas.md)を参照してください。
