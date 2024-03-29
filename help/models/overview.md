---
title: モデル
description: Mix Modelerでモデルを設定および使用する方法について説明します。
feature: Models
exl-id: c43d9bc9-4429-45c2-9247-bd24510a24be
source-git-commit: 86732fe30637aa72ced232d9f331a3cc64baa39b
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 1%

---

# モデル

Mix Modelerのモデル機能を使用すると、ビジネス目標に特有の AI/ML モデルの設定、トレーニング、スコアリングをおこなえます。また、マルチタッチアトリビューションとマーケティングミックスモデリングの間の AI 駆動型の転送学習に対応します。

モデルは、調和されたデータに基づいており、Mix Modelerの適用ワークフローの一部として作成します。

Mix Modelerのモデルとは、マーケターの投資に基づいて特定の結果を測定/予測するために採用される機械学習モデルです。 マーケティングタッチポイントとサマリレベルのデータを入力として使用できます。 Mix Modelerでは、売上高、販売数量、リードなど、様々な変数、ディメンション、結果のセットに基づいてモデルのバリエーションを作成できます。

モデルには以下が必要です。

* 1 回のコンバージョン
* 概要レベルのデータ、マーケティングタッチポイントデータ（イベントデータ）またはその両方で構成される、1 つ以上のマーケティングタッチポイント（チャネル）
* 設定可能なルックバックウィンドウ
* 設定可能なトレーニング期間。

モデルには、オプションで以下を含めることができます。

* 外部要因
* 内部要因
* いわゆる「プリア」（データを観察する前または前にデータの知識または不確実性を表す確率分布）で、チャネル別に事前のコンバージョンのインデックスを作成します。
* 支出共有。マーケティングデータが少ない場合に、相対的な支出の共有をプロキシとして使用します。


## モデルの作成

モデルを作成するには、「 」Mix Modelerで「ステップバイステップ」のガイド付きモデル設定フローを使用します。 **[!UICONTROL Open model canvas]**. 詳しくは、 [モデルの作成](create.md) を参照してください。

## モデルの管理

現在のモデルの表を表示するには、Mix Modeler・インタフェースで次の手順に従います。

1. 選択 ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** をクリックします。

1. 現在のモデルの表が表示されます。

   テーブルの列は、モデルの詳細を指定します。

   | 列名 | 詳細 |
   |---|---|
   | 名前 | モデルの名前 |
   | 説明 | モデルの説明 |
   | コンバージョンイベント | モデルに対して選択した変換。 |
   | 実行頻度 | モデルのトレーニング実行頻度。 |
   | 前回の実行 | モデルの最後のトレーニングの日時。 |
   | ステータス | モデルのトレーニングの最後の実行のステータス。 <br/><span style="color:green">●</span> 成功<br/><span style="color:orange">●</span> トレーニングの問題<br/> <span style="color:orange">●</span> トレーニング待ち <br/><span style="color:red">●</span> 失敗 <br/><span style="color:gray">●</span> _ （最後の実行が進行中の場合） |

   {style="table-layout:auto"}

1. リストに表示される列を変更するには、 ![列設定](../assets/icons/ColumnSetting.svg) 列を切り替え ![チェック](../assets/icons/Checkmark.svg) またはオフ。


### モデルの詳細の表示

モデルの詳細を表示するには：

1. 選択 ![情報](../assets/icons/Info.svg) モデルが詳細と共にポップアップを表示するために使用します。



### モデルインサイト

モデルのインサイトを表示するには、Mix Modelerインターフェイスで次の操作を実行します。

1. 選択 ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** をクリックします。

1. モデルの名前を **[!UICONTROL Last run status]** / <span style="color:green">●</span> **[!UICONTROL Success]** から **[!UICONTROL Models]** 表。 モデルインサイトは、正常にトレーニングされたモデルでのみ使用できます。

1. コンテキストメニューから、「 」を選択します。 **[!UICONTROL Model Insights]**. 次にリダイレクトされます： [モデルインサイト](insights.md).


### 再スコア


モデルのスコアを再設定するには、Mix Modelerインターフェイスで次の手順を実行します。

1. 選択 ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** をクリックします。

1. モデルの名前を **[!UICONTROL Last run status]** / <span style="color:green">●</span> **[!UICONTROL Success]** から **[!UICONTROL Models]** 表。 再スコアリングは、正常にトレーニングされたモデルでのみ使用できます。

1. コンテキストメニューから、「 」を選択します。 **[!UICONTROL Re-score]**. モデルのステータスが更新されるまでに数分かかる場合があります。


### モデルの削除

モデルを削除するには：

1. 削除するモデルの名前を選択します。

1. コンテキストメニューから、「 」を選択します。 **[!UICONTROL Delete]** をクリックしてモデルを削除します。

   >[!WARNING]
   >
   >モデルは直ちに削除されます。


