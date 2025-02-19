---
title: 計画の概要
description: Mix Modelerでプランを表示、選択およびアクションする方法を説明します。
feature: Plans
exl-id: 45a8dc30-3259-493d-8ea5-1899903733a6
source-git-commit: 8e1c748f3e4e267038dcac5bce82f90157e88c32
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 1%

---

# 計画の概要

Mix Modelerのプランを使用すると、ビジネスユニットおよびチャネル別に予算を割り当てることができます。 計画機能は、統一されたデータに基づいて、トレーニング済みモデルの結果と統合されます。

プランは、一般的な KPI のサービスにおける特定の期間（注文、収益など）にわたって、ビジネスがマーケティング関連プロジェクトに費やそうとする自由裁量の投資（予算など）の概要を示します。 プランには、有料広告、スポンサー付き web コンテンツ、イベントなどのチャネルからの費用が含まれる場合があります。

プランには次が必要です。

- モデル、
- データ範囲
- 予算。

計画には、オプションで次の項目を含めることができます。

- 設定済みの認識ウィンドウ、
- 複数のフライト日（それぞれに目標予算がある）
- チャネルおよびフライト日ごとの最小予算制約と最大予算制約。

プランに使用したモデルが新しいデータでスコアリングされている場合、スコアリングされ直したデータを考慮して新しいプランを作成する必要があります。


## プランの作成

プランを作成するには、Mix Modeler プラン作成ウィザードを使用します。 詳しくは、[ プランの作成 ](build.md) を参照してください。

## プランの管理

Mix Modeler インターフェイスで現在の計画のテーブルを表示するには、次の手順を実行します。

1. 左パネルから ![](/help/assets/icons/FileChart.svg) **[!UICONTROL Plans]** を選択します。

1. 現在のプランとそのステータスのテーブルが表示されます。

   表の列には、計画の詳細が示されます。

   | 列名 | 詳細 |
   |---|---|
   | 名前 | プランの名前 |
   | モデル | プランのベースとして使用されるモデル。 |
   | 日付範囲 | プランの完全な日付範囲。 |
   | 予算 | 計画の予算合計。 |
   | 予測リターン | 計画の予測リターン |
   | 予測 ROI | プランの予測 ROI。 |
   | 予測コンバージョン | プランの予測コンバージョン |
   | 予測 CPA | プランの予測 CPA |
   | ステータス | プランのステータス： <p><span style="color:red">●</span> 失敗しました。 <p><span style="color:blue">●</span> 処理、 <p><span style="color:green">●</span> 完了しました。 |

   {style="table-layout:auto"}

   ![ColumnSetting](/help/assets/icons/ColumnSetting.svg) を使用して ![Checkmark](/help/assets/icons/Checkmark.svg) を選択すると、テーブルに表示する列を選択できます。

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

元の計画名に **[!UICONTROL (Copy)]（_n_）** を付けた名前の新規計画が表の上部に追加されます。

### 計画の比較

計画を比較する手順は、次のとおりです。

1. テーブルから 2 つのプランを選択します。
1. 青いアクションバーから ![ 比較 ](/help/assets/icons/Compare.svg)**[!UICONTROL Compare]** を選択します。 **[!UICONTROL Compare plans]** UI が表示されます。


### 計画の削除

計画を削除する手順は、次のとおりです。

1. プランの ![ 詳細 ](/help/assets/icons/More.svg) を選択します。 コンテキストメニューから「**[!UICONTROL Delete]**」を選択します。 <br/> または、テーブルの ![ 選択ボックス ](/help/assets/icons/SelectBox.svg) でプランを選択し、青いアクションバーから ![ 削除 ](/help/assets/icons/Delete.svg)**[!UICONTROL Delete]** を選択します。
1. **[!UICONTROL Delete plan]** の確認ダイアログで「**[!UICONTROL Delete]**」を選択して、計画を削除します。 キャンセルする **[!UICONTROL Cancel]** を選択します。

複数の計画を削除する手順は、次のとおりです。

1. 複数の計画を選択します。
1. 青いアクションバーから、「![ 削除 ](/help/assets/icons/Delete.svg)」 **[!UICONTROL Delete]** 選択して計画を削除します。
1. **[!UICONTROL Delete *x *計画]**確認ダイアログで「**[!UICONTROL Delete]**」を選択して、計画を削除します。 キャンセルする&#x200B;**[!UICONTROL Cancel]**を選択します。


