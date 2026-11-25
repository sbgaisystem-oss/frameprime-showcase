# 料金・Credits・完成後の修正

**現行製品Version：v0.0.3（2026-11-25）。** v0.0.2のStudio・Credit案内改善を維持し、今回の安定性改善後も実ユーザーの通常生成1 Credit、字幕Revision追加0 Creditsを本番で確認しました。動画生成に付随するSNS投稿文・ハッシュタグは追加0 Credits。料金・消費ルールは変更していません。選択言語字幕翻訳は未提供です。

FramePrimeでは、**新しい動画を制作する料金**と、**完成した動画を対応範囲で修正する料金**を分けています。

**現在の公開画面の案内は「2分までの動画生成」です。料金は入力実尺2分以内の対応動画が1本1 Creditです。新規登録特典は10 Creditsで、同条件の10本分の制作Creditに相当します。** すべての素材で制作成功を保証する意味ではありません。2分を超える料金計算は、現在の長尺対応や今後の提供時期を示すものではありません。

## 現在の料金制度と本番確認の範囲

表示と内部精算は同じ整数Creditです。通常の買い切りパック換算では1 Credit＝100円相当で、月額やβ体験の単価は異なります。2026年11月21日に現行の整数料金へ移行しました。登録・購入経路は公開済みで、11月22日の3,000円買い切り→30 Credits、紹介双方各4 Creditsの本番実績があります。**11月21日夜の本番記録には、動画2本の納品と合計2 Creditsの精算もあります。**

**2026年11月23日、制作履歴のない登録済みアカウントで、購入なしの初回動画制作→字幕入り動画の納品・ダウンロード→1 Credit精算を本番確認しました。** 登録はこの制作確認より前に完了しており、消費したのは紹介Creditsです。同じ操作回での新規登録からの通し確認、登録特典Creditsの消費確認、新しい購入Creditsを使う確認とは区別します。

**同日、認証済み利用者がPCの「字幕・動画を修正」から字幕1か所を保存し、修正版の再書き出し・ダウンロードと追加0 Creditsを本番確認しました。** 元の納品動画は保持され、修正前後の残高は同じでした。字幕修正1例の実績で、すべての編集種類・端末を検証したものではありません。

未確認の範囲には、新料金購入→その購入Creditsを使った新規動画納品→精算を一続きに確認する経路が含まれます。月額各商品の実購入も別に残っています。個別の成功実績を、すべての素材・商品・条件での成功保証に拡張しません。

## 投稿文は、Creditを気にせず作成できます

動画生成時に、SNS投稿文やハッシュタグも一緒に準備できます。**投稿文を付けても付けなくても、その動画制作で消費するCreditsは変わりません。** 付随する投稿文の追加消費は0 Creditsです。現在、投稿文だけを新規作成する単独機能は提供していません。過去の投稿準備は閲覧できます。

## SNS投稿文・投稿準備の料金

**対応する動画生成フローで付随するSNS投稿文・ハッシュタグ・投稿準備には追加0 Creditsです。** 動画制作そのもののCredit精算とは別で、投稿文の有無によって動画制作の消費数は変わりません。**現在は投稿文の単独新規作成を提供していません。** 旧β版の「投稿準備パッケージ単位で1 Credit」は現行仕様ではありません。

## 制作・修正の料金契約

### Original Voice generation

A successfully delivered Original Voice generation consumes:

**現在の案内は「2分までの動画生成」です。料金は正の入力実尺2分以内なら1 Creditです。** 料金契約上は、2分超〜8分＝2 Credits、8分超は開始した4分ごとに2 Credits追加（32分＝14 Credits）と定義されています。2分超の値は計算ルールの説明であり、現在の受付・制作・納品範囲や将来の対応予定ではありません。

The generation path uses a reservation / settlement model so the system can distinguish a successful delivery from a terminal failure.

### System-terminal failure

A normal system-terminal failure releases the reservation:

**Net user credit cost: 0**

This is different from a quality-compensation case after a nominal delivery.

### Revision Render

Supported post-delivery Revision Render operations use:

**0 additional user credits**

This means a user can refine the delivered result through the supported revision workflow without paying another generation credit for each revision render.

## 購入プランと利用条件

Monthly and one-time credit plans are part of the approved product contract. All amounts are tax-inclusive JPY. Credits do not expire; unused balances carry over even after subscription cancellation. The following prices are the current adopted catalog with live checkout activated; availability, eligibility, successful payment and completed new-video delivery are separately verified.

### 月額プラン（税込）

| Monthly price | Credits granted monthly | Effective price per Credit* |
| --- | ---: | ---: |
| ¥2,900 | 32 | approx. ¥90.63 |
| ¥5,800 | 70 | approx. ¥82.86 |
| ¥9,800 | 125 | approx. ¥78.40 |
| ¥19,800 | 260 | approx. ¥76.15 |

*Effective unit price assumes all granted Credits are used. No separate per-video cash charge on top of the Credits consumed.

### 買い切りパック（税込）

| One-time price | Credits granted |
| --- | ---: |
| ¥1,000 | 10 |
| ¥3,000 | 30 |
| ¥6,000 | 60 |
| ¥10,000 | 100 |

One-time packs do not auto-renew. Separately, the **¥980 beta trial pack grants 20 Credits, one purchase per account, without automatic renewal**. Existing legacy ¥980/month Founder subscriptions are distinct and are not silently converted.

Credits have **no expiration** and unused balances **carry over**, including after subscription cancellation. Signup bonus = 10 Credits; qualifying referral rewards = 4 Credits for each side; referral budget = 800 Credits. These denominations are applied in the Production financial DB. Signup and checkout are enabled; the limited 2026-11-22 check confirmed the purchased Credits and both referral rewards. Individual consent and eligibility still apply. The complete new-price purchase → new video delivery → Credit settlement sequence remains unverified. The nominal consumption order is referral → subscription → signup bonus → purchased Credits; actual availability and functionality are subject to the current launch status.

**Availability note:** FramePrime v0.0.1 publicly launched on 2026-11-22 at 11:22 JST, as confirmed by the owner. The catalog and limited payment evidence above do not establish successful purchases of every plan or completion of the new-price purchase-to-video-delivery-and-settlement sequence.

## 入力尺による料金計算例（長尺対応の案内ではありません）

**現在の案内は「2分までの動画生成」です。** 下表の2分を超える行は料金制度上の参考計算であり、利用可能な動画尺や今後の提供時期を示しません。

| Input video length | Credits | One-time-pack equivalent (¥100/Credit) |
| --- | ---: | ---: |
| Up to 2 minutes | 1 | ¥100 |
| 4 minutes | 2 | ¥200 |
| 8 minutes | 2 | ¥200 |
| 10 minutes | 4 | ¥400 |
| 20 minutes | 8 | ¥800 |
| 30 minutes | 14 | ¥1,400 |
| 32 minutes | 14 | ¥1,400 |

2分を超える計算例を、現在の長尺対応と読み替えないでください。新料金移行後にも個別動画の納品・精算実績はありますが、新購入から新しい動画への連続E2Eや長尺対応の実証とは別です。

## Why this matters

The model is intended to avoid penalizing iterative refinement.

```text
New creation
  → Public guidance: video generation up to 2 minutes. Billing: 1 Credit for a positive input duration up to 2 minutes; longer billing calculations do not establish long-form support

Supported revision of delivered result
  → 0 additional user credits
```

## Boundary

This document describes the public product behavior at a high level. It does not disclose private billing tables, reservation RPCs, ledger implementation details, privileged database paths, or payment-provider internals.
