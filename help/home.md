---
title: CX エンタープライズアプリケーションにおけるAI
description: CX エンタープライズアプリケーションで生成AI （GenAI）、AI アシスタント、エージェンティック AI、CX エンタープライズパートナー、MCP ツールをどのように使用するかをご確認ください。
TQID: https://experienceleague.adobe.com/heALjEZbowNaygG24oOM2HSlHa9oYVI5ViUNZDr19Ds
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: d8daade8bb7d0259cd18fe7c8f957955dd97b2a0
workflow-type: tm+mt
source-wordcount: 766
ht-degree: 2%

---

# CX Enterprise の AI

このガイドでは、Adobe CX Enterprise アプリケーション全体で利用できるAI機能について説明します。製品情報と運用上のインサイトのための生成AIとAI アシスタント、業務を自動化するためのAgent OrchestratorとExperience Platform Agents、完全会話型でエージェントファーストのエクスペリエンスを実現するCX Enterprise Coworker、独自のAI ツールをCX Enterprise データに接続するためのMCPです。

## CX エンタープライズにおけるAIについて

CX Enterpriseのどこで、どのようにAIが使用されているかについては、こちらをご覧ください。

- [生成AI](./overview/generative-ai.md)は、生成AIとAI アシスタントをサポートするCX エンタープライズ アプリケーションと、それらの比較方法について説明します。
- [Agentic AI](./overview/agentic-ai.md)は、Experience Platform Agentsが既存のCX Enterprise アプリケーションとAI ファースト アプリケーションの両方でどのように機能するかを説明し、それぞれに使用可能なエージェントを一覧表示します。
- [ エージェンティック AI モニタリング ](./overview/monitoring.md)では、エージェントの導入、使用、フィードバック、AI クレジット消費を追跡するダッシュボードについて説明します。
- [ エージェントのジョブとAI クレジットの消費](./overview/ai-credit-consumption.md)は、AI クレジットがエージェントのジョブによって消費される仕組みを説明し、エージェントとジョブのタイプ別の推定消費率を示します。

## AI アシスタント

[AI アシスタント ](./ai-assistant/ai-assistant-ui.md)は、Adobe Experience Platform ベースのアプリケーションで利用できる会話型の生成AI ツールです。 フルスクリーンまたはレールビューのインターフェイスで自然言語プロンプトを使用し、製品情報の取得、問題のトラブルシューティング、運用上のインサイトの取得、Experience Platform Agentsへのアクセスに使用できます。

[AI アシスタント UI ガイド ](./ai-assistant/ai-assistant-ui.md)を読んで、インターフェイスのナビゲーション方法と、エージェントによるプロンプト例の[ プロンプトライブラリ ](./ai-assistant/prompt-library.md)を確認してください。

## Agent OrchestratorおよびExperience Platform agents

[Agent Orchestrator](./agents/agent-orchestrator.md)は、Experience Platform Agentsを強化するエージェント型レイヤーです。 AI アシスタントに質問すると、Agent Orchestratorが作業を計画し、その回答に必要な専門スタッフを呼び出し、人間の監視下で一元的な回答を返します。

このガイドでは、次のExperience Platform Agentsについて説明します。

- [Audience Agent](./agents/audience.md)
- [Data Insights Agent](./agents/cja-data-insights-agent.md)
- [Experimentation Agent](./agents/agent-experiment.md)
- [Field Discovery エージェント](./agents/field-discovery-agent.md)
- [Journey Agent](./agents/ajo-agent.md)
- [Notifications エージェント](./agents/notifications.md)
- [製品サポート担当者](./agents/product-support.md)
- [Adobe Marketing Agent for Microsoft 365 Copilot](./agents/ama-ms.md)

エージェントの完全なリスト、各アプリケーションがサポートするアプリケーション、および適格要件については、「[Agentic AI in CX Enterprise](./overview/agentic-ai.md)」を参照してください。

## CX Enterprise Coworker

CX Enterprise Coworkerは、AI アシスタントのエージェントファーストの進化です。 自然言語で目標を説明します。Coworkerは、一度に1つの質問をする代わりに、作業を計画し、Adobeと接続されたシステムをまたいで実行し、結果を検証し、完成した作業を承認のために返します。 チームメンバーは次の通りです。

- **同僚チャット**: データを探索し、オーディエンスとジャーニーを検証し、CX エンタープライズ アプリケーション全体でマルチステップのタスクを完了するための会話型インターフェイスです。
- **同僚キャンペーン**: キャンペーンの概要、オーディエンスの作成、コンテンツ生成、ジャーニー設計、プルーフを単一の会話体験に統合するAI ネイティブのアプリケーションです。

適格な顧客は、AI アシスタントやExperience Platform AgentsからCoworker Chatへ徐々に移行しています。 体験版の利用条件、AI クレジットの使用状況、アクセス方法については、[CX Enterprise Coworker Trial](./agents/trial.md)を参照してください。

Coworker Chatの実際の動作を確認するには、Playground](./coworker/playground-coworker-chat.md)の[Coworker Chatを説明するか、[AAからCJAへの移行データの検証](./coworker/data-validation-aa-cja.md)や[ コンバージョンのドロップオフの分析](./coworker/analytics-chat.md)などの実際のユースケースを読んでください。

## MCP

[Adobe CX Coworker Gateway](./mcp/overview.md)は、CX Enterpriseの統合モデル コンテキスト プロトコル （MCP） エンドポイントです。 [!DNL Claude]、[!DNL ChatGPT]、[!DNL Cursor]などのMCP対応クライアントを使用できます。これらのクライアントは、Real-Time CDP、Experience Platform、Journey Optimizer、Customer Journey Analytics、Adobe Analyticsなど、組織が使用する権限を持つ製品ツールへの1つの管理された接続です。

## 基本を学ぶ

### アクセス要件

AI アシスタントとExperience Platform Agentsを使用する前に、Adobe管理者が適切な権限を付与する必要があります。 要件はアプリケーションによって異なります。詳しくは、Agent Orchestrator ガイドの[ アクセス ](./agents/agent-orchestrator.md#access)を参照してください。

### プライバシーとセキュリティ

AI アシスタントとExperience Platform Agentsは、サンドボックスに特化したデータ分離や既存のアクセス制御ポリシーの遵守など、プライバシー、セキュリティ、ガバナンスを最優先事項として構築されています。 詳しくは、[AI アシスタントのプライバシー、セキュリティ、ガバナンス ](./ai-assistant/privacy.md)を参照してください。

## ベストプラクティス

AI アシスタントや共同作業者の体験から最大限の価値を引き出すには、次のベストプラクティスに従ってください。

- ターゲットを絞った適切なインサイトを取得するには、プロンプトに&#x200B;**具体的な**&#x200B;を入力します。
- **提供されたソースの引用と説明を確認して、応答**&#x200B;を検証します。
- **コンテキスト設定**&#x200B;を使用して、最も関連性の高いデータソースを質問に使用します。
- **パフォーマンスと精度を長期的に改善するためにフィードバック**&#x200B;を提供します。
- **複数のエージェントからのインサイト**&#x200B;を組み合わせて、より包括的な分析を実行します。

## 法的考慮事項

現在、AI アシスタントは英語のみで回答をサポートしており、言語モデルが間違いを犯すこともあります。 提供された情報を必ず検証し、各回答に含まれる推論手順に従って、どのように生成されたかを把握します。 詳しくは、[法的免責事項](./ai-assistant/legal-disclaimer.md)を参照してください。
