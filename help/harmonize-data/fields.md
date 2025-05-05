---
title: 統一フィールド
description: Mix Modelerのデータの調和の一部として使用するフィールドを定義する方法を説明します。
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
source-git-commit: 9a6c1f1c12ab29da80a1997cfd31ca07b38eaa22
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 10%

---

# 統一フィールド

統一されたフィールドを使用すると、異なるソースから得られた、概念的に同じデータのフィールドを、それぞれのフィールドでそのデータの独自の定義を使用して定義できます。 例えば、クリック数指標は、データのソースに応じて異なる方法で定義および命名できます。 クリック数調和フィールドを使用すると、クリック数データのさまざまなソースに基づいて、クリック指標の共通の命名法を定義できます。

統一フィールドを使用すると、データ調和ワークフローの一部として使用するフィールドを定義できます。 定義したフィールドは、データセットルール、マーケティングタッチポイントおよびコンバージョンの定義に使用できます。

## グローバル調和フィールド

Mix Modelerで使用できるデフォルトのグローバル調和フィールドは次のとおりです。


| フィールド名 | 表示名 | カテゴリ | データタイプ | コメント |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| ブランド | ブランド | ディメンション | 文字列 |           |
| campaign | Campaign | ディメンション | 文字列 |           |
| チャネル | チャネル | ディメンション | 文字列 |           |
| channel_id | チャネル ID | ディメンション | 文字列 |           |
| channel_type_at_source | Sourceのチャネルタイプ | ディメンション | 文字列 |           |
| チャネル | チャネル | ディメンション | 文字列 |           |
| クリック数 | クリック数 | 指標 | 数値 |           |
| conversiontype | コンバージョンタイプ | ディメンション | 文字列 |           |
| 費用 | コスト | 指標 | 通貨 |           |
| データセット | データセット | ディメンション | 文字列 |           |
| date_type | 日付タイプ | ディメンション | 文字列 | 日、週 |
| メール送信済み | 送信済みメール | 指標 | 数値 |           |
| event_date | 日付 | ディメンション | 日時 |           |
| gross_demand | 総需要 | 指標 | 通貨 |           |
| 印象 | 実装 | 指標 | 数値 |           |
| last_updated_date | 最終更新日 | ディメンション | 日時 |           |
| linkvisits | 訪問をリンク | 指標 | 数値 |           |
| mediatype | メディアタイプ | ディメンション | 文字列 |           |
| net_sales | 純売上高 | 指標 | 通貨 |           |
| 注文件数 | 注文件数 | 指標 | 数値 |           |
| sourcetype | Sourceタイプ | ディメンション | 文字列 |           |
| 費用 | 費用 | 指標 | 通貨 |           |
| trafficsource | Traffic Source | ディメンション | 文字列 |           |

{style="table-layout:auto"}

これらのグローバル統一フィールドの上に、独自の統一フィールドを追加、編集または削除することができます。

## 統一フィールドの管理

Mix Modelerインターフェイスで使用可能な統一フィールドのテーブルを表示するには：

1. 左パネルから ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** を選択します。

1. 上部バーの「**[!UICONTROL Fields]**」を選択します。 統一フィールドのテーブルが表示されます。 他のページが使用可能な場合は、![x](/help/assets/icons/ChevronLeft.svg) の **Page _x _で ![ 左向き矢印 ](/help/assets/icons/ChevronRight.svg) または_ 右向き矢印_** を使用して、テーブルのページ間を移動します。

   テーブルの列は、統一フィールドの詳細を指定します

   | 列名 | 詳細 |
   | ---------------------- | ----------|
   | フィールド名 | 統一フィールドの名前。 |
   | 表示名 | 統一フィールドの表示名。 この表示名は、データセットルール、マーケティングタッチポイントおよびコンバージョン定義を定義する際に使用されます。 |
   | カテゴリ | 統一データフィールドが [!UICONTROL Dimension]、[!UICONTROL Metric]、[!UICONTROL Derived] のどれであるかを指定します。 派生カテゴリは、指標ベースの式定義を使用した統一フィールドです。 |
   | データタイプ | データタイプ（[!UICONTROL Number]、[!UICONTROL String]、[!UICONTROL Currency]、[!UICONTROL Date time]）を指定します。 |
   | 作成日 | 統一フィールドの作成日時。 |
   | 所有者 | 統一フィールドがデフォルトのフィールド（[!UICONTROL Global]）か、ユーザーが定義したフィールド（[!UICONTROL Client]）かを示します。 |
   | 最終変更日 | 統一フィールドの最終変更日時。 |
   | 数式 | 派生カテゴリに基づく統一フィールドの数式を指定します。 |

   {style="table-layout:auto"}

1. 特定の統一フィールドを検索するには、![ 検索 ](/help/assets/icons/Search.svg) 統一フィールドを検索 **[!UICONTROL *を使用&#x200B;*]**&#x200B;ます。


### 統一フィールドの追加

統一フィールドを追加するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Fields]** インターフェイスで、次の手順を実行します。

1. 「![ 追加 ](/help/assets/icons/AddCircle.svg)」を選択し **[!UICONTROL Add field]** す。

1. **[!UICONTROL Create]** ダイアログで、次の手順を実行します。

   1. **[!UICONTROL Field name]** （例：`region`）を入力します。
   1. **[!UICONTROL Display name]** （例：`Region`）を入力します。
   1. **[!UICONTROL Dimension]**、**[!UICONTROL Metric]**、**[!UICONTROL Derived]** のいずれかの **[!UICONTROL Category]** を選択します。

      **[!UICONTROL Derived]** を選択した場合は、**[!UICONTROL Formula]** を指定します。 有効な数式を作成するには、**[!UICONTROL Insert Metric]** の 1 つ以上の指標をの 1 つ以上の演算子と組み合わせ **[!UICONTROL + - * / ( )]** す。 例：`[orders]/[impressions]`

   1. **[!UICONTROL Data type]** を選択します。

      - 「カテゴリ」が「Dimension」の場合は、**[!UICONTROL String]** または **[!UICONTROL Date time]**。
      - 「カテゴリ」で「指標」または「派生」を選択した場合は **[!UICONTROL Number]** または **[!UICONTROL Currency]**。

   1. 「**[!UICONTROL Submit]**」を選択して、統一フィールドを追加します。 統一フィールドを追加せずにダイアログを閉じるには、「**[!UICONTROL Close]**」を選択します。

      ![ フィールドの作成 ](/help/assets/create-field.png)


### 統一フィールドの編集

編集できるのは、以前に作成した統一フィールドのみです（所有者はクライアントです）。 グローバル統一フィールドは編集できません。

統一フィールドを編集するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Fields]** インターフェイスで、次の手順を実行します。

1. 編集する統一フィールドを選択します。 例：**[!UICONTROL Region]**。

1. **[!UICONTROL Edit harmonization values]** ペインで、**[!UICONTROL Display name]**、**[!UICONTROL Category]**、**[!UICONTROL Data type]** の値を変更します。 詳しくは [ 統一フィールドの追加 ](#add-a-harmonized-field) を参照してください。

1. 「**[!UICONTROL Submit]**」を選択して、統一フィールドに変更を適用します。

   ![ フィールドの編集 ](/help/assets/edit-field.png)

### 統一フィールドの削除

以前に作成した統一フィールドのみを削除できます（所有者はクライアント）。 グローバル統一フィールドは削除できません。

統一フィールドを削除するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Fields]** インターフェイスで、次の手順を実行します。

1. 削除する統一フィールド（例：**[!UICONTROL Region]**）を選択します。

1. 左 **[!UICONTROL Edit harmonization values]** のペインで ![ 削除 ](/help/assets/icons/Delete.svg)**[!UICONTROL Delete]** を選択します。

   >[!WARNING]
   >
   >   フィールドはすぐに削除されます。

