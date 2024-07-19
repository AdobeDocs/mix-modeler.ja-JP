---
title: モデル
description: Mix Modelerでモデルを設定および使用する方法を説明します。
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 1%

---

# モデル

Mix Modelerのモデル機能を使用すると、ビジネス目標に固有の AI/ML モデルの設定、トレーニング、スコアリングを行えます。また、マルチタッチアトリビューションとマーケティングミックスモデリングの間で、AI 駆動のトランスファーラーニングによってサポートされます。

モデルは、Mix Modelerアプリケーションワークフローの一部として作成する統一データに基づいています。

Mix Modelerのモデルは、マーケターの投資に基づいて指定された成果を測定および/または予測するために使用される機械学習モデルです。 マーケティングタッチポイントおよび概要レベルデータを入力として使用できます。 Mix Modelerを使用すると、売上高、販売数量、リードなど、変数、ディメンション、結果の様々なセットに基づいてモデルのバリアントを作成できます。

モデルには次の要件があります。

* 1 つのコンバージョン、
* 概要レベルデータ、マーケティングタッチポイントデータ（イベントデータ）またはその両方で構成された 1 つ以上のマーケティングタッチポイント（チャネル）
* の設定可能なルックバックウィンドウ
* 設定可能なトレーニングウィンドウ。

モデルには、オプションで次の項目を含めることができます。

* 外部要因、
* 内部要因、
* いわゆる「優先値」（データの観測前または観測前のデータに関する知識または不確実性を表す確率分布）で、チャネル別の以前のコンバージョンをインデックス化します。
* 支出共有：マーケティングデータが疎な場合に、相対的な支出共有をプロキシとして使用します。


## モデルの作成

モデルを作成するには、「**[!UICONTROL Open model canvas]**」を選択すると使用できるMix Modelerステップバイステップのガイド付きモデル設定フローを使用します。 詳しくは、[ モデルの作成 ](create.md) を参照してください。

## モデルの管理

Mix Modelerインターフェイスで現在のモデルのテーブルを表示するには：

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. 現在のモデルのテーブルが表示されます。

   テーブルの列には、モデルに関する詳細が指定されます。

   | 列名 | 詳細 |
   |---|---|
   | 名前 | モデル名 |
   | 説明 | モデルの説明 |
   | コンバージョンイベント | モデルに対して選択した変換。 |
   | 実行頻度 | モデルをトレーニングする実行頻度。 |
   | 前回の実行 | モデルの最後のトレーニングの日時。 |
   | ステータス | モデルのトレーニングの前回の実行ステータス。 <br/><span style="color:green">●</span> Success<br/><span style="color:orange">●</span> Training の問題 <br/> <span style="color:orange">●</span> トレーニングを待機中 <br/><span style="color:red">●</span> 失敗 <br/><span style="color:gray">●</span> _ （前回の実行が進行中の場合） |

   {style="table-layout:auto"}

1. リストに表示される列を変更するには、「![ 列設定 ](/help/assets//icons/ColumnSetting.svg) を選択し、列のオン ![ チェック ](/help/assets//icons/Checkmark.svg) とオフを切り替えます。


### モデルの詳細の表示

モデルの詳細を表示するには：

1. モデルの ![ 情報 ](/help/assets//icons/Info.svg) を選択して、詳細を含むポップアップを表示します。



### モデルインサイト

Mix Modelerインターフェイスでモデルのインサイトを表示するには：

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. **[!UICONTROL Last run status]** が <span style="color:green">●</span> のモデル名を選択します **[!UICONTROL Models]** テーブルから **[!UICONTROL Success]** します。 モデルインサイトは、正常にトレーニングされたモデルでのみ使用できます。

1. コンテキストメニューから「**[!UICONTROL Model Insights]**」を選択します。 [ モデルインサイト ](insights.md) にリダイレクトされます。


### 再スコア


Mix Modelerインターフェイスでモデルのスコアを変更するには：

1. 左パネルから ![](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. **[!UICONTROL Last run status]** が <span style="color:green">●</span> のモデル名を選択します **[!UICONTROL Models]** テーブルから **[!UICONTROL Success]** します。 再スコアは、正常にトレーニングされたモデルでのみ使用できます。

1. コンテキストメニューから「**[!UICONTROL Re-score]**」を選択します。 モデルの更新されたステータスが表示されるまで数分かかる場合があります。


### モデルの削除

モデルを削除するには：

1. 削除するモデルの名前を選択します。

1. 右クリック メニューから、[**[!UICONTROL Delete]**] を選択してモデルを削除します。

   >[!WARNING]
   >
   >モデルはすぐに削除されます。


