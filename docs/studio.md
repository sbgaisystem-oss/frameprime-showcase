# Studio

Studio is FramePrime's **PC-only finishing and revision surface**.

## Availability

Current product boundary:

- **Desktop / PC:** Studio is available.
- **Mobile:** the Studio card may be visible, but the Studio surface is disabled for mobile use.
- Studio is not intended to be a full Premiere / CapCut-class nonlinear editor.

The mobile product remains focused on the simpler creation / delivery / posting workflow, while deeper finishing work stays on PC.

## Studioでできること — AIで作った動画を、必要なところだけ仕上げる

**FramePrimeは、動画をアップロードしてAIで制作し、完成物を確認してSNS投稿を準備するOSです。** Studioはその中の**PC専用の仕上げ・修正画面**です。一般的な動画編集ソフトのように一からタイムラインを組み立てることより、FramePrimeで制作した動画の必要な部分を見つけて直すことを重視しています。

- **字幕を直す：** AIが付けた字幕の文字・タイミングを確認し、対応する編集で修正できます。
- **見せ方を整える：** タイトル、サムネイル、CTA、カットなど、対応する編集項目を調整します。
- **完成動画を再書き出し：** 対応する完成後の修正・再書き出しは追加0 Creditsです。元の納品動画を保持して修正版を受け取れるフローがあります。
- **投稿準備までつなぐ：** SNS投稿文・ハッシュタグ・投稿準備の作成・文章調整は追加0 Credits。投稿文の有無によって、動画制作で消費するCreditsは変わりません。

**実証済みの範囲：** 2026年11月23日、PCで字幕1か所を修正し、保存→再書き出し→ダウンロード、追加0 Creditsを確認しました。すべてのStudio操作・素材・端末で同じ結果を保証するものではありません。

**編集ソフトとの違い：** Premiere ProやCapCut等の全機能を置き換えるものではありません。AI制作から、対応する部分修正、投稿準備までのつながった作業を簡単にすることが価値です。細かな自由編集が必要なら専用編集ソフトが適します。

## What Studio is for

Studio is the place to **finish an existing video**, not the place to judge long-term post performance.

Current finishing surfaces include:

- **Title**
- **Thumbnail**
- **Subtitles**
- **CTA**
- **Cut**

Studio also supports the revision workflow around an already delivered video. On 2026-11-23, one authenticated user on a PC used the delivery screen's subtitle/video correction entry, saved one subtitle-text correction, and received and downloaded a revised render with 0 additional Credits. The original delivered video was retained. This verifies the tested subtitle-correction route; it does not establish that every Studio control or mobile device has been tested.

## Subtitle editing

Studio can expose the generated subtitles with timing and text-editing controls. In supported post-delivery revisions, users can add or split a subtitle interval, save changes, and render a separate revised file in the Library while retaining the original. The minimum-duration automatic correction feature is not asserted as deployed; very short subtitle intervals may still require manual adjustment.

Publicly relevant quality concepts include:

- subtitle coverage completeness,
- collision avoidance,
- text editing,
- presentation adjustments,
- bounded revision of the delivered result.

## Revision Render

Supported post-delivery Revision Render is part of the Studio finishing workflow.

Current public credit contract:

- current public guidance describes video generation up to 2 minutes. Under the billing contract, a positive input duration up to 2 minutes uses 1 Credit. Longer-duration billing rules are documented in [Credits and revisions](credits-and-revisions.md) and do not promise current long-form support or a future release date,
- supported post-delivery revision render → 0 additional user credits.

## Studio vs Growth

The product split is intentional:

```text
Studio
= fix / finish the current video

Growth
= learn from evidence and improve the next video
```

Growth may identify an issue or next action, but it does not silently rewrite the video. A user-initiated correction belongs in Studio.

## Design boundary

Studio is a bounded human correction surface.

The goal is not to turn FramePrime into a general-purpose NLE. The goal is to make the highest-value corrections to FramePrime-generated/delivered video state with less friction.
