---
title: Codex Toolkit
---

# Codex Toolkit

Codex Toolkit は、Codex の運用ルール、スキル、フックをリポジトリごとに配備するための Windows / PowerShell 用ツールキットです。

公開リポジトリ: [ytakasi/codex-toolkit-public](https://github.com/ytakasi/codex-toolkit-public)

## 主な用途

- Codex 用の共通ルール、スキル、フックをリポジトリごとに同期する
- 作るものや機能に応じて profile を選び、必要なAI運用資産だけを配備する
- リポジトリ固有のスキルやフックを、toolkit 由来の資産と分けて管理する
- `.agents` を生成物として扱い、正本とランタイムを分離する

## 基盤構成

- 実装: PowerShell 7 CLI
- 配布単位: `codex-kit` コマンド
- 主な機能: `init`、`sync`、`update`、`status`、`doctor`、`list-profiles`
- 管理対象: Codex skills、hook dispatcher、profile manifest
- 公開形態: private 正本から公開用 snapshot を生成

## 特徴

- 用途に依らない基礎スキルと、Android、定期実行、通知、外部データ取り込みなどの用途別 profile を分けている
- 対象リポジトリには toolkit 由来レイヤーとリポジトリ固有レイヤーを置き、Codex が読む `.agents` は同期で生成する
- profile の一部だけを配備しても破綻しないよう、スキル間の依存と参照先を検証する
- PowerShell 7 前提で、Windows 環境の個人開発運用に寄せている
