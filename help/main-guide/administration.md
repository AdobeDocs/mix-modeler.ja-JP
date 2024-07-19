---
title: 管理
description: Mix Modelerの管理方法を説明します。
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 4d84c93121fc476cc6610ad572bab161bbacfc23
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# 管理

[Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) を使用して、Mix Modelerの商品とユーザーを管理します。

Mix Modelerを正しく機能させるには、適切な権限を設定する必要があります。

Adobe Experience Cloud UI で、次の操作を行います。

1. 左パネルの「**[!UICONTROL ADMINISTRATION]**」の下にある「**[!UICONTROL Permissions]**」を選択します。

1. 左側のパネルから ![ ユーザー ](/help/assets/icons/User.svg)**[!UICONTROL Roles]** を選択します。

1. 既存の役割を選択するか、**[!UICONTROL Create role]** を使用して役割を作成してください（例：**Mix Modeler**）。 既存の役割を選択する場合は、「![ 編集 ](/help/assets/icons/Edit.svg)」 **[!UICONTROL Edit]** を選択して、役割の権限を編集します。 詳しくは、[ 役割の管理 ](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) を参照してください。

1. その役割に 1 つ以上のサンドボックスを選択していることを確認してください。

1. **Adobe Mix Modeler** リソースをロールのリソースの一覧に追加します。

1. 設定する役割に適した **[!UICONTROL Adobe Mix Modeler]** 権限を選択していることを確認してください。 次の役割を 1 つ以上選択できます。

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![Mix ModelerRBAC](/help/assets/mix-modeler-rbac.png)


1. 役割に対して追加の権限を選択してください。 例えば、データセットとスキーマを表示または管理するには、以下を選択します。

   - **[!UICONTROL Data Management]**：関連するオプション（**[!UICONTROL View Datasets]** または **[!UICONTROL Manage Datasets]**）を選択します。

   - **[!UICONTROL Data Modeling]**：関連するオプション（**[!UICONTROL Manage Schemas]** または **[!UICONTROL View Schemas]**）を選択します。

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   「**[!UICONTROL Save]**」を選択して、権限を保存します。

1. **[!UICONTROL Role]** 内の **[!UICONTROL Details]** で、適切な **[!UICONTROL Users]** または **[!UICONTROL User groups]** を追加して、ユーザーにMix Modelerへのアクセスを提供します。
