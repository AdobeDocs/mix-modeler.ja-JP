---
title: マーケティングタッチポイント
description: Mix Modelerでのデータの調和の一環として使用するマーケティングタッチポイントを作成する方法を説明します。
feature: Harmonized Data, Marketing Touch Points
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# マーケティングタッチポイント

マーケティングタッチポイントは、マーケティング投資が数値ベースまたは売上高ベースのコンバージョンに与える影響を評価するために使用される、受信者レベル、個人レベル、cookie レベルのマーケティングイベントです。

マーケティングタッチポイントを定義すると、アトリビューション分析で役立ちます。

## マーケティングタッチポイントの管理

Mix Modelerインターフェイスで使用可能なマーケティングタッチポイントの表を確認するには：

1. 選択 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** をクリックします。

1. 選択 **[!UICONTROL Marketing touchpoint]** 上部のバーから。 マーケティングタッチポイントの表が表示されます。

表の列は、マーケティングタッチポイントに関する詳細を指定します。

| 列名 | 詳細 |
| --- | ---|
| 名前 | マーケティングタッチポイントの名前。 |
| 支出指標 | タッチポイントの支出の計算に使用する調整済みデータ指標。 |
| ボリューム指標 | タッチポイントボリュームの計算に使用する調整済みデータ指標。 |
| 作成日 | マーケティングタッチポイントの作成日時。 |
| 最終変更日 | マーケティングタッチポイントの最後の変更の日時。 |

{style="table-layout:auto"}

## マーケティングタッチポイントの追加

マーケティングタッチポイントを追加するには、 ![DataSearch](../assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Marketing touchpoint]** インターフェイスのMix Modeler:

1. 選択 ![追加](../assets/icons/AddCircle.svg) マーケティングタッチポイントの追加。

1. Adobe Analytics の **[!UICONTROL Marketing touchpoint]** ダイアログ。

   1. 名前を入力 **[!UICONTROL Touchpoint Name]**&#x200B;例： `Luma Touchpoint`.

   1. を定義 **[!UICONTROL Touchpoint rule]**.

      1. 値の選択元 **[!UICONTROL *調和を選択…*]**例：**[!UICONTROL Brand]**.

      1. 演算子の値を選択 ![シェブロン](../assets/icons/ChevronDown.svg)例： **[!UICONTROL is]**.

      1. 値の選択元 **[!UICONTROL *値を選択&#x200B;*]**または、例えば&#x200B;**[!DNL Luma]**.

   1. 次の中から調和されたフィールドを選択： **[!UICONTROL Touchpoint volume]**&#x200B;例： **[!UICONTROL Impressions]**.

   1. 次の中から調和されたフィールドを選択： **[!UICONTROL Touchpoint spend]**&#x200B;例： **[!UICONTROL Cost]**.

      ![マーケティングタッチポイント](../assets/create-touchpoint.png)

   1. マーケティングタッチポイントを作成するには、 **[!UICONTROL Create]**. マーケティングタッチポイントの作成をキャンセルするには、 **[!UICONTROL Cancel]** .

1. 作成すると、タッチポイントがマーケティングタッチポイントテーブルに追加されます。

