---
title: モデルのトレーニングとスコアリング
description: モデルのトレーニングおよびスコアリング方法を説明します。
feature: Models
source-git-commit: 6855d19347b7f6f1477a6265310df5950b8463c9
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# モデルのトレーニングとスコアリング

モデルを [ 作成 ](/help/models/build.md) すると、モデルは自動的にトレーニングされ、スコアリングされます。 モデルを手動で再トレーニングまたは再コア化できます。

## トレイン

新しい増分マーケティングと要因データを含める場合は、モデルの再トレーニングを検討してください。 例えば、前四半期の市場力学が変更されたり、マーケティングデータ配分が大幅に変更されたりしたとします。

モデルを再トレーニングするには、次の手順に従います。

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Train]**] を選択します。 または、青いアクションバーから ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Train]** を選択します。

   **[!UICONTROL Train model]** ダイアログで、次の操作を実行するオプションを選択します。

   * **[!UICONTROL Train model with last 2 years of marketing data]**、または
   * **[!UICONTROL Train model using specific date range of data]**。
日付範囲を指定します。 ![ カレンダー ](/help/assets/icons/Calendar.svg) を使用して、日付範囲を選択できます。 最低 1 年のデータ範囲を選択する必要があります。

   ![ モデルの再トレーニング ](../assets/retrain-model.png)

1. モデルを再トレーニングする **[!UICONTROL Train]** を選択します。


モデルの再トレーニングは、モデルが正常にトレーニングされた場合にのみ実行できます。


## スコア


新しいマーケティングデータに基づいてモデルを増分的にスコアリングしたり、特定の日付範囲でモデルを再コア化したりできます。

次の場合は、モデルの再コアを検討してください。

* 間違ったマーケティングデータを修正します。 例えば、モデルのトレーニングとスコアリングに含めた最近の有料検索データが、1 週間のデータを見逃したとします。
* 調和されたデータの一部として設定したデータセットの更新によって利用可能になった新しい増分マーケティングデータを使用します。

モデルをスコアリングまたは再コアするには：

1. 左パネルから ![](/help/assets/icons/FileData.svg) **[!UICONTROL Models]** を選択します。

1. モデルの ![ 詳細 ](/help/assets/icons/More.svg) を選択し、右クリック メニューから [**[!UICONTROL Score]**] を選択します。 または、青いアクションバーから ![DataRefresh](/help/assets/icons/DataRefresh.svg) **[!UICONTROL Score]** を選択します。

   **[!UICONTROL Score marketing data]** ダイアログで、次の操作を実行するオプションを選択します。

   * **[!UICONTROL Score new marketing data from *mm/dd/yyyy *]**：新しいマーケティングデータを使用してモデルに増分的にスコアを付ける
   * 特定の日付範囲で再コアする **[!UICONTROL Score specific date range of marketing data]**。
日付範囲を指定します。 ![ カレンダー ](/help/assets/icons/Calendar.svg) を使用して、日付範囲を選択できます。

   ![ モデルの再コア ](../assets/rescore-model.png)

1. 「**[!UICONTROL Score]**」を選択します。 特定のデータ範囲を使用してモデルを再スコアリングすると、**[!UICONTROL Existing model is replaced]** のダイアログが表示され、選択した日付範囲の新しいスコアでモデルを置き換えるかどうかを確認するように求められます。 「**[!UICONTROL Replace model]**」を選択して確定します。

>[!IMPORTANT]
>
>モデルの再コアを実行しても、再コアされたモデルに基づいて既に作成されているプランは変更されません。 新しい再コアモデルをプランで使用するには、新しいプランを作成する必要があります。

