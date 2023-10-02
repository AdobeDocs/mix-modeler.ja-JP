---
title: 調整済みフィールド
description: Mix Modelerでのデータの調和の一環として使用するフィールドを定義する方法を説明します。
feature: Harmonized Data, Harmonized Fields
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 11%

---


# 調整済みフィールド

調和されたフィールドを使用すると、異なるソースから得られる概念上同じデータを、それぞれ独自のデータ定義と共に定義できます。 例えば、クリック数指標は、データのソースに応じて異なる名前を付けて定義できます。 クリック数の調和をとったフィールドを使用すると、様々なクリック数データのソースに基づいて、クリック数指標の一般的な命名規則を定義できます。

調和されたフィールドを使用すると、データ調和ワークフローの一部として使用するフィールドを定義できます。 定義したフィールドは、データセットルール、マーケティングタッチポイント、コンバージョンの定義に使用できます。

## グローバルハーモナイゼーションフィールド

デフォルトで使用可能なグローバルハーモナイゼーションフィールドは、次のMix Modelerです。


| フィールド名 | 表示名 | カテゴリ | データタイプ | コメント |
| ---------------------- | ---------------------- | --------- | --------- | --------- |
| ブランド | ブランド | ディメンション | 文字列 |           |
| campaign | Campaign | ディメンション | 文字列 |           |
| チャネル | チャネル | ディメンション | 文字列 |           |
| channel_id | チャネル ID | ディメンション | 文字列 |           |
| channel_type_at_source | ソースでのチャネルタイプ | ディメンション | 文字列 |           |
| チャネル | チャネル | ディメンション | 文字列 |           |
| クリック数 | クリック数 | 指標 | 数値 |           |
| conversiontype | コンバージョンタイプ | ディメンション | 文字列 |           |
| コスト | コスト | 指標 | 通貨 |           |
| データセット | データセット | ディメンション | 文字列 |           |
| date_type | 日付タイプ | ディメンション | 文字列 | 日、週 |
| emailsent | 送信済みメール数 | 指標 | 数値 |           |
| event_date | 日付 | ディメンション | 日時 |           |
| gross_demand | 総需要 | 指標 | 通貨 |           |
| impressions | インプレッション | 指標 | 数値 |           |
| last_updated_date | 最終更新日 | ディメンション | 日時 |           |
| linkvisits | リンク訪問回数 | 指標 | 数値 |           |
| mediatype | メディアタイプ | ディメンション | 文字列 |           |
| net_sales | 純売上高 | 指標 | 通貨 |           |
| 注文件数 | 購入回数 | 指標 | 数値 |           |
| sourcetype | ソースタイプ | ディメンション | 文字列 |           |
| 費やす | 費用 | 指標 | 通貨 |           |
| 交通源 | Traffic Source | ディメンション | 文字列 |           |

{style="table-layout:auto"}

これらのグローバル調和済みフィールドの上に、独自の調和済みフィールドを追加、編集または削除できます。

## 調整済みフィールドの管理

使用可能な調和済みフィールドのテーブルを表示するには、Mix Modelerインターフェイスで次の手順を実行します。

1. 選択 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** をクリックします。

1. 選択 **[!UICONTROL Fields]** 上部のバーから。 調和されたフィールドのテーブルが表示されます。

   テーブルの列には、調和されたフィールドの詳細が指定されます

   | 列名 | 詳細 |
   | ---------------------- | ----------|
   | フィールド名 | 調和済みフィールドの名前。 |
   | 表示名 | 調和されたフィールドの表示名。 この表示名は、データセットルール、マーケティングタッチポイントおよびコンバージョンの定義を定義する際に使用されます。 |
   | カテゴリ | 調和されたデータフィールドが [!UICONTROL Dimension], a [!UICONTROL Metric] または [!UICONTROL Derived]. 派生カテゴリは、指標ベースの数式定義を使用して調整されたフィールドです。 |
   | 所有者 | 調和されたフィールドがデフォルトのフィールドかどうかを示します ([!UICONTROL Global])、またはユーザーが定義した ([!UICONTROL Client]) をクリックします。 |
   | データタイプ | データタイプを指定します ([!UICONTROL Number], [!UICONTROL String], [!UICONTROL Currency], [!UICONTROL DateTime]) をクリックします。 |
   | 作成日時 | 調和されたフィールドの作成日時。 |
   | 最終変更日時 | 調和されたフィールドの最後の変更のデータと時刻。 |
   | 数式 | 派生カテゴリに基づいて、調和されたフィールドの数式を指定します。 |

   {style="table-layout:auto"}

1. 特定の調整済みフィールドを検索するには、 ![検索](../assets/icons/Search.svg) **[!UICONTROL *調整済みフィールドを検索&#x200B;*]**.




### 調整済みフィールドを追加

調和されたフィールドを追加するには、「 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** インターフェイスを次のMix Modelerに設定します。

1. 選択 ![追加](../assets/icons/AddCircle.svg)フィールドを追加します。

1. Adobe Analytics の **[!UICONTROL Create]** ダイアログ：

   1. を入力します。 **[!UICONTROL Field name]**&#x200B;例： `region`.
   1. を入力します。 **[!UICONTROL Display name]**&#x200B;例： `Region`.
   1. を選択します。 **[!UICONTROL Category]**: **[!UICONTROL Dimension]**, **[!UICONTROL Metric]** または **[!UICONTROL Derived]**.

      次を選択した場合： **[!UICONTROL Derived]**、を指定します。 **[!UICONTROL Formula]**. 有効な算術式を作成するには、次の 1 つ以上の指標を組み合わせます： **[!UICONTROL Insert Metric]** 1 つ以上の演算子 **[!UICONTROL + - * / ( )]** . 例：`[orders]/[impressions]`

   1. を選択します。 **[!UICONTROL Data type]**.

      - **[!UICONTROL String]** または **[!UICONTROL DateTime]**( カテゴリが「Dimension」の場合 )
      - **[!UICONTROL Number]** または **[!UICONTROL Currency]** カテゴリが [ 指標 ] または [ 派生 ] の場合。

   1. 選択 **[!UICONTROL Submit]** ：調和されたフィールドを追加します。 選択 **[!UICONTROL Close]** ：調和されたフィールドを追加せずにダイアログを閉じます。

      ![フィールドの作成](../assets/create-field.png)


### 調整済みフィールドの編集

作成済みのハーモナイズされたフィールドのみ編集できます。 グローバル調整済みフィールドは編集できません。

調和されたフィールドを編集するには、「 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** インターフェイスを次のMix Modelerに設定します。

1. 編集する調和済みフィールドを選択します。 例：**[!UICONTROL Region]**。

1. Adobe Analytics の **[!UICONTROL Edit harmonization values]** ペイン、値を変更する **[!UICONTROL Display name]**, **[!UICONTROL Category]**、および **[!UICONTROL Data type]**.

1. 選択 **[!UICONTROL Submit]** ：調和されたフィールドに変更を適用します。

   ![フィールドの編集](../assets/edit-field.png)

### 調和済みフィールドの削除

以前に作成した調和済みフィールドのみを削除できます。 グローバル調整済みフィールドは削除できません。

調和されたフィールドを削除するには、「 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Fields]** インターフェイスを次のMix Modelerに設定します。

1. 削除する調和済みフィールドを選択します（例： ）。 **[!UICONTROL Region]**.

1. 選択 ![削除](../assets/icons/Delete.svg) **[!UICONTROL Delete]** から **[!UICONTROL Edit harmonization values]** 左側のウィンドウ


