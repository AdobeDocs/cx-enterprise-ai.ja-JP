---
description: 生成からメール配信まで、Coworker Campaignsが画像にC2PA メタデータを自動的に添付して保存する方法について説明します。
title: Coworker CampaignsのC2PA メタデータ
hide: true
source-git-commit: 639602b445cba01fce2130006f98e1e388ba7d5b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 4%

---

# Coworker CampaignsのC2PA メタデータ {#overview}

生成AIの透明性に関する新たな法律が制定されつつあり、Adobeでは、さまざまな地域で適用される要件を満たすために取り組んでいます。 [C2PA メタデータ &#x200B;](https://c2pa.org/)は、Adobeがこれらの法律の要件を満たすために使用する来歴ツールです。

C2PA メタデータは、コンテンツがどのように作成または編集されたかを記録する、耐久性のある目に見えないメタデータです。 Workfront Campaignsの生成AI ツールを使用して画像を生成または編集すると、C2PA メタデータが自動的にその画像に添付されます。 お客様の側で操作は必要ありません。

## メールキャンペーンのC2PA メタデータ {#c2pa-metadate-email}

メールキャンペーンで送信された画像はC2PA メタデータを維持するので、受信者は配信されたメールから直接画像の由来と信頼性を確認できます。

## C2PA メタデータを添付するアクション {#actions}

次の表は、Coworker Campaignsの画像生成で実行された画像アクションに基づいて、C2PA メタデータが添付されるタイミングを示しています。

| アクション | 説明 | C2PA メタデータが添付されていますか？ | 使用例 |
| --- | --- | --- | --- |
| **画像を生成** | テキストプロンプトや参照画像から新しい画像を作成したり、既存の画像から類似した画像を生成したりできます。 | 常に最適化。 画像は生成AIによって生成されるので、常に新しいC2PA メタデータを持ちます。 | 電子メールキャンペーンのバナー画像は、目的のビジュアルを説明するテキストプロンプトから生成されます。 |

## コンテンツの種類とその範囲 {#content-types}

* **画像**：対象。 生成AIで画像を生成すると、C2PA メタデータが添付され、Coworker Campaignsの画像生成で実行されるトリミング、テキストオーバーレイ、画像オーバーレイ操作を通じて保存されます。
* **テキスト**：該当しません。 コピーの生成、翻訳、ブランド整列の提案など、Adobe Workfrontのテキストのみの出力には、C2PA メタデータは必要ありません。

## コンテンツが移動するとどうなるか {#content-moves}

Coworker Campaignsは、サポートされている画像アセットに関連するC2PA メタデータを保持します。 画像にCoworker Campaignsに読み込まれた際にC2PA メタデータが含まれている場合、生成されたキャンペーンコンテンツとアウトバウンドメールエクスペリエンスでアセットが使用されるときに、それらの資格情報が保持されます。

## その他のリソース {#resources}

* [Adobe Experience Cloud生成AI ユーザーガイドライン](https://www.adobe.com/jp/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}

* [ガードレールと制限](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/content-management/generate-content/gs-generative#generative-guardrails){target="_blank"}
