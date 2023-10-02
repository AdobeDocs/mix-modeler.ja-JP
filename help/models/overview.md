---
title: モデル
description: Mix Modelerでモデルを設定および使用する方法について説明します。
feature: Models
source-git-commit: 08cfd4239f6bcaf885565f3ae04cbd51869e8c00
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 3%

---


# モデル

Mix Modelerのモデル機能を使用すると、ビジネス目標に特有の AI/ML モデルの設定、トレーニング、スコアリングをおこなえます。また、マルチタッチアトリビューションとマーケティングミックスモデリングの間の AI 駆動型の転送学習に対応します。

モデルは、調和されたデータに基づいており、Mix Modelerの適用ワークフローの一部として作成します。

モデルを作成するには、選択時に使用できる Mix Modeler ステップバイステップのガイド付きモデル設定フローを使用します。 **[!UICONTROL Guide me]**. 詳しくは、 [モデルの作成](create.md) を参照してください。

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
   | データセット | モデルがトレーニングとスコアリングに使用するデータセット。 デフォルトでは、調整済みデータセットです。 |
   | 実行頻度 | モデルのトレーニング実行頻度。 |
   | 前回の実行 | モデルの最後のトレーニングの日時。 |
   | 前回の実行ステータス | モデルのトレーニングの最後の実行のステータス。 <br/><span style="color:green">●</span> 成功<br/><span style="color:orange">●</span> トレーニングの問題<br/> <span style="color:orange">●</span> トレーニング待ち <br/><span style="color:red">●</span> 失敗 |

   {style="table-layout:auto"}

1. リストに表示される列を変更するには、 ![列設定](../assets/icons/ColumnSetting.svg) 列を切り替え ![チェック](../assets/icons/Checkmark.svg) またはオフ。

### モデルの削除

モデルを削除するには：

1. 削除するモデルの名前を選択します。

1. コンテキストメニューから、「 」を選択します。 **[!UICONTROL Delete]** をクリックしてモデルを削除します。

### モデルの詳細の表示

モデルの詳細を表示するには：

1. 詳細を表示するモデルの名前を選択します。

1. コンテキストメニューから、「 」を選択します。 **[!UICONTROL More]**. 選択したモデルの詳細が右側のペインに表示されます。



### モデルインサイト

>[!NOTE]
>
>この選択は、成功したトレーニング済みモデルでのみ使用できます。
>

モデルのインサイトを表示するには、Mix Modelerインターフェイスで次の操作を実行します。

1. 選択 ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** をクリックします。

1. モデルの名前を **[!UICONTROL Last run status]** / <span style="color:green">●</span> **[!UICONTROL Success]** から **[!UICONTROL Models]** 表。

1. コンテキストメニューから、「 」を選択します。 **[!UICONTROL Model Insights]**. 次にリダイレクトされます： [モデルインサイト](insights.md).


