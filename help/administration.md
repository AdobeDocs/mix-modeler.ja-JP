---
title: 管理
description: Adobe Mix Modelerの管理方法
source-git-commit: b5b277e3476bdf6c0c0da85425bba19bea00c594
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 8%

---


# 管理

以下を使用します。 [Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) :Adobe Mix Modeler製品およびユーザーを管理します。

Adobe Mix Modelerが正しく機能するには、正しい権限を設定する必要があります。

Adobe Experience Cloud UI で、

1. 選択 **[!UICONTROL Permissions]** 左側のレールから、その下に **[!UICONTROL ADMINISTRATION]**.

1. 選択 ![人物](assets/icons/User.svg) **[!UICONTROL Roles]** を左側のパネルからクリックします。

1. 既存のロールを選択するか、 **[!UICONTROL Create role]**. 既存の役割を選択した場合は、「 ![編集](assets/icons/Edit.svg) **[!UICONTROL Edit]** ：役割の権限を編集します。 詳しくは、 [役割の管理](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) を参照してください。

1. ロールに対して次の権限を選択していることを確認します。

   * **[!UICONTROL Sandboxes]**:1 つ以上のサンドボックスを選択してください。

   * **[!UICONTROL Data Management]**：必ずオプションを選択してください。 **[!UICONTROL View Datasets]** および **[!UICONTROL Manage Datasets]**.

   * **[!UICONTROL Data Modeling]**：必ずオプションを選択してください。 **[!UICONTROL Manage Schemas]** および **[!UICONTROL View Schemas]**.

   * **[!UICONTROL Destinations]**：必ず **[!UICONTROL Manage and Activate Dataset Destination]**, **[!UICONTROL Destination Authoring]**, **[!UICONTROL Activate Destinations]** および **[!UICONTROL View Destinations]**.

   * **[!UICONTROL Data Ingestion]**：必ず **[!UICONTROL View Sources]** および **[!UICONTROL Manage Sources]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   役割に対して設定されている権限は次のようになります。

   ![権限](assets/permissions.png)

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   選択 **[!UICONTROL Save]** 権限を保存します。

1. In **[!UICONTROL Details]** 範囲 **[!UICONTROL Role]**、適切な **[!UICONTROL Users]** および/または **[!UICONTROL User groups]** ユーザーにAdobe Mix Modelerへのアクセスを提供する。
