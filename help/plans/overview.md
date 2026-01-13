---
title: 計画の概要
description: Mix Modelerでプランを表示、選択およびアクションする方法を説明します。
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 0d11168b71319e6c854482f89dbb1bb68962a880
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# 計画の概要

Mix Modelerのプランを使用すると、ビジネスユニットおよびチャネル別に予算を割り当てることができます。 計画機能は、統一されたデータに基づいて、トレーニング済みモデルの結果と統合されます。

プランでは、特定の期間にわたって、マーケティング関連のプロジェクトにビジネスが費やそうとする裁量的投資（予算など）の概要を説明します。 これらの投資は、一般的な KPI （注文、収益など）に役立ちます。 プランには、有料広告、スポンサー付き web コンテンツ、イベントなどのチャネルからの費用が含まれる場合があります。

プランには次が必要です。

- モデル、
- データ範囲
- 予算。

計画には、オプションで次の項目を含めることができます。

- 設定済みの認識ウィンドウ、
- 複数のフライト日（それぞれに目標予算がある）
- チャネルおよびフライト日ごとの最小予算制約と最大予算制約。

プランに使用したモデルが新しいデータでスコアリングされている場合、再スコアリングされたデータを考慮して新しいプランを作成する必要があります。


## プランの作成

プランを作成するには、Mix Modeler プラン作成ウィザードを使用します。 詳しくは、[ プランの作成 ](build.md) を参照してください。


## プランの管理

Mix Modeler インターフェイスで現在の計画のテーブルを表示するには、次の手順を実行します。

1. 左パネルから ![](/help/assets/icons2/FileChart.svg) **[!UICONTROL Plans]** を選択します。

1. 現在のプランとそのステータスのテーブルが表示されます。

   表の列には、計画の詳細が示されます。

   | 列名 | 詳細 |
   |---|---|
   | 名前 | プランの名前 |
   | モデル | プランのベースとして使用されるモデル。 |
   | 日付範囲 | プランの完全な日付範囲。 |
   | 予算 | 計画の予算合計。 |
   | 目標を計画 | ターゲットベースのプランに対して定義されたターゲット指標。 |
   | 予測リターン | 計画の [ 予測収益 ](/help/main-guide/glossary.md) |
   | 予測 ROI | プランの [ 予測 ROI](/help/main-guide/glossary.md)。 |
   | 予測コンバージョン | プランの [ 予測コンバージョン ](/help/main-guide/glossary.md) |
   | 予測 CPA | 計画の [ 予測 CPA](/help/main-guide/glossary.md) |
   | ステータス | プランのステータス： <p><span style="color:red">●</span> に失敗しました、 <p><span style="color:blue">●</span> 処理、または <p><span style="color:green">●</span> 完了。 |

   {style="table-layout:auto"}

   ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) を使用して ![Checkmark](/help/assets/icons/Checkmark.svg) を選択すると、テーブルに表示する列を選択できます。

   任意の列のテーブルを昇順 ![ArrowMoveUp](/help/assets/icons2/ArrowMoveUp.svg) または降順 ![ArrowMoveDown](/help/assets/icons2/ArrowMoveDown.svg) で並べ替えるには、列のタイトルを選択します。

   **[!UICONTROL Name]**、**[!UICONTROL Model]** または **[!UICONTROL Date range]** の列の並べ替えまたはサイズ変更を行う **[!UICONTROL Name]** は、「![ 山形の下 ](/help/assets/icons/ChevronDown.svg)」、「**[!UICONTROL Model]** ![ 山形の下 ](/help/assets/icons/ChevronDown.svg) **[!UICONTROL Date range]**」または「![ 山形の下 ](/help/assets/icons/ChevronDown.svg)」を選択します。 コンテキストメニューから「**[!UICONTROL Sort ascending]**」、「**[!UICONTROL Sort descending]**」、または「**[!UICONTROL Resize column]**」を選択します。 または、これらの列の列区切り記号の上にマウスポインターを置くと、列のサイズを変更できます。

1. ![ 検索 ](/help/assets/icons/Search.svg) を使用して、1 つ以上の特定のプランについてテーブルを検索およびフィルタリングします。

### プランインサイト

計画のインサイトを表示し、計画を編集する手順は、次のとおりです。

1. 左パネルから ![PLan](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** を選択します。

1. 計画名を選択します。

[ インサイトの計画 ](insights.md) にリダイレクトされます。


### プランの複製

計画を複製する手順は、次のとおりです。

- プランの ![ 詳細 ](/help/assets/icons/More.svg) を選択します。 コンテキストメニューから「**[!UICONTROL Duplicate]**」を選択します。
- または、テーブルの ![ 選択ボックス ](/help/assets/icons/SelectBox.svg) でプランを選択し、青いアクションバーから ![ コピー ](/help/assets/icons/Copy.svg)**[!UICONTROL Duplicate]** を選択します。

元の計画の名前に **[!UICONTROL (Copy)]（_n_）** を付けた名前の新規計画が作成されます。 コピーしたプランの更新された詳細を提供するために、自動的に [ プランの作成 ](build.md) にリダイレクトされます。

- 元のプランの詳細（説明、予算など）がコピーされます。
- 元の計画の予算制約が、新しく作成された計画にコピーされます。
- コピーしたプランのベースとして別のモデルを選択することもできます。
   - コピーした計画には存在するが新しく選択したモデルには存在しないタッチポイントまたはチャネルの場合、これらのタッチポイントまたはチャネルに対する制約は計画から削除されます。
   - コピーした計画には存在しないが、新しく選択したモデルには存在するタッチポイントまたはチャネルの場合、制約は次のように設定されます。
      - 最小値は `0`、
      - 計画フライト範囲の予算に沿った最大値。



### 計画の比較

計画を比較する手順は、次のとおりです。

1. テーブルから 2 つのプランを選択します。
1. 青いアクションバーから ![ 比較 ](/help/assets/icons/Compare.svg)**[!UICONTROL Compare]** を選択します。 **[!UICONTROL Compare plans]** UI が表示されます。


### 計画の削除

計画を削除する手順は、次のとおりです。

1. プランの ![ 詳細 ](/help/assets/icons/More.svg) を選択します。 コンテキストメニューから「**[!UICONTROL Delete]**」を選択します。 <br/> または、テーブルの ![ 選択ボックス ](/help/assets/icons/SelectBox.svg) でプランを選択し、青いアクションバーから ![ 削除 ](/help/assets/icons/Delete.svg)**[!UICONTROL Delete]** を選択します。
1. **[!UICONTROL Delete]** の確認ダイアログで「**[!UICONTROL Delete plan]**」を選択して、計画を削除します。 キャンセルする **[!UICONTROL Cancel]** を選択します。

複数の計画を削除する手順は、次のとおりです。

1. 複数の計画を選択します。
1. 青いアクションバーから、「![ 削除 ](/help/assets/icons/Delete.svg)」 **[!UICONTROL Delete]** 選択して計画を削除します。
1. **[!UICONTROL Delete]** x **[!UICONTROL Delete *計画 *確認ダイアログで「]**」を選択して、計画を削除します。 キャンセルする&#x200B;**[!UICONTROL Cancel]**を選択します。


