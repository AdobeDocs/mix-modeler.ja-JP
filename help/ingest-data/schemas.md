---
title: スキーマ
description: Mix Modelerにデータを取り込むために必要なスキーマを管理する方法について説明します。
feature: Schemas
exl-id: 08289581-5af9-4422-b049-8c24105e2a8e
TQID: https://experienceleague.adobe.com/E41pnyBetoLPOOulNmKh033myMvfF4bV9A2Xd3FXqcs
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: fbd94e4b-f9b8-42a4-8df5-3f917aabae24
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
autotag-review: '2026-05-01T08:56:54.552Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 613
ht-degree: 7%

---

# スキーマ

スキーマを管理するには、Experience Platformに取り込み、Mix Modelerで使用するデータをサポートします。

1. Mix Modelerのインターフェイスに移動します。

1. **[!UICONTROL SETUP]**&#x200B;の下にある![ スキーマ ](/help/assets/icons/Schemas.svg) **[!UICONTROL Schemas]**&#x200B;を選択します。

詳しくは、[ スキーマ UIの概要](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=en)を参照してください。

## 集計データまたは概要データ

Experience Platformで取り込み、Mix Modelerで使用する集計データまたは概要データの基礎となるスキーマのベースとして、XDM Summary Metrics クラスを使用することを強くお勧めします。

XDM Summary Metrics クラスを使用して、次の操作を行います。

- ウォールドガーデンデータ（FacebookやYouTubeからのデータなど）。

- spx （S&amp;P 500株価指数）のデータ、天候データ，

- 価格変更やホリデーカレンダーなど、内部要因データ。

>[!IMPORTANT]
>
>スキーマ定義には、取り込んだデータに必要な指標をサポートするために、少なくとも1つの数値フィールド（Integer、Double、Booleanまたはその他の数値型を使用）を含める必要があります。

以下の&#x200B;**[!DNL ExternalFactorSummarySchema]**&#x200B;に示すように、**[!DNL XDM Summary Metrics]**&#x200B;基本クラスを使用するスキーマは簡単です。

![外部要因スキーマ ](/help/assets/external-factors-schema.png)

このシンプルなスキーマを使用すると、次のようなデータを含むデータセットを取り込むことができます。

- 競合他社指数データ

  | タイムスタンプ | date_type | 因子 | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | 週 | competitor_index | 289.8 |
  | 2020-12-05T00:00:00.000Z | 週 | competitor_index | 291.2 |
  | 2020-12-12T00:00:00.000Z | 週 | competitor_index | 280.07 |
  | ... | ... | ... | ... |

- 祝日データ

  | タイムスタンプ | date_type | 因子 | value |
  |---|---|---|--:|
  | 2020-11-28T00:00:00.000Z | 週 | all_holidays_flag | 0.0 |
  | 2020-12-05T00:00:00.000Z | 週 | all_holidays_flag | 0.0 |
  | 2020-12-12T00:00:00.000Z | 週 | all_holidays_flag | 0.0 |
  | 2020-12-19T00:00:00.000Z | 週 | all_holidays_flag | 0.0 |
  | 2020-12-26T00:00:00.000Z | 週 | all_holidays_flag | 1.0 |
  | ... | ... | ... | ... |


**[!DNL XDM Summary Metrics]**&#x200B;を基本クラスとして使用する&#x200B;**[!DNL LumaPaidMarketingSchema]**&#x200B;のより包括的な例については、以下を参照してください。 スキーマは、指標（**[!DNL AMMMetrics]**）、ディメンション（**[!DNL AMMDimensions]**）、およびその他の顧客固有の情報（**[!DNL CustomerSpecific]**）に専用のフィールドグループ（色で注釈が付いた）を使用します。

![概要スキーマ ](/help/assets/summary-schema.png)

プロファイル取り込みの非同期性を考慮すると、外部ソースから集計データまたはサマリーデータを収集する場合は、スキーマの一部としてExternal Source System Audit Details フィールドグループを使用することをお勧めします。 このフィールドグループは、外部ソースの監査プロパティのセットを定義します。

## 因子標準フィールドフィールドグループ

便宜上、Experience Platformでは、内部要因データと外部要因データの専用の因子標準フィールドグループをサポートしています。多くの場合、サマリーデータ、内部要因データ、外部要因データの一部になっています。 このフィールドグループは、次のフィールドを定義します。

| フィールド表示名 | フィールド名 | フィールドタイプ | データタイプ | 必須 | 説明 |
|---|---|---|---|:-:|---|
| 因子名 | factorName | ディメンション | 文字列 | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | ファクターの名前 |
| 係数の値 | factorValue | 指標 | Double | ![ チェックマーク ](/help/assets/icons/Checkmark.svg) | 係数の値 |
| 因子タイプ | factorType | ディメンション | 文字列（列挙） | | 要因のタイプ。<br/>使用可能な値は次のとおりです。 <ul><li>内部（内部要因）</li><li>外部（外部要因）</li></ul> |
| 値タイプ | valueType | ディメンション | 文字列（列挙） | | 使用可能な値：<ul><li>実際の値（実際の値）</li><li>予測値（Forecasted Value）</li></ul>値がない場合は、「実際」がデフォルト値になります。 |
| 精度 | 精度 | ディメンション | 文字列（列挙） | | 使用可能な値：<ul><li>毎日</li><li>毎週</li><li>毎月</li></ul> |

要約、内部要因、または外部要因のデータセットは、次のデータに基づくことができます。

- 因子標準フィールドグループを&#x200B;**使用**&#x200B;するスキーマ。 このデータセットは、データセットルールを設定すると、**[!UICONTROL Factors]** データセットとして表示されます。 また、データセットのデータセットルールの一部として定義した調整済みフィールドは、モデルの作成時にファクターとして使用できます。
- 因子標準フィールドグループ **で**&#x200B;を使用していないスキーマ。 このデータセットは、データセットルールを設定すると、**[!UICONTROL Summary]** データセットとして表示されます。 データセットは概要データとして設定され、調和データには影響しません。

## サポートされているデータタイプ

現在、Mix ModelerはExperience Platform データタイプのサブセットをサポートしています。 次の基本的なデータタイプ（フィールド）がサポートされています。これは、[ スキーマ構成の基本](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#data-type)に記載されています。

- 文字列
- 整数
- Double
- ブール
- Long
- Short
- Byte
- 日付
- Date-time


>[!MORELIKETHIS]
>
>- [スキーマ](schemas.md)
