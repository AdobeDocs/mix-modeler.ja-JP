---
title: データを調和させる
description: データの調和を図る方法をMix Modeler。
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
source-git-commit: 4f4c7f05e90d73a0ab4865150b1ec4c2af88fc12
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 8%

---

# データを調和させる

Mix Modeler内のデータは、データのソースに応じて異なる特性を持ちます。 データは次のようになります。

* 集計データや概要データ。例えば、ウォールガーデンのデータソースから収集されたデータや、広告掲示板のキャンペーン、イベント、または物理的な広告キャンペーンの実行から収集された（支出など）オフライン広告データ。
* イベントデータ（例：ファーストパーティのデータソースから）。 このイベントデータは、Adobe AnalyticsのAdobe Analyticsソースコネクタを通じて収集したり、Experience PlatformWeb SDK、Mobile SDK、Edge Network API を通じて収集したり、ソースコネクタを使用して取り込んだデータにすることができます。

Mix Modelerの調和化サービスは、集計データとイベントデータを一貫したデータビューに同化します。 このデータビューは、内部および外部の要因データと組み合わされ、Mix Modelerのモデルのソースになります。 サービスは、様々なデータセットで最も高い精度を使用します。 例えば、1 つのデータセットに月単位の精度があり、残りのデータセットの精度が週単位および日単位の精度である場合、調和化サービスは月単位の精度を使用してデータビューを作成します。

## 調和されたデータの例

次のデータセットをMix Modelerに使用できるとします。

**データセット 1**

集計データの精度を「毎日」に設定した、YouTubeのマーケティング活動データセットが含まれます。

| 日付 | 日付タイプ | チャネル | Campaign | ブランド | ジオ | クリック数 | 費用 |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | 日 | YouTube | Y_Fall_02 | BrandX | US | 10000 | 100 |
| 01-01-2022 | 日 | YouTube | Y_Fall_02 | BrandX | US | 1000 | 10 |
| 01-03-2022 | 日 | YouTube | Y_Fall_01 | BrandY | CA | 10000 | 100 |
| 01-04-2022 | 日 | YouTube | Y_Summer_01 | Null | CA | 9000 | 80 |

{style="table-layout:auto"}


**データセット 2**

facebookのマーケティング活動データセットが含まれ、集計データの精度が週に設定されます。

| 日付 | 日付タイプ | チャネル | Campaign | ジオ | クリック数 | 費用 |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | 週 | Facebook | FB_Fall_01 | US | 8000 | 100 |
| 01-08-2022 | 週 | Facebook | FB_Fall_02 | US | 1000 | 10 |
| 01-08-2022 | 週 | Facebook | FB_Fall_01 | US | 7000 | 100 |
| 01-16-2022 | 週 | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**データセット 3**

集計データの精度が 1 日に設定されたコンバージョンデータセット。

| 日付 | 日付タイプ | ジオ | 目標 | 売上高 |
|--- |:---: |---|---|---:|
| 01-01-2022 | 日 | US | ファッション | 200 |
| 01-08-2022 | 日 | US | ファッション | 10 |
| 01-08-2022 | 日 | US | 宝飾品 | 1100 |
| 01-16-2022 | 日 | CA | 宝飾品 | 80 |

{style="table-layout:auto"}


**データセット 4**

顧客からのサンプルのエクスペリエンスイベントデータセット（Web SDK イベント）。

| タイムスタンプ | ID 名前空間 | ID | チャネル | クリック数 |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


週単位の精度を設定して、調整済みデータセットを作成する場合。 イベントデータは週の精度に集計され、調整済みデータセットに追加されます。 結果は次のようになります。

**調整済みデータセット**

| 日付 | 日付タイプ | チャネル | Campaign | ブランド | ジオ | 目標 | クリック数 | 費用 | 売上高 |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | 週 | YouTube | Y_Fall_02 | BrandX | US | Null | 11000 | 110 | Null |
| 01-03-2022 | 週 | YouTube | Y_Fall_01 | BrandY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 | 週 | YouTube | Y_Summer_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | 週 | Facebook | FB_Fall_01 | Null | US | Null | 8000 | 100 | Null |
| 01-08-2022 | 週 | Facebook | FB_Fall_02 | Null | US | Null | 1000 | 10 | Null |
| 01-08-2022 | 週 | Facebook | FB_Fall_01 | Null | US | Null | 7000 | 100 | Null |
| 01-16-2022 | 週 | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | 週 | Null | Null | Null | US | ファッション | Null | Null | 200 |
| 01-03-2022 | 週 | Null | Null | Null | US | ファッション | Null | Null | 10 |
| 01-03-2022 | 週 | Null | Null | Null | US | 宝飾品 | Null | Null | 1100 |
| 01-10-2022 | 週 | Null | Null | Null | CA | 宝飾品 | Null | Null | 80 |
| 01-01-2022 | 週 | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 | 週 | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## 調整済みデータの設定

シンプル化されたのと同様に、調整済みデータセットを作成するには [例](#an-example-of-harmonized-data)を使用する場合は、次の手順に従う必要があります。

1. 追加の [調和されたフィールド](fields.md) 既に利用可能なグローバル調整済みフィールド以外のフィールドを使用する
1. 設定 [データセットルール](dataset-rules.md) 集計またはエクスペリエンスイベントデータセットのフィールドを、調和されたフィールドにマッピングする。
1. 定義 [マーケティングタッチポイント](marketing-touchpoints.md) 定義済みの標準フィールドと追加のハーモナイズ済みフィールドを使用する。
1. 定義 [コンバージョン](conversions.md) 定義済みの標準フィールドと追加のハーモナイズ済みフィールドを使用する。


## 調整済みデータの表示

調和したデータを表示するには、Mix Modelerインターフェイスで次の操作を実行します。

1. 選択 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** をクリックします。

1. 選択 **[!UICONTROL Harmonized Data]** 上部のバーから。 調和したデータの概要は、定義したフィールド、データセットルール、マーケティングタッチポイントおよびコンバージョンに基づいて表示されます。

   1. 調整済みデータの概要の基となる期間を再定義するには、次の期間の日付範囲を入力します。 **[!UICONTROL Date range]** または、 ![カレンダー](../assets/icons/Calendar.svg) をクリックして、データ範囲を選択します。

   1. 調和済みデータテーブルに表示される調和済みフィールド列を変更するには、 ![設定](../assets/icons/Setting.svg) 開く **[!UICONTROL Column settings]** ダイアログ。

      1. 選択 ![SelectBox](../assets/icons/SelectBox.svg) 1 つ以上の列 **[!UICONTROL AVAILABLE COLUMNS]** とを使用します。 ![シェブロン右](../assets/icons/ChevronRight.svg) 次の列を追加： **[!UICONTROL SELECTED COLUMNS]**.

      1. 選択 ![SelectBox](../assets/icons/SelectBox.svg) 1 つ以上の列 **[!UICONTROL SELECTED COLUMNS]** とを使用します。 ![シェブロン左](../assets/icons/ChevronLeft.svg) 選択した列を削除し、これらの列を戻すには **[!UICONTROL AVAILABLE COLUMNS]**.

      1. 次の中から列を選択： **[!UICONTROL DEFAULT SORT]** と切り替えて **[!UICONTROL Ascending]** または **[!UICONTROL Descending]**.

      1. 表示される列の順序を変更するには、列を **[!UICONTROL SELECTED COLUMNS]** ドラッグ&amp;ドロップで上下に移動

   1. 選択 **[!UICONTROL Submit]** をクリックして、列設定の変更を送信します。 選択 **[!UICONTROL Close]** をクリックして、行った変更をキャンセルします。

1. 他のページが利用可能な場合は、 ![左向き矢印](../assets/icons/ChevronLeft.svg) または ![右向き矢印](../assets/icons/ChevronRight.svg) 時刻 **[!UICONTROL Page _x _/_x_]** ページ間を移動するには
