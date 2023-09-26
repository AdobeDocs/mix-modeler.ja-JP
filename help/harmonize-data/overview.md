---
title: データを調和させる
description: Mix Modeler でデータを調整する方法をAdobeします。
feature: Harmonized Data
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 17%

---


# データを調和させる

AdobeMix Modeler のデータは、データのソースに応じて異なる性質を持ちます。 データは次のようになります。

* 集計データ（例えば、ウォールガーデンのデータソースから収集）。
* イベントデータ（例：ファーストパーティのデータソースから）。 このイベントデータは、Adobe AnalyticsのAdobe Analyticsソースコネクタを通じて収集したり、Adobe Experience Platform Web、Mobile SDK、Edge Network API を通じて収集したり、ソースコネクタを使用して取り込んだデータにしたりできます。

AdobeMix Modeler の調和サービスは、集計とイベントのデータを一貫したデータビューに同化します。 このデータビューは、AdobeMix モデラのプランとモデルのソースです。

## 調和されたデータの例

AdobeMix Modeler で使用できる次のデータセットがあるとします。

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
| 01-01-2022 | 週間 | Facebook | FB_Fall_01 | US | 8000 | 100 |
| 01-08-2022 | 週間 | Facebook | FB_Fall_02 | US | 1000 | 10 |
| 01-08-2022 | 週間 | Facebook | FB_Fall_01 | US | 7000 | 100 |
| 01-16-2022 | 週間 | Facebook | FB_Summer_01 | CA | 10000 | 80 |

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
| 12-27-2021 | 週間 | YouTube | Y_Fall_02 | BrandX | US | Null | 11000 | 110 | Null |
| 01-03-2022 | 週間 | YouTube | Y_Fall_01 | BrandY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 | 週間 | YouTube | Y_Summer_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | 週間 | Facebook | FB_Fall_01 | Null | US | Null | 8000 | 100 | Null |
| 01-08-2022 | 週間 | Facebook | FB_Fall_02 | Null | US | Null | 1000 | 10 | Null |
| 01-08-2022 | 週間 | Facebook | FB_Fall_01 | Null | US | Null | 7000 | 100 | Null |
| 01-16-2022 | 週間 | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | 週間 | Null | Null | Null | US | ファッション | Null | Null | 200 |
| 01-03-2022 | 週間 | Null | Null | Null | US | ファッション | Null | Null | 10 |
| 01-03-2022 | 週間 | Null | Null | Null | US | 宝飾品 | Null | Null | 1100 |
| 01-10-2022 | 週間 | Null | Null | Null | CA | 宝飾品 | Null | Null | 80 |
| 01-01-2022 | 週間 | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 | 週間 | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## 調整済みデータの設定

シンプル化されたのと同様に、調整済みデータセットを作成するには [例](#an-example-of-harmonized-data)を使用する場合は、次の手順に従う必要があります。

1. 追加の [調和されたフィールド](fields.md) 既に利用可能なグローバル調整済みフィールド以外のフィールドを使用する
1. 設定 [データセットルール](dataset-rules.md) 集計またはエクスペリエンスイベントデータセットのフィールドを、調和されたフィールドにマッピングする。
1. 定義 [マーケティングタッチポイント](marketing-touchpoints.md) 定義済みの標準フィールドと追加のハーモナイズ済みフィールドを使用する。
1. 定義 [コンバージョン](conversions.md) 定義済みの標準フィールドと追加のハーモナイズ済みフィールドを使用する。


## 調整済みデータの表示

調整済みのデータを表示するには、Mix ModelerAdobeで次の手順を実行します。

1. 選択 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]** をクリックします。

1. 選択 **[!UICONTROL Harmonized Data]** 上部のバーから。 定義したフィールド、データセットルール、マーケティングタッチポイントおよびコンバージョンに基づいて、調和されたデータの概要が表示されます。

   1. 調整済みデータの概要の基となる期間を再定義するには、次の期間の日付範囲を入力します。 **[!UICONTROL Date range]** または、 ![カレンダー](../assets/icons/Calendar.svg) をクリックして、データ範囲を選択します。

   1. 「ハーモナイズされたデータ」テーブルに表示される列を変更するには、 ![設定](../assets/icons/Setting.svg) 開く **[!UICONTROL Column settings]** ダイアログ。

      1. 選択 ![SelectBox](../assets/icons/SelectBox.svg) 1 つ以上の列 **[!UICONTROL AVAILABLE COLUMNS]** とを使用します。 ![シェブロン右](../assets/icons/ChevronRight.svg) 次の列を追加： **[!UICONTROL SELECTED COLUMNS]**.

      1. 選択 ![SelectBox](../assets/icons/SelectBox.svg) 1 つ以上の列 **[!UICONTROL SELECTED COLUMNS]** とを使用します。 ![シェブロン左](../assets/icons/ChevronLeft.svg) 選択した列を削除し、これらの列を戻すには **[!UICONTROL AVAILABLE COLUMNS]**.

      1. 次の中から列を選択： **[!UICONTROL DEFAULT SORT]** と切り替えて **[!UICONTROL Ascending]** または **[!UICONTROL Descending]**.

      1. 表示される列の順序を変更するには、列を **[!UICONTROL SELECTED COLUMNS]** 上下にドラッグ&amp;ドロップします。

   1. 選択 **[!UICONTROL Submit]** をクリックして、列設定の変更を送信します。 選択 **[!UICONTROL Close]** をクリックして、行った変更をキャンセルします。


