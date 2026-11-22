# Overview

FramePrimeは、動画の取り込みからAI編集・字幕・SNS投稿文の準備までを、専用画面で進められる**Webサービス（AI動画制作OS）**です。現在は手元の動画のアップロードから始められ、取得できた投稿後の実測結果を次の制作に活かすことも目指します。X動画URL取り込みは既存機能ですが、現在は一時停止・復旧確認中です（2026年11月23日確認）。再開は確認後に案内します。

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
