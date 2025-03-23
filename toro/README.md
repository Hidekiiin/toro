# toro - ランダム音声チャットアプリ

toroは、Next.js、WebRTC、Socket.ioを使用して構築されたランダム音声チャットアプリケーションです。ユーザーはボタン一つでランダムな相手とマッチングし、リアルタイムの音声通話を楽しむことができます。

## 機能

- ランダムマッチング機能
- リアルタイム音声通話
- シンプルで使いやすいUI
- レスポンシブデザイン

## 技術スタック

- **フロントエンド**: Next.js、React
- **リアルタイム通信**: Socket.io、WebRTC (simple-peer)
- **デプロイ**: Vercel

## セットアップ手順

### 前提条件

- Node.js 14.x以上
- npm または yarn
- Ablyアカウント（無料プランで可）

### ローカル開発環境のセットアップ

1. リポジトリをクローンまたはダウンロードして解凍します

```bash
git clone <リポジトリURL>
# または
# ZIPファイルを解凍
```

2. プロジェクトディレクトリに移動します

```bash
cd toro-app
```

3. 依存パッケージをインストールします

```bash
npm install
# または
yarn install
```

4. 環境変数を設定します

`.env.example`ファイルを`.env`にコピーし、Ablyの API キーを設定します。

```bash
cp .env.example .env
```

`.env`ファイルを編集し、`ABLY_API_KEY`に有効なAbly APIキーを設定します。

5. 開発サーバーを起動します

```bash
npm run dev
# または
yarn dev
```

6. ブラウザで [http://localhost:3000](http://localhost:3000) にアクセスして、アプリケーションを確認します。

## Vercelへのデプロイ手順

### GitHubリポジトリの作成

1. GitHubにログインし、新しいリポジトリを作成します。
2. ローカルのプロジェクトをGitHubリポジトリにプッシュします。

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <GitHubリポジトリURL>
git push -u origin main
```

### Vercelでのデプロイ

1. [Vercel](https://vercel.com/)にアクセスし、アカウントを作成またはログインします。
2. 「New Project」をクリックします。
3. 「Import Git Repository」セクションからGitHubリポジトリを選択します。
4. 環境変数を設定します：
   - `ABLY_API_KEY`: Ablyの API キー
5. 「Deploy」ボタンをクリックしてデプロイを開始します。

デプロイが完了すると、VercelはプロジェクトのURLを提供します。このURLを使用してアプリケーションにアクセスできます。

## Ablyアカウントの作成と設定

1. [Ably](https://ably.com/)にアクセスし、アカウントを作成します。
2. ダッシュボードから新しいアプリケーションを作成します。
3. アプリケーションの詳細ページから API キーをコピーします。
4. このAPIキーを`.env`ファイルとVercelの環境変数に設定します。

## 使い方

1. アプリケーションにアクセスします。
2. 「ランダムマッチング」ボタンをクリックします。
3. システムがランダムな相手を探します。
4. マッチングが成功すると、自動的に音声通話が開始されます。
5. 通話を終了するには「通話を終了」ボタンをクリックします。

## ライセンス

MIT

## 謝辞

このプロジェクトは以下のオープンソースプロジェクトを参考にしています：

- [ably-labs/NextJS-chat-app](https://github.com/ably-labs/NextJS-chat-app)
- [diazlp/random-chat-web-nextjs](https://github.com/diazlp/random-chat-web-nextjs)
