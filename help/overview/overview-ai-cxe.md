---
title: CX エンタープライズにおけるAIについて
description: CX Enterpriseのさまざまなアプリケーションで生成AIとAgentic AIがどのように利用できるかを解説します。まずは、アクセス、プライバシー、セキュリティ要件を確認しましょう。
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
    internal-label: CX Enterprise Coworker
feature_v2:
  - id: f84b2906-3ce9-4ef0-86f6-cda249273937
    internal-label: AI Tools
role_v2:
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: fccf9111460413fe5b89229564a682827152b1ab
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 3%
---
# CX エンタープライズにおけるAIについて

Adobe CX Enterpriseのアプリケーションでは、AIを次の2つの補完的な方法で利用します。コンテンツの作成や回答の取得を直接指示する&#x200B;**生成AI**&#x200B;と、マルチステップの作業を計画および実行する&#x200B;**エージェント型AI**&#x200B;が、お客様の監視下で実行されます。 次のトピックでは、CX Enterpriseで利用できるAIの種類を大まかに説明します。

## このセクションでは

- **[生成AIについて](./generative-ai.md)**&#x200B;生成AIとAI アシスタント機能を提供しているCX Enterprise アプリケーションのカタログを参照すると、製品ポートフォリオ全体における生成AIのリーチを一目で確認することができます。
- **[エージェント型AIについて](./agentic-ai.md)**&#x200B;は、Experience Platform AgentsとAgent Orchestratorの仕組み、既存のCX Enterprise アプリケーションとAI ファースト アプリケーションの違い、および各アプリケーションで使用可能なエージェントについて説明します。
- **[エージェンティック AI モニタリング](./monitoring.md)**&#x200B;では、センターオブエクセレンス チームおよびその他のガバナンス関係者が、組織全体でのエージェントの導入、使用、およびフィードバックを追跡するために使用するダッシュボードについて説明します。
- **[AI クレジットの使用](./ai-credit-consumption.md)**&#x200B;は、エージェントのジョブと同僚の入力がAI クレジットをどのように使用しているかを、エージェントとジョブのタイプ別の見積もり率で説明します。これにより、使用に関する計画と予算を立てることができます。
- **[生成AI コンテンツの透明性](../content-transparency.md)**&#x200B;は、Adobeが生成AIが生成し、生成AIが編集したコンテンツにC2PA メタデータを自動的に添付する方法を説明し、組織の開示義務を理解するのに役立ちます。
- **[CX Enterprise エージェンティック ツール ](https://experienceleague.adobe.com/ja/docs/cx-enterprise-agentic-tools/using/overview)**&#x200B;は、CX Enterprise エージェントを拡張するエージェンティック スキルとツールを取り上げるビデオ チュートリアルです。

## 始める前に {#before-you-begin}

Coworker、AI アシスタント、エージェンティック AIの使用を開始する前に、次のアクセス、プライバシー、セキュリティ要件を確認してください。

### アクセス要件

ユーザーがAI アシスタントとExperience Platform Agentsにアクセスするには、Adobe管理者が適切な権限を付与する必要があります。 要件はアプリケーションによって異なります。詳しくは、Agent Orchestrator ガイドの[ アクセス ](../agents/agent-orchestrator.md#access)を参照してください。 CX Enterprise Coworker アクセスは、実施要件に基づく体験版を通じて個別に展開されます。組織がアクセスを取得する方法については、[共同作業者体験版](../agents/trial.md)を参照してください。

### プライバシーとセキュリティ

AI アシスタントとExperience Platform Agentsは、サンドボックスに特化したデータ分離や既存のアクセス制御ポリシーなど、プライバシー、セキュリティ、ガバナンスを優先します。 詳しくは、[AI アシスタントのプライバシー、セキュリティ、ガバナンス ](../ai-assistant/privacy.md)を参照してください。

## 開始する場所

1. **生成AIについて**&#x200B;と&#x200B;**エージェント型AIについて**&#x200B;をお読みいただき、利用可能な2つのAIの形式と、ライセンスを取得したアプリケーションで各AIが既に利用されている場所について理解してください。
1. **AI クレジットの使用**&#x200B;を読んで、使用がコストにどのように変換されるかを理解してください。これにより、財務と調達に対する期待値を設定できます。
1. ガバナンス チームに&#x200B;**Agentic AI監視** ダッシュボード権限を設定して、導入と使用状況を初日から確認できるようにします。
1. **生成AI コンテンツの透明性**&#x200B;を参照して、AIが生成したコンテンツに対して、チームが公開するコンテンツに自動的に適用される情報開示について確認してください。
1. Adobe管理者と協力して、上記の&#x200B;**アクセス要件**&#x200B;を開始する前に完了し、CX Enterprise アプリケーション ](../home.md)の[AIにユーザーを誘導して、AI アシスタント、Agent Orchestrator、CX Enterprise Coworkerに関する実践的なガイダンスを提供します。
