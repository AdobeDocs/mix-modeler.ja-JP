---
title: 統一フィールド
description: Mix Modelerのデータの調和の一部として使用するフィールドを定義する方法を説明します。
feature: Harmonized Data, Harmonized Fields
exl-id: f051279a-1ae9-49bd-a946-abfc34c90413
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
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
| campaign | キャンペーン | ディメンション | 文字列 |           |
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

1. を選択 ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** 左パネルから。

1. を選択 **[!UICONTROL Fields]** 上部バーから。 統一フィールドのテーブルが表示されます。 他のページが使用可能な場合は、を使用します ![左矢印](/help/assets//icons/ChevronLeft.svg) または ![右矢印](/help/assets//icons/ChevronRight.svg) 時刻 **[!UICONTROL Page _x _件中_x_]** をクリックして、テーブルのページ間を移動します。

   テーブルの列は、統一フィールドの詳細を指定します

   | 列名 | 詳細 |
   | ---------------------- | ----------|
   | フィールド名 | 統一フィールドの名前。 |
   | 表示名 | 統一フィールドの表示名。 この表示名は、データセットルール、マーケティングタッチポイントおよびコンバージョン定義を定義する際に使用されます。 |
   | カテゴリ | 統一データフィールドがであるかどうかを指定します [!UICONTROL Dimension], a [!UICONTROL Metric] または [!UICONTROL Derived]. 派生カテゴリは、指標ベースの式定義を使用した統一フィールドです。 |
   | データタイプ | データタイプ （[!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL Date time]）に設定します。 |
   | 作成日 | 統一フィールドの作成日時。 |
   | 所有者 | 統一フィールドがデフォルトのフィールドかどうかを示します（[!UICONTROL Global]）または、によって定義されています（[!UICONTROL Client]）に設定します。 |
   | 最終変更日 | 統一フィールドの最終変更日時。 |
   | 数式 | 派生カテゴリに基づく統一フィールドの数式を指定します。 |

   {style="table-layout:auto"}

1. 特定の統一フィールドを検索するには、を使用します ![検索](/help/assets//icons/Search.svg) **[!UICONTROL *統一されたフィールドを検索&#x200B;*]**.


### 統一フィールドの追加

統一フィールドを追加するには、 ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** Mix Modelerのインターフェイス：

1. を選択 ![追加](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add field]**.

1. が含まれる **[!UICONTROL Create]** ダイアログ：

   1. を入力 **[!UICONTROL Field name]**、例： `region`.
   1. を入力 **[!UICONTROL Display name]**、例： `Region`.
   1. を選択 **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** または **[!UICONTROL Derived]**.

      選択した場合 **[!UICONTROL Derived]**、を指定します **[!UICONTROL Formula]**. 有効な数式を作成するには、から 1 つ以上の指標を組み合わせます **[!UICONTROL Insert Metric]** 1 つ以上の演算子を使用 **[!UICONTROL + - * / ( )]** . 例：`[orders]/[impressions]`

   1. を選択 **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** または **[!UICONTROL Date time]**:「カテゴリ」が「Dimension」の場合。
      - **[!UICONTROL Number]** または **[!UICONTROL Currency]** カテゴリが「指標」または「派生」の場合。

   1. を選択 **[!UICONTROL Submit]** 統一フィールドを追加します。 を選択 **[!UICONTROL Close]** 統一フィールドを追加せずにダイアログを閉じるには、次の手順を実行します。

      ![フィールドを作成](/help/assets//create-field.png)


### 統一フィールドの編集

編集できるのは、以前に作成した統一フィールドのみです（所有者はクライアントです）。 グローバル統一フィールドは編集できません。

統一フィールドを編集するには、 ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** Mix Modelerのインターフェイス：

1. 編集する統一フィールドを選択します。 例：**[!UICONTROL Region]**。

1. が含まれる **[!UICONTROL Edit harmonization values]** ペイン、値を変更 **[!UICONTROL Display name]**, **[!UICONTROL Category]**、および **[!UICONTROL Data type]**. 参照： [統一フィールドの追加](#add-a-harmonized-field) を参照してください。

1. を選択 **[!UICONTROL Submit]** 統一フィールドに変更を適用します。

   ![フィールドを編集](/help/assets//edit-field.png)

### 統一フィールドの削除

以前に作成した統一フィールドのみを削除できます（所有者はクライアント）。 グローバル統一フィールドは削除できません。

統一フィールドを削除するには、 ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** Mix Modelerのインターフェイス：

1. 削除する統一フィールドを選択します。例： **[!UICONTROL Region]**.

1. を選択 ![削除](/help/assets//icons/Delete.svg) **[!UICONTROL Delete]** から **[!UICONTROL Edit harmonization values]** 左側のウィンドウ。

   >[!WARNING]
   >
   >   フィールドはすぐに削除されます。

