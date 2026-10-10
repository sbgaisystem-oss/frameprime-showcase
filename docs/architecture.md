# Public Architecture

この文書は、外部公開可能な抽象度でFramePrimeの構成を説明します。

```text
User
 ↓
FramePrime UI
 ↓
Video Processing / Intelligence
 ↓
Quality & Safety Gates
 ↓
Deliverable
 ↓
Publishing Preparation
 ↓
Post-performance Evidence
 ↓
Growth
```

## FramePrime UI

ユーザーが動画を投入し、進行状況・完成物・修正・投稿準備・学習へアクセスするSurfaceです。

## Video Processing / Intelligence

動画・音声・字幕などを処理し、制作に必要な構造化Evidenceを作ります。

公開Showcaseでは、特定providerのrouting、private RPC、database schema、内部prompt等は開示しません。

## Quality & Safety Gates

成果物をDeliveryへ進める前に、形式・整合性・安全性などの検証を行います。検証不能な状態を成功として扱わない設計を重視します。

## Deliverable

ユーザーが確認・利用する完成成果物です。必要に応じてStudioから修正フローへ進みます。

## Publishing Preparation

SNSごとに異なる投稿準備を整理します。すべてのSNSについて同一機能を保証する設計ではありません。

## Post-performance Evidence

投稿後に取得できた数値はEvidenceとして扱います。取得不能・未取得・非対応を区別し、欠損を0に置換しません。

## Growth

実測値、動画側の構造化Evidence、本人の過去実績を組み合わせて、次回改善を整理します。

## Future agent surface

FramePrimeのCanonical architecture directionは **Dual Surface / Single Core** です。

GUIは第一級surfaceとして維持し、将来のMCP / Agent Interfaceも同じFramePrime Core、credit semantics、safety、ownership rulesへ収束させます。

MCP / Agent Interfaceは現時点でProduction機能ではありません。

詳細 → [Dual Surface / Single Core](dual-surface-single-core.md)

## Intentionally not disclosed

- provider routing details
- private database schema
- privileged backend / database paths
- secret names or values
- internal machine identifiers
- deployment manifests and digests
- detailed rollback / recovery procedures
- internal prompts and raw evaluation evidence
