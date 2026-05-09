---
title: pcKakakuWatcher
---

# pcKakakuWatcher

pcKakakuWatcher は、PCパーツと周辺機器の価格を定期的に取得し、価格確認と価格変動通知に利用する個人用ツールです。

## 主な用途

- GPU、デスクトップPC、ディスプレイなどの価格を定期的に確認する
- 条件に合う商品を抽出し、価格変動や通知対象を判定する
- 取得結果を履歴として保存し、後から確認できるようにする

## 対象カテゴリ

- GPU
- Monitor
- Desktop PC
- 将来的にはSSD、ミニPC、周辺機器なども対象候補

## 基盤構成

- 実装: .NET の CLI アプリケーション
- 実行方式: GitHub Actions による定期実行
- データ保存: Neon / PostgreSQL
- 通知: Discord Webhook
- 設定管理: PostgreSQL 上の監視設定を読み込み
- 管理ツール: WPF ベースの設定編集・観測結果確認ツール

## 利用API

- 楽天市場商品検索API
- Yahoo!ショッピング商品検索API