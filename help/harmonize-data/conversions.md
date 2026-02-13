---
title: コンバージョン数
description: Mix Modelerのデータの調和の一部として使用するコンバージョンを作成する方法を説明します。
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
source-git-commit: 5468e0aaf37bf2dca8912199ea26e5f8d9069cb5
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 2%

---

# コンバージョン数 {#conversions}


>[!CONTEXTUALHELP]
>id="harmonizeddata_conversions_create"
>title="変換"
>abstract="コンバージョンイベントは、マーケティングアクティビティの影響を特定するビジネス目標です。 例：e コマースの注文、店舗での購入、web サイトへの訪問など。"


コンバージョンイベントは、マーケティングアクティビティの影響を特定するビジネス目標です。 例：e コマースの注文、店舗での購入、web サイトへの訪問など。

アトリビューション分析用のマーケティングコンバージョンを定義します。

## コンバージョンの管理

Mix Modeler インターフェイスで使用可能なコンバージョンの表を確認するには、次の手順を実行します。

1. 左パネルから ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** を選択します。

1. 上部バーの「**[!UICONTROL Conversions]**」を選択します。 コンバージョンのテーブルが表示されます。

テーブルの列には、変換に関する詳細が表示されます。

| 列の名前 | 詳細 |
| --- | ---|
| 名前 | コンバージョンの名前。 |
| 売上高 | コンバージョンから得られる売上高の計算に使用する、統一データ指標。 |
| コンバージョン指標 | 分析のコンバージョン指標として使用する統一データ指標。 |
| カテゴリ | コンバージョンのコンバージョンカテゴリ。 |
| 作成日 | コンバージョンが作成された日時。 |
| 最終変更日 | コンバージョンが最後に変更された日時。 |


## コンバージョンを追加

Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Conversion]** インターフェイスでコンバージョンを追加するには、次の手順を実行します。

1. 「![&#x200B; 追加 &#x200B;](/help/assets/icons/AddCircle.svg)」を選択し **[!UICONTROL Add a conversion]** す。

1. **[!UICONTROL Create conversion]** ダイアログで、次の手順を実行します。

   1. **[!UICONTROL Conversion]** の名前（例：`Store Conversions`）を入力します。

   1. **[!UICONTROL Conversion category]** を定義します。

      1. **[!UICONTROL *調和を選択…*]**&#x200B;の値を選択します（例：`Conversion types`）。

      1. 演算子 ![&#x200B; 山形 &#x200B;](/help/assets/icons/ChevronDown.svg) の値（例：**[!UICONTROL is]**）を選択します。

      1. **[!UICONTROL *値を選択&#x200B;*]**&#x200B;から値を選択するか、値（例：**[!UICONTROL Store]**）を入力します。

   1. **[!UICONTROL Conversion metric for analysis]** から統一フィールド（例：**[!UICONTROL Orders]**）を選択します。

   1. **[!UICONTROL Revenue field]** から統一フィールド（例：**[!UICONTROL Gross Demand]**）を選択します。

   1. 変換を作成するには、「**[!UICONTROL Create]**」を選択します。 コンバージョンの作成をキャンセルするには、「**[!UICONTROL Cancel]**」を選択します。

      ![&#x200B; 代替テキスト &#x200B;](/help/assets/create-conversion.png)

1. 作成されると、変換が変換テーブルに追加されます。


## 詳細を表示

コンバージョンの詳細を表示するには：

1. テーブル内のコンバージョン名にカーソルを合わせたときに「![&#x200B; 詳細 &#x200B;](/help/assets/icons/More.svg)」を選択します。

1. ![&#x200B; 表示 &#x200B;](/help/assets/icons/ViewDetail.svg)**詳細を表示** を選択します。 コンバージョンの詳細を示すダイアログが表示されます。 詳しくは、[&#x200B; コンバージョンの追加 &#x200B;](#add-a-conversion) を参照してください。 「**[!UICONTROL Cancel]**」を選択して、ダイアログを閉じます。

## レポートを表示

コンバージョンのレポートを表示するには：

1. テーブル内のコンバージョン名にカーソルを合わせたときに「![&#x200B; 詳細 &#x200B;](/help/assets/icons/More.svg)」を選択します。

1. ![GraphTrend](/help/assets/icons/GraphTrend.svg)**レポートを表示** を選択します。 コンバージョンのレポートがダイアログに表示されます。

   ![&#x200B; コンバージョン表示レポート &#x200B;](../assets/conversion-view-report.png)

   * レポートする精度を変更するには、**[!UICONTROL Weekly]** ドロップダウンメニューから値を選択します。
   * レポートする期間を変更するには、開始日と終了日を入力するか、![&#x200B; カレンダー &#x200B;](/help/assets/icons/Calendar.svg) を使用してカレンダーポップアップで期間を定義します。

1. 「**[!UICONTROL Close]**」を選択して、ダイアログを閉じます。

## コンバージョンの削除

コンバージョンを削除するには：

1. テーブル内の変換名にカーソルを合わせたときに「![&#x200B; 削除 &#x200B;](/help/assets/icons/Delete.svg)**削除**」を選択します。
1. **[!UICONTROL Delete conversion]** ダイアログの確認ダイアログで、コンバージョンを完全に削除する **[!UICONTROL Delete]** を選択します。
