---
description: AIが生成および編集した画像に対して、Coworker CampaignsがC2PA メタデータ（Content Credentials）を自動的にアタッチして保存する方法を説明します。アクションは必要ありません。
title: Coworker CampaignsのC2PA メタデータ
hide: true
source-git-commit: c03bdd213d3e96de1bee022b98e4809d3100a195
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 8%

---

# Coworker CampaignsのC2PA メタデータ {#overview}

生成AIの透明性に関する新たな法律が制定されつつあり、Adobeでは、さまざまな地域で適用される要件を満たすために取り組んでいます。 [C2PA メタデータ ](https://c2pa.org/) （Content Credentialsとも呼ばれます）は、Adobeがこれらの法律の要件を満たすために使用する来歴ツールです。

C2PA メタデータは、コンテンツがどのように作成または編集されたかを記録する、耐久性のある目に見えないメタデータです。 Workfront Campaignsの生成AI ツールを使用して画像を生成または編集すると、C2PA メタデータが自動的にその画像に添付されます。 お客様の側で操作は必要ありません。

## C2PA メタデータを添付するアクション {#cc-workflows}

次の表は、Coworker Campaignsの画像生成で実行された画像アクションに基づいて、C2PA メタデータが添付されるタイミングを示しています。

| アクション | 説明 | C2PA メタデータが添付されていますか？ | 使用例 |
| --- | --- | --- | --- |
| **画像を生成** | テキストプロンプトや参照画像から新しい画像を作成したり、既存の画像から類似した画像を生成したりできます。 | 常に最適化。 画像は生成AIによって生成されるので、常に新しいC2PA メタデータを持ちます。 | 電子メールキャンペーンのバナー画像は、目的のビジュアルを説明するテキストプロンプトから生成されます。 |

## コンテンツの種類とその範囲 {#cc-content-types}

* **画像**：対象。 生成AIで画像を生成すると、C2PA メタデータが添付され、Coworker Campaignsの画像生成で実行されるトリミング、テキストオーバーレイ、画像オーバーレイ操作を通じて保存されます。
* **テキスト**：該当しません。 コピー生成、翻訳、ブランド整列の提案など、Adobe Workfront キャンペーンでの画像生成のテキストのみの出力には、C2PA メタデータは必要ありません。

## コンテンツが移動するとどうなるか {#cc-content-moves}

Coworker Campaignsは、サポートされている画像アセットに関連付けられているContent Credentialsを保持します。 Coworker Campaignsに読み込まれた画像にContent Credentialsが含まれている場合、生成されたキャンペーンコンテンツとアウトバウンドメールエクスペリエンスでアセットを使用する際に、これらの資格情報が保持されます。 [C2PA メタデータについて詳しく見る](https://helpx.adobe.com/jp/firefly/using/content-credentials.html){target="_blank"}。

<!-- Some ways of bringing images into your content, such as extracting an image from a PDF or from an embedded (base64) source, may not preserve the original C2PA metadata. In these cases, no C2PA metadata can be read from the source, and none is created for the result. -->

## その他のリソース

* [Adobe Experience Cloud生成AI ユーザーガイドライン](https://www.adobe.com/jp/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}

* [Adobeの各製品におけるContent Credentialsの仕組み](https://helpx.adobe.com/jp/firefly/using/content-credentials.html){target="_blank"}

* [ガードレールと制限](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/generate-content/gs-generative#generative-guardrails){target="_blank"}
