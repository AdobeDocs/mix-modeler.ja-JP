---
title: スキーマ
description: データをMix Modelerに取り込むために必要なスキーマを管理する方法を説明します。
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 9085363e951a4e306c64ad28f56e2c15b4a6029a
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---

# スキーマ

スキーマを管理して、Experience Platformで取り込み、Mix Modelerで使用するデータをサポートするには、次の手順を実行します。

1. Mix Modelerインターフェイスに移動します。

1. を選択 ![スキーマ](/help/assets//icons/Schemas.svg) **[!UICONTROL Schemas]**&#x200B;の下 **[!UICONTROL SETUP]**.

を参照してください。 [スキーマ UI の概要](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.htm?lang=ja) を参照してください。

## 集計または概要データ

Experience Platformで取り込みMix Modelerで使用する集計データまたは概要データの基礎となるスキーマのベースとして、XDM Summary Metrics クラスを使用することを強くお勧めします。

XDM Summary Metrics クラスは、次の場合に使用します。

- 壁に囲まれた庭のデータ（例：FacebookまたはYouTubeのデータ）。

- spx （S&amp;P 500 株価指数）のデータや気象データなどの外部要因データ

- 内部要因データ （価格変更、休日カレンダーなど）。

>[!IMPORTANT]
>
>取り込んだデータに必要な指標をサポートするには、スキーマ定義に 1 つ以上の数値フィールド（整数、倍精度浮動小数点数、ブール値、その他の数値タイプを使用）を含める必要があります。

スキーマは、 **[!DNL XDM Summary Metrics]** 基本クラスは、次に示すように単純にすることができます。 **[!DNL ExternalFactorSummarySchema]** 下。

![外部要因スキーマ](/help/assets//external-factors-schema.png)

この単純なスキーマを使用すると、次のようなデータを含んだデータセットを取り込むことができます。

- 競合他社インデックスデータ

  | タイムスタンプ | date_type | 要因 | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | 週間 | competitor_index | 289.8 |
  | 2020-12-05T00:00:00.000Z | 週間 | competitor_index | 291.2 |
  | 2020-12-12T00:00:00.000Z | 週間 | competitor_index | 280.07 |
  | ... | ... | ... | ... |

- 祝日データ

  | タイムスタンプ | date_type | 要因 | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | 週間 | all_holidays_flag | 0.0 |
  | 2020-12-05T00:00:00.000Z | 週間 | all_holidays_flag | 0.0 |
  | 2020-12-12T00:00:00.000Z | 週間 | all_holidays_flag | 0.0 |
  | 2020-12-19T00:00:00.000Z | 週間 | all_holidays_flag | 0.0 |
  | 2020-12-26T00:00:00.000Z | 週間 | all_holidays_flag | 1.0 |
  | ... | ... | ... | ... |


を参照してください。 **[!DNL LumaPaidMarketingSchema]** の使用 **[!DNL XDM Summary Metrics]** 基本クラスとして使用します。 スキーマは、指標に専用のフィールドグループ（色の注釈が付いています）を使用します（**[!DNL AMMMetrics]**）、ディメンション （**[!DNL AMMDimensions]**）、およびその他のお客様固有の情報（**[!DNL CustomerSpecific]**）に設定します。

![概要スキーマ](/help/assets//summary-schema.png)

プロファイル取り込みは非同期なので、外部ソースから集計データや概要データを収集する場合は、外部Source システム監査の詳細フィールドグループをスキーマの一部として使用することをお勧めします。 このフィールドグループは、外部ソースの一連の監査プロパティを定義します。


## サポートされるデータタイプ

現在、Mix Modelerでは、Experience Platformデータタイプのサブセットをサポートしています。 に記載されている次の基本的なデータタイプ（フィールド） [スキーマ構成の基本](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#data-type)、はサポートされています。

- 文字列
- 整数
- Double
- ブール値
- Long
- Short
- Byte
- Date
- Date-time
