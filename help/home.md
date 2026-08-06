---
title: CX Enterprise アプリケーションの AI
description: CX エンタープライズアプリケーションで生成AI （GenAI）、AI アシスタント、エージェンティック AI、CX エンタープライズパートナー、MCP ツールをどのように使用するかをご確認ください。
TQID: https://experienceleague.adobe.com/heALjEZbowNaygG24oOM2HSlHa9oYVI5ViUNZDr19Ds
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4da8c6f87f4227983b19c682fdceb0db9a352122
workflow-type: tm+mt
source-wordcount: 862
ht-degree: 4%

---

# CX Enterprise の AI

このガイドでは、Adobe CX EnterpriseのAI機能（生成AI、AI アシスタント、Agent Orchestrator、Experience Platform Agents、CX Enterprise Workfront、MCP）について説明します。

## AI機能の概要

CX Enterpriseのどこで、どのようにAIが使用されているかについては、こちらをご覧ください。

- [生成AIについて](./overview/generative-ai.md)は、生成AIとAI アシスタントをサポートするCX エンタープライズ アプリケーションと、それらの比較方法について説明します。
- [ エージェント型AIについて](./overview/agentic-ai.md)は、Experience Platform Agentsが既存のCX Enterprise アプリケーションとAI ファースト アプリケーションの両方でどのように機能するかを説明し、それぞれに使用可能なエージェントを一覧表示します。
- [AI モニタリング ](./overview/monitoring.md)では、エージェントの導入、使用状況、フィードバック、AI クレジット消費を追跡するダッシュボードについて説明します。
- [AI クレジットの消費](./overview/ai-credit-consumption.md)は、エージェント ジョブがAI クレジットを消費する方法を、エージェントとジョブのタイプ別の推定消費率で説明します。
- [CX エンタープライズ エージェント ツール ](https://experienceleague.adobe.com/ja/docs/cx-enterprise-agentic-tools/using/overview)では、CX エンタープライズ エージェントを拡張する追加のエージェント スキルとツールについて説明します（ビデオ チュートリアル）。

## AI アシスタント

[AI アシスタント ](./ai-assistant/ai-assistant-ui.md)は、Adobe Experience Platform ベースのアプリケーションで利用できる会話型の生成AI ツールです。 フルスクリーンまたはレールビューのインターフェイスで自然言語プロンプトを使用し、製品情報の取得、問題のトラブルシューティング、運用上のインサイトの取得、Experience Platform Agentsへのアクセスに使用できます。

インターフェイスのナビゲーション方法については、[AI アシスタント UI ガイド ](./ai-assistant/ai-assistant-ui.md)を参照してください。 エージェント別のプロンプトの例については、[ プロンプトライブラリ ](./ai-assistant/prompt-library.md)を参照してください。

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
- [データの検証](./agents/data-validation.md)

エージェントの完全なリスト、各アプリケーションがサポートするアプリケーション、および適格要件については、「[Agentic AI in CX Enterprise](./overview/agentic-ai.md)」を参照してください。

## 同僚

Coworkerは、顧客体験とマーケティングのワークフローを自動化するAI アシスタントの進化であり、日常的な実行ではなくビジネス目標に集中することができます。 一度にひとつの質問をする代わりに、目標を記述します。 チームメンバーは、完成した作業を計画、実行、検証し、承認のために返します。 チームメンバーは次の通りです。

- **[同僚チャット ](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/overview)**: データを探索し、オーディエンスとジャーニーを検証し、CX エンタープライズ アプリケーション全体でマルチステップのタスクを完了するための会話型インターフェイスです。
- **[同僚キャンペーン ](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/campaigns/overview)**: キャンペーンの概要、オーディエンスの作成、コンテンツ生成、ジャーニー設計、プルーフを単一の会話体験に統合するAI ネイティブのアプリケーションです。 組み込みのテンプレート、ベストプラクティス、プロンプトガイダンスを利用して、小規模なアジャイルチームが施策を迅速に立ち上げるのを支援します。
- **同僚プロジェクト** （近日リリース予定）: エンドツーエンドの顧客体験オーケストレーションワークフローを自動化し、チームがタスク、承認、実行を調整して、戦略から納品までの成果を促進するための統合ワークスペースです。 プロジェクトのドキュメントは近日公開予定です。

適格な顧客は、AI アシスタントやExperience Platform AgentsからCoworker Chatへ徐々に移行しています。 [同僚の体験版](./agents/trial.md)を読んで、体験版の利用条件、AI クレジットの使用状況、アクセス方法について確認してください。

Coworker Chatの実際の動作を確認するには、Playground](./coworker/playground-coworker-chat.md)の[Coworker Chatを説明するか、[AAからCJAへの移行データの検証](./coworker/data-validation-aa-cja.md)や[Analyze CJA data](./coworker/chat/analytics-chat.md)などの実際のユースケースを読んでください。

共同作業者チャット、キャンペーン、プロジェクトに関する完全な製品ドキュメントについては、[共同作業者](./coworker/overview.md)を参照してください。 サンドボックス間のオブジェクトレプリケーションについては、[Sandbox Tooling Agentic Skills](./agents/sandbox-tooling.md)を参照してください。

## MCP

[Adobe CX Coworker Gateway](./mcp/overview.md)は、CX Enterpriseの統合モデル コンテキスト プロトコル （MCP） エンドポイントです。 [!DNL Claude]、[!DNL ChatGPT]、[!DNL Cursor]などのMCP互換クライアントを、組織が使用できる製品ツールへの単一の管理された接続として提供します。 これらのツールには、[!DNL Real-Time CDP]、[!DNL Experience Platform]、[!DNL Journey Optimizer]、[!DNL Customer Journey Analytics]、[!DNL Adobe Analytics]および[!DNL Workfront]が含まれます。

CX Coworker Gatewayを初めて利用する場合 接続するには、[CX Coworker Gateway tools](./mcp/access.md)および[CX Coworker Gateway](./mcp/install.md)のインストールを参照してください。

## 基本を学ぶ

### アクセス要件

AI アシスタントとExperience Platform Agentsを使用する前に、Adobe管理者が適切な権限を付与する必要があります。 要件はアプリケーションによって異なります。詳しくは、Agent Orchestrator ガイドの[ アクセス ](./agents/agent-orchestrator.md#access)を参照してください。

### プライバシーとセキュリティ

AI アシスタントとExperience Platform Agentsは、サンドボックスに特化したデータ分離や既存のアクセス制御ポリシーなど、プライバシー、セキュリティ、ガバナンスを優先します。 詳しくは、[AI アシスタントのプライバシー、セキュリティ、ガバナンス ](./ai-assistant/privacy.md)を参照してください。

## ベストプラクティス

AI アシスタントや共同作業者の体験から最大限の価値を引き出すには、次のベストプラクティスに従ってください。

- ターゲットを絞った適切なインサイトを取得するには、プロンプトに&#x200B;**具体的な**&#x200B;を入力します。
- **提供されたソースの引用と説明を確認して、応答**&#x200B;を検証します。
- **コンテキスト設定**&#x200B;を使用して、最も関連性の高いデータソースを質問に使用します。
- **パフォーマンスと精度を長期的に改善するためにフィードバック**&#x200B;を提供します。
- **複数のエージェントからのインサイト**&#x200B;を組み合わせて、より包括的な分析を実行します。

## 法的考慮事項

現在、AI アシスタントは英語での回答のみをサポートしており、言語モデルは時々ミスを犯します。 提供された情報を必ず検証し、各回答に含まれる推論手順に従って、どのように生成されたかを把握します。 詳しくは、[法的免責事項](./ai-assistant/legal-disclaimer.md)を参照してください。

