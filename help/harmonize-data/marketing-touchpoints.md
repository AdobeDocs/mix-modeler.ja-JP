---
title: マーケティングタッチポイント
description: Mix Modeler内のデータの調和の一部として使用するマーケティングタッチポイントを作成する方法を説明します。
feature: Harmonized Data, Marketing Touch Points
exl-id: 42851107-7568-4bc9-92ca-3cba713a522e
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# マーケティングタッチポイント

マーケティングタッチポイントは、数値または収益ベースのコンバージョンに対するマーケティング投資の影響を評価するために使用される、受信者、個人または cookie レベルのマーケティングイベントです。

アトリビューション分析に役立つマーケティングタッチポイントを定義します。

## マーケティングタッチポイントの管理

Mix Modelerインターフェイスで使用可能なマーケティングタッチポイントのテーブルを表示するには：

1. を選択 ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** 左パネルから。

1. を選択 **[!UICONTROL Marketing touchpoint]** 上部バーから。 マーケティングタッチポイントのテーブルが表示されます。 他のページが使用可能な場合は、を使用します ![左矢印](/help/assets//icons/ChevronLeft.svg) または ![右矢印](/help/assets//icons/ChevronRight.svg) 時刻 **[!UICONTROL Page _x _件中_x_]** をクリックして、テーブルのページ間を移動します。

テーブル列は、マーケティングタッチポイントの詳細を指定します。

| 列名 | 詳細 |
| --- | ---|
| 名前 | マーケティングタッチポイントの名前。 |
| 費用指標 | タッチポイント支出の計算に使用する統一データ指標。 |
| ボリューム指標 | タッチポイント量の計算に使用する統一データ指標。 |
| 規則 | 使用するタッチポイントルール。 |
| 作成日 | マーケティングタッチポイントの作成日時。 |
| 最終変更日 | マーケティングタッチポイントの最終変更日時。 |

{style="table-layout:auto"}

## マーケティングタッチポイントの追加

マーケティングタッチポイントを追加するには、 ![DataSearch](/help/assets//icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Marketing touchpoint]** Mix Modelerのインターフェイス：

1. を選択 ![追加](/help/assets//icons/AddCircle.svg) マーケティングタッチポイントを追加します。

1. が含まれる **[!UICONTROL Marketing touchpoint]** ダイアログ。

   1. の名前を入力 **[!UICONTROL Touchpoint Name]**、例： `Luma Touchpoint`.

   1. の定義 **[!UICONTROL Touchpoint rule]**.

      1. から値を選択 **[!UICONTROL *調和されたを選択&#x200B;*]**、例：**[!UICONTROL Brand]**.

      1. 演算子の値を選択 ![山形](/help/assets//icons/ChevronDown.svg)、例： **[!UICONTROL is]**.

      1. から値を選択 **[!UICONTROL *値を選択&#x200B;*]**または値を入力します。例：**[!DNL Luma]**.

   1. から統一フィールドを選択 **[!UICONTROL Touchpoint volume]**、例： **[!UICONTROL Impressions]**.

   1. から統一フィールドを選択 **[!UICONTROL Touchpoint spend]**、例： **[!UICONTROL Cost]**.

      ![マーケティングタッチポイント](/help/assets//create-touchpoint.png)

   1. マーケティングタッチポイントを作成するには、以下を選択します **[!UICONTROL Create]**. マーケティングタッチポイントの作成をキャンセルするには、次を選択します。 **[!UICONTROL Cancel]** .

1. 作成されると、タッチポイントがマーケティングタッチポイントテーブルに追加されます。


## マーケティングタッチポイントの表示

マーケティングタッチポイントを表示するには：

1. を選択 ![詳細](/help/assets//icons/More.svg) テーブルのマーケティングタッチポイント名にカーソルを合わせたとき。

1. を選択 ![表示](/help/assets//icons/ViewDetail.svg) **表示**. マーケティングタッチポイントの詳細を示すダイアログがあります。 参照： [マーケティングタッチポイントの追加](#add-a-marketing-touchpoint) を参照してください。 を選択 **[!UICONTROL Cancel]** をクリックしてダイアログを閉じます。


## マーケティングタッチポイントの削除

マーケティングタッチポイントを削除する手順は次のとおりです。

1. を選択 ![削除](/help/assets//icons/Delete.svg) **削除** テーブルのマーケティングタッチポイント名にカーソルを合わせたとき。
1. が含まれる **[!UICONTROL Delete touchpoint]** ダイアログ確認ダイアログ選択 **[!UICONTROL Delete]** マーケティングタッチポイントを永続的に削除します。

