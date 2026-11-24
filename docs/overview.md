# Overview

FramePrimeは、動画の取り込みからAI編集・字幕・SNS投稿文の準備までを、専用画面で進められる**Webサービス（AI動画制作OS）**です。手元の動画のアップロードまたは対応するX動画URLから始められ、取得できた投稿後の実測結果を次の制作に活かすことも目指します。X動画URL取り込みは2026年11月24日に復旧しました。ご自身が権利を持つ動画や利用許諾のある動画をご利用ください。

**現在の公開画面の案内は「2分までの動画生成」で、新規登録特典は10 Creditsです。** 元の音声言語に沿った字幕と、未提供の選択言語翻訳は区別します。Geminiによる補助的な内容分析は現在停止中で、字幕作成・動画生成とは別です。確認済みの本番実績と未確認の範囲は[FAQ](faq.md)を参照してください。

## Problem

一般的な制作フローでは、動画が完成した時点で制作工程と投稿後の学習が分断されがちです。FramePrimeは、完成動画と投稿結果を同じ改善ループに接続することを重視します。

## Product principle

FramePrimeの中心は、単発の「AI採点」ではありません。

- 動画側で観測できる構造
- 投稿後に取得できた実測KPI
- ユーザー自身の過去投稿との比較

をEvidenceとして残し、次回に何を変えるかを判断しやすくすることを目的とします。

## Evidence-first and private-first

FramePrimeは、AIが書いた説明文そのものよりSource / Feature / Observed Outcomeへ戻れるEvidenceを優先します。

学習もGlobal cross-user corpusより先に、本人の過去動画・本人の実測KPI・本人の構造EvidenceによるPrivate Learningを優先します。

詳細 → [Evidence-first & Private Learning](evidence-and-private-learning.md)

## FramePrime OSの機能のつながり

| 場所・工程 | ユーザーができること | 提供状況・注意 |
| --- | --- | --- |
| 動画入力・制作 | 権利保有動画のアップロードまたは対応するX動画URLから、AI字幕・動画制作へ進む | 現在の案内は入力2分まで。X URLは対応・取得条件あり |
| 完成動画の確認・ライブラリ | 納品された動画を確認・ダウンロードし、制作物を管理する | 対応する画面・操作の範囲は公式サイトで案内 |
| Studio（PC専用） | 字幕・タイトル・サムネイル・CTA・カットなどの対応範囲を仕上げる | PC字幕修正1件と再書き出し追加0 Creditsを実証。すべての操作を実証したものではない |
| SNS投稿準備 | 対応する動画生成時に投稿文・ハッシュタグを一緒に準備 | 投稿文は追加0 Credits。単独での新規投稿文作成は現在非提供。投稿は利用者自身が行う |
| 投稿後の記録・Growth | 投稿結果を記録し、次回制作の改善に役立てる | 取得可能な項目や提供範囲には制約がある。詳細は別文書 |

**動画生成時に投稿文を付ける・付けないことで、新規動画制作のCredit消費は変わりません（投稿文は追加0 Credits）。** 現在、投稿文だけを新規作成する機能は提供していません。過去の投稿準備は閲覧できます。完成後の対応する修正・再書き出しも追加0 Creditsです。Studioは汎用編集ソフトのすべての機能を置き換えるものではありません。

## Two main surfaces

### Studio

**PC-only** の仕上げ・修正Surfaceです。Desktopでは有効、MobileではStudio利用はdisabledです。Title / Thumbnail / Subtitles / CTA / Cut等を扱います。

詳細 → [Studio](studio.md)

### Growth

投稿結果と動画側Evidenceを確認し、次回の改善点を整理する場所です。**Core V1はProduction、全体maturityはACTIVE_EXPANSION**で、provider/API coverageは拡張途中です。

詳細 → [Growth](growth.md)

Growthで見つかった改善点を、必要に応じてStudioで修正するという役割分担を採用しています。

## Authentication / security posture

Current authはpasswordless email OTP。Remembered Email機能はemail addressだけを保持し、OTP/tokenは保存しません。2026年10月12日の認証・認可・情報漏洩に限定した正式な事前監査は完了（closure時点Critical／High 0件）しています。ただし、その後のProduction変更と正式ローンチE2Eは別Gateであり、Security Certificationではありません。

詳細 → [Security and authentication posture](security-and-auth.md)

## Availability

このShowcaseでは、Production実装済み機能とLaunch readinessを分けて表現します。実装済みであっても、正式公開に必要な品質・セキュリティ・UX等のGateが未完了であれば、その状態を明示します。
