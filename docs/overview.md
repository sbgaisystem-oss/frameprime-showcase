# Overview

FramePrimeは、動画制作そのものだけでなく、**投稿準備 → 投稿後の記録 → 次回改善**までを同じプロダクトループに含める動画投稿改善OSです。

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

Current authはpasswordless email OTP。Remembered Email機能はemail addressだけを保持し、OTP/tokenは保存しません。正式なpre-launch security auditは別Launch Gateとして未完了です。

詳細 → [Security and authentication posture](security-and-auth.md)

## Availability

このShowcaseでは、Production実装済み機能とLaunch readinessを分けて表現します。実装済みであっても、正式公開に必要な品質・セキュリティ・UX等のGateが未完了であれば、その状態を明示します。
