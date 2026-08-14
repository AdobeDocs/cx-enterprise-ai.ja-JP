---
description: Coworker Chatのユースケースとサンプルプロンプトを、データインサイト、オーディエンス、ジャーニー、プラットフォーム運用をまたいで、エリアごとに整理して参照できます。
title: 同僚チャットのユースケース
source-git-commit: a19e6a17796fbe8d00a6e5559fc664ae469481f2
workflow-type: tm+mt
source-wordcount: '1284'
ht-degree: 7%

---

# Adobe Workfrontのユースケース{#use-cases}

共同作業チャットでは、複数のUIを操作したり、手作業でクエリを記述したりするのではなく、自然言語を使用して、[!DNL Experience Platform] データをクエリ、分析、アクションできます。 このページでは、実務担当者が最も重視しているユースケースを、データインサイト、オーディエンス、ジャーニー、基本要素、サンドボックスツールなどの作業領域ごとに分類して説明します。 各エントリには、呼び出すスキル、使用するアプリケーション、コピーできるプロンプトのサンプル、独自のデータへの適応、会話による絞り込みなどがあります。

## 顧客理解とデータ活用

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [CJA レポートと指標を取得](data-insights/analytics-chat.md) | CJAにリアルタイムでクエリを実行し、指標、ディメンション、セグメント、データビューを取得します | `cja` | Customer Journey Analytics（CJA） | 「過去30日間のページビューを表示」 ・ 「マスターデータビューの上位セグメントのリスト」 |
| 比較分析 | チャネル、期間、セグメントをまたいで指標を並べて比較できます | `cja-root-cause-analysis`, `cja`, `dx-api`, `knowledge-graph` | Customer Journey Analytics（CJA） | 「チャネル別の収益を前月比で比較」 ・ 「モバイルとデスクトップのコンバージョンは、今四半期でどのように見えますか？」 |
| キャンペーンのパフォーマンス | 一定期間におけるキャンペーン、チャネル、web プロパティのパフォーマンスを測定。 | `cja`, `dx-api`, `knowledge-graph` | | 「先月のAcrobat web キャンペーンのパフォーマンスはどうでしたか？」 |
| Funnel analysis | 各段階での離脱を防ぐための、マルチステップのコンバージョンファネルを順を追って説明します | `cja` | Customer Journey Analytics（CJA） | 「チェックアウトのfunnelについて説明する」 ・ 「PDPから購入までのコンバージョンfunnelを表示する」 |
| 予測 | 過去のCJA データに基づく将来の指標値のプロジェクト | `cja` | Customer Journey Analytics（CJA） | 「今後30日間のセッションを予測」 ・「売上目標を達成する準備は整っているか？」 |
| [根本原因分析](data-insights/root-cause-analysis.md) | 指標が変化した理由：低下、急上昇、異常を診断します | `cja-root-cause-analysis` | Customer Journey Analytics（CJA） | 「先週、コンバージョンが下がったのはなぜですか？」 ・ 「1月15日の売上急増の要因は何か？」 |
| エグゼクティブサマリーとKPI ダイジェスト | 関係者に提供可能なパフォーマンスの要約、処方レコメンデーション、スライドデッキの概要を作成します | `cja-executive-summary`, `cja-bacom-anomaly-tracker-v2`, `cja-cno-weekly-pulse`, `cja-reporting`, `cja`, `dx-api` | Customer Journey Analytics（CJA） | 「先月のエグゼクティブサマリーを教えてください」 ・ 「今四半期のデータからスライドデッキの概要を作成します」 |
| [AA ↔ CJA データ検証](data-insights/data-validation-aa-cja.md) | 特にAdobe AnalyticsからCustomer Journey Analyticsにアップグレードする場合は、Adobe AnalyticsとCustomer Journey Analytics間でデータを比較、監査、調整できます | `aa-cja-validation`, `cja`, `dx-api` | ADOBE ANALYTICS + CJA | 「AA レポートスイートとCJA データビューの比較」 ・ 「AAとCJA間のページビューの検証」 |
| 運用時系列と因果関係分析 | オーディエンス、データセット、ジャーニーに関する過去の時系列データを、因果関係アトリビューションでクエリ、分析します | `operational-stats-causal-analysis` | すべての対象アプリケーション | 「過去90日間のオーディエンスサイズの傾向を表示」 ・ 「データセットの行数が3月3日に急増した理由」 |
| CJAのカスタムスキルの作成 | 分析パターンを、セッションをまたいで保持される、再利用可能で反復可能なスキルに変換します | `cja-skill-creator` | Customer Journey Analytics（CJA） | 「この週次売上分析を再利用可能なスキルに変換」 ・ 「これを月次funnel レポートのスキルとして保存」 |

## オーディエンス

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [自然言語からオーディエンスを作成](audiences/create-audience-from-natural-language.md) | 各段階で利用者の承認を得て、ステップバイステップのオーディエンス作成を連携できます | `audience-creation-flow` | Real-Time CDP（RTCDP） | 「過去30日以内に購入したユーザーのオーディエンスを作成」 ・ 「カリフォルニア州の価値の高いロイヤルティメンバー向けのセグメントを構築」 |
| PQL定義の作成 | XDMのプロパティ、行動イベント、既存のオーディエンスからオーディエンス定義を組み立て、集計と時間ウィンドウをサポート | `segment-definition-assembly` | Real-Time CDP（RTCDP） | 「3つ以上の商品を閲覧したが購入しなかった人のためにPQLを作成する」 ・ 「イベント条件に7日間の時間枠を追加する」 |
| オーディエンスの検索と発見 | ID、名前、セマンティック検索でオーディエンスを検索し、重複を検出して重複を分析 | `audience-search` | Real-Time CDP（RTCDP） | 「すべてのロイヤルティオーディエンスを検索」 ・ 「ホリデーショッパーのセグメントが重複していますか？」 |
| オーディエンスサイズの推定 | ポーリングを使用したAdobe Experience Platform Preview APIを使用して、PQL式のプロファイルリーチを推定します | `audience-size-estimate` | Real-Time CDP（RTCDP） | 「この聴衆の規模はどれくらいですか？」 ・ 「このPQL エクスプレッションのリーチを見積もる」 |
| オーディエンスサイズのウォーターフォール | PQLをサブ述語に分解し、各条件が最終的なオーディエンスサイズにどのように影響するかを示します | `audience-size-waterfall` | Real-Time CDP（RTCDP） | 「このPQLのウォーターフォールを見せてください」 ・ 「各条件がオーディエンスを減らす方法を分解してください」 |
| ターゲティング用のXDM フィールドの検索 | 名前、説明、データ値でフィールドを検索します。フィールドが存在する場所と、すでに使用されている場所を確認します | `field-discovery` | Real-Time CDP（RTCDP） | 「ロイヤルティ顧客のターゲティングに使用できるフィールドはどれですか？」 ・ 「購入履歴に関連するフィールドの検索」 |
| オーディエンスの公開/保存 | 命名規則とコンプライアンスチェックを使用して、Experience Platform Segmentation Serviceにオーディエンス定義を保持します | `audience-publish` | Real-Time CDP（RTCDP） | 「ドラフトとして保存」 ・ 「名前が「Spring Sale Buyers」のオーディエンスを公開」 |

## ジャーニー

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [自然言語からジャーニーを作成](journeys/create-journey-from-natural-language.md) | テキストプロンプトやアップロードされた画像/フローチャートから、AJOでジャーニー作成を調整できます | `journey-create` | Adobe Journey Optimizer（AJO） | 「登録後にメールを送信し、3日間待ってからフォローアップを送信するウェルカムジャーニーを作成する」 ・ 「アップロードされたフローチャート画像からジャーニーを作成する」 |
| ジャーニーの競合の分析 | オーディエンスの重複、スケジュールの競合、アクティブなジャーニー間の重複排除の問題を検出します | `journey-analyze-conflict` | Adobe Journey Optimizer（AJO） | 「カート放棄ジャーニーは他のジャーニーと競合しますか？」 ・ 「アクティブなジャーニー間のオーディエンスの重複をチェック」 |
| ジャーニーのフォールアウトを分析 | ジャーニーの途中で顧客が離脱する場所や理由を特定し、離脱につながる行動パターンを検出します | `journey-analyze-fallout` | Adobe Journey Optimizer（AJO） | 「リエンゲージメントの過程で離脱した顧客はどこにいますか？」 ・ 「ジャーニーXのどのノードのフォールアウトが最も高いか？」 |
| カスタムアクションエラーの分析 | カスタムアクションが失敗しているか、ジャーニー内でエラー率が急増しているかを特定し、失敗がより大きな混乱に連鎖する前に根本原因を診断できます | `journey-analyze-custom-action` | Adobe Journey Optimizer（AJO） | 「ロイヤルティ登録ジャーニーでカスタムアクションが失敗するのはなぜですか？」 ・ 「ウェルカムジャーニーのカスタムアクション ExternalPushのエラー率を表示する」 |
| [ ロイヤルティに関する課題の作成、編集、管理](journeys/create-loyalty-challenge.md) | ロイヤルティプログラム管理を簡素化し、迅速化したい | `loyalty` | Adobe Journey Optimizer（AJO） | 「会員に新しい季節の飲み物を試すように促すチャレンジを作成する」 ・ 「最も高い会員の脱落率でロイヤルティの課題を表示する」。 |

## 基本要素

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| 製品情報とドキュメント | Adobeの公式ドキュメントで、ハウツー、概念、トラブルシューティング、ベストプラクティスに関する質問に回答します | `product-knowledge` | すべての対象アプリケーション | 「ストリーミング宛先を設定するにはどうすればよいですか？」 ・ 「バッチセグメンテーションとストリーミングセグメンテーションの違いは何ですか？」 |
| Experience Platform / Journey Optimizer エンティティのクエリ | プラットフォームエンティティに関する質問の主要なエントリポイントとして機能し、必要に応じてKG、フィールドディスカバリー、またはAPIにルーティングできます | `operational-insights` | すべての対象アプリケーション | 「データセットはいくつありますか？」 ・ 「アクティブなジャーニーをすべて表示」 ・ 「宛先を一覧表示」 |
| ナレッジグラフクエリ | 単一のSQL クエリを使用したカウントの集計、エンティティ間の結合、関係検索、メタデータの検索 | `knowledge-graph` | すべての対象アプリケーション | 「どのオーディエンスがこのデータセットを使用しますか？」 ・ 「スキーマとデータセット間の関係を表示」 |
| Experience Platform/Journey Optimizer/Customer Journey Analytics APIの操作 | ナレッジグラフにない突然変異、リアルタイム状態チェック、およびエンティティタイプに対して、直接API ゲートウェイを提供します | `cxo-api` | すべての対象アプリケーション | 「データセット Xを削除」 ・ 「バッチ取り込みジョブのステータスを確認」 |
| エンティティの解決とリンク | セマンティック検索と字句検索を使用して、実際のExperience Platform エンティティに対するエンティティのメンションを解決し、XDM フィールドを検出します | `entity-linking` | Adobe Experience Platform | 「実際のオーディエンスに『ホリデーショッパー』を解決する」 ・「購入履歴に関連するフィールドを検索する」 |
| カスタムスキルの管理 | 再利用可能なユーザー所有スキルを保存、変更、削除できます。これらのスキルは、セッションをまたいで保持されます | `manage-skill` | すべての対象アプリケーション | 「そのワークフローをスキルとして保存」 ・ 「週次レポートスキルを削除」 ・ 「これを再利用可能なスキルに変換」 |

## サンドボックスツール

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [ サンドボックス間でオブジェクトを移動](/help/agents/sandbox-tooling.md) | 依存関係を自動解決し、スキーマ、オーディエンス、その他のオブジェクト設定をサンドボックス間でシームレスに移行できます | `sandbox-tooling-workflow` | Adobe Experience Platform | 「スキーマのLuma Loyalty Members Platinumを現在のサンドボックスから実稼動サンドボックスに移動」 ・ 「US Gold Loyalty Members オーディエンスをステージに昇格させる」 |
