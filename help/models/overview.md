---
title: モデル
description: Mix Modeler でモデルを設定して使用する方法をAdobeします。
feature: Models
source-git-commit: ac17f5a9fcf036c8e689879578e4b745b789cea3
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 3%

---


# モデル

Adobeミックスモデラーのモデル機能を使用すると、ビジネス目標に特有の AI/ML モデルを設定、トレーニング、スコアリングでき、マルチタッチアトリビューションとマーケティングミックスモデリングの間の AI 駆動型の転送学習に対応できます。

モデルは、Mix Modeler アプリケーションワークフローの一部として作成した調整済みAdobeに基づいています。

モデルを作成するには、選択時に使用できる Mix Modeler ステップバイステップのガイド付きモデル設定フローを使用します。 **[!UICONTROL Guide me]**. 詳しくは、 [モデルの作成](create.md) を参照してください。

## モデルの管理

現在のモデルのテーブルを表示するには、AdobeMix Modeler インタフェースで次の手順を実行します。

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
>この選択は、成功したトレーニング済みモデル（前回の実行ステータスが「成功」のモデル）でのみ使用できます。
>

モデルのインサイトを表示するには、AdobeMix Modeler インタフェースで次の操作を行います。

1. 選択 ![](../assets/icons/FileData.svg) **[!UICONTROL Models]** をクリックします。

1. モデルの名前を **[!UICONTROL Last run status]** / <span style="color:green">●</span> **[!UICONTROL Success]** から **[!UICONTROL Models]** 表

1. コンテキストメニューから、「 」を選択します。 **[!UICONTROL Model Insights]**. 次にリダイレクトされます： [モデルインサイト](insights.md).


