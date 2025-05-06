---
title: データの取り込みの概要
description: データをMix Modelerに取り込む方法を説明します。
feature: Datasets, Event Datasets, Summary Datasets, Aggregate Datasets
exl-id: dc16a601-bbd9-467b-8a7e-c32654d4069a
source-git-commit: bb05cee1d4e2245cf665e5dcea17a30c5c0cf203
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 10%

---

# データの取り込みの概要

Mix Modelerは、イベントレベルのデータ、様々な壁庭からの集計または概要マーケティング労力データ、他のソース（オフライン広告、内部要因、外部要因など）からの集計または概要データで動作します。

お客様は、Experience Platformにデータセットとして取り込まれ、XDM ExperienceEvent または XDM Summary Metrics を基本クラスとして使用するスキーマに基づく、あらゆる種類のデータを使用できます。

例：

* Adobe Analytics ソースコネクタを使用して収集されたデータで、Adobe Analytics スキーマのデフォルトまたはカスタムバージョン（または）に従ったデータセットに変換されたもの
* web、モバイル、またはその他のタイプのデバイスに対する顧客のインタラクションを収集するためにExperience Platform Web SDK、Mobile SDKまたはEdge Network Server API を使用して収集されたデータ。
* ウォールガーデン（Facebook、YouTubeなど）、交通源、オフライン広告データからの集計または概要データ
* モデルの構築に役立つ内部または外部の要因を含む、マーケティング以外の集計または概要データ。

Experience Platformでサポートされているあらゆる種類のメカニズムを使用して、エクスペリエンスイベントレベル、マーケティング活動データの集計、他のソースからのデータを取り込むことができます。 取り込みメカニズムには、Experience Platform SDK、API、ソースコネクタ、ストリーミング取り込み、バッチ取り込みが含まれます。 Adobe Mix Modelerで使用するデータをExperience Platformで取り込む方法については、[ データ取り込みの概要 ](https://experienceleague.adobe.com/ja/docs/experience-platform/ingestion/home) を参照してください。

## ガイドライン

Mix Modelerで使用するデータをExperience Platformに取り込むには、次のガイドラインに従います。

* データセットに追加される増分データには、重複がないようにする必要があります。
* 単一のソースからのすべてのデータは、同じ精度にする必要があります。
* 日付と精度は、データセットとして取り込まれるすべての集計データの基になるスキーマの必須フィールドです
* チャネルは、データセットとして取り込まれたすべてのマーケティング活動/費用データの基になるスキーマの必須フィールドです。


## 例

より標準的なエクスペリエンスイベントデータに加えて、Mix Modelerで通常使用されるデータの例をいくつか以下に示します。

+++ マーケティング活動データの集計

| ジオ | 日付 | 日付タイプ | チャネル | Campaign | クリック | 獲得済み | エンゲージメント | インプレッション | Open | 所有 | 送信済み | 費用 |
|---|:--|---|:---:|---|--:|---|--:|---|---|---|--:|--:|
| アメル | 2021-10-31 | 日 | EMAIL | | 12752 | | | | | | 1132945 | |
| アメル | 2021-10-31 | 日 | FB | | 148844 | | | | | | | 42111 |
| アメル | 2021-10-31 | 日 | YT | | | | 2314452 | | | | | 10540 |
| 日本 | 2021-10-21 | 日 | EMAIL | | 21089 | | | | | | 3283626 | |
| 日本 | 2021-10-21 | 日 | ソーシャル | | | | 621 | | | | | 74512 |

{style="table-layout:auto"}

+++

+++ コンバージョンデータを集計

| ジオ | 日付 | 日付タイプ | 製品 | 販売数 | 収益 |
|---|:---|:---:|---|--:|--:|
| EMEA | 2021-09-13 | 日 | 創造者経済 | 603 | 36537.68 |
| EMEA | 2021-09-13 | 日 | メタバース | 55 | 21704.37 |
| 日本 | 2022-05-30 | 日 | Pro イメージング | 487 | 64469.60 |
| 日本 | 2022-05-30 | 日 | Document Cloud | 642 | 100509.07 |

{style="table-layout:auto"}

+++

+++ 外部要因データ

| データ | 日付タイプ | 要因 | 値 |
|---|:---:|:---:|:---|
| 2020-08-02 | 週間 | SPX | 3325.866 |
| 2020-08-09 | 週間 | SPX | 3364.158 |
| 2020-08-16 | 週間 | SPX | 3385.858 |
| 2020-08-23 | 週間 | SPX | 3497.965 |

{style="table-layout:auto"}

+++

Mix Modelerのデータを操作するには、データセットで収集され、Experience Platformのスキーマに倣ってモデル化されたデータが必要です。 Mix Modeler インターフェイスを使用すると、Experience Platform スキーマとデータセット UI の両方に簡単にアクセスできます。


## 検証

データがMix Modelerで適切に使用可能かどうかを検証するには、次の操作を実行します。

* [ 概要 ](/help/overview.md) でビジュアライゼーションを使用する。
* 統一データセットの [ 統一データ ](/help/harmonize-data/overview.md) からデータをダウンロードして検査します。

データがExperience Platformに正しく取り込まれているかどうかを検証するには、[Experience Platform クエリサービスを使用して SQL クエリを記述し、実行する ](https://experienceleague.adobe.com/en/docs/experience-platform/query/home) ことができます。


>[!MORELIKETHIS]
>
>スキーマとデータセットの管理方法について詳しくは、を参照してください。
>
>* [スキーマ](schemas.md)
>* [データセット](datasets.md)
