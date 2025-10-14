---
title: モデルを作成
description: Mix Modelerでモデルを構築する方法を説明します。
feature: Models
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: b08a24856e28a1377728bc2c511f6ea483cbd0fd
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# モデルを作成

AI を利用したカスタムモデルを作成するために、インターフェイスにはステップバイステップのガイド付きモデル設定フローが用意されています。

Mix Modelerの ![&#x200B; モデル &#x200B;](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** インターフェイスで、「**[!UICONTROL Open model canvas]**」を選択します。

## セットアップ

**[!UICONTROL Setup]** の手順で、名前と説明を定義します。

1. モデル **[!UICONTROL Name]** （例：`Demo model`）を入力します。 **[!UICONTROL Description]** （例：`Demo model to explore AI featues of Mix Modeler`）を入力します。

   ![&#x200B; モデルの名前と説明 &#x200B;](/help/assets/model-name-description.png)

1. 「**[!UICONTROL Next]**」を選択して、次の手順に進みます。 モデル設定をキャンセルするには、「**[!UICONTROL Cancel]**」を選択します。

## 設定

モデルは **[!UICONTROL Configure]** の手順で設定します。 設定には、コンバージョン目標、マーケティングタッチポイント、適格なデータ母集団、外部要因と内部要因などの定義が含まれます。

1. **[!UICONTROL Conversion goal]** のセクションで以下を実行します。

   ![&#x200B; モデル – コンバージョンステップ &#x200B;](/help/assets/model-conversion-step.png)

   1. コンバージョンをコンバージョ **[!UICONTROL Conversion]** ドロップダウンメニューから選択します。 使用可能なコンバージョンは、[!UICONTROL Harmonized datasets] で [&#x200B; コンバージョン &#x200B;](../harmonize-data/conversions.md) の一部として定義したコンバージョンです。 例：**[!UICONTROL Online Conversion]**。

   1. ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a conversion]** を選択して、モデル設定内から直接変換を作成できます。



1. **[!UICONTROL Marketing touchpoints]** セクションでは、[!UICONTROL Harmonized datasets] で [&#x200B; マーケティングタッチポイント &#x200B;](../harmonize-data/marketing-touchpoints.md) の一部として定義したマーケティングタッチポイントに対応する 1 つ以上のマーケティングタッチポイントを選択できます。


   ![&#x200B; モデル – マーケティングタッチポイントステップ &#x200B;](/help/assets/model-marketing-touchpoint-step.png)

   1. **[!UICONTROL Touchpoint include]** ドロップダウンメニューからマーケティングタッチポイントを 1 つ以上選択します。

      * ![CrossSize75](/help/assets/icons/CrossSize75.svg) を使用して、タッチポイントを削除できます。
      * **[!UICONTROL Clear all]** を使用して、すべてのタッチポイントを削除できます。

   1. ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a touchpoint]** を選択して、モデル設定内から直接マーケティングタッチポイントを作成できます。

   >[!NOTE]
   >
   >データが重複しているタッチポイントを含むモデルは設定できません。また、費用を含むタッチポイントが少なくとも 1 つ必要です。

1. デフォルトでは、統一ビューのすべてのデータに対してスコアが生成されます。 母集団のサブセットにのみスコアを付けるには、「**[!UICONTROL Eligible data population]**」セクションのコンテナを使用して 1 つ以上のフィルターを定義します。

   ![&#x200B; モデル – 適格なデータ母集団 &#x200B;](/help/assets/model-eligible-data-population-step.png)

   * 各コンテナに対して 1 つ以上のイベントを定義します。

      1. 各イベントに対して：

         1. **[!UICONTROL _統一フィールドを選択_]** から指標またはディメンションを選択します。

         1. 適切な演算子（**[!UICONTROL equals]**、**[!UICONTROL not equals]**、**[!UICONTROL less than]**、**[!UICONTROL greater than]**、**[!UICONTROL starts with]**、**[!UICONTROL doesn't start with]**、**[!UICONTROL ends with]**、**[!UICONTROL doesn't end with]**、**[!UICONTROL contains]**、**[!UICONTROL doesn't contain]**、**[!UICONTROL is in]** または **[!UICONTROL is not in]**）を選択します。

         1. **[!UICONTROL _値を入力または選択_]** で値を入力または選択します。

      1. コンテナにイベントを追加するには、「![&#x200B; 追加 &#x200B;](/help/assets/icons/AddCircle.svg)」を選択し **[!UICONTROL Add event]** す。

      1. コンテナからイベントを削除するには、「![&#x200B; 閉じる &#x200B;](/help/assets/icons/CrossSize75.svg) を選択します。

      1. コンテナで定義したすべてのイベントまたは複数のイベントを使用してフィルタリングするには、「**[!UICONTROL Any of]**」または「**[!UICONTROL All of]**」を選択します。 それに応じて、ラベルが **[!UICONTROL Include ... Or ...]** から **[!UICONTROL Include ... And ...]** に変更されます。

   * 適格なデータ母集団コンテナを追加するには、「![&#x200B; 追加 &#x200B;](/help/assets/icons/AddCircle.svg)」 **[!UICONTROL Add eligible population]** を選択します。

   * 適格なデータ母集団コンテナを削除するには、コンテナ内で ![&#x200B; 詳細 &#x200B;](/help/assets/icons/More.svg) を選択し、コンテキストメニューから「**[!UICONTROL Remove marketing touchpoint]**」を選択します。

   * コンテナ間で **AND** および **OR** を選択し、適格なデータ母集団に対してより複雑な定義を作成します。


1. 外部要因を含むデータセットをモデルに追加するには、「**[!UICONTROL External factors dataset]**」セクションの 1 つ以上のコンテナを使用します。 外部要因の例としては、S&amp;P インデックスがあります。

   ![&#x200B; モデル – 外部要因データセット &#x200B;](/help/assets/model-external-factors-dataset-step.png)

   * コンテナごとに、次の手順を実行します。

      1. **[!UICONTROL External factor name]** （例：`External Factors`）を入力します。

      1. **[!UICONTROL Dataset]** ドロップダウンメニューからデータセットを選択します。 ![&#x200B; データ &#x200B;](/help/assets/icons/Data.svg) を選択して、データセットを管理できます。 詳しくは、[&#x200B; データセット &#x200B;](../ingest-data/datasets.md) を参照してください。

      1. **[!UICONTROL Impact on conversion]** ドロップダウンメニューからオプション（**[!UICONTROL Auto select]**、**[!UICONTROL Positive]**、**[!UICONTROL Negative]** のいずれか）を選択します。 デフォルトのオプションは **[!UICONTROL Auto select]** です。このオプションを使用すると、モデルが影響を判断できます。 デフォルトの設定は上書きできます。

   * 追加の外部要因データセットコンテナを追加するには、「![&#x200B; 追加 &#x200B;](/help/assets/icons/AddCircle.svg)」 **[!UICONTROL Add external factor]** プションを選択します。

   * 外部要因データセットコンテナを削除するには、「![RemoveCircle](/help/assets/icons/RemoveCircle.svg)」を選択します。




1. 内部要因を含むデータセットをモデルに追加するには、「**[!UICONTROL Internal factors dataset]**」セクションの 1 つ以上のコンテナを使用します。 内部要因の例としては、メールマーケティングデータがあります。

   ![&#x200B; モデル – 内部要因データセット &#x200B;](/help/assets/model-internal-factors-dataset-step.png)

   * コンテナごとに、次の手順を実行します。

      1. **[!UICONTROL Internal factor name]** （例：`Email Marketing Data`）を入力します。

      1. **[!UICONTROL _データセットを選択_]** からデータセットを選択します。 ![&#x200B; データ &#x200B;](/help/assets/icons/Data.svg) を選択して、データセットを管理できます。 詳しくは、[&#x200B; データセット &#x200B;](../ingest-data/datasets.md) を参照してください。

      1. **[!UICONTROL Impact on conversion]** ドロップダウンメニューからオプション（**[!UICONTROL Auto select]**、**[!UICONTROL Positive]**、**[!UICONTROL Negative]** のいずれか）を選択します。

   * 内部要因データセットコンテナを追加するには、「![&#x200B; 追加 &#x200B;](/help/assets/icons/AddCircle.svg)」 **[!UICONTROL Add internal factor]** プションを選択します。

   * 内部要因データセットコンテナを削除するには、「![RemoveCircle](/help/assets/icons/RemoveCircle.svg)」を選択します。



1. モデルのルックバックウィンドウを定義するには、... **[!UICONTROL weeks prior to the conversion]** ードに `1` ～ `52` の値 **[!UICONTROL Give contribution credit to touchpoints occurring within]** 入力します。

1. 「**[!UICONTROL Next]**」を選択して、次の手順に進みます。 さらに設定が必要な場合は、赤いアウトラインとテキストで、必要な追加設定を説明します。 <br/> 「**[!UICONTROL Back]**」を選択して前の手順に戻ります。 <br/> 「**[!UICONTROL Cancel]**」を選択すると、モデル設定がキャンセルされます。


## アドバンス

詳細設定は、**[!UICONTROL Advanced]** の手順で指定できます。 この手順では、モデルをマルチタッチアトリビューション（MTA）に対して有効にできます。

1. **[!UICONTROL Spend share]** のセクションで以下を実行します。

   * マーケティングデータが分散している場合にマーケティング投資率の履歴を使用してモデルに通知するには、**[!UICONTROL Allow spend share]** をアクティブ化します。 この設定は、特に次のシナリオで推奨されます。
      * チャネルに十分な観測がありません（例：低い支出頻度、インプレッション数、クリック数）。
      * データがスパースな可能性のある、スパイキーだが通常の、そして潜在的に高価なメディア（一部のブランドのテレビなど）をモデリングしている場合。

     >[!NOTE]
     >
     >1 回限りの投資（スーパーボウル広告など）の場合は、支出配分に依存するのではなく、要因としてそのデータを取り込むことを検討します。
     >


1. **[!UICONTROL MTA enabled]** のセクションで以下を実行します。

   * モデルの MTA 機能を有効にするには、**[!UICONTROL MTA enabled]** をアクティブにします。 MTA を有効にしている場合は、モデルのトレーニングとスコアリングが完了すると、マルチタッチのアトリビューションインサイトを利用できます。 詳しくは、[&#x200B; モデルインサイト &#x200B;](insights.md#attribution) の「[&#x200B; アトリビューション &#x200B;](insights.md)」タブを参照してください。

1. **[!UICONTROL Prior knowledge]** のセクションで以下を実行します。

   ![&#x200B; モデル – 予備知識 &#x200B;](/help/assets/model-prior-knowledge-step.png)

   1. **[!UICONTROL Rule type]** （デフォルトは **[!UICONTROL Absolute values]**）を選択します。

   1. **[!UICONTROL Contribution proportion]** 列を使用して、**[!UICONTROL Name]** の下にリストされているすべてのチャネルの貢献度の割合を指定します。

   1. 必要に応じて、各チャネルに **[!UICONTROL Level of confidence]** の割合を追加できます。

   1. 必要に応じて、**[!UICONTROL Clear all]** を使用して、**[!UICONTROL Contribution proportion]** 列と **[!UICONTROL Level of confidence]** 列のすべての入力値をクリアします。


## スケジュール

**[!UICONTROL Schedule]** の手順で、モデルのトレーニングとスコアリングのスケジュールを設定できます。

1. **[!UICONTROL Schedule]** のセクションでは、モデルのトレーニングとスコアリングをスケジュールできます。

   ![&#x200B; スケジュール モデル &#x200B;](../assets/model-schedule.png)

   スケジュール済モデルのスコアリングおよびトレーニングを実行する手順は、次のとおりです。

   1. **[!UICONTROL Enable scheduled model scoring and training]** をオンにします。
   1. **[!UICONTROL Scoring frequency]** を選択：

      * **[!UICONTROL Daily]**：有効な時間（例：`05:22 pm`）を入力するか、![Clock](/help/assets/icons/Clock.svg) を使用します。
      * **[!UICONTROL Weekly]**：曜日を選択して有効な時間（例：`05:22 pm`）を入力するか、![Clock](/help/assets/icons/Clock.svg) を使用します。
      * **[!UICONTROL Monthly]**: 「実行するタイミング」ドロップダウンメニューから日付を選択し、有効な時刻（例：`05:22 pm`）を入力するか、![&#x200B; 時計 &#x200B;](/help/assets/icons/Clock.svg) を使用します。

   1. ドロップダウンメニューから **[!UICONTROL Training frequency]** （**[!UICONTROL Monthly]**、**[!UICONTROL Quarterly]**、**[!UICONTROL Yearly]**、**[!UICONTROL None]** のいずれか）を選択します。

1. **[!UICONTROL Define training window]** のセクションで、次のいずれかを選択します。

   ![&#x200B; モデル – トレーニングウィンドウを定義 &#x200B;](/help/assets/model-define-training-window.png)

   * **[!UICONTROL Have Mix Modeler select a helpful training window]** と

   * **[!UICONTROL Manually input a training window]**。選択した場合、年 **[!UICONTROL Include events the following years prior to a conversion]** を定義します。


1. 「**[!UICONTROL Finish]**」を選択して、モデルの設定を完了します。

   * **[!UICONTROL Create instance?]** ダイアログで、「**[!UICONTROL Ok]**」を選択して、トレーニング実行とスコアリング実行の最初のセットをすぐにトリガーにします。 モデルがステータス ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]** で表示されます。

     キャンセルする **[!UICONTROL Cancel]** を選択します。

   * さらに設定が必要な場合は、赤いアウトラインとテキストで、必要な追加設定を説明します。

   「**[!UICONTROL Back]**」を選択して前の手順に戻ります。

   モデル設定をキャンセルするには、「**[!UICONTROL Cancel]**」を選択します。
