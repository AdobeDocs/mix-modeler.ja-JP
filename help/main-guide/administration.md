---
title: 管理
description: Mix Modelerの管理方法を説明します。
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
source-git-commit: 995f15b6d2dd99d5304a4cda7b1fa5f8a1d00023
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# 管理

の使用 [Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) Mix Modelerの商品およびユーザーを管理します。

Mix Modelerを正しく機能させるには、適切な権限を設定する必要があります。

Adobe Experience Cloud UI で、次の操作を行います。

1. を選択 **[!UICONTROL Permissions]** 左パネルの下から **[!UICONTROL ADMINISTRATION]**.

1. を選択 {{user}} **[!UICONTROL Roles]** 左パネルから。

1. 既存の役割を選択するか、を使用して役割を作成します **[!UICONTROL Create role]** （例： **Mix Modeler**）に設定します。 既存の役割を選択する場合は、 {{edit}} **[!UICONTROL Edit]** ：役割の権限を編集します。 参照： [役割の管理](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) を参照してください。

1. その役割に 1 つ以上のサンドボックスを選択していることを確認してください。

1. を追加 **Adobe Mix Modeler** resource：役割のリソースのリストに追加します。

1. 正しいを選択していることを確認します **[!UICONTROL Adobe Mix Modeler]** 設定する役割の権限。 次の役割を 1 つ以上選択できます。

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![MIX MODELER RBAC](/help/assets/mix-modeler-rbac.png)


1. 役割に対して追加の権限を選択してください。 例えば、データセットとスキーマを表示または管理するには、以下を選択します。

   - **[!UICONTROL Data Management]**：関連するオプションを選択します。 **[!UICONTROL View Datasets]** または **[!UICONTROL Manage Datasets]**.

   - **[!UICONTROL Data Modeling]**：関連するオプションを選択します。 **[!UICONTROL Manage Schemas]** または **[!UICONTROL View Schemas]**.

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   を選択 **[!UICONTROL Save]** 権限を保存します。

1. 対象： **[!UICONTROL Details]** 内 **[!UICONTROL Role]**、適切なを追加します **[!UICONTROL Users]** または **[!UICONTROL User groups]** Mix Modelerへのアクセスをユーザーに提供する。
