---
title: 最新のMix Modeler リリースノートを見る
description: Mix Modeler の最新のリリースノート
feature-set: Experience Cloud
feature: Release Notes
exl-id: 38a47672-2af2-437c-b769-4d5febb941f5
source-git-commit: dd7a7260464b27b8ef257004b1c2a64d70ffe122
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 5%

---

# 最新のMix Modeler リリースノート

**最終更新**: 2026年2月26日（PT）。

このリリースノートでは、Mix Modelerの最新リリースについて説明します。 Mix Modeler リリースは継続的な配信モデルで動作します。これにより、ほぼ毎月のリリース頻度を把握できます。 そのため、これらのリリースノートは更新されるので、定期的に確認してください。

## 2026 年 3 月

| 機能 | 説明 | [&#x200B; ロールアウト開始](#release-strategy) | [一般提供](#release-strategy) |
|---|---|---|---|
| **チャネル adstock** | [Channel adstock](/help/models/build.md#channel-adstock)を通じて、ドメインの専門知識、実験結果、または以前のチャネル分析をモデルの詳細設定に直接組み込むことができます。 モデルのチャネル分析内で[&#x200B; チャネル広告インサイト &#x200B;](/help/models/insights.md#channel-adstock)を表示します。 | 2026年3月30日（PT） | 2026年3月30日（PT） |

## 2026年2月

| 機能 | 説明 | [&#x200B; ロールアウト開始](#release-strategy) | [一般提供](#release-strategy) |
|---|---|---|---|
| **調整済み要因ワークフロー** | 要素は、[調整済み要素ワークフロー](/help/harmonize-data/overview.md#factors)の一部として管理されるようになりました。 これにより、[因子データを定義](/help/ingest-data/schemas.md#factor-standard-fields-field-group)する方法、[&#x200B; データセット ルールの一部として内部要因と外部要因を管理する方法](/help/harmonize-data/dataset-rules.md#factor-datasets)、および[&#x200B; モデル &#x200B;](/help/models/build.md#configure)で因子データを使用する方法が簡略化されます。 | 2026 年 2 月 25 日（Pt） | 2026 年 2 月 25 日（Pt） |
| **[!UICONTROL Granular incrementality reporting]** | 統一されたフィールドを定義して、[詳細なインサイト レポートフィールド &#x200B;](/help/models/build.md#granular-insights-reporting-fields)を使用してモデルのレポートをドリルダウンできるようにします。モデルを個別に作成する必要はありません。 | 2026年2月18日（PT） | 2026年2月18日（PT） |

## 2026年1月

| 機能 | 説明 | [&#x200B; ロールアウト開始](#release-strategy) | [一般提供](#release-strategy) |
|---|---|---|---|
| **[!UICONTROL Dataset rules]** | [&#x200B; データセット ルール テーブル &#x200B;](/help/harmonize-data/dataset-rules.md)を更新しました。 1つ以上のデータセットルールを検索し、テーブルから直接データセットルールを表示、編集または削除できます。 | 2026年1月13日（PT） | 2026年1月13日（PT） |
| **[!UICONTROL Current spend]** | モデルインサイトの[限界応答曲線ビジュアライゼーション &#x200B;](/help/models/insights.md#marginal-response-curves)に現在の支出点を追加します。 | 2026年1月13日（PT） | 2026年1月13日（PT） |
| **[!UICONTROL Sort and resize columns]** | [&#x200B; モデル &#x200B;](/help/models/overview.md)および[&#x200B; プラン &#x200B;](/help/plans/overview.md) テーブルに列の並べ替えとサイズ変更を追加しました。 | 2026年1月13日（PT） | 2026年1月13日（PT） |
| **修正点** | 次のチケットの修正： <ul><li>AMM-3328：新しい演算子のフィールド入力が無効になりました</li><li>AMM-3359：日付選択とコンボボックスのロックが発生する。</li><li>AMM-3441：計画を複製すると、日付範囲と予算が自動的に入力されません。</li></ul> | 2026年1月13日（PT） | 2026年1月13日（PT） |


## リリース戦略

[!UICONTROL Mix Modeler]では、機能フラグ（「トグル」とも呼ばれます）を使用して新しい機能の表示を制御し、フルリリース前に制御されたスケール テストを可能にします。 このリリース戦略には、次のフェーズが含まれます。

* **制限付きテスト**：段階的なリリースは、内部Adobe ユーザーによるテストから始まります。 そして、その機能が顧客のニーズと期待を満たしていることを確認するために、少数の顧客アカウントが利用できるようにします。

* **ロールアウトの開始**：段階的なリリースのロールアウトは、制限付きテスト フェーズで開始されます。 その後、数ヶ月にわたって、リリースの可用性を0%から100%に拡大します。 段階的なロールアウトは、Experience Cloud Organization レベルで行われるため、組織内の権限のあるユーザーはすべて同じエクスペリエンスを受け取ります。

