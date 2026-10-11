# Security Policy

FramePrimeに関するセキュリティ上の問題が疑われる場合、**公開Issueには詳細を書き込まないでください**。

Security reporting contact: **support@frameprime.app**
件名例: `Security report — FramePrime`

可能な範囲で、次の情報をお知らせください。

- 影響を受ける画面・機能
- 発生日時
- 再現条件
- 想定される影響
- 連絡方法

秘密鍵、パスワード、実顧客情報そのものは送らないでください。

現時点では、受領・対応について固定SLAやバグ報奨金制度を案内していません。問題の重大性と再現状況に応じて確認します。

この文書は、本Repositoryを通じたProduction sourceの開示や、無制限のセキュリティテスト許可を意味しません。


## Public security posture

For a high-level description of FramePrime authentication and implemented security boundaries, see [docs/security-and-auth.md](docs/security-and-auth.md).

Important: implemented controls and a completed pre-launch audit are not the same as security certification. The formal pre-launch authentication / authorization / information-leakage audit is completed with **0 Critical / High findings at closure**; ongoing security review remains required.
