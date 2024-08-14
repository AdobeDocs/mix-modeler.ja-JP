---
title: データガバナンス
description: 収集したエクスペリエンスデータを制御できる、Experience Platformのサービスおよびツールの使用方法を説明します。 したがって、お客様はビジネス・プラクティス、法的義務、開発プロセスを遵守できます。
feature: Administration
source-git-commit: 6776a91563f120db1341adef923aab4b0f582c9d
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 11%

---

# データガバナンス

Mix ModelerとExperience Platformの統合により、Mix Modelerは、Experience Platformに組み込まれているデータガバナンス機能を活用できるようになります。 ドキュメントのこの節では、Mix Modelerで使用できるデータガバナンス機能の詳細を説明します。

Experience Platformデータガバナンスを使用すると、Experience Platformを通じてデータが受け取るジャーニー全体を通じて、データを制御し把握できます。 このジャーニーでは、データ品質、データ系列、データのカタログ化などを維持します。

必要に応じて、Mix ModelerのExperience Platformサーフェスで使用されるデータセットに関して作成されるデータ使用ラベルおよびポリシーです。 例えば、これらのラベルは、統一データ内のデータセットルールの一部であるデータセットを削除する際にユーザーを停止または警告します。 データセットルールを作成する際に、ユーザーに対して制限されたスキーマフィールドを非表示にする

データガバナンスの統合により、コンプライアンスをより効率的に管理できます。 組織のデータ管理人は、使用を制限するポリシーを設定できます。その結果、データ管理人が定義したポリシーに準拠するデータを使用できます。 詳しくは、[ラベルとポリシー](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/data-governance)に関するドキュメントを参照してください。

次のデータガバナンス機能を使用できます。

| 機能 | 詳細 |
|---|---|
| アクセス制御 | 役割ベースのアクセス制御および属性ベース（フィールドレベル）のアクセス制御がサポートされています。 詳しくは、[ アクセス制御 ](access-controls.md) を参照してください。 |
| 監査ログ | ユーザーが特定のMix Modelerカテゴリを作成、更新、削除すると、Experience Platform監査機能は監査ログにアクティビティを記録します。 詳しくは、[ 監査ログ ](audit-logs.md) を参照してください。 |
| ポリシー | 統一データワークフローの一部として、Experience Platform定義のポリシーが適用されます。 データ使用ラベルの違反が報告され、ユーザーに表示されます。 詳しくは、[ ポリシー ](policies.md) を参照してください。 |
| 暗号化 | モデルの入出力に使用されるすべてのデータセットは、Experience Platformガイドラインに従います。 Experience Platformデータ暗号化は、保存中および送信中のデータに適用されます。 |
| データハイジーン | モデルの入力および出力に使用されるすべてのデータセットは、Experience Platformガイドラインに従います。 Experience Platformは、様々なタイプのデータ有効期限のサポートなど、カスタマーデータライフサイクルを管理するための一連のツールを提供します。 統一データの一部として使用されるソースデータセットをExperience Platformから削除すると、通知が表示されます。 詳しくは、[ データセットルール ](/help/harmonize-data/dataset-rules.md) を参照してください。 |
| 顧客管理キー | Privacy Security Shield または Healthcare Shield アドオンを使用してMix Modelerのライセンスを取得している場合、顧客管理キー機能を使用して Azure Key Vault を利用し、API を介して独自のキーを取り込むことができます。 Mix Modelerのモデル内で処理されるデータを完全に管理できます。 |
