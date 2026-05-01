---
title: データの取り込みの概要
description: Mix Modelerにデータを取り込む方法について説明します。
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
TQID: https://experienceleague.adobe.com/XPr8Av7skzHBYoU6WtNw8PtHFrPH-MokICrLwoB2-J0
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: e0abf868-dae2-4c1c-83e9-b21799232845
  - id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
subfeature_v2:
  - id: ad7101f7-ae92-401b-a25a-d3060d42989d
  - id: d1167c89-f64a-42ca-ac95-1d91b7790df2
  - id: ee1bf083-e090-4def-936b-c111d29f42d0
  - id: a4dc3e7d-bd07-4ac8-8e49-ff2e8fecf1e7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:11:34.506Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 584
ht-degree: 17%

---

# データの取り込みの概要

Mix Modelerは、さまざまなウォールドガーデンからのイベントレベルのデータ、集計または要約マーケティング活動データを扱います。 オフライン広告、内部要因、外部要因など、他のソースからのデータを集約または要約して使用できます。

お客様は、Experience Platformにデータセットとして取り込まれ、XDM ExperienceEventまたはXDM Summary Metricsをベースクラスとして使用するスキーマに基づく、あらゆる種類のデータを使用できます。

例：

* Adobe Analytics ソースコネクタを使用して収集されたデータ。 Adobe Analyticsスキーマのデフォルトまたはカスタムバージョンに準拠するデータセットに変換されます。
* Experience Platform Web SDK、モバイルSDK、Edge Network Server APIを使用して、web、モバイル、その他のタイプのデバイスでお客様とのやり取りを収集するデータ。
* ウォールドガーデン（Facebook、YouTubeなど）、トラフィックソース、オフライン広告データからデータを集約または要約します。
* モデル構築に役立つ内部要因または外部要因を含む、マーケティング以外の集計データまたは概要データ。

Experience Platformでサポートされている任意の種類の仕組みを使用して、エクスペリエンスイベントレベル、マーケティング活動データ、その他のソースからデータを取り込むことができます。 Experience Platform SDK、API、ソースコネクタ、ストリーミングやバッチ取り込みなど。 Adobe Mix Modelerで使用するためにExperience Platformでデータを取り込む方法について詳しくは、[&#x200B; データ取り込みの概要](https://experienceleague.adobe.com/ja/docs/experience-platform/ingestion/home)を参照してください。

## ガイドライン

Mix Modelerで使用するためにExperience Platformにデータを取り込むには、次のガイドラインに従います。

* データセットに追加される増分データに重複が生じないようにします。
* 単一のソースからのデータはすべて、同じ粒度である必要があります。
* 日付と精度は、データセットとして取り込まれたすべての集計データの基礎となるスキーマの必須フィールドです
* チャネルは、データセットとして取り込まれたすべてのマーケティング活動/支出データの基礎となるスキーマの必須フィールドです。


## 例

ここでは、Mix Modelerで一般的に使用されるデータの例をいくつか紹介します。

+++ マーケティング活動データの集計

| 地域 | 日付 | 日付タイプ | チャネル | Campaign | Click | アーンド | エンゲージメント | インプレッション | オープン | 所有 | 送信済み | 支出 |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| AMER | 2021-10-31 | 日 | EMAIL | | 12752 | | | | | | 1132945 | |
| AMER | 2021-10-31 | 日 | FB | | 148844 | | | | | | | 42111 |
| AMER | 2021-10-31 | 日 | YT | | | | 2314452 | | | | | 10540 |
| JPN | 2021-10-21 | 日 | EMAIL | | 21089 | | | | | | 3283626 | |
| JPN | 2021-10-21 | 日 | ソーシャル | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ コンバージョンデータの集計

| 地域 | 日付 | 日付タイプ | 製品 | 販売個数 | 売上高 |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | 日 | クリエイターエコノミー | 603 | 36537.68 |
| EMEA | 2021-09-13 | 日 | メタバース | 55 | 21704.37 |
| JPN | 2022-05-30 | 日 | Pro Imaging | 487 | 64469.60 |
| JPN | 2022-05-30 | 日 | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ 外部要因データ

| データ | 日付タイプ | 因子 | 値 |
|---|:---:|:---:|:---|
| 2020-08-02 | 週 | SPX | 3325.866 |
| 2020-08-09 | 週 | SPX | 3364.158 |
| 2020-08-16 | 週 | SPX | 3385.858 |
| 2020-08-23 | 週 | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Mix Modelerでデータを使用するには、データセットで収集され、Experience Platformのスキーマに従ってモデル化されたデータが必要です。 Mix Modeler インターフェイスでは、Experience Platform スキーマとデータセット UIの両方に簡単にアクセスできます。


## 検証

Mix Modelerでデータが適切に使用可能かどうかを検証するには、次の操作を行います。

* [概要](/help/overview.md)でビジュアライゼーションを使用します。
* 調和されたデータセットの[調和されたデータ &#x200B;](/help/harmonize-data/overview.md)からデータをダウンロードして検査します。

データがExperience Platformに正しく取り込まれているかどうかを検証するには、Experience Platform クエリサービス [&#128279;](https://experienceleague.adobe.com/ja/docs/experience-platform/query/home)を使用してSQL クエリを書き込み、実行できます。


>[!MORELIKETHIS]
>
>スキーマとデータセットの管理方法について詳しくは、以下を参照してください。
>
>* [スキーマ](schemas.md)
>* [データセット](datasets.md)
