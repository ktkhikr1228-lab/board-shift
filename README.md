This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

# オセロ拡張戦略ゲーム

## 概要

Next.js（TypeScript）を用いて制作中の、オセロをベースにした拡張型戦略ゲームです。

通常のオセロに加えて、

* 制限時間制
* CPU対戦
* ポイント（GP）システム
* 特殊効果
* ローグライク要素

などを組み合わせ、毎回異なる戦略が生まれるゲームを目指しています。

---

## 使用技術

* Next.js
* TypeScript
* React
* useState

---

## 現在の実装

### 盤面管理

* 64マスを1次元配列で管理
* Stone型：

  * "black"
  * "white"

### 実装済みロジック

* placeStone(index)
* checkDirection(index, direction, board, player)
* canPlaceStone(index, board, player)

### 判定処理

* 8方向探索
* 合法手判定
* 石反転処理

---

## 現在の課題

### 反転バグ

後半になると関係ない石まで反転する場合がある。

### 行またぎ問題

横方向探索時に、
7→8 のような不正接続が発生している可能性がある。

### 合法手判定

置けない場所に置ける、
または合法手が弾かれる場合がある。

---

## 今後の展望

### CPU対戦

* ランダムAI
* 合法手評価AI

### ターン制強化

* 制限時間付きターン
* テンポ重視のゲーム設計

### 盤面ギミック

* 盤面交換
* 条件付き特殊効果

### GP（ポイント）システム

獲得ポイントを使用し、

* 盤面拡張
* 特殊駒
* 他ゲーム要素との融合

などを実装予定。

### ローグライク化

* ランダムイベント
* 毎試合異なるルール
* 永続強化

を組み合わせ、繰り返し遊べるゲームを目指しています。

---

## 制作目的

オセロの「挟む」という分かりやすいルールをベースに、
戦略性やビルド要素を追加することで、
毎回異なる試行錯誤を楽しめるゲームを目指しています。


Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
