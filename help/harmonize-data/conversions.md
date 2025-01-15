---
title: コンバージョン数
description: Mix Modeler内のデータの調和の一部として使用するコンバージョンを作成する方法を説明します。
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 665b344dfa94275d71e0ecf198d9bb9b73ea584b
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---

# コンバージョン数

コンバージョンイベントは、マーケティングアクティビティの影響を特定するビジネス目標です。 例：e コマースの注文、店舗での購入、web サイトへの訪問など。

アトリビューション分析用のマーケティングコンバージョンを定義します。

## コンバージョンの管理

Mix Modelerインターフェイスで使用可能なコンバージョンのテーブルを表示するには、次の手順を実行します。

1. 左パネルから ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** を選択します。

1. 上部バーの「**[!UICONTROL Conversions]**」を選択します。 コンバージョンのテーブルが表示されます。

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

コンバージョンを追加するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Conversion]** インターフェイスで、次の手順を実行します。

1. 「![ 追加 ](/help/assets/icons/AddCircle.svg)」を選択し **[!UICONTROL Add a conversion]** す。

1. **[!UICONTROL Create conversion]** ダイアログで、次の手順を実行します。

   1. **[!UICONTROL Conversion]** の名前（例：`Store Conversions`）を入力します。

   1. **[!UICONTROL Conversion category]** を定義します。

      1. **[!UICONTROL *調和を選択…*]**の値を選択します（例：`Conversion types`）。

      1. 演算子 ![ 山形 ](/help/assets/icons/ChevronDown.svg) の値（例：**[!UICONTROL is]**）を選択します。

      1. **[!UICONTROL *値を選択&#x200B;*]**から値を選択するか、値（例：**[!UICONTROL Store]**）を入力します。

   1. **[!UICONTROL Conversion metric for analysis]** から統一フィールド（例：**[!UICONTROL Orders]**）を選択します。

   1. **[!UICONTROL Revenue field]** から統一フィールド（例：**[!UICONTROL Gross Demand]**）を選択します。

   1. 変換を作成するには、「**[!UICONTROL Create]**」を選択します。 コンバージョンの作成をキャンセルするには、「**[!UICONTROL Cancel]**」を選択します。

      ![ 代替テキスト ](/help/assets/create-conversion.png)

1. 作成されると、変換が変換テーブルに追加されます。


## 詳細を表示

コンバージョンの詳細を表示するには：

1. テーブル内のコンバージョン名にカーソルを合わせたときに「![ 詳細 ](/help/assets/icons/More.svg)」を選択します。

1. ![ 表示 ](/help/assets/icons/ViewDetail.svg)**詳細を表示** を選択します。 コンバージョンの詳細を示すダイアログが表示されます。 詳しくは、[ コンバージョンの追加 ](#add-a-conversion) を参照してください。 「**[!UICONTROL Cancel]**」を選択して、ダイアログを閉じます。

## レポートを表示

コンバージョンのレポートを表示するには：

1. テーブル内のコンバージョン名にカーソルを合わせたときに「![ 詳細 ](/help/assets/icons/More.svg)」を選択します。

1. ![GraphTrend](/help/assets/icons/GraphTrend.svg)**レポートを表示** を選択します。 コンバージョンのレポートがダイアログに表示されます。

   ![ コンバージョン表示レポート ](../assets/conversion-view-report.png)

   * レポートする精度を変更するには、**[!UICONTROL Weekly]** ドロップダウンメニューから値を選択します。
   * レポートする期間を変更するには、開始日と終了日を入力するか、![ カレンダー ](/help/assets/icons/Calendar.svg) を使用してカレンダーポップアップで期間を定義します。

1. 「**[!UICONTROL Close]**」を選択して、ダイアログを閉じます。

## コンバージョンの削除

コンバージョンを削除するには：

1. テーブル内の変換名にカーソルを合わせたときに「![ 削除 ](/help/assets/icons/Delete.svg)**削除**」を選択します。
1. **[!UICONTROL Delete conversion]** ダイアログの確認ダイアログで、コンバージョンを完全に削除する **[!UICONTROL Delete]** を選択します。
