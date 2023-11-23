---
title: スコアリングデータ
description: モデルのスコアリングデータをMix Modelerで保持する方法を説明します。
feature: Models
source-git-commit: 3596b83937b3f61ac453940f3a666d8aaf713679
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 10%

---


# スコアリングデータ

モデルのスコアリングの一環として、スコアリングデータは、データセット内のExperience Platformに保持されます。 このデータセットは、スキーマインスタンスの各モデルに対して作成されたMix Modelerに準拠します。

スコアリングデータのスキーマの名前は、次のようになります。 `AMM AI Schema - <name of model> <id>`. 例：`AMM AI Schema - Model for Online Conversion 10120`。

モデルのスコアリングデータを保持するデータセットの名前は、次のようになります。 `AMM AI Aggregrate Scores - <id>`例： `AMM AI Aggregrate Scores - 10120`.


## スキーマ

スキーマには、スコアに関する詳細を含むオブジェクトを持つフィールドグループが含まれます。 このオブジェクトは、次のフィールドで構成されます。

| フィールド名 | タイプ | 定義 |
|---|---|---|
| **campaignGroup** | 文字列 | キャンペーングループの名前。 |
| **campaignName** | 文字列 | キャンペーンの名前。 |
| **投稿** | Double | 特定のタッチポイントに対するこのコンバージョンに起因する貢献度。 |
| **conversionEndDate** | 日付 | 変換ウィンドウの終了日です。 |
| **conversionName** | 文字列 | 変換定義の設定手順で作成された変換の名前。 |
| **conversionStartDate** | 日付 | 変換ウィンドウの開始日です。 |
| **地域** | 文字列 | コンバージョンが発生した地理的な場所。 |
| **mediaChannel** | 文字列 | タッチポイントの設定手順で使用されたチャネルの名前。 |
| **mediaSubChannel** | 文字列 | サブチャネルの名前。 |
| **売上高** | Double | 特定のタッチポイントに対するこのコンバージョンに起因する売上高。 |
| **scoreCreatedTime** | 日時 | このスコアレコードが作成された時間。 |
| **touchpointEndDate** | 日付 | タッチポイントウィンドウの終了日です。 |
| **touchpointName** | 文字列 | タッチポイントの定義の設定手順中に作成されたタッチポイントの名前です。 現在、タッチポイントはメディアチャネルで定義されています。 |
| **touchpointStartDate** | 日付 | タッチポイントウィンドウの開始日です。 |

