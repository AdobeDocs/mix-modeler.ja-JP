---
title: 管理
description: Mix Modelerの管理方法について説明します。
feature: Administration
exl-id: 76d6d15d-a838-4ee2-9929-e55ea8946b80
TQID: https://experienceleague.adobe.com/0MxMv6Due-i9-8JxKTb3vk2NDZ5mc6Pj4yEe-liCszg
autotag-review: '2026-05-01T09:07:55.299Z'
product_v2:
  - id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2:
  - id: fe2edbb1-46f9-4347-a27c-577cab3640cb
subfeature_v2:
  - id: abe9e290-7d2f-4131-b71e-ef9900865044
  - id: a6da0571-746e-4d59-89a4-7b691b1c3b9a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 7%

---

# 管理

[Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)を使用して、Mix Modeler製品とユーザーを管理します。

Mix Modelerを適切に機能させるには、適切な権限を設定する必要があります。

Adobe Experience Cloud UIの場合：

1. 左側のパネルの&#x200B;**[!UICONTROL ADMINISTRATION]**&#x200B;の下にある&#x200B;**[!UICONTROL Permissions]**&#x200B;を選択します。

1. 左側のパネルから「![&#x200B; ユーザー](/help/assets/icons/User.svg) **[!UICONTROL Roles]**」を選択します。

1. 既存のロールを選択するか、**[!UICONTROL Create role]**&#x200B;を使用してロールを作成します（例：**Mix Modeler**）。 既存の役割を選択した場合は、![編集](/help/assets/icons/Edit.svg) **[!UICONTROL Edit]**&#x200B;を選択して、その役割の権限を編集します。 詳しくは、[役割の管理](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)を参照してください。

1. 役割に1つ以上のサンドボックスが選択されていることを確認します。

1. ロールのリソースのリストに&#x200B;**Adobe Mix Modeler** リソースを追加します。

1. 設定する役割に対して適切な&#x200B;**[!UICONTROL Adobe Mix Modeler]**&#x200B;権限を選択していることを確認してください。 次の1つ以上の役割を選択できます。

   - **[!UICONTROL View Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL Manage Adobe Mix Modeler Harmonized Data]**
   - **[!UICONTROL View Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Models Configuration]**
   - **[!UICONTROL View Adobe Mix Modeler Plans Configuration]**
   - **[!UICONTROL Manage Adobe Mix Modeler Plans Configuration]**

     ![Mix Modeler RBAC](/help/assets/mix-modeler-rbac.png)


1. 役割に追加の権限を選択していることを確認します。 例えば、データセットとスキーマを表示または管理するには、次を選択します。

   - **[!UICONTROL Data Management]**：関連するオプションを選択：**[!UICONTROL View Datasets]**&#x200B;または&#x200B;**[!UICONTROL Manage Datasets]**。

   - **[!UICONTROL Data Modeling]**：関連するオプションを選択：**[!UICONTROL Manage Schemas]**&#x200B;または&#x200B;**[!UICONTROL View Schemas]**。

   <!--
    * **[!UICONTROL Data Governance]**: ensure you select **[!UICONTROL View User Activity Log]** and **[!UICONTROL View Data Usage Policies]**.
    -->

   <!--![Permissions](assets/permissions-including-privacy.png)-->

   **[!UICONTROL Save]**&#x200B;を選択して権限を保存します。

1. **[!UICONTROL Role]**&#x200B;内の&#x200B;**[!UICONTROL Details]**&#x200B;で、適切な&#x200B;**[!UICONTROL Users]**&#x200B;または&#x200B;**[!UICONTROL User groups]**&#x200B;を追加して、ユーザーにMix Modelerへのアクセス権を提供します。
