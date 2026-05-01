---
title: データガバナンスの概要
description: 収集したエクスペリエンスデータを制御できるExperience Platformのサービスとツールの使用方法について説明します。 そのため、ビジネス慣行、法的義務、開発プロセスを遵守する必要があります。
feature: Administration
exl-id: 87407c29-e158-48bf-bde9-b3c16a16107e
TQID: https://experienceleague.adobe.com/vc5z266rexOpAuR1HJCj-ltOLZmkccBDvfi8JUsuiJ4
product_v2: id: b88c80e3-31df-4609-989d-d4dac0e6d973
feature_v2: id: f6633d1c-3d2d-4f48-95d4-4bbc9913db52
subfeature_v2: id: bf7ac0fc-effb-4f0c-b93f-658412718d3cid: fd80ec6b-9b9e-448a-a6d0-b0c9a15da6b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b4dd41a7-ccf8-4e9d-918e-acaab534a307id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
autotag-review: '2026-05-01T09:16:50.195Z'
source-git-commit: 5579087b9381c4d8e909ed5fe3099fd42d5c6799
workflow-type: tm+mt
source-wordcount: 462
ht-degree: 11%

---

# データガバナンスの概要

Mix ModelerとExperience Platformの統合により、Mix Modelerは、Experience Platformの組み込みのデータガバナンス機能を活用する機能を提供します。 この節では、Mix Modelerで使用可能なデータガバナンス機能の詳細について説明します。

Experience Platform Data Governanceは、Experience Platformを介してデータが通過するジャーニー全体を通して、データを制御し、理解する機能を提供します。 このジャーニーには、データ品質、データの系統、データのカタログ化などの維持が含まれます。

必要に応じて、Mix Modeler内のExperience Platform サーフェスで使用されるデータセットに作成されるデータ使用ラベルとポリシー。 例えば、これらのラベルは、調和データ内のデータセットルールの一部であるデータセットを削除する際に、ユーザーを停止または警告します。 または、データセットルールの作成時にユーザーに制限されているスキーマフィールドを非表示にします。

データガバナンス統合により、コンプライアンスをより効率的に管理できます。 組織のデータ管理人は、使用を制限するポリシーを設定できます。 その結果、データ管理人が定義したポリシーに準拠するデータを使用できます。 詳しくは、[ラベルとポリシー](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance)に関するドキュメントを参照してください。

次のデータガバナンス機能を使用できます。

| 機能 | 詳細 |
|---|---|
| アクセス制御 | ロールベースのアクセス制御と属性ベース（フィールドレベル）のアクセス制御がサポートされています。 詳しくは、[ アクセス制御](access-controls.md)を参照してください。 |
| 監査ログ | ユーザーが特定のMix Modeler カテゴリを作成、更新または削除すると、Experience Platform監査機能は監査ログにアクティビティを記録します。 詳しくは、[監査ログ ](audit-logs.md)を参照してください。 |
| ポリシー | 統一されたデータワークフローの一部として、Experience Platform定義ポリシーが適用されます。 データ使用ラベルの違反は、ユーザーに報告され、表示されます。 詳しくは、[ ポリシー](policies.md)を参照してください。 |
| 暗号化 | モデルの入力と出力に使用されるすべてのデータセットは、Experience Platform ガイドラインに従います。 Experience Platformのデータ暗号化は、保存中および転送中のデータに適用されます。 |
| データハイジーン | モデルの入力とアウトに使用されるすべてのデータセットは、Experience Platform ガイドラインに従います。 Experience Platformには、様々な種類のデータ有効期限のサポートなど、顧客データのライフサイクルを管理するための一連のツールが用意されています。 調和済みデータの一部として使用されているExperience Platformからソースデータセットを削除すると、通知が送信されます。 詳しくは、[ データセットルール ](/help/harmonize-data/dataset-rules.md)を参照してください。 |
| 顧客管理キー | Privacy Security Shield アドオンを使用してMix Modelerのライセンスを取得した場合は、Customer Managed Keys機能を使用してAzure Key Vaultを活用し、API経由で独自のキーを取得できます。 Mix Modelerのモデル内で処理されるデータを包括的に管理できます。 |
