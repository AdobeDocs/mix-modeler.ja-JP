---
title: モデルの作成
description: Mix Modelerでモデルを作成する方法を説明します。
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# モデルの作成

モデルを作成するには、 ![モデル](/help/assets//icons/FileData.svg) **[!UICONTROL Models]** Mix Modelerのインターフェイスで、を選択します **[!UICONTROL Open model canvas]**.

AI を利用したカスタムモデルを作成するために、インターフェイスにはステップバイステップのガイド付きモデル設定フローが用意されています。

1. が含まれる **[!UICONTROL Setup]** 手順：

   1. モデルを入力 **[!UICONTROL Name]**、例： `Demo model`. を入力 **[!UICONTROL Description]**、例： `Demo model to explore AI featues of Mix Modeler`.

      ![モデルの名前と説明](/help/assets//model-name-description.png)

   1. を選択 **[!UICONTROL Next]** をクリックして、次の手順に進みます。 を選択 **[!UICONTROL Cancel]** をクリックして、モデル設定をキャンセルします。

1. が含まれる **[!UICONTROL Configure]** 手順：

   1. が含まれる **[!UICONTROL Conversion goal]** セクションのコンテナ内：

      1. を入力 **[!UICONTROL Conversion name]** 変換用（例：） `Conversion`

      1. コンバージョンを次から選択 **[!UICONTROL *統一フィールドを選択&#x200B;*]**。の一部として定義した使用可能なコンバージョンが含まれます。 [コンバージョン](../harmonize-data/conversions.md) 。対象： [!UICONTROL Harmonized datasets]. 例：**[!UICONTROL Online Conversion]**。

      1. 以下を選択できます。 ![返信](/help/assets//icons/Reply.svg) **[!UICONTROL Create new conversion]** を使用して、モデル設定内から直接コンバージョンを作成します。

         ![モデル – コンバージョンステップ](/help/assets//model-conversion-step.png)

   1. が含まれる **[!UICONTROL Marketing touchpoints]** セクションには、一部として定義したマーケティングタッチポイントに対応する、多数のマーケティングタッチポイントコンテナが表示されます [マーケティングタッチポイント](../harmonize-data/marketing-touchpoints.md) 。対象： [!UICONTROL Harmonized datasets].

      * コンテナごとに、次の手順を実行します。

         1. を変更できます **[!UICONTROL Marketing touchpoint name]**.

         1. 次の中からマーケティングタッチポイントを選択 **[!UICONTROL _マーケティングタッチポイントを選択_]**.

         1. 以下を選択できます。 ![返信](/help/assets//icons/Reply.svg) **[!UICONTROL Create new marketing touchpoint]** モデル設定内から直接マーケティングタッチポイントを作成します。

      * マーケティングタッチポイントコンテナを追加するには、を選択します ![追加](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add marketing touchpoint]**.

      * マーケティングタッチポイントコンテナを削除するには、コンテナ内で、以下を選択します ![詳細](/help/assets//icons/More.svg)を選択し、 **[!UICONTROL Remove container]** コンテキストメニューから。

        ![モデル – マーケティングタッチポイントステップ](/help/assets//model-marketing-touchpoint-step.png)

   1. デフォルトでは、統一ビューのすべてのデータに対してスコアが生成されます。 母集団のサブセットにのみスコアを付けるには、のコンテナを使用して 1 つ以上のフィルターを定義します。 **[!UICONTROL Eligible data population]** セクション。

      * 各コンテナに対して 1 つ以上のイベントを定義します。

         1. 各イベントに対して：

            1. 指標またはディメンションを次から選択 **[!UICONTROL _統一フィールドを選択_]**.

            1. 適切な演算子を選択します。 **[!UICONTROL equals]**, **[!UICONTROL not equals]**, **[!UICONTROL less than]**, **[!UICONTROL greater than]**, **[!UICONTROL starts with]**, **[!UICONTROL doesn't start with]**, **[!UICONTROL ends with]**, **[!UICONTROL doesn't end with]**, **[!UICONTROL contains]**, **[!UICONTROL doesn't contain]**, **[!UICONTROL is in]**、または **[!UICONTROL is not in]**.

            1. で値を入力または選択 **[!UICONTROL _値を入力または選択_]**.

         1. コンテナにイベントを追加するには、以下を選択します ![追加](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add event]**.

         1. コンテナからイベントを削除するには、以下を選択します ![閉じる](/help/assets//icons/Close.svg).

         1. コンテナで定義されたすべてのイベントまたは複数のイベントを使用してフィルタリングするには、以下を選択します。 **[!UICONTROL Any of]** または **[!UICONTROL All of]**. それに応じて、ラベルは次のように変更されます。 **[!UICONTROL Include ... Or ...]** 対象： **[!UICONTROL Include ... And ...]**.

      * 適格なデータ母集団コンテナを追加するには、 ![追加](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add eligible population]**.

      * 適格なデータ母集団コンテナを削除するには、コンテナ内で、 ![詳細](/help/assets//icons/More.svg)を選択し、 **[!UICONTROL Remove marketing touchpoint]** コンテキストメニューから。

        ![モデル – 対象データ母集団](/help/assets//model-eligible-data-population-step.png)

   1. 外部要因を含むデータセットをモデルに追加するには、内の 1 つ以上のコンテナを使用します **[!UICONTROL External factors dataset]** セクション。

      * コンテナごとに、次の手順を実行します。

         1. を入力 **[!UICONTROL Factor name]** 時刻 **[!UICONTROL _係数を入力_]**.

         1. からデータセットを選択 **[!UICONTROL _データセットを選択_]**. 以下を選択できます。 ![データ](/help/assets//icons/Data.svg) でデータセットを管理します。 参照： [データセット](../ingest-data/datasets.md) を参照してください。

      * 外部要因データセットコンテナを追加するには、以下を選択します ![追加](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add external factor]**.

      * 外部要因データセットコンテナを削除するには、コンテナ内で、次を選択します ![詳細](/help/assets//icons/More.svg)を選択し、 **[!UICONTROL Remove external factor]** コンテキストメニューから。

        ![モデル – 外部要因データセット](/help/assets//model-external-factors-dataset-step.png)


   1. 内部要因を含むデータセットをモデルに追加するには、内の 1 つ以上のコンテナを使用します **[!UICONTROL Internal factors dataset]** セクション。

      * コンテナごとに、次の手順を実行します。

         1. を入力 **[!UICONTROL Factor name]** 時刻 **[!UICONTROL _係数を入力_]**.

         1. からデータセットを選択 **[!UICONTROL _データセットを選択_]**. 以下を選択できます。 ![データ](/help/assets//icons/Data.svg) でデータセットを管理します。 参照： [データセット](../ingest-data/datasets.md) を参照してください。

      * 内部要因データセットコンテナを追加するには、以下を選択します ![追加](/help/assets//icons/AddCircle.svg) **[!UICONTROL Add internal factor]**.

      * 追加の内部要因データセットコンテナを削除するには、コンテナ内で、次のオプションを選択します ![詳細](/help/assets//icons/More.svg)、および **[!UICONTROL Remove internal factor]** コンテキストメニューから。

        ![モデル – 内部要因データセット](/help/assets//model-internal-factors-dataset-step.png)

   1. モデルのルックバックウィンドウを定義するには、以下の値を入力します `1` および `52` 。対象： **[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]**.

   1. を選択 **[!UICONTROL Next]** をクリックして、次の手順に進みます。 さらに設定が必要な場合は、赤いアウトラインとテキストで、必要な追加設定を説明します。 <br/>を選択 **[!UICONTROL Back]** 前の手順に戻ります。 <br/>を選択 **[!UICONTROL Cancel]** をクリックして、モデル設定をキャンセルします。

1. が含まれる **[!UICONTROL Advanced]** 手順：

   1. が含まれる **[!UICONTROL Define training window]** セクション、次から選択

      * **[!UICONTROL Have Mix Modeler select a helpful training window]** および

      * **[!UICONTROL Manually input a training window]**。選択した場合、で年数を定義します **[!UICONTROL Include events the following years prior to a conversion]**.

        ![モデル – トレーニングウィンドウを定義](/help/assets//model-define-training-window.png)

   1. が含まれる **[!UICONTROL Spend share]** セクション：

      * マーケティング・データが疎の場合にマーケティング投資比率の履歴を使用してモデルに通知するには、次をアクティブ化します **[!UICONTROL Allow spend share]**.

   1. が含まれる **[!UICONTROL Prior knowledge]** セクション：

      1. 「**[!UICONTROL Rule type]**」を選択します。

      1. の下にリストされているいずれかのチャネルについて、貢献度の割合を指定します。 **[!UICONTROL Name]**、を使用 **[!UICONTROL Contribution proportion]** 列。

      1. 必要に応じて、各チャネルのに **[!UICONTROL Level of confidence]** 割合。

      1. 必要に応じて、を使用します **[!UICONTROL Clear all]** すべての入力値を消去する手順は、次のとおりです： **[!UICONTROL Contribution proportion]** および **[!UICONTROL Level of confidence]** 列。

         ![モデル – 予備知識](/help/assets//model-prior-knowledge-step.png)

1. を選択 **[!UICONTROL Finish]** モデルの設定を完了します。

   * が含まれる **[!UICONTROL Create instance?]** ダイアログ、選択 **[!UICONTROL Ok]** トレーニング実行とスコアリング実行の最初のセットをすぐにトリガーするには： モデルがステータスと共に表示されます <span style="color:orange">●</span> **[!UICONTROL Awaiting training]**。

     を選択 **[!UICONTROL Cancel]** をキャンセルします。

   * さらに設定が必要な場合は、赤いアウトラインとテキストで、必要な追加設定を説明します。

   を選択 **[!UICONTROL Back]** 前の手順に戻ります。

   を選択 **[!UICONTROL Cancel]** をクリックして、モデル設定をキャンセルします。
