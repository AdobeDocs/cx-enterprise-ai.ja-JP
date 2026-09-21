---
title: Data Management Agent for Adobe Experience Platform
description: CX CoworkerのData Management Agentを使用して、Adobe Experience Platform データセットを検索および分析し、データレイクの保持ポリシーを管理する方法について説明します。
source-git-commit: 40f144c7a06592c78dccc6c17f19554b62f667c9
workflow-type: tm+mt
source-wordcount: '1016'
ht-degree: 3%
---
# Data Management エージェント

>[!AVAILABILITY]
>
>Data Management Agentは、Adobe CX Enterprise Coworkerにアクセスできるすべてのお客様が利用できます。

Experience Event データセットのデータレイクの保持を把握および管理するには、CX CoworkerのData Management Agentを使用します。 Adobe Experience Platformデータレイク内のExperience Event データセットが成長するにつれ、クエリやダウンストリームプロセスの完了に時間がかかり、保持要件の管理が困難になる可能性があります。 自然言語で達成したい目標を記述します。 Data Management Agentは、関連するExperience Event データセットを見つけ出し、それらが積極的に使用されているかを分析し、提案された保持期間がデータにどの程度影響するかをモデル化します。 行動する準備ができたら、リテンションポリシーを設定、変更、削除し、変更される前に確認を求めることができます。

## Data Management Agentの機能 {#what-the-data-management-agent-can-do}

Data Management Agentには4つのスキルがあります。

>[!NOTE]
>
>データセットのリスト、データセットの使用状況の分析、データセットの保持スキルの分析は読み取り専用です。 データレイクの保持ポリシーを変更できるのは、データセットの保持を管理スキルのみです。変更を適用する前に、明示的な確認が必要です。

| スキル | 説明 |
|---|---|
| **データセットのリスト** | リテンションレビューを開始する場所を決定する際に使用します。 ストレージサイズ、行数、既存の保持設定、プロファイルの有効化を含むExperience Event データセットのリストを表示して、データレイクリテンションポリシーの候補となる可能性のあるデータセットをすばやく特定できます |
| **データセットの使用状況を分析** | データセットがデータレイクの保持ポリシーの候補として適しているかどうかを判断する前に、を使用します。 最近の取り込み、クエリアクティビティ、下流アプリケーションの使用などのシグナルにもとづいて、特定のデータセットがどの程度アクティブに使用されるかを分類します。 |
| **データセット保持を分析** | リテンション期間にコミットする前に使用します。 データセットのストレージ指標とデータの年齢を表示し、その年齢分布を使用して、潜在的な保持期間が保持または削除するデータの量を概算します。 |
| **データセット保持の管理** | 行動する準備ができたときに使用します。 データセットに対して、データレイクの保持ポリシーを設定、変更、削除します。何かが変更される前に、プレビューと確認に影響を与えます。 |

## スコープ：データレイクのリテンションツールとほかのデータ管理ツールの比較 {#scope}

Experience Event データセットを検索して分析し、データレイクの保持ポリシーを設定、変更、削除する必要がある場合は、Data Management Agentを使用します。

データレイクの保持ポリシーが目標に適したオプションであるかどうかわからない場合は、[適切なデータライフサイクル管理機能の選択](https://experienceleague.adobe.com/ja/docs/experience-platform/data-lifecycle/choose-a-capability)を参照して、使用可能な保持オプションと削除オプションを比較してください。

これらのスキルでは、次の関連する機能は管理されません。

- **プロファイルストア保持ポリシー。** プロファイルストアにエクスペリエンスイベントが残る期間を管理するには、プロファイルが有効なエクスペリエンスイベント データセットにエクスペリエンスイベントの有効期限ポリシーを設定します。 [&#x200B; エクスペリエンスイベントの有効期限](https://experienceleague.adobe.com/ja/docs/experience-platform/profile/event-expirations)を参照してください。
- **サンドボックス全体の仮名プロファイルデータの有効期限。** 設定された条件を満たすと、サンドボックス全体で仮名プロファイルデータを自動的に削除するには、[仮名プロファイル &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/profile/pseudonymous-profiles)を参照してください。
- **データセットの有効期限。** 今後の日付にデータセット全体を削除するようにスケジュールするには、[&#x200B; データセットの有効期限](https://experienceleague.adobe.com/ja/docs/experience-platform/data-lifecycle/ui/dataset-expiration)を参照してください。
- **レコードの削除。** プライバシーまたは衛生上の理由から個々のプロファイルレコードを削除するには、[&#x200B; レコード削除](https://experienceleague.adobe.com/ja/docs/experience-platform/data-lifecycle/ui/record-delete)を参照してください。

## 前提条件 {#prerequisites}

始める前に、次のことを確認してください。

- Adobe Experience Platformと、レビューするデータセットを含むサンドボックスにアクセスします。
- 使用するデータセットと保持アクションに必要なAdobe Experience Platform権限。 Data Management Agentは、既存のExperience Platform権限を使用し、追加のアクセス権を付与しません。 Adobe Experience Platformの権限と役割の仕組みについては、[&#x200B; アクセス制御の概要](https://experienceleague.adobe.com/ja/docs/experience-platform/access-control/home)を参照してください。
- CX CoworkerにインストールされたAdobe CXO プラグイン。

プラグインのインストール手順については、[Coworker UI ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)を参照してください。

## Data Management Agentの使用 {#use-the-data-management-agent}

自然言語を使用して、CX Coworkerを通じてData Management Agentと対話します。 目標を記述し、フォローアップの質問で結果を絞り込みます。

>[!NOTE]
>
>始める前に、確認するデータセットを含むサンドボックスで作業していることを確認してください。

Data Management Agentを使用するには：

1. **[!UICONTROL CX Coworker]**&#x200B;に移動します。 アクセスの詳細については、[Coworker UI ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide)を参照してください。
1. 達成したい目標を記述した要求を入力します。
1. 結果を確認し、フォローアップの質問をもとに調査を継続します。

リクエストでデータレイクの保持ポリシーが変更された場合、Data Management Agentは提案された影響を示し、変更を適用する前に確認を必要とします。

データセットの特定、使用状況と保持の影響の分析、データレイク保持ポリシーの管理のためのエンドツーエンドのワークフローについては、[&#x200B; データレイク保持の管理](../coworker/chat/use-cases/data-management/manage-data-lake-retention.md)を参照してください。

## Data Management Agentの仕組み {#how-the-data-management-agent-works}

Data Management Agentは、決定論的計算を使用してデータセットの使用状況を分析するため、同じ入力が同じ使用階層を生成します。 また、AIが生成した見積もりに頼るのではなく、プログラムによって維持率を計算できます。 顧客維持率は、データの年齢分布にもとづいているため、依然として近似値です。 Agentは、Adobe Experience Platform サービスから直接データを取得し、データセットに関する最新情報を提供します。

## 制限事項 {#limitations}

Data Management Agentは、データレイクの保持ポリシーの適切な候補となる可能性のあるデータセットを特定できますが、データセットが必要かどうかを判断しません。 明示的な確認なしに、保持ポリシーを適用、変更、削除することはできません。

## 次の手順 {#next-steps}

Experience Event データセットでデータレイクの保持を検索、分析、管理する各スキルの使用方法については、[&#x200B; データレイクの保持の管理](../coworker/chat/use-cases/data-management/manage-data-lake-retention.md)を参照してください。

保持の動作や設定など、Adobe Experience Platformでのデータレイク保持ポリシーの動作について詳しくは、[Experience Event データセット保持（TTL）ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/catalog/datasets/experience-event-dataset-retention-ttl-guide)を参照してください。
