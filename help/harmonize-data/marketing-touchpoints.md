---
title: マーケティングタッチポイント
description: Mix Modelerのデータの調和の一部として使用するマーケティングタッチポイントを作成する方法を説明します。
feature: Harmonized Data, Marketing Touch Points
exl-id: 42851107-7568-4bc9-92ca-3cba713a522e
source-git-commit: b3e52a34f26574961823c08859f17e2e6f1fdcd3
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 11%

---

# マーケティングタッチポイント {#marketing-touchpoints}

>[!CONTEXTUALHELP]
>id="harmonizeddata_marketingtouchpoint"
>title="マーケティングタッチポイント"
>abstract="マーケティングタッチポイントは、数値または売上高ベースのコンバージョンに対するマーケティング投資の影響を評価するために使用される、受信者、個人または cookie レベルのマーケティングイベントです。"


マーケティングタッチポイントは、数値または売上高ベースのコンバージョンに対するマーケティング投資の影響を評価するために使用される、受信者、個人または cookie レベルのマーケティングイベントです。

アトリビューション分析に役立つマーケティングタッチポイントを定義します。

## マーケティングタッチポイントの管理

Mix Modeler インターフェイスで使用可能なマーケティングタッチポイントのテーブルを表示するには：

1. 左パネルから ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]** を選択します。

1. 上部バーの「**[!UICONTROL Marketing touchpoint]**」を選択します。 マーケティングタッチポイントのテーブルが表示されます。 他のページが使用可能な場合は、![x](/help/assets/icons/ChevronLeft.svg) の ![x](/help/assets/icons/ChevronRight.svg) で **[!UICONTROL Page _左向き矢印 _または_ 右向き矢印_]** を使用して、テーブルのページ間を移動します。

テーブル列は、マーケティングタッチポイントの詳細を指定します。

| 列名 | 詳細 |
| --- | ---|
| 名前 | マーケティングタッチポイントの名前。 |
| 費用指標 | タッチポイント支出の計算に使用する統一データ指標。 |
| ボリューム指標 | タッチポイント量の計算に使用する統一データ指標。 |
| 規則 | 使用するタッチポイントルール。 |
| 作成日 | マーケティングタッチポイントの作成日時。 |
| 最終変更日 | マーケティングタッチポイントの最終変更日時。 |


## マーケティングタッチポイントの追加

マーケティングタッチポイントを追加するには、Mix Modelerの ![DataSearch](/help/assets/icons/DataCheck.svg) **[!UICONTROL Harmonized data]**/**[!UICONTROL Marketing touchpoint]** インターフェイスで、次の手順を実行します。

1. ![&#x200B; 追加 &#x200B;](/help/assets/icons/AddCircle.svg) マーケティングタッチポイントを追加」を選択します。

1. **[!UICONTROL Marketing touchpoint]** ダイアログで、次の手順を実行します。

   1. **[!UICONTROL Touchpoint Name]** の名前（例：`Luma Touchpoint`）を入力します。

   1. **[!UICONTROL Touchpoint rule]** を定義します。

      1. **[!UICONTROL *統一された値を選択&#x200B;*]**&#x200B;から値を選択します（例：**[!UICONTROL Brand]**）。

      1. 演算子 ![&#x200B; 山形 &#x200B;](/help/assets/icons/ChevronDown.svg) の値を選択します（例：**[!UICONTROL is]**）。

      1. **[!UICONTROL *値を選択&#x200B;*]**&#x200B;から値を選択するか、値（例：**[!DNL Luma]**）を入力します。

   1. **[!UICONTROL Touchpoint volume]** から統一フィールド（例：**[!UICONTROL Impressions]**）を選択します。

   1. **[!UICONTROL Touchpoint spend]** から統一フィールド（例：**[!UICONTROL Cost]**）を選択します。

      ![&#x200B; マーケティングタッチポイント &#x200B;](/help/assets/create-touchpoint.png)

   1. マーケティングタッチポイントを作成するには、「**[!UICONTROL Create]**」を選択します。 マーケティングタッチポイントの作成をキャンセルするには、「**[!UICONTROL Cancel]**」を選択します。

1. 作成されると、タッチポイントがマーケティングタッチポイントテーブルに追加されます。


## 詳細を表示

マーケティングタッチポイントの詳細を表示するには：

1. テーブル内のマーケティングタッチポイント名にカーソルを合わせると、![&#x200B; 詳細 &#x200B;](/help/assets/icons/More.svg) を選択できます。

1. ![&#x200B; 表示 &#x200B;](/help/assets/icons/ViewDetail.svg)**表示** を選択します。 マーケティングタッチポイントの詳細を示すダイアログがあります。 詳しくは [&#x200B; マーケティングタッチポイントの追加 &#x200B;](#add-a-marketing-touchpoint) を参照してください。 「**[!UICONTROL Cancel]**」を選択して、ダイアログを閉じます。


## レポートを表示

マーケティングタッチポイントのレポートを表示するには：

1. テーブル内のマーケティングタッチポイント名にカーソルを合わせると、![&#x200B; 詳細 &#x200B;](/help/assets/icons/More.svg) を選択できます。

1. ![GraphTrend](/help/assets/icons/GraphTrend.svg)**レポートを表示** を選択します。 マーケティングタッチポイントのレポートを示すダイアログが表示されます。

   ![&#x200B; マーケティングタッチポイントビューレポート &#x200B;](../assets/marketingtouchpoint-view-report.png)

   * レポートする精度を変更するには、**[!UICONTROL Weekly]** ドロップダウンメニューから値を選択します。
   * レポートする期間を変更するには、開始日と終了日を入力するか、![&#x200B; カレンダー &#x200B;](/help/assets/icons/Calendar.svg) を使用してカレンダーポップアップで期間を定義します。

1. 「**[!UICONTROL Close]**」を選択して、ダイアログを閉じます。

## マーケティングタッチポイントの削除

マーケティングタッチポイントを削除する手順は次のとおりです。

1. テーブル内のマーケティングタッチポイント名にカーソルを合わせると、「![&#x200B; 削除 &#x200B;](/help/assets/icons/Delete.svg)**削除**」を選択できます。
1. **[!UICONTROL Delete touchpoint]** ダイアログの確認ダイアログで、マーケティングタッチポイントを永続的に削除する **[!UICONTROL Delete]** を選択します。

