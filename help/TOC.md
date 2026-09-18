---
audience: user
user-guide-title: CX Enterprise の AI
user-guide-description: 実用的なドキュメント、実装ガイダンス、参考資料を通じて、AI アシスタント、同僚、エージェント、MCPの構築、設定、統合、拡張の方法を学びましょう。
description: 顧客体験におけるAI ツールについて詳しく見る。 CX EnterpriseのAIを使用して、製品知識を向上させ、運用上のインサイトを得ることができます。
solution: Experience Cloud
role: Admin,User,Developer,Leader
dummy: true
source-git-commit: 4ae7aa9127368da137582ce3aad3259fa815a497
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 20%
---

# CX Enterprise の AI {#experience-cloud-ai}

- [CX Enterprise の AI](home.md)
- CX エンタープライズにおけるAIについて {#overview}
  - [CX エンタープライズにおけるAIについて](./overview/overview-ai-cxe.md)
  - [どのように拡大するのか](./overview/generative-ai.md)
  - [エージェンティック AIについて](./overview/agentic-ai.md)
  - [AI クレジットの使用について](./overview/ai-credit-consumption.md)
  - [Agentic AI モニタリングダッシュボード](./overview/monitoring.md)
  - [エージェント型ツール](https://experienceleague.adobe.com/ja/docs/cx-enterprise-agentic-tools/using/overview)
  - [生成 AI コンテンツの透明性](content-transparency.md)
- CX Enterprise Coworker {#coworker}
  - [Cowakerについて](./coworker/overview.md)
  - チャット {#chat}
    - [概要](./coworker/chat/overview.md)
    - [UI ガイド](./coworker/chat/ui-guide.md)
    - {hide-from-toc}[遊び場での同僚のチャット &#x200B;](./coworker/playground-coworker-chat.md)
    - ユースケース {#use-cases}
      - [Adobe Workfrontのユースケース](./coworker/chat/use-cases/overview.md)
      - データインサイト {#data-insights}
        - [CJAデータの分析](./coworker/chat/use-cases/data-insights/analytics-chat.md)
        - [トレンドと根本原因を探る](./coworker/chat/use-cases/data-insights/root-cause-analysis.md)
        - [アップグレード時にAAからCJA データを検証する](./coworker/chat/use-cases/data-insights/data-validation-aa-cja.md)
        - [CJA レポート用のデータセット品質の検証](./coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)
      - オーディエンス {#audiences}
        - [プラットフォームの健全性を評価し、オーディエンスを構築する](./coworker/chat/use-cases/audiences/create-audience-from-natural-language.md)
      - ジャーニー {#journeys}
        - [自然言語を使用したジャーニーの作成](./coworker/chat/use-cases/journeys/create-journey-from-natural-language.md)
      - ロイヤルティ {#loyalty}
        - [ロイヤルティに関する課題を作成し、インサイトを獲得](./coworker/chat/use-cases/journeys/create-loyalty-challenge.md)
      - 最適化 {#optimization}
        - [Target アクティビティの起動](./coworker/chat/use-cases/optimization/target.md)
      - サンドボックスツール {#sandbox-tooling}
        - [エージェント型スキルのサンドボックスツール](./agents/sandbox-tooling.md)
      - アラート {#alerts}
        - [顧客アラートのスキル](./agents/customer-alerts.md)
      - Content Advisor {#content-advisor}
        - [マーケティングアセットの生成](./coworker/chat/use-cases/content-advisor/generate-assets.md)
        - [ブランドコンプライアンスのチェック](./coworker/chat/use-cases/content-advisor/brand-compliance.md)
  - カスタマイズ {#customizations}
    - スキル {#skills}
      - [スキルとは？](./coworker/customizations/skills/what-are-skills.md)
      - [最初のスキルを作成](./coworker/customizations/skills/create-your-first-skill.md)
      - [高品質なゲートスキルの構築と実行](./coworker/customizations/skills/run-a-quality-gate-skill.md)
      - [スキルの管理と繰り返し](./coworker/customizations/skills/manage-and-iterate-on-skills.md)
  - キャンペーン {#campaigns}
    - [概要](./coworker/campaigns/overview.md)
    - [メールキャンペーンの作成](./coworker/campaigns/create-an-email-campaign.md)
    - {hide-from-toc}[&#x200B; キャンペーンを起動して管理](./coworker/campaigns/launch-manage-campaign.md)
    - [ユースケース](./coworker/campaigns/use-cases.md)
    - [プロンプトのベストプラクティス](./coworker/campaigns/prompting-best-practices.md)
    - [C2PA メタデータ](./coworker/campaigns/c2pa-metadata.md)
    - コネクタ {#connectors}
      - [Marketo Engage](./coworker/campaigns/connectors/marketo.md)
      - [Hubspot](./coworker/campaigns/connectors/hubspot.md)
    - [リリースノート](./coworker/campaigns/release-notes.md)
- AI アシスタント {#ai-assistant}
  - [AI アシスタント UI ガイド](./ai-assistant/ai-assistant-ui.md)
  - [プロンプトライブラリ](./ai-assistant/prompt-library.md)
  - [プライバシー](./ai-assistant/privacy.md)
  - [免責事項](./ai-assistant/legal-disclaimer.md)
- Agents {#agents}
  - [Agent Orchestrator](./agents/agent-orchestrator.md)
  - [Audience Agent](./agents/audience.md)
  - [Data Insights Agent](./agents/cja-data-insights-agent.md)
  - [実験エージェント](./agents/agent-experiment.md)
  - [Field Discovery エージェント](./agents/field-discovery-agent.md)
  - [Journey Agent](./agents/ajo-agent.md)
  - [製品サポート担当者](./agents/product-support.md)
  - [Adobe Marketing Agent for Microsoft 365 Copilot](./agents/ama-ms.md)
  - [Notifications エージェント](./agents/notifications.md)
  - [共同作業者の体験版](./agents/trial.md)
  - [データの検証](./agents/data-validation.md)
  - Data Engineering {#data-engineering}
    - {hide-from-toc}[Data Engineering Agent](./agents/data-engineering/overview.md)
- MCP {#mcp}
  - {hide-from-toc}[Adobe CX Coworker Gateway](./mcp/overview.md)
  - {hide-from-toc}[Real-Time CDP MCP ベータ版](./mcp/beta/rtcdp-mcp.md)
  - 基本を学ぶ {#mcp-get-started}
    - {hide-from-toc}[CX Coworker Gateway Toolsへのアクセス](./mcp/access.md)
    - {hide-from-toc}[CX Coworker Gatewayのインストール &#x200B;](./mcp/install.md)
    - {hide-from-toc}[CX Coworker Gatewayの セッションコンテキストツール &#x200B;](./mcp/context-tools.md)
  - 製品ツール {#mcp-product-tools}
    - {hide-from-toc}[Real-Time CDP ツール &#x200B;](./mcp/rtcdp-mcp.md)
    - {hide-from-toc}[Experience Platform ツール &#x200B;](./mcp/aep-mcp.md)
    - {hide-from-toc}[Journey Optimizer ツール &#x200B;](./mcp/ajo-mcp.md)
    - {hide-from-toc}[Customer Journey Analytics ツール &#x200B;](./mcp/cja-mcp.md)
    - {hide-from-toc}[Adobe Analytics ツール &#x200B;](./mcp/analytics-mcp.md)
    - [Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview)
    - [ターゲット](https://experienceleague.adobe.com/en/docs/target/using/mcp/target-mcp)

