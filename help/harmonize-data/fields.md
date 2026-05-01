---
title: 調和されたフィールド
description: Mix Modelerでデータを調和させる一環として使用するフィールドを定義する方法について説明します。
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
TQID: https://experienceleague.adobe.com/NlB6aA4AO-0Tpbb9SibgUz0eVUgs8roO9Mju2M8tl7s
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
subfeature_v2:
  - id: d4b8ba18-64c1-4413-be54-74405ec7f558
  - id: b4655f7e-1a6e-4fa3-a7c5-3c34d4786e49
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:13:17.577Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 688
ht-degree: 11%

---

# 調和されたフィールド

統一されたフィールドを使用すると、概念的に同じデータのフィールドを定義できます。これらのフィールドは、データの定義が異なるソースから作成されます。 例えば、クリック指標は、データソースごとに定義し、名前を付けることができます。 「統一されたクリック数」フィールドでは、クリックデータの様々なソースに基づいて、クリック指標の一般的な命名規則を定義できます。

調和されたフィールドを使用すると、データの調和ワークフローの一部として使用するフィールドを定義できます。 定義したフィールドは、データセットルール、マーケティングのタッチポイント、コンバージョンの定義に使用できます。

## グローバルな調和フィールド

Mix Modelerで使用できるデフォルトのグローバル調和フィールドは次のとおりです。


| フィールド名 | 表示名 | カテゴリ | データタイプ | コメント |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| ブランド | ブランド | ディメンション | 文字列 |           |
| キャンペーン | Campaign | ディメンション | 文字列 |           |
| チャネル | チャネル | ディメンション | 文字列 |           |
| channel_id | チャネル ID | ディメンション | 文字列 |           |
| channel_type_at_source | Sourceのチャネルタイプ | ディメンション | 文字列 |           |
| チャネル | チャネル | ディメンション | 文字列 |           |
| クリック数 | クリック数 | 指標 | 数値 |           |
| conversiontype | コンバージョンタイプ | ディメンション | 文字列 |           |
| コスト | コスト | 指標 | 通貨 |           |
| データセット | データセット | ディメンション | 文字列 |           |
| date_type | 日付タイプ | ディメンション | 文字列 | 日、週 |
| email sent | メール送信済み | 指標 | 数値 |           |
| event_date | 日付 | ディメンション | 日時 |           |
| gross_demand | 総需要 | 指標 | 通貨 |           |
| インプレッション | 影響 | 指標 | 数値 |           |
| last_updated_date | 最終更新日 | ディメンション | 日時 |           |
| linkvisits | リンク訪問 | 指標 | 数値 |           |
| mediatype | メディアタイプ | ディメンション | 文字列 |           |
| net_sales | 純売上高 | 指標 | 通貨 |           |
| 注文件数 | 注文 | 指標 | 数値 |           |
| sourcetype | Source Type | ディメンション | 文字列 |           |
| 費用 | 支出 | 指標 | 通貨 |           |
| trafficsource | Traffic Source | ディメンション | 文字列 |           |

{style="table-layout:auto"}

これらのグローバルに統一されたフィールドの上に、独自の統一されたフィールドを追加、編集または削除できます。

## 統一されたフィールドの管理

使用可能な調和フィールドの表を表示するには、Mix Modeler インターフェイスで次の操作を行います。

1. 左側のパネルから「![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**」を選択します。

1. 上部バーから&#x200B;**[!UICONTROL Fields]**&#x200B;を選択します。 調和されたフィールドのテーブルが表示されます。 さらにページがある場合は、![左の矢印](/help/assets/icons/ChevronLeft.svg)または![右の矢印](/help/assets/icons/ChevronRight.svg) （**[!UICONTROL Page _x _/_x_]**）を使用して、テーブルのページ間を移動します。

   表の列には、調和されたフィールドに関する詳細が示されます

   | 列の名前 | 詳細 |
   | ---------------------- | ----------|
   | フィールド名 | 調和フィールドの名前。 |
   | 表示名 | 調和フィールドの表示名。 この表示名は、データセットルール、マーケティングタッチポイント、コンバージョン定義を定義する際に使用されます。 |
   | カテゴリ | 調和データフィールドが[!UICONTROL Dimension]、[!UICONTROL Metric]または[!UICONTROL Derived]のどれであるかを指定します。 派生カテゴリは、指標ベースの数式定義を使用して調整されたフィールドです。 |
   | データタイプ | データ型（[!UICONTROL Number]、[!UICONTROL String]、[!UICONTROL Currency]、[!UICONTROL Date time]）を指定します。 |
   | 作成日 | 調和フィールドの作成日時。 |
   | 所有者 | 調和されたフィールドが既定のフィールド （[!UICONTROL Global]）であるか、ユーザー（[!UICONTROL Client]）によって定義されているかを示します。 |
   | 最終変更日 | 調和されたフィールドの最後の変更のデータと時間。 |
   | 数式 | 派生カテゴリに基づく調和フィールドの数式を指定します。 |

   {style="table-layout:auto"}

1. 特定の調和フィールドを検索するには、![検索](/help/assets/icons/Search.svg) **[!UICONTROL *調和フィールドを検索&#x200B;*]**&#x200B;を使用します。


### 調和フィールドの追加

調和されたフィールドを追加するには、Mix Modelerの![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** インターフェイスで次の操作を行います。

1. 「![追加](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add field]**」を選択します。

1. **[!UICONTROL Create]** ダイアログで、次の操作を行います。

   1. **[!UICONTROL Field name]**&#x200B;を入力します（例：`region`）。
   1. **[!UICONTROL Display name]**&#x200B;を入力します（例：`Region`）。
   1. **[!UICONTROL Category]**&#x200B;を選択：**[!UICONTROL Dimension]**、**[!UICONTROL Metric]**&#x200B;または&#x200B;**[!UICONTROL Derived]**。

      **[!UICONTROL Derived]**&#x200B;を選択する場合は、**[!UICONTROL Formula]**&#x200B;を指定します。 有効な算術式を作成するには、**[!UICONTROL Insert Metric]**&#x200B;の1つ以上の指標を1つ以上の演算子&#x200B;**[!UICONTROL + - * / ( )]**&#x200B;と組み合わせます。 例：`[orders]/[impressions]`

   1. **[!UICONTROL Data type]**&#x200B;を選択します。

      - **[!UICONTROL String]**&#x200B;または&#x200B;**[!UICONTROL Date time]**。カテゴリが選択されている場合はDimensionです。
      - 選択したカテゴリが指標または派生の場合は&#x200B;**[!UICONTROL Number]**&#x200B;または&#x200B;**[!UICONTROL Currency]**。

   1. **[!UICONTROL Submit]**&#x200B;を選択して、調和フィールドを追加します。 調和フィールドを追加せずにダイアログを閉じるには、**[!UICONTROL Close]**&#x200B;を選択します。

      ![&#x200B; フィールドを作成](/help/assets/create-field.png)


### 調和フィールドの編集

以前に作成した調和フィールドのみを編集できます（所有者はクライアントです）。 グローバルに統一されたフィールドは編集できません。

調和されたフィールドを編集するには、Mix Modelerの![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** インターフェイスで次の操作を行います。

1. 編集する調和フィールドを選択します。 例：**[!UICONTROL Region]**。

1. **[!UICONTROL Edit harmonization values]** ペインで、**[!UICONTROL Display name]**、**[!UICONTROL Category]**&#x200B;および&#x200B;**[!UICONTROL Data type]**&#x200B;の値を変更します。 詳しくは、[調和フィールドの追加](#add-a-harmonized-field)を参照してください。

1. 調和フィールドに変更を適用するには、**[!UICONTROL Submit]**&#x200B;を選択します。

   ![&#x200B; フィールドを編集](/help/assets/edit-field.png)

### 調和フィールドの削除

以前に作成した調整済みフィールドのみを削除できます（所有者はクライアントです）。 グローバルに統一されたフィールドは削除できません。

調和されたフィールドを削除するには、Mix Modelerの![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** インターフェイスで次の操作を行います。

1. 削除する調整済みフィールド （例：**[!UICONTROL Region]**）を選択します。

1. 左側の&#x200B;**[!UICONTROL Edit harmonization values]** ペインから![削除](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]**&#x200B;を選択します。

   >[!WARNING]
   >
   >   フィールドはすぐに削除されます。

