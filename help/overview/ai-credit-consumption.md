---
title: AI クレジット消費
description: CX エンタープライズアプリケーションでのAI クレジットの消費について説明します。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
last-update: '2026-05-21T00:00:00.000Z'
feature_v2: id: f84b2906-3ce9-4ef0-86f6-cda249273937
source-git-commit: 34a3227d726a6249a6dedea420828b84ad1547a7
workflow-type: tm+mt
source-wordcount: 966
ht-degree: 5%

---

# AI クレジットの消費

CX エンタープライズアプリケーションでのAI クレジットの消費について説明します。

## AI クレジット

_AI クレジット_&#x200B;は、アクションまたはジョブの実行を定量化する使用状況ベースの指標です。

## AI クレジットを使用する対象サービス

* [CX Enterprise Coworker](#cx-enterprise-coworker-credit-rate)
* [AEP Agents](#aep-agents-credit-rate)

### CX Enterprise Coworkerのクレジット率

導入期間が限られている場合、同僚の入力は、1入力あたり25個のAI クレジットの割合でAI クレジットを使用します。 この料金は期間限定で、変更される場合があります。

### AEP Agentsのクレジット率

_エージェントジョブ_&#x200B;は、お客様からの指示に従って、AEP エージェントが特定の結果を得るために実行する一連のタスクとアクションです。

AI アシスタントによる自然言語プロンプトを使用し、エージェントに特定のジョブの実行を依頼できます。 これらのデータに基づいて、Agent Orchestratorは適切な担当者を調整し、関連するCX Enterprise アプリケーション内の各ステップを実行します。

AIによるクレジットの使用状況は、実行されるジョブの複雑さと価値によって異なります。

* 単純な（多くの場合シングルステップ）タスクでは、クレジットの消費が少なくなります
* 複雑な（多くの場合マルチステップ）タスクでは、より多くのクレジットが消費されます
* 高度な推論、検証、マルチエージェントの調整、または統合を伴うタスクは、より多くのクレジットを消費します

ライセンス済みのCX Enterprise アプリケーションで使用可能なAEP AgentsとAgent ジョブを確認するには、[CX Enterprise Agentic AI機能カタログ ](https://agentic-capability-explorer.entapp.adproto.com/)を参照してください。

#### エージェントの予測ジョブのクレジット率

| エージェント | ジョブ | サポートされているアプリケーション | 推定AI クレジット | サンプルプロンプト |
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Audience Agent | オーディエンス/アカウントのアイデア立案 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 50 | <ul><li><em>富裕層の購入者のフィールドを表示</em></li><li><em>顧客の環境設定に関連するすべてのフィールドを検索</em></li></ul> |
| Audience Agent | オーディエンス/アカウント管理 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li><em>重複するオーディエンスがありますか？</em></li><li><em>最大5人のオーディエンスを表示します。</em></li><li><em>どの宛先にもアクティブ化されていないオーディエンスを表示</em></li><li><em> ライブジャーニーで使用されているすべてのオーディエンスを一覧表示</em></li></ul> |
| Audience Agent | オーディエンス/アカウント分析 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2C Edition）</li></ul> | 25 | <ul><li><em>先週20%以上増加したオーディエンスはどれですか？</em></li><li><em>30日前の値と比較して、オーディエンス「ロイヤルプラチナ」はどの程度変化していますか？</em></li><li><em>最も急成長しているオーディエンスは何ですか？</em></li></ul> |
| Audience Agent | 購買グループのアイデア創出 | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li><em>これらの製品の意図を示しているアカウントはどれですか？</em></li><li><em>XYZの製品インテント別の上位の人物を表示します。</em></li><li><em>5人以上のメンバーがいる購買グループはどれですか？</em></li></ul> |
| Data Insights Agent | データ分析と可視化 | <ul><li>Customer Journey Analytics（B2CおよびB2B エディション）</li></ul> | 25 | <ul><li><em>7月のトレンド注文</em></li><li><em>地域別の収益を表示します。</em></li><li><em>3月から6月までの性別で注文を表示します。</em></li><li><em>6月の利益別の上位10のSKUは何ですか</em></li><li><em>月別の購入割合</em></li><li><em>製品カテゴリ別の収益の割合</em></li></ul> |
| Journey Agent | ジャーニーの構想 | <ul><li>Adobe Journey Optimizer（B2B edition）</li></ul> | 25 | <ul><li><em>Web サイト上のコンテンツでエンゲージしているユーザーに焦点を当て、ソリューションの意図を持って空白アカウントのジャーニーを作成します</em></li></ul> |
| Journey Agent | ジャーニー分析 | <ul><li>Adobe Journey Optimizer（B2BおよびB2C エディション）</li></ul> | 50 | <ul><li><em>7月4日のキャンペーンのジャーニーのノード別のフォールアウトを分析します。</em></li><li><em> ジャーニーX</em>のスケジュールに競合があります</li><li><em> ジャーニーX</em>のオーディエンス重複の競合を表示する</li></ul> |
| Journey Agent | ジャーニー管理 | <ul><li>Adobe Journey Optimizer（B2BおよびB2C エディション）</li></ul> | 25 | <ul><li><em> ライブジャーニーはいくつありますか？</em></li><li><em> オーディエンス X.</em>を使用するすべてのジャーニーを一覧表示する</li><li><em>現在テストモードにあるすべてのジャーニーを一覧表示</em></li></ul> |
| 製品サポート担当者 | ナレッジベースのトラブルシューティング | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2CおよびB2B エディション）</li><li>Customer Journey Analytics（B2CおよびB2B エディション）</li></ul> | 0 | <ul><li><em> ライセンス使用状況ダッシュボードとExperience Platform ホームページでプロファイル数が異なるのはなぜですか？</em></li><li><em> ジャーニーがトリガーされない理由は何ですか？</em></li><li><em>Adobe Experience Platformでは、リアルタイムのエクスペリエンスをどのように構築できますか？</em></li><li><em>Adobe Experience Platformでアラートを設定および使用する方法は？</em></li><li><em>Adobe Experience Platform アクティベーションの平均プロファイルリッチネス制限は何ですか？</em></li></ul> |
| 製品サポート担当者 | サポートケースの作成と追跡 | <ul><li>Real-Time CDP（B2B、B2C、B2P エディション）</li><li>Adobe Journey Optimizer（B2CおよびB2B エディション）</li><li>Customer Journey Analytics（B2CおよびB2B エディション）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li><em>失敗したセグメント化ジョブの新しいサポートチケットを作成</em></li><li><em>E-001772068 チケットのステータスは？</em></li></ul> |
| Content Advisor エージェント | コンテンツ発見 | <ul><li>Adobe Experience Manager</li></ul> | 5 | <ul><li><em>WKND オファーキャンペーンを作成するためのコンテンツフラグメントを表示します。</em></li><li><em>製品パッケージ PNG画像を検索します。</em></li><li><em>WKND フォルダー内のOffice タグ付きの画像を表示します。</em></li><li><em> フォルダーWKNDにsvgsがありますか？</em></li><li><em>すべてのローン申し込みフォームを表示します。</em></li><li><em>従業員のオンボーディングフォームを探しています。</em></li></ul> |
| Content Advisor エージェント | <ul><li>コンテンツの最適化</li></ul> | <ul><li>Adobe Experience Manager AssetsとDynamic Media</li></ul> | 10 | <ul><li><em>80%の画質で2000 pxのレンディションをJPEGとして作成します。</em></li><li><em>Instagram ストーリーのレンディションを作成します。</em></li><li><em> プロモーションバナーの上に30%割引のグラフィックで画像をオーバーレイし、中央から100 px配置します。</em></li><li><em>PNGの背景色を#ff8932に変更します。</em></li></ul> |
| Brand Governance エージェント | <ul><li>ブランドポリシーチェック</li></ul><ul><li>Content Hubでの権限</li></ul><ul><li>アセットの有効期限</li></ul> | <ul><li>Adobe Experience Manager Sites（ブランドポリシー）</li></ul><ul><li>Adobe Experience Manager Assets</li></ul> | 25 | <ul><li><em>このページはブランドと一致していますか？`https://www.website/en.html`</em></li><li><em>既存のすべてのContent Hub ABAC ルールを表示</em></li><li><em> アセットの有効期限がまもなく切れますか？</em></li></ul> |
| Brand Experience Agent | <ul><li>コンテンツの更新</li><li>Formsによる制作</li><li>パイプラインのトラブルシューティング</li></ul> | <ul><li>Adobe Experience Manager Cloud Services</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li><em>`URL`に、見出しをHello world</em>に更新します</li><li><em>名前、電子メール、メッセージフィールドを使用して連絡先フォームを作成する</em></li><li><em>失敗したパイプラインのトラブルシューティング </em></li><li><em>失敗したパイプラインをメイン プログラムに一覧表示します。</em></li></ul> |
| Brand Experience Agent | サイトの近代化 | Adobe Experience Manager Cloud Services | 100 | <ul><li><em> ページを移行`https://wknd-trendsetters.site`</em></li></ul> |

>[!NOTE]
>
>実際のAIのクレジット消費量は、実行されるステップの数と1 ステップあたりのイテレーションによって異なる場合があります。

## このトピックの詳細ヘルプ

* [CX エンタープライズにおける生成AI](generative-ai.md)
* [CX Enterprise のエージェント型 AI](agentic-ai.md)
* [Adobe Experience Platform Agents利用制限トライアル](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
