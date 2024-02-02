---
title: コンバージョン数
description: Mix Modelerでのデータの調和の一環として使用するコンバージョンを作成する方法を説明します。
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 1%

---

# コンバージョン数

コンバージョンイベントとは、マーケティングアクティビティの影響を識別するビジネス目標です。 e コマースでの注文、店舗での購入、Web サイトへの訪問など。

アトリビューション分析用のマーケティングコンバージョンを定義します。

## コンバージョンの管理

「Mix Modeler」インターフェイスで使用可能な変換の表を確認するには、次の手順を実行します。

1. 選択 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** をクリックします。

1. 選択 **[!UICONTROL Conversions]** 上部のバーから。 コンバージョンの表が表示されます。

テーブルの列で、変換の詳細を指定します。

| 列名 | 詳細 |
| --- | ---|
| 名前 | 変換の名前。 |
| 売上高 | コンバージョンによる売上高の計算に使用する調整済みデータ指標。 |
| コンバージョン指標 | 分析のコンバージョン指標として使用するデータ指標を調整します。 |
| カテゴリ | コンバージョンのコンバージョンカテゴリ。 |
| 作成日 | コンバージョンが作成された日時。 |
| 最終変更日 | 変換が最後に変更された日時。 |

{style="table-layout:auto"}

## コンバージョンの追加

コンバージョンを追加するには、 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** インターフェイスのMix Modeler:

1. 選択 ![追加](../assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**.

1. Adobe Analytics の **[!UICONTROL Create conversion]** ダイアログ：

   1. 名前を入力 **[!UICONTROL Conversion]**&#x200B;例： `Store Conversions`.

   1. 次を定義： **[!UICONTROL Conversion category]**.

      1. 値の選択元 **[!UICONTROL *調和を選択…*]**例： `Conversion types`.

      1. 演算子の値を選択 ![シェブロン](../assets/icons/ChevronDown.svg)例： **[!UICONTROL is]**.

      1. 値の選択元 **[!UICONTROL *値を選択&#x200B;*]**または、例えば&#x200B;**[!UICONTROL Store]**.

   1. 次の中から調和されたフィールドを選択： **[!UICONTROL Conversion metric for analysis]**&#x200B;例： **[!UICONTROL Orders]**.

   1. 次の中から調和されたフィールドを選択： **[!UICONTROL Revenue field]**&#x200B;例： **[!UICONTROL Gross Demand]**.

   1. 変換を作成するには、 **[!UICONTROL Create]**. 変換処理の作成をキャンセルする場合は、 **[!UICONTROL Cancel]**.

      ![代替テキスト](../assets/create-conversion.png)

1. 変換処理が作成されると、変換処理がコンバージョンテーブルに追加されます。


## コンバージョンを表示する

コンバージョンを表示するには：

1. 選択 ![その他](../assets/icons/More.svg) 表のコンバージョン名の上にマウスポインターを置くとき。

1. 選択 ![表示](../assets/icons/ViewDetail.svg) **表示**. 変換の詳細がダイアログに表示されます。 詳しくは、 [コンバージョンの追加](#add-a-conversion) を参照してください。 選択 **[!UICONTROL Cancel]** をクリックしてダイアログを閉じます。


## コンバージョンの削除

コンバージョンを削除するには：

1. 選択 ![削除](../assets/icons/Delete.svg) **削除** 表のコンバージョン名の上にマウスポインターを置くとき。
1. Adobe Analytics の **[!UICONTROL Delete conversion]** ダイアログの確認ダイアログを選択 **[!UICONTROL Delete]** をクリックして、変換後のデータを完全に削除します。
