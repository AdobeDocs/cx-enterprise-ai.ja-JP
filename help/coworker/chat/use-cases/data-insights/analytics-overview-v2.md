---
title: Adobe Customer Journey Analyticsのデータを分析する（チャット）
description: Adobe CX Enterprise Coworker Chatを使用してAdobe Customer Journey Analyticsのデータを分析し、ファネルを構築して、カスタマージャーニーのどの段階で顧客が脱落しているのかを把握する方法を紹介します。
hold: true
product_v2:
  internal-label: CX Enterprise Coworker
feature_v2:
  internal-label: CX Enterprise Coworker
source-git-commit: 347fdd194c7ae8335266917314ab70bf0e031f6b
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 2%
---

# Coworker Chatでデータを分析

Adobe CX Enterprise Coworker Chatの概要と、自社のデータを分析する方法について解説します。

Coworker Chatなら、自然言語を使ってAdobe Adobeのプロダクトタスクを自動化し、柔軟なプランニング、カスタマイズ可能なスキル、インテリジェントな実行によってアイデアをすばやくアクションに結び付けることができます。 Coworkerの一般的な詳細については、[CX Enterprise Coworkerの概要](/help/coworker/overview.md)を参照してください。

## データ分析の仕組み

Coworker Chatは、以前はAnalysis Workspaceでのみ可能だった高度なデータ分析を実行できます。 Coworker Chatは、Customer Journey AnalyticsデータビューやAdobe Analyticsレポートスイートからデータにアクセスし、データを検索して、自然言語プロンプトで回答を得ることができます。

Coworker チャットでビジュアライゼーションを作成する場合は、Analysis Workspaceでいつでも開いて、より手動制御を行うことができます。

## 同僚チャットで分析を開始

最初に、知りたいことを分かりやすい言葉で説明しましょう。 Coworker Chatは分析計画を立て、データビューやレポートスイートのクエリを行い、ビジュアライゼーションや概要を作成します。

次のユースケースは、達成したい目標でグループ化されています。 各グループには、最も適した役割がリストされています。

### パフォーマンスを測定

**アナリスト、** ビジネスユーザーに最適

| ユースケース | 関数 |
| --- | --- |
| [Customer Journey AnalyticsとAdobe Analytics データの分析](/help/coworker/chat/use-cases/data-insights/analytics-chat.md)<p>![Customer Journey AnalyticsとAdobe Analytics データの分析](../../assets/coworker-funnel-response-card.png)</p> | データビューやレポートスイートに関する自然言語の質問に答え、ファネルやその他のビジュアライゼーションを構築し、顧客が離脱する原因を見つけ出します。 Analysis Workspaceで任意のビジュアライゼーションを開いて、さらに詳しく分析できます。<p>詳しくは、[同僚チャットを使用したAdobe CX Analytics データの分析](/help/coworker/chat/use-cases/data-insights/analytics-chat.md)を参照してください。</p> |
| [ パフォーマンスを比較](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#query-and-analyze-data) | チャネル、期間、セグメントをまたいで指標を並べて比較できます。<p>詳しくは、「Adobe CX Analytics データを共同作業チャットで分析する」の[ データのクエリと分析](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#query-and-analyze-data)を参照してください。</p> |
| [施策のパフォーマンスを測定](/help/coworker/chat/use-cases/overview.md#data-insights) | キャンペーン、チャネル、web プロパティの特定の期間におけるパフォーマンスを確認できます。<p>詳しくは、「Coworker Chat ユースケースの[ データインサイト ](/help/coworker/chat/use-cases/overview.md#data-insights)」を参照してください。</p> |
| [ ファネルの分析](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#query-and-analyze-data) | マルチステップのコンバージョンファネルを進め、各ステージでの離脱を確認します。<p>**アナリスト：**&#x200B;に最適</p><p>詳しくは、「Adobe CX Analytics データを共同作業チャットで分析する」の[ データのクエリと分析](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#query-and-analyze-data)を参照してください。</p> |

### 指標が変化した理由

**アナリスト：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [ トレンドと根本原因を探る](/help/coworker/chat/use-cases/data-insights/root-cause-analysis.md)<p>![ トレンドと根本原因を探る](../../assets/data-validation-aa-cja/trend-line-card.png)</p> | Customer Journey AnalyticsとAdobe Analyticsのデータの傾向と、パフォーマンスの変化を促す要因を手動でのクエリなしで特定します。<p>詳しくは、[Customer Journey Analyticsと共同作業者](/help/coworker/chat/use-cases/data-insights/root-cause-analysis.md)を参照してください。</p> |
| [運用上の傾向と原因を分析](/help/coworker/chat/use-cases/overview.md#data-insights) | オーディエンス、データセット、ジャーニーに関する過去の時系列データをクエリし、変更の原因を特定できます。<p>**管理者、アナリスト：**&#x200B;に最適</p><p>詳しくは、「Coworker Chat ユースケースの[ データインサイト ](/help/coworker/chat/use-cases/overview.md#data-insights)」を参照してください。</p> |

### 将来のパフォーマンスを予測

**アナリスト：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [予測指標](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#query-and-analyze-data) | 売上目標を達成するための進捗状況など、過去のCustomer Journey AnalyticsやAdobe Analyticsのデータから得られた将来の指標値をプロジェクトします。<p>詳しくは、「Adobe CX Analytics データを共同作業チャットで分析する」の[ データのクエリと分析](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#query-and-analyze-data)を参照してください。</p> |

### 関係者とインサイトを共有する

**アナリスト、** ビジネスユーザーに最適

| ユースケース | 関数 |
| --- | --- |
| [ エグゼクティブの概要とKPI ダイジェストの作成](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#executive-summaries-and-performance-digests) | 関係者に提供可能なパフォーマンスの概要、レコメンデーション、スライドデッキの概要を作成します。<p>詳しくは、「Adobe CX Analytics data with Coworker Chat」の[ エグゼクティブサマリーとパフォーマンスダイジェスト ](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#executive-summaries-and-performance-digests)を参照してください。</p> |

### 実装計画またはアップグレード

**管理者：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [実装の計画](/help/coworker/chat/use-cases/data-insights/implementation-guide.md)<p>![実装の計画](../../assets/ui-guide-6.png)</p> | Customer Journey Analyticsの実装、Adobe Analyticsからのアップグレード、EdgeでのContent Analytics、Marketing Campaign Analytics、ストリーミングメディアコレクションの設定などについて、パーソナライズされたステップバイステップの計画を作成します。 計画には、所有者、労力の見積もり、依存関係、検証手順などの詳細が含まれます。<p>詳しくは、[同僚との実装の計画](/help/coworker/chat/use-cases/data-insights/implementation-guide.md)を参照してください。</p> |
| [実装チェックリストを生成](/help/coworker/chat/use-cases/data-insights/intelligent-checklist.md)<p>![実装チェックリストを生成](../../assets/data-validation-aa-cja/date-detail.png)</p> | Customer Journey Analyticsの導入計画をCoworker Projectsのチェックリストに変換し、手順の割り当て、ステータスの追跡、承認ゲートの追加を可能にします。<p>詳しくは、[同僚プロジェクトを使用した実装チェックリストの生成](/help/coworker/chat/use-cases/data-insights/intelligent-checklist.md)を参照してください。</p> |

### データが正確であることを確認する

**管理者：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード時にデータを検証](/help/coworker/chat/use-cases/data-insights/data-validation-aa-cja.md)<p>![Adobe AnalyticsからCustomer Journey Analyticsへのアップグレード時にデータを検証](../../assets/data-validation-aa-cja/trend-bar-card.png)</p> | Adobe Analytics レポートスイートとCustomer Journey Analytics データビュー間のディメンション、指標、傾向を比較し、アップグレードをサポートするための修正を推奨します。<p>**管理者、アナリスト：**&#x200B;に最適</p><p>詳しくは、「[Adobe AnalyticsからCustomer Journey Analyticsにアップグレードする際にCoworkerでデータを検証する](/help/coworker/chat/use-cases/data-insights/data-validation-aa-cja.md)」を参照してください。</p> |
| [ ストリーミングメディア実装の検証](/help/coworker/chat/use-cases/data-insights/streaming-media-validation.md)<p>![ ストリーミングメディア実装の検証](../../assets/ui-guide-8.png)</p> | データストリーム、スキーマ、データセット、データビュー、セッションデータを確認して、ストリーミングメディアトラッキングが設定され、データが正しく収集されていることを確認します。<p>詳しくは、[ ストリーミングメディア実装を共同作業者と検証](/help/coworker/chat/use-cases/data-insights/streaming-media-validation.md)するを参照してください。</p> |
| [Customer Journey Analyticsのデータセット品質を検証](/help/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)<p>![Customer Journey Analyticsのデータセット品質を検証](../../assets/data-validation-aep/dataset-validation.png)</p> | Customer Journey Analyticsレポートに使用するデータセットを特定し、スキーマ、ID品質、フィールド品質をチェックすることで、ダッシュボードを構築する前に問題を解決できます。<p>詳しくは、「[Coworkerでのデータ検証スキルを使用したCustomer Journey Analytics データの検証](/help/coworker/chat/use-cases/data-insights/validate-dataset-quality-for-cja.md)」を参照してください。</p> |
| [Experience Platformに取り込んだ後のデータの検証](/help/coworker/chat/use-cases/data-insights/data-validation-aep.md)<p>![Experience Platformに取り込んだ後のデータの検証](../../assets/data-validation-aep/null-values.png)</p> | Experience Platformのデータセットとフィールドに対して統計チェックとセマンティックチェックを実行し、無効な値やマッピングの問題などのデータ品質の問題を見つけます。<p>詳しくは、[Experience Platform データを共同作業者と検証](/help/coworker/chat/use-cases/data-insights/data-validation-aep.md)するを参照してください。</p> |

### 繰り返す分析の自動化

**アナリスト：**&#x200B;に最適

| ユースケース | 関数 |
| --- | --- |
| [ カスタム Customer Journey Analytics スキルの作成](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#create-custom-skills) | 繰り返し利用できる分析を、セッション全体で永続的な再利用可能なスキルに変換します。<p>詳しくは、「Analytics Adobe CX Analytics data with Coworker Chat」の[ カスタムスキルの作成](/help/coworker/chat/use-cases/data-insights/analytics-chat.md#create-custom-skills)を参照してください。</p> |

これらのユースケース（使用するスキルやサンプルプロンプトなど）について詳しくは、[ データインサイトのユースケース ](/help/coworker/chat/use-cases/overview.md#data-insights)を参照してください。


