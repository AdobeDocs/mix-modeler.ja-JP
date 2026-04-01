---
title: プランの概要
description: Mix Modelerでプランを表示、選択、およびアクションする方法について説明します。
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 7836e378a0f9068fc868dcede0ab8b3e2803776a
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# プランの概要

Mix Modelerのプランでは、事業部門やチャネルごとに予算を割り当てることができます。 計画機能は、調和データに基づいてトレーニングされたモデルの結果と統合されます。

特定の期間にマーケティング関連のプロジェクトに費やす予定の任意の投資（予算など）の概要が記載されています。 これらの投資は、一般的なKPI （注文、売上など）に対応しています。 プランには、有料広告、スポンサー付きweb コンテンツ、イベントなどのチャネルからの費用が含まれます。

プランには以下が必要です。

- モデル，
- データ範囲，
- 予算ですね。

プランには、オプションで次の項目を含めることができます。

- 設定された認識ウィンドウ，
- 予算、ユースケース、航空券の購入日を，
- チャネルとフライト日ごとの最小および最大の予算制約。

プランに使用したモデルが新しいデータでスコアリングされている場合は、スコアリングされたデータを考慮して新しいプランを作成する必要があります。


## プランの構築

プランを作成するには、Mix Modeler プラン作成ウィザードを使用します。 詳しくは、[&#x200B; プランの作成](build.md)を参照してください。


## プランの管理

現在のプランの表を表示するには、Mix Modeler インターフェイスで次の操作を行います。

1. 左側のパネルから![](/help/assets/icons2/FileChart.svg) **[!UICONTROL Plans]**&#x200B;を選択します。

1. 現在の計画とそのステータスの表が表示されます。

   表の列には、計画に関する詳細が示されます。

   | 列の名前 | 詳細 |
   |---|---|
   | **[!UICONTROL Name]** | プランの名前 |
   | **[!UICONTROL Model]** | プランのベースとして使用されるモデル。 |
   | **[!UICONTROL Date range]** | プランの完全な日付範囲。 |
   | **[!UICONTROL Budget]** | プランの総予算。 |
   | **[!UICONTROL Plan target]** | ターゲットベースのプランに定義されたターゲット指標。 |
   | **[!UICONTROL Forecasted return]** | プランの[予測収益](/help/main-guide/glossary.md) |
   | **[!UICONTROL Forecasted ROI]** | [は、プランのROIを予測](/help/main-guide/glossary.md)しました。 |
   | **[!UICONTROL Forecasted conversion]** | プランの[予測コンバージョン &#x200B;](/help/main-guide/glossary.md) |
   | **[!UICONTROL Forecasted CPA]** | プランの[予測CPA](/help/main-guide/glossary.md)です |
   | **[!UICONTROL Status]** | プランのステータス：<br/>![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Failed]**、<br/>![StatusBlue](/help/assets/icons/StatusBlue.svg) **[!UICONTROL Processing]**、または<br/>![StatusGreen](/help/assets/icons/StatusGreen.svg) **[!UICONTROL Complete]**。 |

   ![ColumnSetting](/help/assets/icons/ColumnSetting.svg)を使用して、テーブルに表示する列![Checkmark](/help/assets/icons/Checkmark.svg)を選択できます。

   昇順![ArrowMoveUp](/help/assets/icons2/ArrowMoveUp.svg)または降順![ArrowMoveDown](/help/assets/icons2/ArrowMoveDown.svg)の任意の列でテーブルを並べ替えるには、列のタイトルを選択します。

   **[!UICONTROL Name]**、**[!UICONTROL Model]**&#x200B;または&#x200B;**[!UICONTROL Date range]**&#x200B;列を並べ替えるか、サイズを変更するには、**[!UICONTROL Name]** ![ChevronDown](/help/assets/icons/ChevronDown.svg)、**[!UICONTROL Model]** ![ChevronDown](/help/assets/icons/ChevronDown.svg)または&#x200B;**[!UICONTROL Date range]** ![ChevronDown](/help/assets/icons/ChevronDown.svg)を選択します。 コンテキストメニューから、**[!UICONTROL Sort ascending]**、**[!UICONTROL Sort descending]**、または&#x200B;**[!UICONTROL Resize column]**&#x200B;を選択します。 または、列の区切り記号にカーソルを合わせて、列のサイズを変更することもできます。

1. ![検索](/help/assets/icons/Search.svg)を使用して、1つ以上の特定のプランのテーブルを検索してフィルタリングします。

### プランインサイト

プランのインサイトを表示し、プランを編集するには：

1. 左側のパネルから「![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]**」を選択します。

1. プラン名を選択します。

「[&#x200B; プランのインサイト &#x200B;](insights.md)」にリダイレクトされます。


### プランの複製

プランを複製するには：

- プランの![詳細](/help/assets/icons/More.svg)を選択します。 コンテキストメニューから、**[!UICONTROL Duplicate]**&#x200B;を選択します。
- または、テーブル ![SelectBox](/help/assets/icons/SelectBox.svg)でプランを選択し、青いアクションバーから![Copy](/help/assets/icons/Copy.svg) **[!UICONTROL Duplicate]**&#x200B;を選択します。

元のプランの名前に&#x200B;**[!UICONTROL (Copy)]（_n_）**&#x200B;が付いた新しいプランが作成されます。 コピーしたプランの更新された詳細を提供するため、[&#x200B; プラン作成](build.md)に自動的にリダイレクトされます。

- 元のプランの詳細（説明、予算など）がコピーされます。
- 元のプランの予算制約は、新しく作成したプランにコピーされます。
- コピーしたプランのベースとして別のモデルを選択するオプションがあります。
   - コピーしたプランに存在するが、新しく選択したモデルには存在しないタッチポイントまたはチャネルの場合、これらのタッチポイントまたはチャネルの制約はプランから削除されます。
   - コピーしたプランには存在しないが、新しく選択したモデルには存在するタッチポイントまたはチャネルの場合、制約は次のように設定されます。
      - 最小値`0`,
      - 計画フライト範囲予算に沿った最大値。



### プランの比較

プランを比較するには：

1. テーブルから2つのプランを選択します。
1. 青いアクションバーから「![比較](/help/assets/icons/Compare.svg) **[!UICONTROL Compare]**」を選択します。 **[!UICONTROL Compare plans]** UIが表示されます。


### プランの削除

プランを削除するには：

1. プランの![詳細](/help/assets/icons/More.svg)を選択します。 コンテキストメニューから、**[!UICONTROL Delete]**&#x200B;を選択します。 <br/>または、テーブル ![SelectBox](/help/assets/icons/SelectBox.svg)でプランを選択し、青いアクションバーから![削除](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]**&#x200B;を選択します。
1. **[!UICONTROL Delete plan]**&#x200B;確認ダイアログで「**[!UICONTROL Delete]**」を選択して、プランを削除します。 キャンセルする場合は&#x200B;**[!UICONTROL Cancel]**&#x200B;を選択してください。

複数のプランを削除するには：

1. 複数のプランを選択します。
1. 青いアクションバーから、![削除](/help/assets/icons/Delete.svg) **[!UICONTROL Delete]**&#x200B;を選択してプランを削除します。
1. **[!UICONTROL Delete *x *プラン]**&#x200B;確認ダイアログで「**[!UICONTROL Delete]**」を選択して、プランを削除します。 キャンセルする場合は&#x200B;**[!UICONTROL Cancel]**&#x200B;を選択してください。


