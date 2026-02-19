---
title: 現在のMix Modelerのリリースノートを表示
description: Mix Modeler の最新のリリースノート
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: 011b9b83569925ca9ff4f1ee472288473fbe8502
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 4%

---

# 最新のMix Modeler リリースノート

**最終更新日**:2026 年 1 月 13 日（PT）

これらのリリースノートは、Mix Modelerの最新リリースをカバーしています。 Mix Modeler リリースは、継続的な配信モデルに基づいて動作します。このモデルにより、毎月のおおよそのリリースサイクルが可能になります。 したがって、これらのリリースノートは更新されるので、定期的に確認してください。


## 2026年2月

| 機能 | 説明 | [ ロールアウト開始 ](#release-strategy) | [ 一般公開 ](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Granular incrementality reporting]** | 統一されたフィールドを定義すると、個別のモデルを作成する代わりに、[ 詳細なインサイトレポートフィールド ](/help/models/build.md#granular-insights-reporting-fields) を使用してモデルのレポートをドリルダウンできます。 | 2026 年 2 月 18 日（Pt） | 2026 年 2 月 18 日（Pt） |

## 2026年1月

| 機能 | 説明 | [ ロールアウト開始 ](#release-strategy) | [ 一般公開 ](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [ 更新されたデータセットルールテーブル ](/help/harmonize-data/dataset-rules.md)。 1 つ以上のデータセットルールを検索し、テーブルから直接データセットルールを表示、編集または削除できます。 | 2026 年 1 月 13 日（Pt） | 2026 年 1 月 13 日（Pt） |
| **[!UICONTROL Current spend]** | モデルインサイトの [ 限界応答曲線ビジュアライゼーション ](/help/models/insights.md#marginal-response-curves) に現在の支出ポイントを追加します。 | 2026 年 1 月 13 日（Pt） | 2026 年 1 月 13 日（Pt） |
| **[!UICONTROL Sort and resize columns]** | [ モデル ](/help/models/overview.md) および [ プラン ](/help/plans/overview.md) テーブルに列の並べ替えとサイズ変更を追加しました。 | 2026 年 1 月 13 日（Pt） | 2026 年 1 月 13 日（Pt） |
| **修正点** | 次のチケットの修正： <ul><li>AMM-3328：係数の新しい演算子でフィールド入力が無効になる</li><li>AMM-3359：日付選択とコンボボックスがロックされる。</li><li>AMM-3441：計画の複製で、日付範囲と予算が自動入力されない。</li></ul> | 2026 年 1 月 13 日（Pt） | 2026 年 1 月 13 日（Pt） |


## リリース方法

[!UICONTROL Mix Modeler] では、機能フラグ（「トグル」とも呼ばれます）を使用して新機能の表示/非表示を制御し、完全リリース前の制御スケールテストを行うことができます。 このリリース戦略には、次のフェーズが含まれます。

* **限定的テスト**：段階的なリリースはAdobeの内部ユーザーによるテストで始まります。 その後、少数の顧客アカウントのグループに公開して、機能が顧客のニーズと期待に応えているかどうかを確認します。

* **ロールアウトの開始**：段階的なリリースのロールアウトは限定的テストフェーズから始まります。 リリースはその後、数か月かけて、お客様への可用性を 0% から 100% に拡張していきます。 ロールアウトはExperience Cloudの組織レベルで段階的に行われるので、組織内の資格のあるユーザーはすべて同じエクスペリエンスを受け取ります。
