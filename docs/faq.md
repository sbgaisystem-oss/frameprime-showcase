# FAQ

## FramePrimeは動画生成AIそのものですか？

FramePrimeは単一の生成モデルではなく、動画制作・字幕・投稿準備・記録・学習をつなぐ動画投稿改善OSです。

## 投稿まで全部自動化されますか？

すべてのSNSへの完全自動投稿を保証していません。SNSごとに対応範囲が異なり、ユーザー自身が行う操作もあります。

## Growthの数値はAIの予測ですか？

実測KPIと動画分析は分離して扱います。取得できたKPIは実測Evidenceとして扱い、動画分析による原因候補・改善候補と混同しません。

## 取得できなかったKPIは0になりますか？

原則として0へ置換しません。未取得、非対応、権限不足などを区別することを重視します。


## Original Voiceの生成には何credit必要ですか？

正常にDELIVEREDしたOriginal Voice生成は **1 user credit** を消費します。通常のsystem terminal failureはreservationが解放され、net 0 user creditsです。

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

いいえ。Passwordless auth、owner-scoped/RLS境界、secret非公開、fail-closed等の対策は実装されていますが、Launch向けの **OTP / RLS / secret / IDOR / public-permissionを含む総合Security Auditはまだopen gate** です。Security certified / fully auditedとは表現しません。

## Productionソースコードは公開されていますか？

いいえ。このRepositoryはDocumentation Showcaseです。Production source、internal prompt、credential、private infrastructure等は対象外です。

## 多言語字幕やNative appはありますか？

Launch後Backlog / future directionです。READMEのAvailable nowには含めません。

## セキュリティ問題を見つけた場合は？

公開Issueに詳細を書かず、[SECURITY.md](../SECURITY.md)の連絡方法を利用してください。
