---
title: Mix Modelerでのモデルの構築
description: モデルの高度なオプションを設定、設定、指定する方法など、Mix Modelerでモデルを構築する方法を説明します。 Adobe Workfrontの導入をサポートします。
feature: Models
solution: Mix Modeler
exl-id: e1093c09-1e23-460b-92de-cfb0061112fd
source-git-commit: dd7a7260464b27b8ef257004b1c2a64d70ffe122
workflow-type: tm+mt
source-wordcount: '1557'
ht-degree: 0%

---

# モデルを構築

AIを活用したカスタムモデルを構築するために、インターフェイスにはステップバイステップのガイド付きモデル設定フローが用意されています。

[!DNL Mix Modeler]の![&#x200B; モデル &#x200B;](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** インターフェイスで、**[!UICONTROL Open model canvas]**&#x200B;を選択します。

## セットアップ

**[!UICONTROL Setup]** ステップで名前と説明を定義します。

1. モデル **[!UICONTROL Name]**&#x200B;を入力します（例：`Demo model`）。 **[!UICONTROL Description]**&#x200B;を入力します（例：`Demo model to explore AI features of Mix Modeler`）。

   ![&#x200B; モデル名と説明](/help/assets/model-name-description.png)

1. **[!UICONTROL Next]**&#x200B;を選択して次の手順に進みます。 モデル設定をキャンセルするには、**[!UICONTROL Cancel]**&#x200B;を選択します。

## 設定 {#configure}

>[!CONTEXTUALHELP]
>id="model_marketingtouchpoints_select"
>title="マーケティングタッチポイント"
>abstract="マーケティングのタッチポイントは、受信者、個人、またはCookie レベルのマーケティングイベントで、マーケティング投資が数値または収益ベースのコンバージョンに与える影響を評価するために使用されます。<br/><br/>重複するデータを持つタッチポイントでモデルを設定することはできず、支出を伴うタッチポイントが少なくとも1つ必要です。"


モデルは&#x200B;**[!UICONTROL Configure]** ステップで設定します。 コンバージョンの目標、マーケティング接点、適格なデータ母集団、外部要因および内部要因などの定義を設定できます。

1. **[!UICONTROL Conversion goal]** セクション：

   ![&#x200B; モデル – コンバージョンステップ &#x200B;](/help/assets/model-conversion-step.png)

   1. **[!UICONTROL Conversion]** ドロップダウンメニューからコンバージョンを選択します。 使用可能なコンバージョンは、[!UICONTROL Harmonized datasets]の[&#x200B; コンバージョン &#x200B;](../harmonize-data/conversions.md)の一部として定義したコンバージョンです。 例：**[!UICONTROL Online Conversion]**。

   1. ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a conversion]**&#x200B;を選択して、モデル設定内から直接コンバージョンを作成できます。



1. **[!UICONTROL Marketing touchpoints]** セクションでは、[!UICONTROL Harmonized datasets]の[&#x200B; マーケティング タッチポイント &#x200B;](../harmonize-data/marketing-touchpoints.md)の一部として定義したマーケティング タッチポイントに対応する1つ以上のマーケティング タッチポイントを選択できます。


   ![&#x200B; モデル – マーケティング タッチポイント ステップ &#x200B;](/help/assets/model-marketing-touchpoint-step.png)

   1. **[!UICONTROL Touchpoint include]** ドロップダウンメニューから1つ以上のマーケティングのタッチポイントを選択します。

      * ![CrossSize75](/help/assets/icons/CrossSize75.svg)を使用して、タッチポイントを削除できます。
      * **[!UICONTROL Clear all]**&#x200B;を使用して、すべてのタッチポイントを削除できます。

   1. ![LinkOutLight](/help/assets/icons/LinkOutLight.svg) **[!UICONTROL Create a touchpoint]**&#x200B;を選択して、モデル設定内から直接マーケティングタッチポイントを作成できます。

   >[!NOTE]
   >
   >重複するデータを持つタッチポイントを使用してモデルを設定することはできず、支出を含むタッチポイントが少なくとも1つ必要です。

1. デフォルトでは、調和ビューのすべてのデータに対してスコアが生成されます。 母集団のサブセットのみをスコアリングするには、**[!UICONTROL Eligible data population]** セクションのコンテナを使用して1つ以上のフィルターを定義します。

   ![&#x200B; モデル – 対象となるデータ母集団](/help/assets/model-eligible-data-population-step.png)

   * 各コンテナについて、1つ以上のイベントを定義します。

      1. 各イベントについて：

         1. **[!UICONTROL _調和フィールド_]**&#x200B;から指標またはディメンションを選択します。

         1. 適切な演算子を選択：**[!UICONTROL equals]**、**[!UICONTROL not equals]**、**[!UICONTROL less than]**、**[!UICONTROL greater than]**、**[!UICONTROL starts with]**、**[!UICONTROL doesn't start with]**、**[!UICONTROL ends with]**、**[!UICONTROL doesn't end with]**、**[!UICONTROL contains]**、**[!UICONTROL doesn't contain]**、**[!UICONTROL is in]**&#x200B;または&#x200B;**[!UICONTROL is not in]**。

         1. 値を&#x200B;**[!UICONTROL _に入力するか、値を選択します。値を入力するか、値を選択します_]**。

      1. コンテナに追加のイベントを追加するには、![追加](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add event]**&#x200B;を選択します。

      1. コンテナからイベントを削除するには、![閉じる](/help/assets/icons/CrossSize75.svg)を選択します。

      1. コンテナで定義されている複数のイベントのすべてまたは任意のイベントを使用してフィルタリングするには、**[!UICONTROL Any of]**&#x200B;または&#x200B;**[!UICONTROL All of]**&#x200B;を選択します。 ラベルが&#x200B;**[!UICONTROL Include ... Or ...]**&#x200B;から&#x200B;**[!UICONTROL Include ... And ...]**&#x200B;に対応して変更されます。

   * 適格なデータ母集団コンテナを追加するには、![追加](/help/assets/icons/AddCircle.svg) **[!UICONTROL Add eligible population]**&#x200B;を選択します。

   * 適格なデータ母集団コンテナを削除するには、コンテナ内で![More](/help/assets/icons/More.svg)を選択し、コンテキストメニューから&#x200B;**[!UICONTROL Remove container]**&#x200B;を選択します。

   * コンテナ間で&#x200B;**And**&#x200B;と&#x200B;**Or**&#x200B;を選択して、対象となるデータ母集団に対するより複雑な定義を構築します。

1. 内部要因または外部要因を含むデータセットは、**[!UICONTROL Factor dataset]** セクションで管理できます。

   ![&#x200B; モデル – 因子データセット ステップ &#x200B;](../assets/model-factors-dataset-step.png)

   * 因子データセットを追加するには、**[!UICONTROL Add Factor]**&#x200B;を選択します。 モデルには最大30個の要素を追加できます。

      1. ドロップダウンメニューから&#x200B;**[!UICONTROL Factor dataset]**&#x200B;を選択します。 使用可能な要因は、[&#x200B; データセット ルール &#x200B;](/help/harmonize-data/dataset-rules.md#create-a-dataset-rule)で調和フィールドを定義した要因です。
選択したデータセットに基づいて、**[!UICONTROL Factor type]**&#x200B;は&#x200B;**[!UICONTROL Internal]**&#x200B;または&#x200B;**[!UICONTROL External]**&#x200B;です。

      1. ドロップダウンメニューから&#x200B;**[!UICONTROL Impact on conversion]**&#x200B;を選択します。 利用できるオプションは&#x200B;**[!UICONTROL Auto]**、**[!UICONTROL Positive]**&#x200B;または&#x200B;**[!UICONTROL Negative]**&#x200B;です。 デフォルトのオプションは&#x200B;**[!UICONTROL Auto]**&#x200B;です。これにより、モデルは因子データセットの影響を判断できます。

   * 因子データセットを削除するには、![CrossSize200](/help/assets/icons/CrossSize400.svg)を選択します。


1. モデルのルックバックウィンドウを定義するには、**[!UICONTROL Define lookback window]** セクションの&#x200B;**[!UICONTROL Give contribution credit to touchpoints occurring within]** ... **[!UICONTROL weeks prior to the conversion]**&#x200B;に`1`から`52`までの値を入力します。

1. モデルのトレーニングウィンドウを定義するには、**[!UICONTROL Define training window]**&#x200B;で、コンバージョンのスコアリングを開始する場所を選択します。

   ![&#x200B; モデル – トレーニングウィンドウを定義](/help/assets/model-define-training-window.png)

   次のいずれかを選択できます。

   * **[!UICONTROL Have Mix Modeler select a helpful training window]**&#x200B;および

   * **[!UICONTROL Manually input a training window]**. 選択すると、**[!UICONTROL Include events the following years prior to a conversion]**&#x200B;の年数を定義します。

   この入力はモデルに必要です。 **[!UICONTROL Advanced]** ステップで設定できるチャネル アドストックの上限を設定する年数です。

1. **[!UICONTROL Next]**&#x200B;を選択して次の手順に進みます。 追加の設定が必要な場合は、赤いアウトラインとテキストで、追加の設定が必要な内容を説明します。<br/>**[!UICONTROL Back]**&#x200B;を選択して、前の手順に戻ります。<br/>モデル設定をキャンセルするには、**[!UICONTROL Cancel]**&#x200B;を選択します。


## アドバンス {#advanced}

>[!CONTEXTUALHELP]
>id="model_advanced_channeladstock"
>title="Channel adstock"
>abstract="ドメインの専門知識、実験結果、または以前のチャネル分析をモデル設定に直接組み込みます。 Adstock設定は、モデルが現実の期待に沿うように導き、出力の解釈可能性と信頼性を向上させるのに役立ちます。 ルックバック週とチャネルごとのラグ週の合計は、設定されたトレーニングウィンドウの8分の1に上限が設定されます。 このキャップを使用すると、モデルがアドストック効果を学習するのに十分なデータを取得できます。"

**[!UICONTROL Advanced]** ステップで詳細設定を指定できます。 この手順では、[費用シェア &#x200B;](#spend-share)を定義し、[&#x200B; マルチタッチアトリビューション（MTA） &#x200B;](#mta)のモデルを有効にし、[事前知識](#prior-knowledge)を定義し、[&#x200B; チャネル adstock](#channel-adstock)を定義できます。

### 費用の共有

**[!UICONTROL Spend share]** セクション：

* 過去のマーケティング投資比率を使用して、マーケティングデータがスパースな場合にモデルに通知するには、**[!UICONTROL Allow spend share]**&#x200B;をアクティブにします。 この設定は、特に次のシナリオで推奨されます。
   * チャネルには十分な観測値がありません（たとえば、購入頻度が低い、インプレッション数やクリック数など）。
   * 例えば、データが希薄なメディア（一部のブランドではTVなど）を日常的に使用し、急上昇を遂げているメディアを制作します。

  >[!NOTE]
  >
  >1回限りの投資（スーパーボウル広告など）の場合、そのデータを支出シェアに頼るのではなく、要因として組み込みます。
  >

### MTA

**[!UICONTROL MTA enabled]** セクション：

* モデルのMTA機能を有効にするには、**[!UICONTROL MTA enabled]**&#x200B;を有効にします。 MTAを有効にしている場合、モデルのトレーニングとスコアリングを行うと、マルチタッチアトリビューションインサイトを利用できるようになります。 [&#x200B; モデルインサイト &#x200B;](insights.md)の「[&#x200B; アトリビューション &#x200B;](insights.md#attribution)」タブを参照してください。


### 事前知識

**[!UICONTROL Prior knowledge]** セクション：

![&#x200B; モデル – 事前知識](/help/assets/model-prior-knowledge-step.png)

1. **[!UICONTROL Rule type]**&#x200B;を選択します。デフォルトは&#x200B;**[!UICONTROL Absolute values]**&#x200B;です。

1. **[!UICONTROL Contribution proportion]**&#x200B;列を使用して、**[!UICONTROL Name]**&#x200B;にリストされているチャネルの貢献率を指定します。

1. 必要に応じて、各チャネルに&#x200B;**[!UICONTROL Level of confidence]** パーセントを追加できます。

1. 必要に応じて、**[!UICONTROL Clear all]**&#x200B;を使用して、**[!UICONTROL Contribution proportion]**&#x200B;列と&#x200B;**[!UICONTROL Level of confidence]**&#x200B;列のすべての入力値をクリアします。


### Channel adstock

**[!UICONTROL Channel adstock]** セクションでは、モデルで定義した各チャネル（マーケティングチャネル）に対して、個別のadstock ルックバック（キャリーオーバーまたはディケイ効果）とラグ（遅延応答時間）を定義できます。

このチャネル広告設定では、さまざまなマーケティングチャネルが長期的なビジネス成果に与える影響を、きめ細かく制御できます。 あるいは、システムのデフォルト設定と画一的な設定を使用することもできます。

チャネル広告の設定は、チャネル固有のニュアンスをキャプチャするのに役立ちます。 例えば、TV キャンペーンの長期的な影響、有料検索の短期的な影響、インフルエンサーの支出と観察可能なコンバージョンのタイムラグなどがあります。 Adobe Stockのルックバックパラメーターとラグパラメーターを試して、より正確でカスタマイズされた、信頼できるインサイトを生成することができます。 最終的に、チャネル広告の設定により、より正確な予算配分と優れたビジネス上の意思決定がもたらされます。

![&#x200B; チャネル adstock](/help/assets/channel-ad-stock.png)

チャネル adstockを設定するには：

* 各チャネル （**[!UICONTROL Name]**）に対して、**[!UICONTROL Lag (weeks)]**、**[!UICONTROL Min Lookback (weeks)]**、**[!UICONTROL Max Lookback (weeks)]**&#x200B;の値を定義します。 各値について：

   * 値を増やすには![Add](/help/assets/icons/Add.svg)を使用し、値を減らすには![Subtract](/help/assets/icons/Subtract.svg)を使用するか、手動で値を入力します。

  ラグ週の合計とチャネルごとの最大ルックバック週の合計は、設定されたトレーニングウィンドウの1/8に上限が設定されます。 このキャップを使用すると、モデルがアドストック効果を学習するのに十分なデータを取得できます。 例えば、2年間のトレーニングウィンドウの場合、チャネルの最大&#x200B;**[!UICONTROL Lag (weeks)]**&#x200B;と&#x200B;**[!UICONTROL Lookback (weeks)]**&#x200B;は13週間です。 このキャップは、値を定義するときに適用されます。


## オプションを設定

[&#x200B; トレーニングとスコアリング &#x200B;](#schedule)をスケジュールし、**[!UICONTROL Set options]**&#x200B;手順でモデルの[詳細インサイト レポート フィールド &#x200B;](#granular-insights-reporting-fields)を指定できます。


### スケジュール

**[!UICONTROL Schedule]** セクションでは、モデルのトレーニングとスコアリングをスケジュールできます。

![&#x200B; モデルのスケジュール &#x200B;](../assets/model-schedule.png)

モデルのスコアリングとトレーニングをスケジュールするには、次の手順に従います。

1. **[!UICONTROL Enable scheduled model scoring and training]**&#x200B;を有効にします。
1. **[!UICONTROL Scoring frequency]**&#x200B;を選択：

   * **[!UICONTROL Daily]**：有効な時間（例：`05:22 pm`）を入力するか、![時計](/help/assets/icons/Clock.svg)を使用してください。
   * **[!UICONTROL Weekly]**：曜日を選択し、有効な時間（例：`05:22 pm`）を入力するか、![時計](/help/assets/icons/Clock.svg)を使用します。
   * **[!UICONTROL Monthly]**：毎回の実行メニューから月の曜日を選択し、有効な時間（例：`05:22 pm`）を入力するか、![時計](/help/assets/icons/Clock.svg)を使用します。

1. ドロップダウンメニューから&#x200B;**[!UICONTROL Training frequency]**&#x200B;を選択します：**[!UICONTROL Monthly]**、**[!UICONTROL Quarterly]**、**[!UICONTROL Yearly]**、または&#x200B;**[!UICONTROL None]**。


### 詳細なインサイトのレポートフィールド

**[!UICONTROL Granular insights reporting fields]** セクションでは、きめ細かい増分レポート機能を使用しています。 この機能を使用すると、調整されたフィールドを選択して、コンバージョンとタッチポイントの増分スコアを分解できます。

![詳細なインサイトのレポートフィールドを定義](/help/assets/granular-insights-reporting-fields.png)

調和のとれたフィールドを定義することで、個別のモデルを作成する代わりに、詳細なレポート列を使用してモデルのレポートをドリルダウンできます。

例えば、収益に焦点を当てながら、キャンペーン、メディアタイプ、地域、トラフィックソースのパフォーマンスにも関心を持っているモデルを構築します。 きめ細かい増分レポート機能がなければ、4つの個別のモデルを構築する必要があります。 きめ細かい増分レポート機能を使用すると、キャンペーン、メディアタイプ、地域、トラフィックソースごとに収益モデルを分類できます。

1. **[!UICONTROL Includes]**&#x200B;の下の&#x200B;**[!UICONTROL _調和フィールド_]**&#x200B;から1つ以上の調和フィールドを選択します。 選択した調和フィールドがパネルに追加されます。
1. **[!UICONTROL *調和フィールド&#x200B;*]**![CrossSize100](/help/assets/icons/CrossSize100.svg)を選択して、選択した調和フィールドを含む調和フィールドをコンテナから削除します。
1. 選択したすべての調和フィールドを削除するには、**[!UICONTROL Clear all]**&#x200B;を選択します。

きめ細かい増分レポート用に選択された調和フィールドは、モデルのスコアリングの結果であるExperience Platform [&#x200B; スキーマ &#x200B;](/help/ingest-data/schemas.md)および[&#x200B; データセット &#x200B;](/help/ingest-data/datasets.md)の一部として使用できます。 詳細なインサイト レポート フィールドは、**[!UICONTROL conversionPassthrough]**&#x200B;および&#x200B;**[!UICONTROL touchpointPassthrough]** オブジェクト内にあります。

詳細な増分レポート用に有効になっているモデルのスキーマのconversionPassthrough オブジェクトとtouchpointPassthrough オブジェクトの![&#x200B; スクリーンショット &#x200B;](/help/assets/schema-granular-insights-reporting.png)


## 終了

* モデル設定を完了するには、**[!UICONTROL Finish]**&#x200B;を選択します。

   * **[!UICONTROL Create instance?]** ダイアログで「**[!UICONTROL Ok]**」を選択して、最初のトレーニングとスコアリングの実行を直ちにトリガーします。 お使いのモデルはステータス ![StatusOrange](/help/assets/icons/StatusOrange.svg) **[!UICONTROL Awaiting training]**&#x200B;でリストされます。

     キャンセルする場合は&#x200B;**[!UICONTROL Cancel]**&#x200B;を選択してください。

   * 追加の設定が必要な場合は、赤いアウトラインとテキストで、追加の設定が必要な内容を説明します。

* **[!UICONTROL Back]**&#x200B;を選択して、前の手順に戻ります。

* モデル設定をキャンセルするには、**[!UICONTROL Cancel]**&#x200B;を選択します。

