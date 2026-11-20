# FAQ

## FramePrimeは動画生成AIそのものですか？

FramePrimeは単一の生成モデルではなく、動画制作・字幕・投稿準備・記録・学習をつなぐ動画投稿改善OSです。

## 動画を入れると何ができあがりますか？

対応する制作フローでは、AIによる字幕や編集の支援を受け、完成動画を確認できます。投稿に備えてキャプション案・ハッシュタグ・投稿前チェックリストも確認できます。完成内容は使用する機能や動画素材によって異なり、すべての機能が自動で適用されるとは限りません。現在は正式ローンチ前で、一般向けの新規登録・生成・購入は停止中です。

## 投稿まで全部自動化されますか？

現在、SNSへの自動投稿・投稿代行は提供していません。FramePrimeで投稿用の動画や文章を準備し、SNSへの実際の投稿操作は利用者本人が行います。

## Growthの数値はAIの予測ですか？

実測KPIと動画分析は分離して扱います。取得できたKPIは実測Evidenceとして扱い、動画分析による原因候補・改善候補と混同しません。

## 取得できなかったKPIは0になりますか？

原則として0へ置換しません。未取得、非対応、権限不足などを区別することを重視します。


## 動画1本に何Creditsかかりますか？（Original Voice）

正式な消費ルールは、**入力動画2分以内なら1 Credit、2分超〜8分なら2 Credits、8分超〜12分なら4 Credits**。以降も入力動画が4分長くなるごとに2 Credits追加します（32分=14 Credits）。**完成後の動画尺ではなく、アップロードした入力動画の実際の長さ**が基準です。買い切りの通常単価なら1 Creditは100円相当ですが、プランによって単価は変わります。表示・内部台帳とも整数Creditに統一します。**金融DBは2026年11月21日に新段階式へ移行済みです。ただしStripe Edge・Frontendは未配信で、一般向けの購入・生成は未提供です。** 通常のsystem terminal failureはreservationが解放され、net 0 user creditsです。

## Creditの購入方式は？

正式な月額は **2,900円/32、5,800円/68、9,800円/122、19,800円/282 Credits** です。買い切りは **1,000円/10、3,000円/30、6,000円/60、10,000円/100 Credits**。別枠のβ体験980円/20 Creditsは生涯1回・自動更新なし。すべて税込で、Creditは期限なし・繰越可能です。詳細は[Credits and revisions](credits-and-revisions.md)。登録特典10 Credits・紹介報酬双方4 Credits（予算800 Credits）も新整数仕様です。これらの付与数は金融DBへ適用済みですが、Stripe Edge・Frontendは未配信で、一般購入・新規登録・紹介報酬は停止中です。

## 完成後の修正でもcreditを消費しますか？

対応するpost-delivery Revision Renderは **0 additional user credits** です。新規生成と、完成後の修正を別のcredit contractとして扱います。

## Geminiが動画そのものを作っていますか？

いいえ。Gemini Video Analysis V2は **READ ONLY / NON-BLOCKING / authoring authority NONE** です。Gemini分析が失敗しても、その失敗をgeneration / render / delivery failureへ昇格させません。

## 3秒HookはGeminiが決めていますか？

その説明は正確ではありません。FramePrimeはFinal Render側で **3s Hook / Opening Static / First Visual Change / Frame Change / Visual Evidence** などの構造Evidenceを扱い、Geminiのsemantic analysisとはauthorityを分離しています。

## Geminiでは何を分析しますか？

content summaryに加え、Topic Clarity、Value Proposition Clarity、Demonstration Strength、Visual / Speech Alignment、Cognitive Load、Payoff Matchなどのbounded semantic signalsを扱います。これらは将来の再生数を保証する予測値ではありません。

## Jev / JevBox / Cursor / HyperFramesはFramePrimeで何に使われますか？

役割は分かれています。Jevはdecision/evaluation provenance、JevBox-inspired Creative Memoryはsource-grounded retrieval、Cursorはdevelopment tooling、HyperFramesはcode-to-video quality-evaluation lineage / offline-shadow evaluationで利用されます。これらを一括してProduction runtime dependencyとは扱いません。

## FramePrimeのEvidence-firstとは何ですか？

AIが書いた説明文そのものを事実の正本にせず、動画identity、時間範囲、観測Feature、観測KPI、source/provenanceへ戻れるEvidenceを優先する考え方です。

## Private Learningとは何ですか？

Global cross-user learningより先に、本人の過去動画・本人の実測KPI・本人の構造EvidenceからPersonal Baselineを作る方向です。Global corpus / vector / KG / cross-user learningは別Gateです。

## 字幕は単に生成するだけですか？

いいえ。FramePrimeは**coverage completeness**と**collision avoidance**を別の品質問題として扱います。また、source audio/transcriptの根拠が不足・曖昧な場合は、unsupported subtitleを創作で埋めるよりfail-closedを優先します。

## LangfuseはFramePrimeの判断を本番で直接変更しますか？

いいえ。Langfuse × Jev/P1のevaluation mirrorは **READ ONLY / NON-AUTHORITATIVE** として扱われ、production routingやoutput mutationのauthorityにはしません。

## MCPでFramePrimeを使えますか？

現時点ではProduction機能ではありません。Canonical architecture directionは **Dual Surface / Single Core** で、将来のMCP / Agent InterfaceもGUIと同じFramePrime Core、credit semantics、safety、ownership rulesへ収束させる方針です。

## Studioはスマホでも使えますか？

現在のStudioは **PC専用** です。Desktopでは有効ですが、MobileではStudioカードが表示されても利用はdisabledです。

## Studioでは何ができますか？

Studioは今ある動画を仕上げるSurfaceです。現在の主な編集面は **Title / Thumbnail / Subtitles / CTA / Cut** で、対応するRevision Renderも含みます。一般目的のNLEを目指しているわけではありません。

## Growthは何のためにありますか？

Growthは、投稿後の実測KPI、動画側の構造Evidence、本人の過去投稿との比較から、**何が起きたか / なぜ起きた可能性があるか / 次に何を変えるか**を整理するためのSurfaceです。

## Growthは完成済みですか？

**Growth Core V1はProductionです。ただし全体はACTIVE_EXPANSIONです。** Xのexact-window KPI等のCurrent機能は動作していますが、全SNS・全指標・全adapterが完成しているわけではありません。provider/API availabilityに依存し、cross-platform coverageは拡張途中です。

## FramePrimeのログイン方式は？

Currentは **passwordless email OTP** です。PWA / Home Screenでは6桁email OTPを使用します。PC browserでは既存のemail verification compatibilityも維持しています。

## なぜFramePrime独自のパスワードを使わないのですか？

Current design rationaleは、FramePrime独自のpassword credentialを増やさず、ユーザーが管理するcredential surfaceを小さくし、PWAでも低摩擦にログインできるようにするためです。これはemail OTPが全てのpassword/MFA設計より強いという意味ではありません。

## remembered emailにOTPやtokenも保存されますか？

いいえ。Remembered Email機能は最後に使ったemail addressを利便性のために保持しますが、**OTPとauth tokenはその機能ではpersistしません**。

## セキュリティ監査は完了していますか？

2026年10月12日に、対象を認証・認可・情報漏洩に限定した正式な事前監査は完了し、closure時点のCritical／Highは0件でした。ただし、これはSecurity Certificationではなく、後続のProduction変更・正式ローンチE2Eの成立を意味しません。

## Productionソースコードは公開されていますか？

いいえ。このRepositoryはDocumentation Showcaseです。Production source、internal prompt、credential、private infrastructure等は対象外です。

## 多言語字幕やNative appはありますか？

Launch後Backlog / future directionです。READMEのAvailable nowには含めません。

## セキュリティ問題を見つけた場合は？

公開Issueに詳細を書かず、[SECURITY.md](../SECURITY.md)の連絡方法を利用してください。
