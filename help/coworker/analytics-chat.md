---
title: Adobe Customer Journey Analyticsのデータを分析する（チャット）
description: Adobe CX Enterprise Collaborker Chatを使用して、Customer Journey Analyticsのデータを分析し、ファネルを構築し、カスタマージャーニーのどの段階で顧客が脱落しているのかを確認する方法を説明します。
source-git-commit: 6e3ab12f1d9ec706e745749b7ca47b91a09ff8b3
workflow-type: tm+mt
source-wordcount: '2104'
ht-degree: 5%

---

# Adobe Customer Journey Analyticsのデータを分析する（チャット）

>[!AVAILABILITY]
>
>この記事で説明する機能は、リリースの限定的なテスト段階にあり、お使いの環境ではまだ利用できない場合があります。 このメモは、機能が一般公開された時点で削除されます。 Customer Journey Analytics リリースプロセスについて詳しくは、[Customer Journey Analytics機能リリース &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/releases/latest)を参照してください。

Adobe CX Enterprise Coworker Chatでは、以前はAnalysis Workspaceでのみ可能だった高度なデータ分析を実行できます。 Coworker Chatは、Customer Journey Analyticsのデータビューからデータにアクセスし、そのデータを検索して、自然言語プロンプトに対する回答を得ることができます。

分析を開始する前に、Coworker Chat インターフェイスと設定オプションについて説明し、CoworkerがCustomer Journey Analyticsと、使用するデータを含むデータビューに接続されていることを確認します。

## 同僚とのチャットを始める

### インターフェイスと設定オプション

Customer Journey Analytics データでCoworker Chatを使用する前に、ログインして次の機能の設定オプションを管理する方法について説明します。

* チャット入力

* 会話

* Marketplaces

* MCP サーバー

* メモリ

* プラグイン

* スキル

* その他

詳しくは、[同僚チャット UI ガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/cx-enterprise-coworker/content/chat/ui-guide)を参照してください。

### Customer Journey Analyticsのユースケース

Adobe CX Enterprise Coworker Chatでは、Customer Journey Analyticsのユースケースと、実務担当者が使用しているサンプルプロンプトを確認できます。 各プロンプトは、コピーできるように構築され、独自のデータやコンテキストに適応させ、会話を通じて洗練させられます。

詳しくは、[&#x200B; ユースケース &#x200B;](https://experienceleague.adobe.com/ja/docs/cx-enterprise-coworker/content/chat/use-cases)を参照してください。

## Workfront ChatがCustomer Journey Analyticsに接続されていることを確認します

1. Coworker Chatで、CoworkerがCustomer Journey Analyticsに接続されていることを確認します。

1. 左側のパネルで「MCP」アイコンを選択し、接続されているMCP サーバーのリストで&#x200B;[!UICONTROL **cja-mcp**]&#x200B;が使用可能であることを確認します。

   ![同僚の左側のパネルで強調表示されたMCP アイコン &#x200B;](assets/data-validation-aa-cja/coworker-mcp-cja.png)

1. （条件付き） [!UICONTROL **cja-mcp**]&#x200B;がまだ接続されていない場合は、[!UICONTROL **MCP Server**]&#x200B;を追加を選択し、[!UICONTROL **サーバー名**] フィールドにcjaを指定して、表示されたら選択し、[!UICONTROL **サーバー**]&#x200B;を追加を選択します。

## 適切なデータビューへの接続

データビューとは、データの解釈方法を決定するCustomer Journey Analyticsのコンテナです。

Customer Journey Analyticsでは、さまざまなデータビューにアクセスでき、それぞれに異なるディメンションと指標が含まれており、データを分析する際に利用することができます。

### 使用するデータビューを決める

同僚に、回答したい質問の種類を伝え、その情報を提供するのに最適なデータビューにアクセスできるかどうかを尋ねます。 また、[&#x200B; データビューをメモリ &#x200B;](#add-a-data-view-preference-in-memory)の環境設定として設定することもできます。

**あなた：**

>[!BEGINSHADEBOX]

カスタマージャーニーのどこで顧客が脱落しているのかを把握したい。 Customer Journey Analyticsのどのデータビューにアクセスすれば、この質問に答えることができますか？

>[!ENDSHADEBOX]

**同僚チャット応答：**

>[!BEGINSHADEBOX]

3つのデータビューにアクセスできます。 `Customer lifecycle` データビューには、次のディメンションと指標が含まれており、質問に答えるのに最適です。

>[!ENDSHADEBOX]

**あなた：**

>[!BEGINSHADEBOX]

では、そのデータビューを使ってみましょう。

>[!ENDSHADEBOX]

**同僚チャット応答：**

>[!BEGINSHADEBOX]

さて、このチャットセッションでの今後の質問に答えるために`Customer lifecycle` データビューを使用します。

>[!ENDSHADEBOX]

### メモリにデータビューの環境設定を追加する

Coworker Chatには、すべてのチャットにまたがる情報へのアクセスを提供できるメモリ機能が含まれています。 同僚のメモリに、好みのデータビューをプリファレンスとして追加することをお勧めします。

1. Coworker Chatの左側のナビゲーションで、「メモリ」アイコンを選択します。

1. メモリーページの「保存された環境設定」セクションで、Coworker Chatでチャットで使用する1つ以上のデータビューを指定します。

   ![左側のパネルのメモリ セクション &#x200B;](assets/data-validation-aa-cja/coworker-memory.png)

## Customer Journey Analytics での分析

Coworkerがビジュアライゼーションを作成した後、Customer Journey AnalyticsのAnalysis Workspaceでビジュアライゼーションを開くと、より詳細なコントロールを使用してより詳細な分析を行うことができます。 Customer Journey Analyticsの新しいAnalysis Workspace プロジェクトでビジュアライゼーションが開きます。

新しいAnalysis Workspace プロジェクトでビジュアライゼーションを開くには：

1. Coworkerで作成されたビジュアライゼーションの横にある「[!UICONTROL **CJAで分析**]」を選択します。

1. Customer Journey Analyticsでビジュアライゼーションを開くと、Analysis Workspaceのドラッグ&amp;ドロップ操作のブラウザーインターフェイスを使用して変更を加えたり、分析をさらに細分化したり、オーディエンスを作成したりできます。 Workspaceプロジェクトは、誰とでも共有できます。

   Analysis Workspaceについて詳しくは、[Analysis Workspaceの概要](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-workspace/home)を参照してください。

## 例：顧客の脱落する箇所の特定

ビジネス上のあらゆる質問を分析するために、データを使用するようにCoworker Chatに依頼できます。

たとえば、マーケティングマネージャー、マーチャンダイザー、グロース担当者は、顧客がどこで購入への道筋を放棄したのか、なぜ離脱したのか、コンバージョン率を高めるために何ができるかを把握する必要があります。

>[!NOTE]
>
>以下の図は、架空のretailer [!DNL TechPulse Electronics]のサンプルデータを示しています。このデータは、会話の形を示すために使用されます。

### 質問の種類

「フォールアウトビジュアライゼーション」とは何か、またどの指標がどのスロットに入るかを知る必要はありません。 重視する結果を平易な言葉で記述しましょう。

* 「どこで買い物に行く途中で人々を失っているのか？」
* 「商品ビューからチェックアウトまで、funnelのコンバージョン率はいくらですか？」
* 「カートと購入の間に最もリークするマーケティングチャネルはどれですか？」
* 「モバイルやデスクトップでのカート放棄の状況は悪化していますか？」
* 「有料ソーシャル広告の人々は、メールの人々とは異なるコンバージョンになりますか？」

### 会話

#### &#x200B;1. ビジネス上の課題から始めましょう

**あなた：**

>[!BEGINSHADEBOX]

購買に至る過程で顧客が失っている場所はどこか？

>[!ENDSHADEBOX]

**同僚チャット応答：**

同僚とのチャットでは、適切なビジュアライゼーションの選択、顧客接点のシーケンス化、さらには推奨される次のステップの追加などが可能です。

>[!BEGINSHADEBOX]

![同僚のfunnelの応答](assets/data-validation-aa-cja/coworker-funnel-response.png)

これはfunnelの質問です。funnelでコンバージョンを実行し、購入に至るまでの過程で離脱がどこで発生するかを確認します。

顧客を失う原因：

| Funnel ステップ | カウント | 次へのコンバージョン | 脱落 |
| --- | --- | --- | --- |
| Sessions | 137,476 | 45.0%が商品を閲覧 | 55%の企業が商品を閲覧せずに離脱 |
| 製品ビュー | 61,845 | 55.0% カートに追加 | 45%参照するが追加しない |
| 買い物かごに追加 | 34,045 | 16.4%購入 | 83.6% カート放棄 |
| 購入 | 5,582 | — | — |

**大きな発見：買い物かごはあなたの最大の漏れです**

28,463人が商品をカートに入れたが、購入を完了しなかった。 これは83.6%のカートから購入までのドロップオフ率であり、失敗のシングルポイントとして圧倒的に大きい数値です。

つまり、カート追加者の10%だけをコンバージョンすれば、約2,846件の購入が加算されることになります。 現在のデータ規模では、それは大きな売上につながる可能性があります。

**優先事項について説明します：**

| 優先度 | 問題点 | 機会の規模 |
| --- | --- | --- |
| #1 | 買い物かごからの放棄（83.6%減少） | 28,463人のバイヤーが離脱 |
| #2 | 製品ビューへのセッション（55%が閲覧しない） | 75,631件のセッション（製品エンゲージメントなし） |
| #3 | 商品ビューをカートに追加（45%が追加不可） | 2万7,800人に関心があるもののコミットしていない |

**次の手順の推奨：**

1. マーケティングチャネルごとにカートの放棄を分解する – 特定のチャネルは、カートに追加するものの、購入することはない、低意図のトラフィックをもたらしていますか？
1. デバイスタイプごとにカート放棄を検証する – モバイルチェックアウトはコンバージョンを妨げるのでしょうか？
1. 最も放棄される製品を特定する（価格の問題）? 配送サプライズ？

**次に掘り下げたいのはどれですか？** チャネルの内訳を確認すれば、「ほぼ購入者」と実際の購入者のどちらが多いマーケティング活動をもたらすかを直接把握できます。

>[!ENDSHADEBOX]

#### &#x200B;2. リークをドリルインする

**あなた：**

>[!BEGINSHADEBOX]

続いて、マーケティングチャネルごとに説明します

>[!ENDSHADEBOX]

**同僚チャット応答：**

>[!BEGINSHADEBOX]

![同僚のfunnelの応答](assets/data-validation-aa-cja/coworker-funnel-response2.png)

カスタム **マーケティングチャネル** ディメンションがあります。 ここでfunnelを引き出して、チャネルごとのコンバージョン率を計算し、各チャネルがリークする場所を特定します。

**評決：漏洩がチャネル固有ではありません**

これは本当に明らかな発見です。 Funnelのチャネルごとの内訳は次のとおりです。

| チャネル | Sessions | 製品ビュー | カートに追加するには | 購入手続き | 全体的なコンバージョン | 収益/セッション |
| --- | --- | --- | --- | --- | --- | --- |
| 有料検索 | 43,958 | 45.1% | 54.6% | 16.6% | 4.09% | $499.58 |
| オーガニック検索 | 31,492 | 44.9% | 54.9% | 16.9% | 4.17% | $494.76 |
| ダイレクト | 25,661 | 43.6% | 55.4% | 15.8% | 3.82% | $497.29 |
| メール | 17,586 | 45.3% | 55.4% | 16.2% | 4.07% | $501.13 |
| ソーシャル広告 | 12,684 | 45.4% | 55.7% | 16.0% | 4.03% | $512.17 |
| 表示 | 6,511 | 45.3% | 55.7% | 16.2% | 4.09% | $501.45 |

**重要ポイント：**

1. 買い物かごから購入までのドロップオフは、あらゆるチャネルで一様に悪くなっています（83～84%）。 つまり、問題はトラフィックの質ではなく、あらゆるチャネルが同様にエンゲージメントの高い訪問者を提供することです。 そうしたリスクは、マーケティング部門ではなく、決済体験そのものに存在します。
1. コンバージョン率が大幅に向上または低下したチャネルはない。 全体のコンバージョン率は3.8%から4.2%の間で非常に高く、セッションあたりの売上はほぼ同じです（495 ドルから512 ドル）。
1. 配信数が最も重要な場所：有料検索で最も多くの顧客が失われ（9,015件のカート放棄）、次いでオーガニック検索（6,449件のカート放棄）となっています。 トラフィックを最も促進する最大の収益機会です。

**戦略的に何を伝えるか**

マーケティングチャネルは本来の役割を果たしています。人々の関心を惹き、カートへの追加を同程度のスピードで進めています。 問題はマーケティングの下流にあります。チェックアウトと支払いの流れは現金が漏れている場所です。

**次の調査の推奨：**

1. デバイスタイプごとにカートの放棄を分析する – モバイルチェックアウトは適切か、それとも顧客を不快にさせるか？
1. 最も放棄された商品に注目する。決済時に価格や発送に関する驚きはありますか？
1. 「holiday_flash_sale」キャンペーンのチェックアウトコンバージョン率が向上したかどうかを確認します。緊急性を重視したキャンペーンでは、チェックアウトのつまずきを克服できます

**次にどの角度を探索しますか？**

>[!ENDSHADEBOX]

#### &#x200B;3. 調査を継続

**あなた：**

>[!BEGINSHADEBOX]

興味を引く： デバイスの種類ごとに分類してみましょう。

>[!ENDSHADEBOX]

**同僚チャット応答：**

>[!BEGINSHADEBOX]

![同僚のfunnelの応答](assets/data-validation-aa-cja/coworker-funnel-response3.png)

**見つかりました：モバイル チェックアウトが壊れています**

Funnelは、決済プロセスが完了するまで端末をまたいで同じ機能を提供します。その後、モバイルは崖から落ちます。

| デバイス | Sessions | 製品ビュー | カートに追加するには | 購入手続き | 全体的なコンバージョン |
| --- | --- | --- | --- | --- | --- |
| Desktop | 70,172 | 44.9% | 54.8% | 23.2% | 5.70% |
| タブレット | 14,149 | 44.7% | 55.6% | 14.3% | 3.56% |
| モバイル | 53,449 | 44.9% | 55.3% | 8.1% | 2.02% |

**喫煙銃**

| 指標 | Desktop | モバイル | 間隔 |
| --- | --- | --- | --- |
| カートから購入率 | 23.2% | 8.1% | 15% ポイント |
| モバイル | — | 2.8倍悪い | — |
| カート放棄 | 13,274 | 12,178 | ほぼ同じ絶対量 |

モバイルデバイスでの閲覧とカートへの追加体験は良好です（閲覧率は約45%、カートへの追加率は約55%）。 人々は同じように興味を持ち、熱心です。 しかし、モバイルのチェックアウトフローにコンバージョンの原因があることに気がつきました。

**収益機会**

モバイルチェックアウトのコンバージョン率がPCと同程度であれば、追加購入者数は約1,991人に上ります。これは、エクスペリエンスを修正することで、総購入量が35%増加します。

**起こりそうなことについて**

データパターン（等しいエンゲージメント、壊滅的なチェックアウトドロップ）は、次のような古典的なシグナルです。

* 小さな画面で支払いフォームが処理しにくい（自動入力の問題、フォームレイアウト）
* チェックアウト時に明らかになった予想外のコスト（送料、税金）がステッカーショックの原因になります
* ゲストチェックアウトが利用できない、またはモバイルのログインウォールがある
* モバイルでの決済処理中にページの読み込みまたはタイムアウトが発生する

**次の手順の推奨：**

1. 商品カテゴリーごとにモバイルカートの放棄を分類する – 高価格商品では悪化しますか（モバイル決済の信頼に関する問題が発生することを示唆しています）?
1. 最もモバイルトラフィックを促進しているマーケティングチャネルは何か？有料の広告費をモバイルfunnelに誘導しているチャネルは何か？
1. ページやサイトセクションのシグナルがあるかどうかを確認する – モバイルユーザーが放棄する前に最後にアクセスしたチェックアウトページを確認できるか？

**どちらを調査しますか。それとも、UX チームとチェックアウト チームに伝えるのに十分な証拠ですか？**

>[!ENDSHADEBOX]

#### &#x200B;4. 決定に変換

**あなた：**

>[!BEGINSHADEBOX]

では、どうすればよいでしょうか？

>[!ENDSHADEBOX]

**同僚チャット応答：**

>[!BEGINSHADEBOX]

データから分かるように、次のことに注力します。

* **モバイル チェックアウトを修正します。チャネルの問題ではありません。** あらゆるチャネルで、オーディエンスが同様の健全な割合でカートに入れるようにしているため、広告費は全体的に効果を発揮しています。 売上は、修正の対象となるモバイルチェックアウトフローにおいて失われています。
* **支払いとフォームの摩擦を開始します。** これらは、購買意欲の高いモバイル顧客がカートを放棄する最も一般的な理由です。 通常、モバイルウォレットのオプションを提供し、フォームを短縮することが最速の成果です。
* **修正後に再度確認します。** チェックアウトが完了したら、モバイルのカートから購入への割合が、デスクトップの23.2%に上昇するかどうかを確認します。

これをプロジェクトとして保存して追跡できるようにするのか、モバイルカートから購入までのしきい値を下回った場合にアラートを設定するのか？

>[!ENDSHADEBOX]

### 何が起こったのか

平易な言葉で言える4つの質問があり、Coworkerがサポートしてくれました。

* マルチステップのコンバージョンを構築するfunnelでは、最大のリークとしてカートから購入へとフラグを立てます
* 原因としてマーケティングチャネルを除外：あらゆるチャネルでのリーク率はほぼ同じです
* 実際の問題をモバイルでのチェックアウトに分離し、その解決方法を購入額の35%向上で定量化します
* モバイル決済やフォームでのつまずきなど、特定の修正を優先しましょう。 これは、デスクトップのコンバージョン率が23.2%であることを基準としています

<!--

## Example #2: Find which marketing efforts drive revenue

You can ask Coworker Chat to use your data to analyze any business question.

For example, as a marketing manager, demand generation lead, or CMO, you might want to know which marketing efforts actually deserve credit for revenue so you can confidently decide where to put your marketing spend, rather than rewarding whichever channel happened to get the last click.

>[!NOTE]
>
>The figures below are illustrative sample data for a fictional retailer, [!DNL TechPulse Electronics], used to show the shape of the conversation.

### The types of questions you can ask

You don't need to know what an "attribution model" is, or how to configure an Attribution panel. Instead, describe the outcome you care about in plain language:

* "Which channels actually drive our revenue, not just the last click?"
* "If I change how I give credit for a sale, does my best channel change?"
* "Which campaigns start customer journeys versus close them?"
* "Am I over-investing in paid search because it always gets the last click?"
* "What role does email play in conversions it never gets credit for?"

### The conversation

#### 1. Start with the business question

**You:**

>[!BEGINSHADEBOX]

Which marketing channels actually drive our revenue?

>[!ENDSHADEBOX]

**Coworker Chat response:**

Notice that Coworker Chat picks the right analysis, starts with the model most reports default to, and immediately flags what that model can't tell you.

>[!BEGINSHADEBOX]

![Coworker Chat showing attributed revenue by marketing channel under a last-touch model](assets/data-validation-aa-cja/coworker-attribution-response.png)

This is an attribution question — let me attribute revenue to your marketing channels so you can see who's earning it.

I'll start with **last-touch attribution**, since that's what most out-of-the-box reports show. It gives all the credit for a sale to the last channel a person used before purchasing.

| Marketing channel | Attributed revenue (last touch) | Share |
| --- | --- | --- |
| Paid search | $948,000 | 34% |
| Organic search | $614,000 | 22% |
| Direct | $474,000 | 17% |
| Email | $307,000 | 11% |
| Paid social | $251,000 | 9% |
| Display | $195,000 | 7% |

**The headline: paid search looks like your hero**

Under last touch, paid search earns a third of all revenue — more than any other channel. If this were the only view you had, you'd likely pour more budget into paid search.

**One important caveat before you do that**

Last touch only tells you who *closed* the sale. It says nothing about who *started* the journey or *assisted* along the way. A channel that introduces people to your brand weeks before they buy gets zero credit here, even if the purchase never would've happened without it.

To know whether paid search is really driving revenue — or just harvesting demand other channels created — you need to compare attribution models.

**Recommended next step:**

Compare the same channels across first-touch, last-touch, and linear models. If paid search stays on top across all of them, it's a genuine driver. If it shrinks under first touch, it's a closer, not a creator.

**Want me to run that comparison?**

>[!ENDSHADEBOX]

#### 2. Compare attribution models

**You:**

>[!BEGINSHADEBOX]

Yes, compare it across models.

>[!ENDSHADEBOX]

**Coworker Chat response:**

>[!BEGINSHADEBOX]

![Coworker Chat comparing channel revenue share across first-touch, last-touch, and linear attribution models](assets/data-validation-aa-cja/coworker-attribution-response2.png)

Here's each channel's share of revenue under three models. First touch credits the channel that started the journey, last touch credits the one that closed it, and linear splits credit evenly across every touch.

| Marketing channel | First touch | Last touch | Linear |
| --- | --- | --- | --- |
| Paid search | 19% | 34% | 26% |
| Organic search | 20% | 22% | 21% |
| Direct | 9% | 17% | 13% |
| Email | 18% | 11% | 15% |
| Paid social | 21% | 9% | 15% |
| Display | 13% | 7% | 10% |

**The verdict: your "best" channel depends entirely on how you count**

This is the finding that changes budget decisions.

1. **Paid search closes far more than it starts.** It jumps from 19% of first touches to 34% of last touches. That's the signature of a *harvester* — it captures people who are already ready to buy, often after another channel introduced them. Valuable, but it's finishing journeys, not creating them.
1. **Paid social and email are badly undercredited by last touch.** Paid social starts 21% of journeys but gets credit for only 9% of sales. Email starts 18% but closes 11%. These channels are doing the expensive work at the top of the funnel and handing warm prospects to paid search.
1. **Organic search is your steady workhorse.** It sits around 20% across every model — it both starts and closes journeys reliably.

**Why this matters for budget**

If you cut paid social or email based on their weak last-touch numbers, you'd starve the top of your funnel — and paid search would have far fewer ready-to-buy people to close. You'd likely see paid search revenue fall too, even though you didn't touch its budget.

**Recommended next step:**

Look at the campaign level to see exactly which efforts start journeys versus close them. That's where you can act — trimming or protecting specific campaigns rather than whole channels.

**Want me to break this down by campaign?**

>[!ENDSHADEBOX]

#### 3. Keep investigating

**You:**

>[!BEGINSHADEBOX]

Let's break it down by campaign.

>[!ENDSHADEBOX]

**Coworker Chat response:**

>[!BEGINSHADEBOX]

![Coworker Chat showing top campaigns ranked by their role as initiators or closers of customer journeys](assets/data-validation-aa-cja/coworker-attribution-response3.png)

There's a **Campaign Name** dimension. Here are your highest-involvement campaigns, comparing the revenue they start (first touch) against the revenue they close (last touch).

| Campaign | Starts (first touch) | Closes (last touch) | Role |
| --- | --- | --- | --- |
| brand_awareness_q3 | $412,000 | $103,000 | Initiator |
| email_winback | $214,000 | $88,000 | Initiator |
| holiday_flash_sale | $268,000 | $249,000 | All-rounder |
| retargeting_dynamic | $71,000 | $339,000 | Closer |
| branded_search_always_on | $84,000 | $498,000 | Closer / harvester |

**The pattern: some of your "worst" campaigns are actually your best starters**

* **brand_awareness_q3** and **email_winback** start far more revenue than they close. On a last-touch ROI report, these look like underperformers you might cut. In reality, they're filling the top of your funnel — the journeys other campaigns finish.
* **retargeting_dynamic** and **branded_search_always_on** are the opposite. They close a lot but start almost nothing. They're efficient closers, but they can only close demand that already exists. Branded search, in particular, is largely capturing people who were going to search for you by name anyway.
* **holiday_flash_sale** does both — it introduces new shoppers and closes them, which is why urgency-driven promotions often look strong under any model.

**What this tells you strategically**

The campaigns you'd cut first on a last-touch report — the awareness and win-back efforts — are the ones creating the demand your closers depend on. Judge initiators on the journeys they start, and closers on the journeys they finish.

**Recommended next steps:**

1. Protect the initiator campaigns even though their last-touch ROI looks weak — they're feeding the funnel.
1. Right-size the branded search spend — test whether trimming it changes total revenue, since much of that demand may convert anyway.
1. Adopt a balanced model — like linear or a position-based model — as your default reporting view, so no channel gets systematically over- or under-rewarded.

**Want me to save this as a project, or is this enough to take into your budget planning?**

>[!ENDSHADEBOX]

#### 4. Turn it into a decision

**You:**

>[!BEGINSHADEBOX]

So how should I allocate budget?

>[!ENDSHADEBOX]

**Coworker Chat response:**

>[!BEGINSHADEBOX]

Based on what the data shows, here's where I'd focus:

* **Stop judging upper-funnel channels on last touch alone.** Paid social and email start about 20% of your revenue each, but last touch credits them for less than half of that. Protect their budgets — they're creating the demand paid search closes.
* **Treat branded search as a harvester, not a driver.** It closes a lot but starts almost nothing. Test trimming it, since much of that demand may convert through other paths anyway.
* **Make a balanced model your default.** Reporting on linear or a position-based model instead of last touch will stop you from over-rewarding closers and under-funding the channels that start journeys.
* **Re-check after you rebalance.** Watch whether total revenue holds steady as you shift spend toward initiators — that's the signal your funnel is healthier, not just your last-touch report.

Want me to save this as a project so you can track it, or build a calculated metric that reports revenue on a balanced attribution model going forward?

>[!ENDSHADEBOX]

### What just happened

In four plain-language questions, Coworker helped us:

* Attribute revenue to marketing channels and flag that the default last-touch view tells only part of the story
* Compare attribution models and reveal that the "best" channel changes completely depending on how credit is counted
* Discover that paid social and email start far more revenue than they ever get credit for closing
* Identify which campaigns initiate journeys versus close them, and walk away with a budget direction: protect the initiators, right-size the harvesters, and report on a balanced model

-->
