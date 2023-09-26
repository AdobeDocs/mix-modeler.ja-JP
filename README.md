---
source-git-commit: 1eb0be76c037d83b5b39782eace9aedbf846e03d
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 40%

---
# 記事のコントリビューション

アドビのコミュニティはもとより、ドキュメントチーム外部のアドビ従業員からのコントリビューションもお待ちしています。

## アドビのオープンソースの行動規範

このプロジェクトでは、[アドビオープンソース行動規範](code-of-conduct.md) または [.NET Foundation 行動規範](https://dotnetfoundation.org/code-of-conduct)を採用しています。詳しくは、[投稿](contributing.md)の記事を参照してください。

## Adobeコンテンツへの投稿方法

**従業員でない場合は、Adobe** 外部コミュニティの投稿を送信できます。 コミュニティの投稿はアドビの社内システムに読み込まれ、編集されて公開リポジトリに結合されます。 次に、公開リポジトリーが最新の変更と同期され、プライベートリポジトリーに結合されます。

**従業員の場合はAdobe**&#x200B;を使用すると、プライベートに直接投稿できます [AdobeGitHub リポジトリ](https://git.corp.adobe.com/AdobeDocs/). 詳しくは、Adobe従業員向けのAdobe Experience Leagueオーサリングガイドを参照してください。

## 外部寄稿者

### 軽微な変更

軽微な更新をおこなう場合は、次の手順に従います。

1. 編集するトピックに移動します。
1. 「このコンテンツは役に立ちましたか？」 ブラウザーウィンドウの下部に表示されるバナー **詳細なフィードバックオプション**.
1. クリック **編集を提案** GitHub UI で変更を反映したプル要求 (PR) を送信します。

   詳しくは、全般的な事項について説明した[アドビドキュメントのコントリビューターガイド](https://experienceleague.adobe.com/docs/contributor/contributor-guide/introduction.html?lang=ja)を参照してください。

このリポジトリー内のドキュメントやコード例に対して提案される軽微な変更や補足説明には、アドビの利用規約が適用されます。

### コミュニティからの大きな変更または新しいトピック

Adobeコミュニティのメンバーが新しいトピックを作成したり、大きな変更を投稿したりする場合は、 **問題** 」タブをクリックして問題を送信し、ドキュメントチームとの会話を開始します。 計画に同意したら、Adobe作成者と協力して改訂を公開します。

**注意：** ドキュメントやコード例の大幅な変更を含むプル要求を送信すると、オンライン投稿使用許諾契約 (CLA) の送信を求めるメッセージがプル要求に表示されます。 プル要求を確認する前に、オンラインフォームに必要事項を記入しておく必要があります。

### ツール

コミュニティのコントリビューターは、基本的な編集をするときには GitHub の UI を使用し、大きな変更を加えるときにはリポジトリーをフォークします。

詳しくは、[アドビドキュメントのコントリビューターガイド](https://experienceleague.adobe.com/docs/contributor/contributor-guide/introduction.html?lang=ja)を参照してください。

## 内部貢献者

Adobe Experience Cloudソリューションの製品チームのテクニカルライター、プログラムマネージャーまたは開発者で、技術記事の投稿や作成が職務となっている場合は、 [プライベートリポジトリ](https://git.corp.adobe.com/AdobeDocs).

## トピックの形式設定

このリポジトリ内の記事はすべて、GitHub 固有の Markdown を使用しています。 Markdown に詳しくない場合は、以下を参照してください。

* [Markdown の基本](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/)（英語）
* [印刷可能な Markdown のクイックリファレンス](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)（英語）

## ラベル

公開リポジトリーでは、プルリクエストに以下のような自動ラベルが割り当てられ、プルリクエストワークフローの管理とプルリクエストの処理状況の把握に役立ちます。

* **Change sent to author**：保留中のプルリクエストの通知が作成者に送信されました。
* **ready- to- merge**：プルリクエストレビューチームによるレビューの準備ができました。
