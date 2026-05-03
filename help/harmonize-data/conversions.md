---
title: コンバージョン数
description: Mix Modelerでデータを調和させる一環として使用するコンバージョンの作成方法について説明します。
feature: Harmonized Data, Conversions
exl-id: a8559426-452a-43e8-9a60-0c0bc97d863c
TQID: https://experienceleague.adobe.com/rjFYd9XMTc5z4frFlq41PJqh9Zim-qoHSToyZenTPXE
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: a567f0f7-0057-4079-8ded-5b24cc25af15
subfeature_v2:
  - id: bc2f5225-03d4-4bc8-89ec-99d78c30e6dd
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T09:15:50.061Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 424
ht-degree: 10%

---

# コンバージョン数 {#conversions}


>[!CONTEXTUALHELP]
>id="harmonizeddata_conversions_create"
>title="変換"
>abstract="コンバージョンイベントは、マーケティングアクティビティの影響を識別するビジネス目標です。 例：e コマースの注文、店舗での購入、web サイトへの訪問など。"


コンバージョンイベントは、マーケティングアクティビティの影響を識別するビジネス目標です。 例：コマース注文、実店舗での購入、web サイトへの訪問など

アトリビューション分析用にマーケティングコンバージョンを定義します。

## コンバージョンの管理

使用可能なコンバージョンの表を表示するには、Mix Modeler インターフェイスで次の操作を行います。

1. 左側のパネルから「![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**」を選択します。

1. 上部バーから&#x200B;**[!UICONTROL Conversions]**&#x200B;を選択します。 コンバージョンのテーブルが表示されます。

表の列には、変換に関する詳細が示されます。

| 列の名前 | 詳細 |
| --- | ---|
| 名前 | コンバージョンの名前。 |
| 売上高 | コンバージョンからの収益を計算するために使用する調和されたデータ指標。 |
| コンバージョン指標 | 分析の変換指標として使用する調和データ指標。 |
| カテゴリ | コンバージョンのコンバージョンカテゴリ。 |
| 作成日時 | コンバージョンの作成日時。 |
| 最終変更日 | コンバージョンの最後の変更の日時。 |


## コンバージョンの追加

コンバージョンを追加するには、Mix Modelerの![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** > **[!UICONTROL Conversion]** インターフェイスで次の操作を行います。

1. 「![追加](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add a conversion]**」を選択します。

1. **[!UICONTROL Create conversion]** ダイアログで、次の操作を行います。

   1. **[!UICONTROL Conversion]**&#x200B;の名前（例：`Store Conversions`）を入力してください。

   1. **[!UICONTROL Conversion category]**&#x200B;を定義します。

      1. **[!UICONTROL *調和を選択…*]**&#x200B;から値を選択します（例：`Conversion types`）。

      1. 演算子![Chevron](/help/assets/icons/ChevronDown.svg)の値（例：**[!UICONTROL is]**）を選択します。

      1. **[!UICONTROL *値&#x200B;*]**&#x200B;から値を選択するか、値（例：**[!UICONTROL Store]**）を入力します。

   1. **[!UICONTROL Conversion metric for analysis]**&#x200B;から調和されたフィールド （例：**[!UICONTROL Orders]**）を選択します。

   1. **[!UICONTROL Revenue field]**&#x200B;から調和されたフィールド （例：**[!UICONTROL Gross Demand]**）を選択します。

   1. コンバージョンを作成するには、**[!UICONTROL Create]**&#x200B;を選択します。 コンバージョンの作成をキャンセルするには、**[!UICONTROL Cancel]**&#x200B;を選択します。

      ![代替テキスト &#x200B;](/help/assets/create-conversion.png)

1. 作成すると、コンバージョンがコンバージョンテーブルに追加されます。


## 詳細を表示

コンバージョンの詳細を表示するには、次の手順に従います。

1. テーブル内のコンバージョン名にカーソルを合わせると、![詳細](/help/assets/icons/More.svg)を選択します。

1. ![表示](/help/assets/icons/ViewDetail.svg) **詳細を表示**&#x200B;を選択します。 ダイアログにコンバージョンの詳細が表示されます。 詳しくは、[&#x200B; コンバージョンの追加](#add-a-conversion)を参照してください。 ダイアログを閉じるには、**[!UICONTROL Cancel]**&#x200B;を選択します。

## レポートを読む

コンバージョンのレポートを表示するには：

1. テーブル内のコンバージョン名にカーソルを合わせると、![詳細](/help/assets/icons/More.svg)を選択します。

1. 「![GraphTrend](/help/assets/icons/GraphTrend.svg) **レポートを表示**」を選択します。 ダイアログには、コンバージョンのレポートが表示されます。

   ![&#x200B; コンバージョンビューレポート &#x200B;](../assets/conversion-view-report.png)

   * レポートする精度を変更するには、**[!UICONTROL Weekly]** ドロップダウンメニューから値を選択します。
   * レポートする期間を変更するには、開始日と終了日を入力するか、![&#x200B; カレンダー](/help/assets/icons/Calendar.svg)を使用してカレンダーのポップアップで期間を定義します。

1. ダイアログを閉じるには、**[!UICONTROL Close]**&#x200B;を選択します。

## コンバージョンの削除

コンバージョンを削除するには：

1. テーブルのコンバージョン名にカーソルを合わせると、![削除](/help/assets/icons/Delete.svg) **削除**&#x200B;を選択します。
1. **[!UICONTROL Delete conversion]** ダイアログの確認ダイアログで、**[!UICONTROL Delete]**&#x200B;を選択してコンバージョンを完全に削除します。
