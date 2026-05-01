---
title: データセットの概要を調和
description: Mix Modelerでデータを調和させる方法をご確認ください。
feature: Harmonized Data
exl-id: 6cb70762-e3b2-46a0-b028-1d6daf3edae5
TQID: https://experienceleague.adobe.com/9ki9Q-ZAmwmiyYFt-EAaa1ybylaoMauTvoxQ9ux1IEI
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
subfeature_v2:
  - id: bc2f5225-03d4-4bc8-89ec-99d78c30e6dd
  - id: d4b8ba18-64c1-4413-be54-74405ec7f558
  - id: ba4fd72c-282e-4fb6-abc1-08e6fb87b2ad
  - id: b4655f7e-1a6e-4fa3-a7c5-3c34d4786e49
  - id: b2d4aeb9-eabe-49f6-8edb-bb2862d5980b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b4dd41a7-ccf8-4e9d-918e-acaab534a307
autotag-review: '2026-05-01T09:10:10.340Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 1382
ht-degree: 17%

---

# データセットの概要を調和

Mix Modelerのデータは、データソースによって異なります。 データは次のようになります。

* ウォールドガーデンのデータソースから収集したデータや、屋外広告キャンペーン、イベント、物理的な広告キャンペーンの実行から収集したオフライン広告データ（支出など）などを集計し、
* イベントデータ :1st パーティデータソースからのデータなど このイベントデータは、Adobe AnalyticsからAdobe Analytics ソースコネクタを介して収集するか、Experience Platform Web、モバイル SDK、Edge Network APIを介して収集するか、ソースコネクタを使用して取り込んだデータを使用して収集できます。

Mix Modelerの調和サービスは、集約データとイベントデータを一貫性のあるデータビューに統合します。 このデータビューは、Mix Modelerのモデルのソースです。 このサービスは、様々なデータセットにわたって最も高い粒度を使用します。 例えば、あるデータセットの精度が月単位で、残りのデータセットの精度が週単位と日単位の精度である場合、調和サービスは月単位の精度を使用してデータビューを作成します。

## 要因

モデル構築では要素が重要であり、ビジネスに全体的な影響を与える要素を把握する必要があります。 マーケティングデータと関連しない要因があるかもしれません。

* 内部要因は組織ごとに異なり、コンバージョンに影響を与える可能性があります。 たとえば、セールスシーズンやプロモーションなどです。

* 外部要因は、組織がコントロールできない要因ですが、達成するコンバージョンに影響を与える可能性があります。 CPI、S&amp;P 500などの例を紹介します。

Mix Modelerのファクター機能では、調整されたファクターのワークフローを使用します。 このワークフローは、要因の管理方法を簡素化し、モデル間の一貫性を確保し、直感的なエクスペリエンスを提供します。

調整済み要因のワークフローの一部として：

1. [&#x200B; データセット ルール &#x200B;](/help/harmonize-data/dataset-rules.md#create-a-dataset-rule)の因子データセットの因子に対して、調整済みフィールドを定義します。
1. [調和されたデータを](/help/harmonize-data/dataset-rules.md#sync-data)同期します。
1. [&#x200B; モデル設定で要素](/help/models/build.md#configure)を使用します。

### 移行

調整済み要因ワークフローをまだ導入していないモデルがあり、Experience Platform データセットに基づく要因ワークフローを使用している場合があります。 これらのモデルは、調整された要因ワークフローに基づく新しい要因でモデルが更新されるまで、元のデータセットに基づく要因を引き続き表示します。

データセットに基づく要因ワークフローを使用するモデルを複製する場合：

* モデルが調和していない場合、古い要素設定は複製されたモデルに引き継がれません。 新しい調整済み因子ワークフローを使用して因子を追加する必要があります。
* モデルが調整されている場合、要因は引き継ぎ、保持または更新されます。

## 調和されたデータの例

Mix Modelerで次のデータセットを使用できることが想定されます。

**データセット 1**

YouTubeのマーケティング活動データセットが含まれます。集計データセットの詳細は日単位に設定されます。

| 日付 | 日付タイプ | チャネル | Campaign | ブランド | 地域 | クリック数 | 支出 |
|---|:--:|---|---|---|---|---:|---:|
| 12-31-2021 | 日 | YouTube | Y_Fall_02 | BrandX | 米国 | 10000 | 100 |
| 01-01-2022 | 日 | YouTube | Y_Fall_02 | BrandX | 米国 | 1000 | 10 |
| 01-03-2022 | 日 | YouTube | Y_Fall_01 | BrandY | CA | 10000 | 100 |
| 01-04-2022 | 日 | YouTube | Y_Summer_01 | Null | CA | 9000 | 80 |

{style="table-layout:auto"}


**データセット 2**

Facebookのマーケティング活動データセットが含まれます。集計データの詳細は週単位に設定されます。

| 日付 | 日付タイプ | チャネル | Campaign | 地域 | クリック数 | 支出 |
|--- |:---:|--- |---|---|---:|---:|
| 01-01-2022 | 週 | Facebook | FB_Fall_01 | 米国 | 8000 | 100 |
| 01-08-2022 | 週 | Facebook | FB_Fall_02 | 米国 | 1000 | 10 |
| 01-08-2022 | 週 | Facebook | FB_Fall_01 | 米国 | 7000 | 100 |
| 01-16-2022 | 週 | Facebook | FB_Summer_01 | CA | 10000 | 80 |

{style="table-layout:auto"}


**データセット 3**

コンバージョンデータセット。集計データセットの詳細が日単位に設定されます。

| 日付 | 日付タイプ | 地域 | 目標 | 売上高 |
|--- |:---: |---|---|---:|
| 01-01-2022 | 日 | 米国 | ファッション | 200 |
| 01-08-2022 | 日 | 米国 | ファッション | 10 |
| 01-08-2022 | 日 | 米国 | ジュエリー | 1100 |
| 01-16-2022 | 日 | CA | ジュエリー | 80 |

{style="table-layout:auto"}


**データセット 4**

お客様からのエクスペリエンスイベントデータセットのサンプル（Web SDK イベント）。

| タイムスタンプ | ID 名前空間 | ID ID | チャネル | クリック数 |
|--- |--- |--- |--- |---:|
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-01-2022 00:01:01.000 | ECID | 64fd46ff-8c63-43b4-85a7-92b953113ba0 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 2ca2a16e-caf0-4fa9-9a8b-9774b39547c4 | CSE | 1 |
| 01-08-2022 00:01:01.000 | ECID | 5ce99bfb-e44a-40d9-b8cd-c5408bda7cdc | CSE | 1 |

{style="table-layout:auto"}


週単位に設定した粒度で、調和のとれたデータセットを構築します。 イベントデータは週の精度に集計され、調和されたデータセットに追加されます。 結果は次のとおりです。

**調和されたデータセット**

| 日付 | 日付タイプ | チャネル | Campaign | ブランド | 地域 | 目標 | クリック数 | 支出 | 売上高 |
|--- |:---:|--- |--- |--- |---|---|---:|---:|---:|
| 12-27-2021 | 週 | YouTube | Y_Fall_02 | BrandX | 米国 | Null | 11000 | 110 | Null |
| 01-03-2022 | 週 | YouTube | Y_Fall_01 | BrandY | CA | Null | 10000 | 100 | Null |
| 01-03-2022 | 週 | YouTube | Y_Summer_01 | Null | CA | Null | 9000 | 80 | Null |
| 01-01-2022 | 週 | Facebook | FB_Fall_01 | Null | 米国 | Null | 8000 | 100 | Null |
| 01-08-2022 | 週 | Facebook | FB_Fall_02 | Null | 米国 | Null | 1000 | 10 | Null |
| 01-08-2022 | 週 | Facebook | FB_Fall_01 | Null | 米国 | Null | 7000 | 100 | Null |
| 01-16-2022 | 週 | Facebook | FB_Summer_01 | Null | CA | Null | 10000 | 80 | Null |
| 12-27-2021 | 週 | Null | Null | Null | 米国 | ファッション | Null | Null | 200 |
| 01-03-2022 | 週 | Null | Null | Null | 米国 | ファッション | Null | Null | 10 |
| 01-03-2022 | 週 | Null | Null | Null | 米国 | ジュエリー | Null | Null | 1100 |
| 01-10-2022 | 週 | Null | Null | Null | CA | ジュエリー | Null | Null | 80 |
| 01-01-2022 | 週 | CSE | Null | Null | Null | Null | 2 | Null | Null |
| 01-08-2022 | 週 | CSE | Null | Null | Null | Null | 2 | Null | Null |

{style="table-layout:auto"}


## 調和データの設定

簡素化された[例](#an-example-of-harmonized-data)のように、調和されたデータセットを構築するには、次の手順に従う必要があります。

1. 既に使用可能なグローバルな調和フィールドを超えて使用する追加の[調和フィールド &#x200B;](fields.md)を定義します。
1. [&#x200B; データセットルール &#x200B;](dataset-rules.md)を設定して、集計（要因または概要）またはエクスペリエンスイベントデータセットからフィールドを調和フィールドにマッピングします。
1. 定義した標準フィールドと追加の調和フィールドを使用して、[&#x200B; マーケティングのタッチポイント &#x200B;](marketing-touchpoints.md)を定義します。
1. 定義した標準フィールドと追加の調和フィールドを使用して、[&#x200B; コンバージョン &#x200B;](conversions.md)を定義します。


## 調和データの表示

Mix Modeler インターフェイスで、調和されたデータを確認するには、次の手順を実行します。

1. 左側のパネルから「![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized datasets]**」を選択します。

1. 上部バーから&#x200B;**[!UICONTROL Harmonized data]**&#x200B;を選択します。 調整済みデータの概要は、定義したフィールド、データセットルール、マーケティングのタッチポイント、コンバージョンにもとづいて表示されます。

   1. 調和データの再計算の基となる期間を再定義するには、**[!UICONTROL Date range]**&#x200B;の日付範囲を入力するか、![&#x200B; カレンダー](/help/assets/icons/Calendar.svg)を使用してデータ範囲を選択します。

   1. 調和データテーブルに表示される調和フィールド列を変更するには、![設定](/help/assets/icons/Setting.svg)を使用して&#x200B;**[!UICONTROL Column settings]** ダイアログを開きます。

      1. ![SelectBox](/help/assets/icons/SelectBox.svg)を&#x200B;**[!UICONTROL AVAILABLE COLUMNS]**&#x200B;から1つ以上の列を選択し、![Chevron right](/help/assets/icons/ChevronRight.svg)を使用してこれらの列を&#x200B;**[!UICONTROL SELECTED COLUMNS]**&#x200B;に追加します。 定義済みの標準の調和フィールド（**[!UICONTROL Factor Name]**、**[!UICONTROL Factor Value]**、**[!UICONTROL Factor Type]**、**[!UICONTROL Factor Value Type]**&#x200B;など、因子データセットに関連するフィールドを含む）はすべて使用できます。

      1. ![SelectBox](/help/assets/icons/SelectBox.svg)を&#x200B;**[!UICONTROL SELECTED COLUMNS]**&#x200B;から1つ以上の列を選択し、![Chevron left](/help/assets/icons/ChevronLeft.svg)を使用して選択した列を削除し、これらの列を&#x200B;**[!UICONTROL AVAILABLE COLUMNS]**&#x200B;に戻します。

      1. **[!UICONTROL DEFAULT SORT]**&#x200B;から列を選択し、**[!UICONTROL Ascending]**&#x200B;または&#x200B;**[!UICONTROL Descending]**&#x200B;を切り替えます。

      1. 表示される列の順序を変更するには、**[!UICONTROL SELECTED COLUMNS]**&#x200B;の列をドラッグ&amp;ドロップで上下に移動できます。

   1. **[!UICONTROL Submit]**&#x200B;を選択して、列設定の変更を送信します。 変更をキャンセルするには、**[!UICONTROL Close]**&#x200B;を選択します。

1. さらにページがある場合は、![左の矢印](/help/assets/icons/ChevronLeft.svg)または![右の矢印](/help/assets/icons/ChevronRight.svg) （**[!UICONTROL Page _x _/_x_]**）を使用して、ページ間を移動します。

1. 必要に応じて、調和データをダウンロードできます。

   1. ![&#x200B; ダウンロード &#x200B;](/help/assets/icons/Download.svg) [!BADGE &#x200B; ベータ &#x200B;]を選択します。
   1. ポップアップで、![AddCircle](/help/assets/icons/AddCircle.svg) **[!UICONTROL Create]**&#x200B;を選択します。
   1. **[!UICONTROL Report name]**&#x200B;を入力します（例：`Test Report`）。
   1. ![FileCSV](/help/assets/icons/FileCSV.svg) **[!UICONTROL Report]**&#x200B;を選択します。

   指定したレポート名と現在の日時（例：`Test Report_2025_04_23_9-5-18.csv`）に基づくタイトルを含むCSV レポートが、デフォルトのダウンロード フォルダーにダウンロードされます。


## ベストプラクティス

調整済みデータセットを作成する場合は、次のベストプラクティスを適用してください。

### スキーマ

* データタイプのミスマッチを回避。 取り込んだデータセットのレコード内のフィールドのデータタイプが、基礎となるスキーマでそのフィールドに設定したデータタイプに準拠していない場合、不一致が発生します。
* 誤ったスキーマタイプを避ける： データのスキーマと一致しないデータセットを使用して、特定のタイプのデータを取り込もうとすると、スキーマタイプが正しくありません。 例えば、外部要因データセットを使用して概要データを取り込もうとします。

### データマッピング

* イベントデータセットごとにIDを適切に設定していることを確認してください。

### 低いデータ品質

* タイムスタンプ付きデータを必要とするデータセットのすべてのレコードに対して、日付形式と時刻形式を一貫して使用します。
* 集計または要約データセットのレコードに対して、同じ粒度（日または週）を使用していることを確認します。

### データ計算

* データセット内で行が重複することを避ける。
* アップロードする各データセットが、一意のチャネルとコンバージョンタイプに特化していることを確認してください。 複数のデータセットをまたいで重複した顧客接点やコンバージョンが、モデルの出力と品質に影響を与えます。

