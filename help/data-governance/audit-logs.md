---
title: 監査ログ
description: Mix Modelerから監査ログにアクセスする方法について説明します。
feature: Administration
exl-id: aa65aac5-bea4-43ff-b0d0-9e8a6a97d3ca
source-git-commit: e6f24c96e873804b37011a1afafb7012d999fc1b
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 13%

---

# 監査ログ

システムで実行されるアクティビティの透明性と可視性を高めるために、Mix Modeler ワークフロー内のユーザーアクティビティがExperience Platform監査ログに取り込まれ、ユーザーによるMix Modeler カテゴリの変更を把握できます。 これらのログは、監査証跡を形成することで、問題のトラブルシューティングに役立て、企業のデータ管理ポリシーや規制要件に効果的に準拠するのに役立ちます。

<!-- 
DO WE HAVE TO ADD THIS
If you are subject to the Health Insurance Portability and Accountability Act (HIPAA) and create, receive, maintain, or transmit permitted sensitive personal data through Mix Modeler, you are responsible for executing a BAA with Adobe and licensing Healthcare Shield.
-->

監査ログは、誰がいつ、どのようなアクションを実行したかを通知します。 ログに記録される各アクションには、アクションのタイプ、日時、アクションを実行したユーザーの電子メール ID、アクションのタイプに関連する追加の属性を示すメタデータが含まれます。 これは、Mix Modelerでユーザーが実行した作成、更新、削除アクションを追跡します。

監査ログを調べるには、Mix Modeler インターフェイスで次の操作を行います。

1. **[!UICONTROL PRIVACY]**&#x200B;から![&#x200B; タスクリスト &#x200B;](/help/assets/icons/TaskList.svg) **[!UICONTROL Audits]**&#x200B;を選択します。

1. **[!UICONTROL Audits]**&#x200B;で、**[!UICONTROL Activity log]**&#x200B;を見つけることができます。 アクティビティログには、次のMix Modeler カテゴリ、アクション、ステータスのエントリが表示されます。

   | カテゴリ | アクション | ステータス |
   |---|---|---|
   | Mix Modeler データセットルール | 作成 | 許可または拒否 |
   | Mix Modeler データセットルール | 更新 | 許可または拒否 |
   | Mix Modeler データセットルール | 削除 | 許可または拒否 |
   | Mix Modelerフィールド | 作成 | 許可または拒否 |
   | Mix Modelerフィールド | 更新 | 許可または拒否 |
   | Mix Modelerフィールド | 削除 | 許可または拒否 |
   | Mix Modeler Marketing Touchpoint | 作成 | 許可または拒否 |
   | Mix Modeler Marketing Touchpoint | 更新 | 許可または拒否 |
   | Mix Modeler Marketing Touchpoint | 削除 | 許可または拒否 |
   | Mix Modeler コンバージョン | 作成 | 許可または拒否 |
   | Mix Modeler コンバージョン | 更新 | 許可または拒否 |
   | Mix Modeler コンバージョン | 削除 | 許可または拒否 |
   | Mix Modeler Model | 作成 | 許可または拒否 |
   | Mix Modeler Model | 更新 | 許可または拒否 |
   | Mix Modeler Model | 削除 | 許可または拒否 |
   | Mix Modeler Model | Rescore | 許可または拒否 |
   | Mix Modeler Model | 複製 | 許可または拒否 |
   | Mix Modeler Model | トレーニング/リトレイン | 許可または拒否 |
   | Mix Modeler Model | メタデータのダウンロード/保存 | 許可または拒否 |
   | Mix Modeler プラン | 作成 | 許可または拒否 |
   | Mix Modeler プラン | 更新 | 許可または拒否 |
   | Mix Modeler プラン | 関連モデルを変更 | 許可または拒否 |
   | Mix Modeler Data Harmonization | トリガーシンク | 許可または拒否 |


1. アクティビティ ログのエントリを選択してパネルを開き、詳細を確認します。

   ![Mix Modeler監査](/help/assets/mix-modeler-audit.png)

1. **[!UICONTROL Category]**、**[!UICONTROL Action]**、**[!UICONTROL Request ID]**、**[!UICONTROL User]**、**[!UICONTROL Status]**&#x200B;または&#x200B;**[!UICONTROL Date]**&#x200B;の範囲でフィルタリングするには、![&#x200B; フィルター](/help/assets/icons/Filter.svg)を選択します。

1. アクティビティログに表示される列を変更するには、![列](/help/assets/icons/ColumnSetting.svg)を選択し、**[!UICONTROL Customize table]** ダイアログで、表示する列を選択します。 選択を適用するには&#x200B;**[!UICONTROL Apply]**&#x200B;を選択し、選択をキャンセルするには&#x200B;**[!UICONTROL Cancel]**&#x200B;を選択します。

1. 監査ログをダウンロードするには、![&#x200B; ダウンロード &#x200B;](/help/assets/icons/Download.svg) **[!UICONTROL Download log]**&#x200B;を選択します。 **[!UICONTROL Download log]** ダイアログで、形式として&#x200B;**[!UICONTROL CSV]**&#x200B;または&#x200B;**[!UICONTROL JSON]**&#x200B;のいずれかを選択し、**[!UICONTROL Download]**&#x200B;を選択します。

## 監査ログへのアクセス

この機能が組織で有効になっている場合、アクティビティが発生すると、監査ログが自動的に収集されます。 監査ログ収集を手動で有効にする必要はありません。

監査ログを表示および書き出すには、監査ログへのアクセス制御権限が付与されている必要があります。 Mix Modeler機能の個別の権限を管理する方法については、[&#x200B; アクセス制御ドキュメント &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/home)を参照してください。
