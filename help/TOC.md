---
audience: user
user-guide-title: CX Enterprise の AI
user-guide-description: 実用的なドキュメント、実装ガイダンス、参考資料を通じて、AI アシスタント、同僚、エージェント、MCPの構築、設定、統合、拡張の方法を学びましょう。
description: 顧客体験におけるAI ツールについて詳しく見る。 CX EnterpriseのAIを使用して、製品知識を向上させ、運用上のインサイトを得ることができます。
solution: Experience Cloud
role: Admin,User,Developer,Leader
dummy: true
source-git-commit: 7b207cc5ff5f53df5bc0684fb48ac98186f23393
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 18%

---


# CX Enterprise の AI {#experience-cloud-ai}

- [CX エンタープライズアプリケーションにおけるAI](home.md)
- CX エンタープライズにおけるAIについて {#overview}
  - [どのように拡大するのか](./overview/generative-ai.md)
  - [エージェンティック AIについて](./overview/agentic-ai.md)
  - [AI クレジットの使用について](./overview/ai-credit-consumption.md)
  - [Agentic AI モニタリングダッシュボード](./overview/monitoring.md)
  - [エージェント型ツール](https://experienceleague.adobe.com/ja/docs/cx-enterprise-agentic-tools/using/overview)
  - [生成AI コンテンツの透明性](content-transparency.md)
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
  - [Adobe CX Coworker Gateway](./mcp/overview.md)
  - {hide-from-toc}[Real-Time CDP MCP ベータ版](./mcp/beta/rtcdp-mcp.md)
  - 基本を学ぶ {#mcp-get-started}
    - [CX Coworker Gateway ツールへのアクセス](./mcp/access.md)
    - [CX Coworker Gatewayのインストール](./mcp/install.md)
    - [CX Coworker Gatewayのセッションコンテキストツール](./mcp/context-tools.md)
  - 製品ツール {#mcp-product-tools}
    - [Real-Time CDP tools](./mcp/rtcdp-mcp.md)
    - [Experience Platform tools](./mcp/aep-mcp.md)
    - [Journey Optimizer tools](./mcp/ajo-mcp.md)
    - [Customer Journey Analytics tools](./mcp/cja-mcp.md)
    - [Adobe Analytics tools](./mcp/analytics-mcp.md)
    - [Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview)
- Coworker {#coworker}
  - [Cowakerについて](./coworker/overview.md)
  - キャンペーン {#campaigns}
    - [概要](./coworker/campaigns/overview.md)
    - [メールキャンペーンの作成](./coworker/campaigns/create-an-email-campaign.md)
    - [ユースケース](./coworker/campaigns/use-cases.md)
    - [プロンプトのベストプラクティス](./coworker/campaigns/prompting-best-practices.md)
    - [C2PA メタデータ](./coworker/campaigns/c2pa-metadata.md)
    - コネクタ {#connectors}
      - [Marketo Engage](./coworker/campaigns/connectors/marketo.md)
      - [Hubspot](./coworker/campaigns/connectors/hubspot.md)
    - [リリースノート](./coworker/campaigns/release-notes.md)
  - カスタマイズ {#customizations}
    - スキル {#skills}
      - [スキルとは？](./coworker/customizations/skills/what-are-skills.md)
      - [最初のスキルを作成](./coworker/customizations/skills/create-your-first-skill.md)
  - チャット {#chat}
    - [概要](./coworker/chat/overview.md)
    - [UI ガイド](./coworker/chat/ui-guide.md)
    - ユースケース {#use-cases}
      - [Adobe Workfrontのユースケース](./coworker/chat/use-cases/overview.md)
      - データインサイト {#data-insights}
        - [CJAデータの分析](./coworker/chat/use-cases/data-insights/analytics-chat.md)
        - [トレンドと根本原因を探る](./coworker/chat/use-cases/data-insights/root-cause-analysis.md)
        - [アップグレード時にAAからCJA データを検証する](./coworker/chat/use-cases/data-insights/data-validation-aa-cja.md)
      - オーディエンス {#audiences}
        - [プラットフォームの健全性を評価し、オーディエンスを構築する](./coworker/chat/use-cases/audiences/create-audience-from-natural-language.md)
      - ジャーニー {#journeys}
        - [自然言語を使用したジャーニーの作成](./coworker/chat/use-cases/journeys/create-journey-from-natural-language.md)
        - [ロイヤルティに関する課題を作成し、インサイトを獲得](./coworker/chat/use-cases/journeys/create-loyalty-challenge.md)
  - {hide-from-toc}[遊び場での共同作業チャット](./coworker/playground-coworker-chat.md)
    - [ エージェント型スキルのサンドボックスツール](./agents/sandbox-tooling.md)
    - [顧客アラートのスキル ](./agents/customer-alert-skills.md)
