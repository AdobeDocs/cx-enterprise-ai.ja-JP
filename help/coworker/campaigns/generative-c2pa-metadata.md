---
description: AIが生成および編集した画像に対して、Coworker CampaignsがC2PA メタデータ（Content Credentials）を自動的にアタッチして保存する方法を説明します。アクションは必要ありません。
title: Coworker CampaignsのC2PA メタデータ
hide: true
source-git-commit: 785b5d106cb029d68506c90385786cbdae164991
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 2%

---

# Coworker CampaignsのC2PA メタデータ {#overview}

生成AIの透明性に関する新たな法律が制定されつつあり、Adobeでは、さまざまな地域で適用される要件を満たすために取り組んでいます。 [C2PA メタデータ &#x200B;](https://c2pa.org/) （Content Credentialsとも呼ばれます）は、Adobeがこれらの法律の要件を満たすために使用する来歴ツールです。

C2PA メタデータは、コンテンツがどのように作成または編集されたかを記録する、耐久性のある目に見えないメタデータです。 Workfront Campaignsの生成AI ツールを使用して画像を生成または編集すると、C2PA メタデータが自動的にその画像に添付されます。 お客様の側で操作は必要ありません。

## C2PA メタデータを添付するアクション {#cc-workflows}

次の表は、Coworker Campaignsの画像生成で実行された画像アクションに基づいて、C2PA メタデータが添付されるタイミングを示しています。

| アクション | 説明 | C2PA メタデータが添付されていますか？ | 使用例 |
| --- | --- | --- | --- |
| **画像を生成** | テキストプロンプトや参照画像から新しい画像を作成したり、既存の画像から類似した画像を生成したりできます。 | 常に最適化。 画像は生成AIによって生成されるので、常に新しいC2PA メタデータを持ちます。 | 電子メールキャンペーンのバナー画像は、目的のビジュアルを説明するテキストプロンプトから生成されます。 |
| **画像を切り抜く** （中央またはスマート切り抜き） | 要求された寸法に合わせて画像を調整する | ソース画像に既にC2PA メタデータがある場合のみ。 切り抜きは、通常C2PA メタデータを消去する画像のピクセルを再作成します。そのため、Coworker Campaignsの画像生成では、切り抜く前にソース画像から画像を読み取り、それを再作成して、切り抜いた結果に再添付します。 切り抜き自体は、新しい生成AI アクションを追加するものではなく、既存の生成AI アクションを保持します。 | 生成されたバナー画像は、web ページに合わせて切り抜かれます。C2PA メタデータは切り抜き中に保持されます。<br> プッシュ通知の背景として使用されるアップロードされたストック写真は、画面に合わせて切り抜かれます。ストック写真には生成AI アクションが含まれていないため、C2PA メタデータは作成されません。 |
| **テキストオーバーレイを追加** | 生成されたテキストを背景画像の上にレンダリング | 背景画像にC2PA メタデータが既に含まれている場合のみ。 オーバーレイをレンダリングすると、背景からテキストを加えた新しい画像が生成され、通常はC2PA メタデータが消去されるので、Coworker Campaignsの画像生成では、事前に背景画像から画像を読み取り、それを再構築して結果に再添付します。 オーバーレイ手順では、新しい生成AI アクションは追加されません。 | プロモーション見出しは、ランディングページ用に生成された背景画像上にテキストオーバーレイとしてレンダリングされます。背景画像のC2PA メタデータは保持されます。 |
| **画像をオーバーレイ** | 複数の画像を合成 | いずれかのソース画像にC2PA メタデータがある場合、結合された画像は、そのすべてを単一のC2PA メタデータセットに結合して保持します。 合成すると、ソースから新しい画像が生成され、通常はそのC2PA メタデータが消去されるので、Coworker Campaignsの画像生成では、合成する前に各メタデータを読み取り、次に、生成AI アクションに貢献したすべてのソースを一覧表示するC2PA メタデータレコードを1つ組み合わせて作成します。 | 生成された製品画像と、メールヘッダー用に生成された背景を合成すると、生成AIの両方のソースを反映したC2PA メタデータが取り込まれます。<br> アップロードされた2枚のブランド写真が1つのコラージュに合成されます。どちらのソースも生成AI アクションを実行しないため、C2PA メタデータは作成されません。 |

## コンテンツの種類とその範囲 {#cc-content-types}

* **画像**：対象。 生成AIで画像を生成すると、C2PA メタデータが添付され、Coworker Campaignsの画像生成で実行されるトリミング、テキストオーバーレイ、画像オーバーレイ操作を通じて保存されます。
* **テキスト**：該当しません。 コピー生成、翻訳、ブランド整列の提案など、Adobe Workfront キャンペーンでの画像生成のテキストのみの出力には、C2PA メタデータは必要ありません。

## コンテンツが移動するとどうなるか {#cc-content-moves}

Coworker Campaignsは、サポートされている画像アセットに関連付けられているContent Credentialsを保持します。 Coworker Campaignsに読み込まれた画像にContent Credentialsが含まれている場合、生成されたキャンペーンコンテンツとアウトバウンドメールエクスペリエンスでアセットを使用する際に、これらの資格情報が保持されます。 [C2PA メタデータについて詳しく見る](https://helpx.adobe.com/jp/firefly/using/content-credentials.html){target="_blank"}。

<!-- Some ways of bringing images into your content, such as extracting an image from a PDF or from an embedded (base64) source, may not preserve the original C2PA metadata. In these cases, no C2PA metadata can be read from the source, and none is created for the result. -->

>[!MORELIKETHIS]
>
>[Adobe Experience Cloud生成AI ユーザーガイドライン &#x200B;](https://www.adobe.com/jp/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
