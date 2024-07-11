---
title: コンバージョン数
description: Mix Modeler内のデータの調和の一部として使用するコンバージョンを作成する方法を説明します。
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 1%

---

# コンバージョン数

コンバージョンイベントは、マーケティングアクティビティの影響を特定するビジネス目標です。 例：e コマースの注文、店舗での購入、web サイトへの訪問など。

アトリビューション分析用のマーケティングコンバージョンを定義します。

## コンバージョンの管理

Mix Modelerインターフェイスで使用可能なコンバージョンのテーブルを表示するには、次の手順を実行します。

1. を選択 ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** 左パネルから。

1. を選択 **[!UICONTROL Conversions]** 上部バーから。 コンバージョンのテーブルが表示されます。

テーブルの列には、変換に関する詳細が表示されます。

| 列名 | 詳細 |
| --- | ---|
| 名前 | コンバージョンの名前。 |
| 収益 | コンバージョンから得られる売上高の計算に使用する、統一データ指標。 |
| コンバージョン指標 | 分析のコンバージョン指標として使用する統一データ指標。 |
| カテゴリ | コンバージョンのコンバージョンカテゴリ。 |
| 作成日 | コンバージョンが作成された日時。 |
| 最終変更日 | コンバージョンが最後に変更された日時。 |

{style="table-layout:auto"}

## コンバージョンを追加

コンバージョンを追加するには、次の手順を実行します ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** Mix Modelerのインターフェイス：

1. を選択 ![追加](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. が含まれる **[!UICONTROL Create conversion]** ダイアログ：

   1. の名前を入力 **[!UICONTROL Conversion]**、例： `Store Conversions`.

   1. の定義 **[!UICONTROL Conversion category]**.

      1. から値を選択 **[!UICONTROL *調和を選択…*]**、例： `Conversion types`.

      1. 演算子の値を選択 ![山形](/help/assets//icons/ChevronDown.svg)、例： **[!UICONTROL is]**.

      1. から値を選択 **[!UICONTROL *値を選択&#x200B;*]**または値を入力します。例：**[!UICONTROL Store]**.

   1. から統一フィールドを選択 **[!UICONTROL Conversion metric for analysis]**、例： **[!UICONTROL Orders]**.

   1. から統一フィールドを選択 **[!UICONTROL Revenue field]**、例： **[!UICONTROL Gross Demand]**.

   1. 変換を作成するには、以下を選択します。 **[!UICONTROL Create]**. コンバージョンの作成をキャンセルするには、以下を選択します **[!UICONTROL Cancel]**.

      ![代替テキスト](/help/assets//create-conversion.png)

1. 作成されると、変換が変換テーブルに追加されます。


## コンバージョンを表示

コンバージョンを表示するには：

1. を選択 ![詳細](/help/assets//icons/More.svg) テーブルのコンバージョン名にカーソルを合わせたとき。

1. を選択 ![表示](/help/assets//icons/ViewDetail.svg) **表示**. コンバージョンの詳細を示すダイアログが表示されます。 参照： [コンバージョンを追加](#add-a-conversion) を参照してください。 を選択 **[!UICONTROL Cancel]** をクリックしてダイアログを閉じます。


## コンバージョンの削除

コンバージョンを削除するには：

1. を選択 ![削除](/help/assets//icons/Delete.svg) **削除** テーブルのコンバージョン名にカーソルを合わせたとき。
1. が含まれる **[!UICONTROL Delete conversion]** ダイアログ確認ダイアログ選択 **[!UICONTROL Delete]** をクリックして、変換を完全に削除します。
