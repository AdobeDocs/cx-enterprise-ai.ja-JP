---
description: Coworker Chatのユースケースとサンプルプロンプトを、データインサイト、オーディエンス、ジャーニー、プラットフォーム運用をまたいで、エリアごとに整理して参照できます。
title: 同僚チャットのユースケース
feature_v2:
  - id: fdae8433-07cd-42e7-acce-738afe63f6bb
source-git-commit: 46299bb3b1cd8179f277940d67bcb876b3f4e9fc
workflow-type: tm+mt
source-wordcount: 3050
ht-degree: 7%

---

# Adobe Workfrontのユースケース{#use-cases}

共同作業チャットを使用すると、複数のUIを移動したり、手動でクエリを記述したりするのではなく、自然言語を使用して[!DNL Experience Platform] データをクエリ、分析、アクションできます。 このページでは、実務担当者が最も重視しているユースケースを、データインサイト、オーディエンス、ジャーニー、基本要素、サンドボックスツールなどの作業領域ごとに分類して説明します。 各エントリには、呼び出すスキル、使用するアプリケーション、コピーできるプロンプトのサンプル、独自のデータへの適応、会話による絞り込みなどがあります。

>[!NOTE]
>
>近日リリース予定：
>
>Adobe AEMの新しいエージェント機能は、より迅速な作業を支援するために構築された、CX Enterprise Coworkerを通じて提供されます。
>
>対象となるすべてのお客様は、CoworkerのAdobe Experience Manager エージェンティック機能にローリングベースでアクセスできます。
>
>AEMの[AI - AEMのエージェンティック機能の概要](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/overview)も参照してください。

## ブランド体験

### Experience Production - Sites ユースケース

>[!NOTE]
>
>AEMの[Agentic Capabilities: Brand Experience - Experience Production - Sites](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-sites)も参照してください。

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| AEM ページの更新 | コンテンツ要素の更新、削除、置き換え、追加などのアクションを実行し、エクスペリエンスを正確かつ最新の状態に保ちます。 入力には、自然言語またはPDFやスクリーンショットなどの視覚的な注釈を使用できます。 | `aem-sites-pages-update` | Adobe Experience Manager（AEM） | &lt;URL>の見出しを「Hello World<br><br>」に更新し、&lt;URL>の「コーヒークイズを取る」ボタンをより魅力的なバージョンに変更します<br><br>添付された<br><br>に基づいて&lt;URL>を更新します。8月に実施しているコーヒーマシンを購入し、コーヒーフリーの2袋を入手するプロモーションについて、ページの下部に新しいティーザーセクションを追加したいと思います。 また、コーヒーを飲む友人の画像を見つけて、ティーザーでそれを使用することもできます |
| AEMの一括更新 | コンテンツ要素の削除、置き換え、追加など、複数のページをまたいで同時に一括アクションを実行し、エクスペリエンスを正確かつ最新の状態に保ちます。 | `aem-sites-pages-bulkreplace` | Adobe Experience Manager（AEM） | &lt;aem path>で、コピー「MyBarista\」を含むすべてのページを「BrewPass」に更新します |
| Figmaからビジュアルコンテンツフラグメントへ | 自然言語を使用して、FigmaからAdobe Experience Managerにデザインを直接読み込みます。 このスキルにより、必要なコンテンツモデル、コンテンツフラグメント、アセット、ビジュアライゼーションテンプレートが自動的に作成されるため、ビジネスユーザーは手作業で設定しなくても、デザインからwebに対応したコンテンツを数分で作成することができます。 | `aem-sites-visualcontentfragments-create` | Adobe Experience Manager（AEM） | &lt;Figma_URL>からインポート |

### Experience Production - Formsのユースケース

>[!NOTE]
>
>AEMの[Agentic Capabilities: Brand Experience - Experience Production - Forms](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/experience-production/use-cases#use-cases-forms)も参照してください。

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| フォームを作成 | 新しいアダプティブフォームを、平易な説明、添付された概要、画像、またはPDFから生成します | `aem-forms-adaptiveform-create` | Adobe Experience Manager（AEM） | 「従業員オンボーディングフォームの作成」 <br><br> 「添付された概要（画像またはpdf）を使用してフォームを作成」 <br><br> 「Create a &lt;form type> adaptive form」 |
| フォームの編集/更新 | 既存のフォームの変更（フィールドの追加と編集、シンプルなレイアウトの調整、送信アクションの設定、添付されたガイドラインドキュメントからの変更の適用） | `aem-forms-adaptiveform-edit` | Adobe Experience Manager（AEM） | 「姓フィールドの下にミドルネーム フィールドを追加」 <br><br> 「名フィールドと姓フィールドを2列のレイアウトに入れる」, 50/50&quot;<br><br> 「REST エンドポイントにデータを送信するフォームを設定」 <br><br> 「添付されたガイドライン ドキュメントに一致するようにこのフォームを更新」 <br><br> 「次に&lt; フィールド > フィールドを追加」 |
| ビジネスロジックの追加 | 他のフィールドの値に基づいてフィールドを表示または非表示にするなど、簡単なルールを作成できます | `aem-forms-adaptiveform-edit` | Adobe Experience Manager（AEM） | 「従業員タイプが請負業者の場合にのみ会社フィールドを表示」 <br><br> 「他のフィールドが&lt;value>の場合にのみ&lt;field> フィールドを表示」 |
| 埋め込みフォーム | 既存または新しく作成したフォームを、指定したAEM Sites ページに配置します（Edge Delivery Services ページでのみサポート） | `aem-forms-adaptiveform-embed` | Adobe Experience Manager（AEM） | 「このフォームをサイトのホームページに埋め込む」 <br><br> 「このフォームを&lt; ページパス >に埋め込む」 |

### 開発

>[!NOTE]
>
>AEMの[&#x200B; エージェンティック機能：ブランドエクスペリエンス – 開発](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/development/use-cases)も参照してください。

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| 失敗したCloud Manager パイプラインの診断と修正 | 失敗したパイプライン実行を調査し、根本原因を特定し、レビュー用の修正（差分を含む）を生成します | `cloud-manager-pipeline-troubleshooting` | Adobe Experience Manager（AEM） | 「ビルドパイプラインが失敗した理由」 <br><br> 「壊れた製品パイプラインの修正を提案する」 |
| Cloud Manager パイプラインの管理 | ログ、アーティファクト、変数、設定など、AEM Cloud Manager パイプラインを作成、実行、モニタリングします | `cloud-manager-pipeline-management` | Adobe Experience Manager（AEM） | 「プログラム 12345のパイプラインのリスト」 <br><br> 「開発パイプラインの実行が失敗した理由」 |
| Cloud Manager環境の管理 | RDE、環境変数、ログ、バックアップなどのAEM Cloud Manager環境を作成、設定、管理します | `cloud-manager-environment-management` | Adobe Experience Manager（AEM） | &quot;プログラム 12345の環境を一覧表示&quot;<br><br>&quot;RDEをリセット&quot; |
| Cloud Manager プログラムの管理 | パイプラインと環境を含むAEM Cloud Manager プログラムの一覧表示、検査、削除 | `cloud-manager-program-management` | Adobe Experience Manager（AEM） | 「自分のCloud Manager プログラムを一覧表示」 <br><br> 「プログラム 12345の詳細を表示」 |
| AEM リリースアップデートスケジュールの管理 | 自動メンテナンス用に毎日のサイレントアワーとアップデート不要の期間を設定し、Adobeのグローバルコードフリーズウィンドウを表示します | `cloud-manager-release-management` | Adobe Experience Manager（AEM） | 「現在の休眠時間枠は何ですか？」 <br><br> 「12月20日から1月2日までの更新料無料の期間をスケジュールする」 |

### オンボーディング - AEM Assetsのユースケース

>[!NOTE]
>
>AEMの[&#x200B; エージェンティック機能：ブランドエクスペリエンス – オンボーディング &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-experience/onboarding/use-cases)も参照してください。

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| ガイド付きのエンドツーエンドのオンボーディング | 必要な特定のオンボーディングタスクがわからない場合は、オンボーディングライフサイクル全体、リポジトリ選択、フォルダーへの委任、タグ、メタデータ、インポート、検索サブスキルを調整します。 | `aem-onboarding-workflow` | Adobe Experience Manager（AEM）Assets | 「AEM Assetsへのオンボーディング」 <br><br> 「AEM DAM オンボーディングの手順」 |
| フォルダー階層の設計と作成 | ビジネスニーズやCSV入力に基づいて、AEM Assets（`/content/dam`以下）でスケーラブルなフォルダー構造を推奨および作成します。 | `aem-folder-management` | Adobe Experience Manager（AEM）Assets | 「ライフスタイルマーケティングアセットのフォルダー構造を推奨」 <br><br> 「このCSV ファイルに基づいてフォルダーを作成」 |
| タグのデザインと作成 | `/content/cq:tags`の下に制御されたタグ語彙をデザインして作成します – 名前空間、階層タグ、およびバッチタグ操作。 | `aem-tag-taxonomy` | Adobe Experience Manager（AEM）Assets | 「商品カテゴリの名前空間を使用したタグ分類の設計」 <br><br> 「このCSVからタグをインポート」 <br><br> 「AEMでこれらの階層タグを作成」 |
| メタデータフォームの作成と割り当て | カスタムメタデータフォームを設計および作成し、オーサリング UI コンテンツ作成者が使用するカスタムメタデータフォームは、CSV、テーブル、要件ドキュメントまたは説明から任意でフォルダーに割り当てられます。 | `aem-metadata-form` | Adobe Experience Manager（AEM）Assets | 「このフィールドのリストからメタデータフォームを作成する」 <br><br> 「このフォームを`campaigns` フォルダーに割り当てる」 |

## Content Advisor - AEM Assets ユースケース

### コンテンツ発見

>[!NOTE]
>
>AEMの[Agentic Capabilities: Content Advisor - Content Discovery](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/discovery/use-cases)も参照してください。

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| セマンティックテーマで検索 | AIを活用したセマンティックマッチングにより、コンセプト、ムード、ビジュアルテーマごとにアセットを検索できます。 | `aem-assets-discovery` | Adobe Experience Manager（AEM）Assets | &quot;Find me morning coffee lifestyle images&quot; |
| カスタムメタデータで検索 | カスタムメタデータフィールド（コーヒーブレンド、ブランド、ローストレベルなど）でアセットをフィルタリングします。 | `aem-assets-discovery` | Adobe Experience Manager（AEM）Assets | 「`Coffee Blend`が`Morning Muse`のアセットを検索する」 <br><br> 「ライセンスの有効期限が切れていないアセットを取得する」 <br><br> 「キャンペーン名が設定されていないアセットを検索する（適切な結果を得るには、プロパティにインデックスを付ける必要があります）」 |
| 承認ステータスで検索 | 承認ステータスに基づいてアセットをフィルタリングします。 たとえば、「承認済み」、「レビュー中」、「却下」、「ステータスが欠落している」などです。 | `aem-assets-discovery` | Adobe Experience Manager（AEM）Assets | 「`Campaign` フォルダー内のすべての承認済みアセットを表示する」 |
| フォルダー/パスで検索 | AEMのフォルダー名を参照する自然言語プロンプトを解釈して、アセットを識別できます。 リポジトリ内を手動で移動することなく、プロンプトでフォルダーについて説明するだけで、適切なコンテンツを見つけるために必要なクリック数を大幅に削減できます。 | `aem-assets-discovery` | Adobe Experience Manager（AEM）Assets | 「フォルダー`WKND`にsvgがありますか？<br><br>」「フォルダー`WKND`の2025年11月1日以降に変更されたアセットを表示」 |

### コンテンツの最適化

>[!NOTE]
>
>AEMの[Agentic Capabilities: Content Advisor - Content Optimization](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/content-advisor/content-optimization/use-cases)も参照してください。

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| 高解像度レンディションの作成とチャネルに最適化されたレンディション | 指定された解像度と品質レベルでアセットの新しいレンディションを生成するので、手作業での編集なしでチャネルに対応したバリエーションを簡単に準備できます。 また、Instagram ストーリーなどのプラットフォーム固有の要件に合わせてレンディションを制作し、アセットが形式、比率、品質のガイドラインを自動的に満たすようにすることもできます。 | `aem-assets-content-optimisation` | Adobe Experience Manager（AEM）Assets | 「Create a `2000px` rendition as `JPEG` with `80% quality`」 <br><br> 「Create a rendition for an Instagram story」 |
| ブランドオーバーレイと複合生成 | 正確な配置で既存のアセットにプロモーショングラフィック、オーバーレイ、バッジを適用し、キャンペーンに対応したコンポジットの迅速な作成をサポートします。 | `aem-assets-content-optimisation` | Adobe Experience Manager（AEM）Assets | 「プロモーションバナーの上に`30%`個の割引グラフィックを配置し、中央から`100px`配置した画像をオーバーレイする」 |
| 画像の強化、背景色の調整、方向の変換 | ビジュアルの改善（シャープ画像）の適用、背景色の置き換え、方向変換の実行を行います。 | `aem-assets-content-optimisation` | Adobe Experience Manager（AEM）Assets | 「`PNG`の背景色を`#ff8932`に変更」 <br><br> 「画像をシャープにする」 <br><br> 「画像を水平方向にミラーリングする」 |

## ブランドガバナンス

>[!NOTE]
>
>AEMの[&#x200B; エージェンティック機能：ブランドガバナンス &#x200B;](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agentic-capabilities/brand-governance/use-cases)も参照してください。

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| ガイドラインとセグメントの検索 | セグメント、市場、カテゴリーごとに分類された詳細なブランドガイドラインを取得します | enterprise-context | Adobe Experience Manager（AEM） | 「このブランドのトーンオブボイスのガイドラインは何ですか？」 <br> 「ヘルスの垂直方向で使用される請求項カテゴリのリスト」 |
| ブランドガイドラインに照らし合わせたコンテンツの評価 | 設定されたブランドチェックに照らし合わせて、公開/編集されたページ、テキストブロック、画像を評価します | aem-governance | Adobe Experience Manager（AEM） | 「このランディングページをSecurBank ガイドラインに照らして評価する」 <br> 「このキャッチフレーズはトーンオブボイスのチェックに合格しますか？」 |
| AEM権限のデバッグ | 権限ポリシー、ACL、継承ルールをデバッグまたは理解します。 | aem-governance | Adobe Experience Manager（AEM） | 「プリンシパル管理者が`https://author/`に`/content/folder/us`を書き込むことができる理由？」 <br> 「なぜ`https://author`に`/content/dam`でサンプル オーサーを書き込むことができないのか」 |

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
| [&#x200B; ロイヤルティに関する課題の作成、編集、管理](journeys/create-loyalty-challenge.md) | ロイヤルティプログラム管理を簡素化し、迅速化したい | `loyalty` | Adobe Journey Optimizer（AJO） | 「会員に新しい季節の飲み物を試すように促すチャレンジを作成する」 ・ 「最も高い会員の脱落率でロイヤルティの課題を表示する」。 |

## 基本要素

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| 製品情報とドキュメント | Adobeの公式ドキュメントで、ハウツー、概念、トラブルシューティング、ベストプラクティスに関する質問に回答します | `product-knowledge` | すべての対象アプリケーション | 「ストリーミング宛先を設定するにはどうすればよいですか？」 ・ 「バッチセグメンテーションとストリーミングセグメンテーションの違いは何ですか？」 |
| Experience Platform / Journey Optimizer エンティティのクエリ | プラットフォームエンティティに関する質問の主要なエントリポイントとして機能し、必要に応じてKG、フィールドディスカバリー、またはAPIにルーティングできます | `operational-insights` | すべての対象アプリケーション | 「データセットはいくつありますか？」 ・ 「アクティブなジャーニーをすべて表示」 ・ 「宛先を一覧表示」 |
| ナレッジグラフクエリ | 単一のSQL クエリを使用したカウントの集計、エンティティ間の結合、関係検索、メタデータの検索 | `knowledge-graph` | すべての対象アプリケーション | 「どのオーディエンスがこのデータセットを使用しますか？」 ・ 「スキーマとデータセット間の関係を表示」 |
| Experience Platform/Journey Optimizer/Customer Journey Analytics APIの操作 | ナレッジグラフにない突然変異、リアルタイム状態チェック、およびエンティティタイプに対して、直接API ゲートウェイを提供します | `cxo-api` | すべての対象アプリケーション | 「データセット Xを削除」 ・ 「バッチ取り込みジョブのステータスを確認」 |
| エンティティの解決とリンク | セマンティック検索と字句検索を使用して、実際のExperience Platform エンティティに対するエンティティのメンションを解決し、XDM フィールドを検出します | `entity-linking` | Adobe Experience Platform | 「実際のオーディエンスに『ホリデーショッパー』を解決する」 ・「購入履歴に関連するフィールドを検索する」 |
| カスタムスキルの管理 | 再利用可能なユーザー所有スキルを保存、変更、削除できます。これらのスキルは、セッションをまたいで保持されます | `manage-skill` | すべての対象アプリケーション | 「そのワークフローをスキルとして保存」 ・ 「週次レポートスキルを削除」 ・ 「これを再利用可能なスキルに変換」 |
| ストリーミング容量とデータ侵害の監視 | サンドボックスをまたいで、現在および過去のストリーミング利用状況、キャパシティ、侵害ステータスを確認できます | `observability-streaming-capacity`, `observability-streaming-usage`, `observability-capacity-breaches` | Adobe Experience Platform | 「現在のサンドボックスの現在のストリーミング容量は何ですか？」 ・ 「先週の現在のサンドボックスの容量制限に違反していますか？」 |
| [&#x200B; ヘルスチェックの評価結果を表示](https://experienceleague.adobe.com/ja/docs/experience-platform/run-and-operate/health-checks/overview) | サンドボックスの最新のヘルスチェック評価を表示し、失敗したチェックをドリルダウンして、影響を受けるエンティティを確認します | `rao-view-latest-health-checks-assessment` | Adobe Experience Platform | 「私のサンドボックスのどこが悪いのですか？」 ・ 「最新のヘルスチェック評価について教えてください」 ・ 「カスタム名前空間説明チェックの問題は何ですか？」 |
| ヘルスチェックの問題を修正 | 変更が行われる前に承認を得て、フラグ付きのID名前空間、結合ポリシー、スキーマの問題をチャットから直接修正します | `rao-remediate-identity-namespace-description`, `rao-remediate-merge-policy-duplicate-name`, `rao-remediate-missing-audit-field-group`, `rao-remediate-default-merge-policy-naming` | Adobe Experience Platform | 「ID名前空間の説明を修正」 ・ 「重複する結合ポリシー名を修正」 ・ 「監査フィールドグループが欠落しているスキーマを修正」 ・ 「デフォルトの結合ポリシーの名前付けを修正」 |

## サンドボックスツール

| 使用例 | 説明 | スキル | アプリケーション | サンプルプロンプト |
| --- | --- | --- | --- | --- |
| [&#x200B; サンドボックス間でオブジェクトを移動](/help/agents/sandbox-tooling.md) | 依存関係を自動解決し、スキーマ、オーディエンス、その他のオブジェクト設定をサンドボックス間でシームレスに移行できます | `sandbox-tooling-workflow` | Adobe Experience Platform | 「スキーマのLuma Loyalty Members Platinumを現在のサンドボックスから実稼動サンドボックスに移動」 ・ 「US Gold Loyalty Members オーディエンスをステージに昇格させる」 |
