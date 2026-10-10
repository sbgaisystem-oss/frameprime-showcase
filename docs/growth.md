# Growth

Growthは、FramePrimeで**結果から学び、次の動画を良くする**ためのSurfaceです。

## Product maturity

Current public status:

- **Growth Core V1: PRODUCTION**
- **Growth Auto Reflection / X exact-window collection: Production capability**
- **Overall Growth maturity: ACTIVE_EXPANSION**

This means the core learning surface exists and is operating, but broader provider coverage is not complete.

Metric availability depends on the social platform, API scope, account type, permissions, and FramePrime's implemented adapter coverage. A metric or provider that is not available is not fabricated.

Do not summarize Growth as either:

> “not implemented”

or

> “complete for every SNS and every metric.”

A more accurate summary is:

> “Growth Core V1 is live, while cross-platform breadth and advanced learning coverage are still expanding.”

## Principle

Growthは「AIが伸びる動画を予言する場所」ではありません。

優先するのは次の3種類のEvidenceです。

1. 投稿後に取得できた実測KPI
2. 動画側で観測できた構造
3. ユーザー自身の過去投稿との比較

## Current information architecture

### 01 投稿後の数値変化

取得可能なViews、Watch Time、Share Rate、Save Rate、Comment Rate等を扱います。

SNSや権限によって取得できる項目は異なります。

### 02 動画側の数値構造化

3s Hook、Opening Static、First Visual Change、Frame Change、Visual Evidence等、動画そのものから得られる構造を扱います。

### 03 過去動画との比較

本人の過去投稿をPersonal Baselineとして比較します。異なるSNSのraw viewsを単純ランキングすることは目的にしません。

### 04 改善レビュー

Evidenceに紐づいたNext Actionを整理します。一度に多数を変えるのではなく、比較可能なOne-change Testを重視します。

### 05 分析状況

KPI Status、Hook Evidence、Source Context、Data Coverageを表示し、どこまでEvidenceが揃っているかを明示します。

## Data integrity

FramePrimeでは、たとえば次の状態を区別する考え方を採用しています。

- measured
- not fetched
- unsupported
- provider missing
- permission failure
- acquisition failure
- not applicable

欠損値を便宜上0に置換すると、改善判断を誤るためです。

## Private Learning

Growthの学習方向は **private-first** です。

本人の過去動画、本人の実測KPI、本人の構造EvidenceからPersonal Baselineを作り、Evidence-linkedな比較へつなげます。

Current guardrail:

- 10本未満: 個人パターンを断定しない
- 10–29本: descriptive median / rangeまで
- 30本以上: sample sizeとlimitationを明示したexploratory relationship analysisを許可

これは統計的因果保証ではありません。

詳細 → [Evidence-first & Private Learning](evidence-and-private-learning.md)

## Prediction boundary

動画分析は、原因候補や改善候補を示すために利用できますが、再生数・フォロワー増などの未来値を実測値のように表示することは目的にしません。また、相関を因果として断定しません。
