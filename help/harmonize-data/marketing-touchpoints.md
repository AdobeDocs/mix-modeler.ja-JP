---
title: マーケティングタッチポイント
description: Mix Modeler内のデータの調和の一部として使用するマーケティングタッチポイントを作成する方法を説明します。
feature: Harmonized Data, Marketing Touch Points
exl-id: 42851107-7568-4bc9-92ca-3cba713a522e
source-git-commit: 665b344dfa94275d71e0ecf198d9bb9b73ea584b
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# マーケティングタッチポイント

マーケティングタッチポイントは、数値または収益ベースのコンバージョンに対するマーケティング投資の影響を評価するために使用される、受信者、個人または cookie レベルのマーケティングイベントです。

アトリビューション分析に役立つマーケティングタッチポイントを定義します。

## マーケティングタッチポイントの管理

Mix Modelerインターフェイスで使用可能なマーケティングタッチポイントのテーブルを表示するには：

1. 左パネルから ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** を選択します。

1. 上部バーの「**[!UICONTROL Marketing touchpoint]**」を選択します。 マーケティングタッチポイントのテーブルが表示されます。 他のページが使用可能な場合は、![x](/help/assets/icons/ChevronLeft.svg) の **[!UICONTROL Page _x _で ![ 左向き矢印 ](/help/assets/icons/ChevronRight.svg) または_ 右向き矢印_]** を使用して、テーブルのページ間を移動します。

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

マーケティングタッチポイントを追加するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Marketing touchpoint]** インターフェイスで、次の手順を実行します。

1. ![ 追加 ](/help/assets/icons/AddCircle.svg) マーケティングタッチポイントを追加」を選択します。

1. **[!UICONTROL Marketing touchpoint]** ダイアログで、次の手順を実行します。

   1. **[!UICONTROL Touchpoint Name]** の名前（例：`Luma Touchpoint`）を入力します。

   1. **[!UICONTROL Touchpoint rule]** を定義します。

      1. **[!UICONTROL *統一された値を選択&#x200B;*]**から値を選択します（例：**[!UICONTROL Brand]**）。

      1. 演算子 ![ 山形 ](/help/assets/icons/ChevronDown.svg) の値を選択します（例：**[!UICONTROL is]**）。

      1. **[!UICONTROL *値を選択&#x200B;*]**から値を選択するか、値（例：**[!DNL Luma]**）を入力します。

   1. **[!UICONTROL Touchpoint volume]** から統一フィールド（例：**[!UICONTROL Impressions]**）を選択します。

   1. **[!UICONTROL Touchpoint spend]** から統一フィールド（例：**[!UICONTROL Cost]**）を選択します。

      ![ マーケティングタッチポイント ](/help/assets/create-touchpoint.png)

   1. マーケティングタッチポイントを作成するには、「**[!UICONTROL Create]**」を選択します。 マーケティングタッチポイントの作成をキャンセルするには、「**[!UICONTROL Cancel]**」を選択します。

1. 作成されると、タッチポイントがマーケティングタッチポイントテーブルに追加されます。


## 詳細を表示

マーケティングタッチポイントの詳細を表示するには：

1. テーブル内のマーケティングタッチポイント名にカーソルを合わせると、![ 詳細 ](/help/assets/icons/More.svg) を選択できます。

1. ![ 表示 ](/help/assets/icons/ViewDetail.svg)**表示** を選択します。 マーケティングタッチポイントの詳細を示すダイアログがあります。 詳しくは [ マーケティングタッチポイントの追加 ](#add-a-marketing-touchpoint) を参照してください。 「**[!UICONTROL Cancel]**」を選択して、ダイアログを閉じます。


## レポートを表示

マーケティングタッチポイントのレポートを表示するには：

1. テーブル内のマーケティングタッチポイント名にカーソルを合わせると、![ 詳細 ](/help/assets/icons/More.svg) を選択できます。

1. ![GraphTrend](/help/assets/icons/GraphTrend.svg)**レポートを表示** を選択します。 マーケティングタッチポイントのレポートを示すダイアログが表示されます。

   ![ マーケティングタッチポイントビューレポート ](../assets/marketingtouchpoint-view-report.png)

   * レポートする精度を変更するには、**[!UICONTROL Weekly]** ドロップダウンメニューから値を選択します。
   * レポートする期間を変更するには、開始日と終了日を入力するか、![ カレンダー ](/help/assets/icons/Calendar.svg) を使用してカレンダーポップアップで期間を定義します。

1. 「**[!UICONTROL Close]**」を選択して、ダイアログを閉じます。

## マーケティングタッチポイントの削除

マーケティングタッチポイントを削除する手順は次のとおりです。

1. テーブル内のマーケティングタッチポイント名にカーソルを合わせると、「![ 削除 ](/help/assets/icons/Delete.svg)**削除**」を選択できます。
1. **[!UICONTROL Delete touchpoint]** ダイアログの確認ダイアログで、マーケティングタッチポイントを永続的に削除する **[!UICONTROL Delete]** を選択します。

