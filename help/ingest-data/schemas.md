---
title: スキーマ
description: データを Mix Modeler に取り込むために必要なAdobeを管理する方法を説明します。
feature: Datasets
source-git-commit: abbfc78e9fa774a240d000131f35d3dc257c15ea
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 6%

---


# スキーマ

スキーマを管理するには、Adobe Experience Platformで取り込むデータをサポートし、AdobeMix Modeler で使用します。

1. Mix Modeler インタフェースのAdobeに移動します。

1. 選択 ![スキーマ](../assets/icons/Schemas.svg) **[!UICONTROL Schemas]**，の下 **[!UICONTROL DATA MANAGEMENT]**.

詳しくは、 [スキーマ UI の概要](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.htm?lang=ja) を参照してください。

## データの集計または概要

Experience Platformで取り込み、AdobeMix Modeler で使用する集計または概要データの基になるスキーマのベースとして、XDM Summary Metrics クラスを使用することを強くお勧めします。

以下に、 **[!DNL LumaPaidMarketingSchema]** XDM 概要指標を基本クラスとして使用し、指標 (**[!DNL AMMMetrics]**)，ディメンション (**[!DNL AMMDimensions]**) やその他の顧客固有の情報 (**[!DNL CustomerSpecific]**) をクリックします。

![概要スキーマ](../assets/summary-schema.png)

一連の監査プロパティを定義する場合は、外部ソースから集計データや概要データを収集するスキーマの一部として、「外部ソースシステム監査詳細」フィールドグループを使用することを強くお勧めします。
