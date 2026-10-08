---
title: 同僚でのSQL データの準備
description: CoworkerのSQL データ準備を使用して、SQL クエリを生成、最適化、トラブルシューティング、スケジュールする方法を説明します。
source-git-commit: 8e28bb38bd27c1e57ac7c62f74196d146d8519ca
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 3%
---
# 同僚でのSQL データの準備

CoworkerでSQL Data Preparationを使用して、自然言語プロンプトを使用して一般的な[Data Distiller](https://experienceleague.adobe.com/ja/docs/experience-platform/query/data-distiller/overview) タスクを実行します。 SQLの生成、既存のクエリのトラブルシューティングまたは最適化、結果のプレビュー、定期的な実行のクエリのスケジュールを実行できます。

>[!AVAILABILITY]
>
>CoworkerのSQL データ準備は、制限付き可用性で利用できます。

## 前提条件 {#prerequisites}

CoworkerでSQL データ準備を使用する前に、次のことを確認してください。

- Data Distillerの使用権限。
- 共同作業者へのアクセス：

## 基本を学ぶ {#get-started}

最初に、Coworkerを開き、達成したいSQL タスクまたは結果を説明する自然言語リクエストを入力します。

リクエストで使用するデータセットを特定できます。 タスクを完了するために追加情報が必要な場合は、続行する前にフォローアップで質問することができます。

CoworkerがSQLを生成または更新した後、会話を続行して結果をプレビューしたり、クエリを調整したり、保存したり、繰り返し実行のためにスケジュールしたりできます。

Coworker インターフェイスの使用に関するガイダンスについては、[Coworker UI ガイド ](https://experienceleague.adobe.com/en/docs/coworker/content/chat/ui-guide)を参照してください。

## サポートされている機能 {#supported-capabilities}

SQL データ準備は、次のタスクに使用できます。

| 機能 | 説明 |
| --- | --- |
| **SQL オーサリング** | 実行するデータ操作の自然言語説明からSQLを生成します。 |
| **SQL最適化** | 既存のData Distillerクエリを分析し、意図した結果を維持しながらパフォーマンスを向上させるために最適化します。 |
| **SQL エラーの診断と修正** | 既存のSQL クエリのエラーを診断し、根本原因を説明し、修正されたSQLを生成します。 |
| **クエリのスケジュール設定とアラート** | 繰り返し実行するクエリを保存してスケジュールし、サポートされるクエリアラートを設定します。 |

## 会話でのSQL データ準備の使用 {#work-with-sql-data-preparation}

SQL データ準備機能を別々のワークフローとして扱う代わりに、同じ同僚の会話で組み合わせることができます。

例えば、次のことができます。

1. 目的の結果を記述して、SQLを生成します。
2. 最大5行のクエリ結果をプレビューできます。
3. 生成されたSQLに関するクエリを絞り込んだり、質問したりできます。
4. クエリを保存します。
5. 繰り返し実行するクエリをスケジュールし、アラートを設定します。

同僚は、適切なデータセットの特定やスケジュールのタイムゾーンの確認など、追加の情報が必要な場合、フォローアップで質問することができます。

クエリのプレビューでは、最大5行が返されます。 Experience Platformで直接クエリを実行して操作するには、[ クエリエディターUI ガイド ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/user-guide)を参照してください。

SQL クエリ結果の5行のプレビューと、クエリをテンプレートとして保存したり、定期的な実行のためにスケジュールしたりするオプションを示す![同僚の応答](./assets/sql-data-prep/query-preview.png)

### 自然言語からSQLを生成する {#generate-sql}

達成したい結果や変換がわかっているが、対応するSQLをCoworkerが生成したい場合は、SQL オーサリングを使用します。

適切なデータからSQLを生成するために、チームメンバーは関連するデータセットを特定し、検証することができます。 リクエストで適切なデータセットを特定するのに十分な情報が提供されない場合、続行する前にフォローアップで質問することができます。

次に例を示します。

> こんにちは！ test_luma_web_events_1000を使用して、顧客エンゲージメントをイベントタイプ別に要約します。 イベントタイプ、イベントの合計、ユニーク顧客を表示します。 イベントタイプごとに1行を返し、ユニークな顧客で最も高い顧客から最も低い顧客まで結果を並べ替えます。

Coworkerは生成されたSQLを返し、クエリを実行して結果のプレビューを提供できます。

![同僚の応答は、イベントの種類ごとに顧客エンゲージメントを要約するために生成されたSQLを示し、その後、合計イベントと一意の顧客のテーブルのプレビューと結果の分析を示します。](./assets/sql-data-prep/authoring-result.png)

Experience Platformで直接クエリを作成および実行する方法について詳しくは、[ クエリエディターUI ガイド ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/user-guide)を参照してください。

### 既存のSQLの最適化 {#optimize-sql}

既にData Distiller クエリがあり、意図した結果を変更することなくパフォーマンスを向上させたい場合は、SQL最適化を使用します。

Coworkerに変更の説明を依頼し、元のSQLと最適化されたSQLを比較し、検証またはクエリ計画の情報を提供できます。

次に例を示します。

> まったく同じ結果を維持しながら、次のクエリをData Distillerのパフォーマンスに最適化します。 変更した内容と、最適化されたクエリが論理的に同等である理由を説明します。
>
> ```sql
> SELECT
>         p.customer_id,
>         p.first_name,
>         p.last_name,
>         p.loyalty_status,
>         COUNT(o.order_id) AS total_orders,
>         SUM(CAST(o.order_total AS DOUBLE)) AS total_revenue
> FROM test_luma_profiles_1000 p
> INNER JOIN test_luma_orders_1000 o
>         ON p.customer_id = o.customer_id
> GROUP BY
>         p.customer_id,
>         p.first_name,
>         p.last_name,
>         p.loyalty_status
> ORDER BY total_revenue DESC;
> ```
>
> 完全な応答、特に元のSQL、最適化されたSQL、同等の説明、およびEXPLAIN/検証結果を送信します。

指定されたクエリが既に最適化されている場合、変更が必要ないと判断し、その評価を説明できます。

![同僚の応答は、最適化のために既存のSQL クエリを分析し、クエリ計画の結果と等価評価を使用して、変更が必要ないことを説明しています。](./assets/sql-data-prep/optimize-query.png)

SQL オーサリング機能を通じて生成されたSQLは、既に最適化されています。 最適化のために新しく生成されたSQLを別途送信する必要はありません。

SQL構文とサポートされているコマンドについては、[ クエリサービス SQL リファレンス ](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/overview)を参照してください。

### SQL エラーの診断と修正 {#diagnose-sql-errors}

既存のクエリが失敗し、原因の特定とSQLの修正に役立つ場合は、SQL エラー診断を使用します。

Coworkerは、クエリを分析し、エラーの原因を特定し、問題を説明し、修正されたSQLを提供します。

次に例を示します。

> こんにちは！ 次のクエリは失敗しています。 エラーを診断し、根本原因を説明し、修正されたクエリを提供します。
>
> ```sql
> SELECT
>         o.order_id,
>         o.product_id,
>         p.product_name,
>         o.order_total
> FROM test_luma_orders_1000 o
> JOIN test_luma_product_catalog_1000 p
>         ON o.productid = p.productid;
> ```
>
> 修正されたクエリでは、両方のデータセットの適切な製品ID フィールドを使用する必要があります。

クエリを修正した後、Coworkerにクエリを実行して結果をプレビューするように依頼できます。

![同僚の応答が、誤ったproduct ID フィールド名によって発生したSQL クエリ エラーを診断し、product_id フィールドを使用する修正されたSQLを提供しています。](./assets/sql-data-prep/diagnose-error.png)

### クエリのスケジュール設定とアラートの設定 {#schedule-queries}

クエリの生成、修正、またはプレビューの後、会話を続行して保存し、定期的な実行のためにスケジュールを設定できます。

次に例を示します。

> このクエリを毎日6:00 AMに実行するようにスケジュールします。 クエリが失敗した場合のアラートの設定。

必要な情報が見つからないか、あいまいな場合は、スケジュールを作成する前にフォローアップで質問します。 例えば、要求された実行時間に関連付けられたタイムゾーンを確認するように求めることができます。

必要なスケジュールの詳細を確認すると、Coworkerは、保存されたクエリテンプレート、スケジュール、タイムゾーン、ステータス、および失敗アラートの概要を返します。

![保存されたテンプレート、スケジュール、タイムゾーン、終了日、スケジュールの状態、失敗アラートなど、スケジュールされたSQL クエリを確認する同僚の応答](./assets/sql-data-prep/schedule-query.png)

クエリスケジュール、繰り返し設定、出力データセット、およびアラートについて詳しくは、[ クエリスケジュール ](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/query-schedules)を参照してください。

## 次の手順 {#next-steps}

SQL Data Preparationで使用されるData Distiller機能とQuery Service機能について詳しくは、次のドキュメントを参照してください。

- [Data Distillerの概要](https://experienceleague.adobe.com/ja/docs/experience-platform/query/data-distiller/overview)
- [クエリエディターUI ガイド](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/user-guide)
- [クエリスケジュール](https://experienceleague.adobe.com/en/docs/experience-platform/query/ui/query-schedules)
- [クエリサービス SQL リファレンス](https://experienceleague.adobe.com/en/docs/experience-platform/query/sql/overview)
