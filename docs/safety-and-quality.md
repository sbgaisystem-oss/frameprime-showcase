# Safety and Quality

FramePrimeは、生成処理の成功だけでなく、最終成果物が要求された状態になっているかを確認することを重視します。

## Subtitle coverage

字幕では、動画内の必要な発話・情報が不必要に欠落しないことを重視します。

## Collision avoidance

字幕・テロップが重要な映像要素と衝突する場合、表示位置を調整できる設計を採用します。

## Source-grounded audio safety

FramePrimeでは、source audio / transcriptの根拠が不足・曖昧な場合に unsupported subtitle を創作で埋めるより、fail-closedを優先します。

詳細 → [Subtitle & audio safety](subtitle-and-audio-safety.md)

## Revision workflow

完成後の修正は、元の制作処理と区別したRevisionとして扱い、修正後の成果物が成立していることを確認します。

## Fail-closed thinking

検証不能な状態を成功として扱うより、未成立・取得不能・失敗を区別して残すことを優先します。

## Non-blocking analysis

投稿後分析や補助的な動画分析は、動画生成そのものの成功条件と不用意に結びつけないことを重視します。

## Public disclosure boundary

このShowcaseは安全設計の考え方を説明するものであり、内部の閾値、provider別判定、private prompt、privileged path、復旧手順等を公開するものではありません。
