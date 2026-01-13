---
title: スキーマ
description: データをMix Modelerに取り込むために必要なスキーマを管理する方法を説明します。
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
source-git-commit: 7524c2ffc0408b04e6bef5bd5deedc1feea0b682
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 7%

---

# スキーマ

Experience Platformで取り込み、Mix Modelerで使用するデータをサポートするスキーマを管理するには：

1. Mix Modeler インターフェイスに移動します。

1. ![&#x200B; の下の「](/help/assets/icons/Schemas.svg) スキーマ **[!UICONTROL Schemas]**」 **[!UICONTROL SETUP]** を選択します。

詳しくは、[&#x200B; スキーマ UI の概要 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.htm?lang=ja) を参照してください。

## 集計または概要データ

Experience Platformで取り込みMix Modelerで使用する集計または概要データの基礎となるスキーマのベースとして、XDM Summary Metrics クラスを使用することを強くお勧めします。

XDM Summary Metrics クラスは、次の場合に使用します。

- 壁に囲まれた庭のデータ、例えば Facebook やYouTubeからのデータ。

- spx （S&amp;P 500 株価指数）のデータや気象データなどの外部要因データ

- 内部要因データ （価格変更、休日カレンダーなど）。

>[!IMPORTANT]
>
>取り込んだデータに必要な指標をサポートするには、スキーマ定義に 1 つ以上の数値フィールド（整数、倍精度浮動小数点数、ブール値、その他の数値タイプを使用）を含める必要があります。

次の **[!DNL XDM Summary Metrics]** に示すように、**[!DNL ExternalFactorSummarySchema]** 基本クラスを使用するスキーマは単純にすることができます。

![&#x200B; 外部要因スキーマ &#x200B;](/help/assets/external-factors-schema.png)

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


**[!DNL LumaPaidMarketingSchema]** を基本クラスとして使用する **[!DNL XDM Summary Metrics]** の包括的な例については、以下を参照してください。 スキーマは、指標（**[!DNL AMMMetrics]**）、ディメンション（**[!DNL AMMDimensions]**）およびその他の顧客固有の情報（**[!DNL CustomerSpecific]**）に対して、専用のフィールドグループ（色で注釈が付いています）を使用します。

![&#x200B; 概要スキーマ &#x200B;](/help/assets/summary-schema.png)

プロファイル取り込みは非同期なので、外部ソースから集計データや概要データを収集する場合は、外部Source システム監査の詳細フィールドグループをスキーマの一部として使用することをお勧めします。 このフィールドグループは、外部ソースの一連の監査プロパティを定義します。

## [ 要素標準フィールド ] フィールド グループ

便宜上、Experience Platformでは、内部および外部要因データ用の専用の要素標準フィールドグループをサポートしています。これは、多くの場合、概要、内部要因、外部要因データの一部です。 このフィールドグループは、次のフィールドを定義します。

| フィールドの表示名 | フィールド名 | フィールドタイプ | データタイプ | 必須 | 説明 |
|---|---|---|---|:-:|---|
| 要素名 | factorName | ディメンション | 文字列 | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | 要因の名前 |
| 要素値 | factorValue | 指標 | Double | ![&#x200B; チェックマーク &#x200B;](/help/assets/icons/Checkmark.svg) | 係数の値 |
| 要素タイプ | factorType | ディメンション | 文字列（列挙） | | 係数のタイプ。<br/> 使用可能な値は次のとおりです。 <ul><li>内部（内部要因）</li><li>外部（外部要因）</li></ul> |
| 値タイプ | valueType | ディメンション | 文字列（列挙） | | 使用可能な値：<ul><li>実際（実際の値）</li><li>予測（予測値）</li></ul>値がない場合、デフォルト値は「実際」です。 |
| 精度 | 精度 | ディメンション | 文字列（列挙） | | 使用可能な値：<ul><li>毎日</li><li>毎週</li><li>毎月</li></ul> |

概要、内部要因、外部要因のデータセットは、次に基づくことができます。

- 「ファクタ標準フィールド」グループを **使用** するスキーマ このデータセットは、データセットルールを設定する際に、**[!UICONTROL Factors]** のデータセットとして表示されます。 また、定義した統一フィールドは、データセットのデータセットルールの一部として、モデルを作成する際の要因として使用できます。
- 要素標準フィールドグループを使用 **ない** スキーマ。 このデータセットは、データセットルールを設定する際に、**[!UICONTROL Summary]** のデータセットとして表示されます。 データセットは概要データとして設定され、統一データには影響しません。

## サポートされるデータタイプ

現在、Mix Modelerは、Experience Platform データタイプのサブセットをサポートしています。 [&#x200B; スキーマ構成の基本）に記載されている次の基本データタイプ（フィールド &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=ja#data-type) がサポートされています。

- 文字列
- 整数
- Double
- ブール値
- Long
- Short
- Byte
- 日付
- Date-time


>[!MORELIKETHIS]
>
>- [スキーマ](schemas.md)
