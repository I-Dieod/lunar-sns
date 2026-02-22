# Lunar - 創作経済プラットフォーム

ユーザー全員がクリエイターであり、自由に作品を発表し、経済的に支え合う創作メタバース・SNS型プラットフォーム

## 🌙 プロジェクト概要

- **プロジェクト名**: Lunar
- **コンセプト**: 自分の分身を作り、誰もが自由に創作活動を行う交流プラットフォーム
- **対応ジャンル**: イラスト、3D、音楽、動画、プログラミング、文章、その他全創作物
- **プラットフォーム手数料**: 5%（業界最低水準）

## 🎯 将来像

「[超かぐや姫](https://www.cho-kaguyahime.com/)」に登場する仮想空間"ツクヨミ"のような、**創作者のより自由かつ多様な表現の舞台となり、相互支援を可能とするメタバース**の実現を目指します。

### ツクヨミの世界観
> 「自分の分身を作り誰もが自由に創作活動を行う＜ツクヨミ＞」
> 
> VRChatで作成したワールドがPixivFanBox、Patreonのようなクリエイター支援経済システムを内包した交流プラットフォーム

Lunarは、この理想を現実世界で実装することに挑戦します。

## 🎨 プロジェクトの特徴

### 1. **すべてのユーザーがクリエイター**
閲覧者ではなく、全員が創作者として参加。作品を発表し、他者を支援する双方向の経済圏。

### 2. **最低手数料5%**
主要プラットフォーム（Pixiv Booth 10%、Patreon 5-12%）と比較して最低水準の手数料を実現。クリエイターファースト。

### 3. **全ジャンル対応**
イラスト、3Dモデル、音楽、動画だけでなく、**プログラミング成果物**も対象。GitHub的な創作物共有も可能。

### 4. **段階的なVR移行**
まずWebプラットフォームで経済システムを実証し、その後UnityベースのVR空間へ拡張。

## 🛠 技術スタック

### フロントエンド
- Next.js 14 (App Router)
- TypeScript
- Tailwind CSS
- shadcn/ui

### バックエンド
- Supabase (認証・DB・ストレージ・Realtime)
- PostgreSQL

### 決済
- Stripe (投げ銭・サブスクリプション・Connect)

### ホスティング
- Vercel

### VR（Phase 4以降）
- Unity
- WebGL / WebXR 対応

## 📅 開発計画

### Phase 1: MVP開発 (Month 1-2) 🚧
- [x] プロジェクト設計
- [ ] データベース設計
- [ ] ユーザー認証
- [ ] プロフィール管理
- [ ] 作品投稿・閲覧
- [ ] 基本的なUI

**目標**: 友人5-10人でクローズドβ

---

### Phase 2: 経済システム (Month 3-4)
- [ ] Stripe Connect統合
- [ ] 投げ銭機能
- [ ] サブスクリプション
- [ ] クリエイターダッシュボード
- [ ] 収益管理・引き出し機能

**目標**: 月間流通額10万円、クリエイター30人

---

### Phase 3: SNS機能拡充 (Month 5-6)
- [ ] いいね・コメント機能
- [ ] フォロー・タイムライン
- [ ] 通知システム
- [ ] 検索・タグ機能
- [ ] トレンド表示

**目標**: 月間流通額100万円、クリエイター100人

---

### Phase 4: VR空間移行 (Month 7-12)
- [ ] Unity VR開発
- [ ] 3Dアバターシステム
- [ ] VR空間内での作品展示
- [ ] バックエンド連携（REST API）
- [ ] VR内決済システム

**目標**: VRプロトタイプ完成、企業提携交渉開始

## 🚀 クイックスタート

### 前提条件
- Node.js 18以上
- Supabaseアカウント
- Stripeアカウント（決済実装時）

### インストール

```bash
# 1. リポジトリをクローン
git clone https://github.com/I-Dieod/lunar.git
cd lunar

# 2. 依存関係をインストール
npm install

# 3. 環境変数を設定
cp .env.local.example .env.local
# .env.local を編集してSupabaseの認証情報を入力

# 4. 開発サーバー起動
npm run dev
```

http://localhost:3000 にアクセス

### Supabaseセットアップ

1. https://supabase.com でプロジェクト作成
2. SQL Editorで `supabase_schema.sql` を実行
3. Storageでバケット作成（`works`, `avatars`）
4. API認証情報を `.env.local` に設定

詳細は [SETUP_GUIDE.md](SETUP_GUIDE.md) を参照

## 📂 プロジェクト構成

```
lunar-sns/
├── src/
│   ├── app/              # Next.js App Router
│   │   ├── (auth)/      # 認証関連ページ
│   │   ├── (main)/      # メインアプリケーション
│   │   └── api/         # API Routes
│   ├── components/       # Reactコンポーネント
│   │   ├── ui/          # shadcn/ui
│   │   ├── auth/        # 認証関連
│   │   ├── works/       # 作品関連
│   │   └── layout/      # レイアウト
│   ├── hooks/           # カスタムフック
│   ├── lib/             # ユーティリティ
│   └── types/           # TypeScript型定義
├── public/              # 静的ファイル
└── docs/                # ドキュメント
```

詳細は [PROJECT_STRUCTURE.md](PROJECT_STRUCTURE.md) を参照

## 📚 ドキュメント

- [セットアップガイド](SETUP_GUIDE.md) - 環境構築の詳細手順
- [プロジェクト構成](PROJECT_STRUCTURE.md) - ディレクトリ構成と役割
- [Week 1-2 タスク](WEEK_1-2_TASKS.md) - 最初の2週間の開発タスク
- [データベーススキーマ](supabase_schema.sql) - テーブル定義とRLS

## 📊 開発状況

### ✅ 完了
- プロジェクト設計
- データベース設計
- 技術スタック選定
- 基本アーキテクチャ設計

### 🚧 進行中（Week 1-2）
- 認証機能実装
- 基本UI作成
- プロフィール管理

### 📋 予定
- 作品投稿機能（Week 3-4）
- 経済システム（Month 2-3）
- SNS機能（Month 4）
- VR移行（Month 5-8）

## 🤝 コントリビューション

現在は個人開発プロジェクトですが、Phase 2完了後にコントリビューター募集予定です。

興味がある方は以下からコンタクトください：
- Issue作成
- Discord
- Twitter DMでご連絡
- Discordサーバーよりご連絡  

https://discord.gg/VKvYnqCAtT

## 📜 ライセンス

MIT License

## 👤 作者

**I.D.**

### コンタクト
- **GitHub**: [@I-Dieod](https://github.com/I-Dieod)
- **X (Twitter)**: [@idchang2026](https://x.com/idchang2026)
- **Discord**: i.dieod (UID: 1383504941200703539)

開発進捗はTwitterで随時報告中 📡

## 🙏 謝辞

### インスピレーション元

このプロジェクトは、アニメ「**[超かぐや姫](https://www.cho-kaguyahime.com/)**」に登場する仮想空間"ツクヨミ"にインスパイアされて開始しました。

> 「ツクヨミ」は作中で、クリエイターが自由に表現し、経済的にも支え合える理想の創作プラットフォームとして描かれています。Lunarは、この架空の世界を現実に実装する試みです。

### 関連作品・企業

- **原作**: 『超かぐや姫』（[ファミ通文庫](https://famitsubunko.jp/product/322509000503.html) / [KADOKAWA](https://www.kadokawa.co.jp/product/322509000193/)）
- **アニメ制作**: [株式会社ツインエンジン](https://twinengine.jp/news/17464)
- **配信**: [Netflix](https://www.netflix.com/browse?jbv=81756595)

「超かぐや姫」の世界観とキャラクター、および"ツクヨミ"のコンセプトはKADOKAWAおよび製作委員会に帰属します。本プロジェクトは非公式の個人開発であり、原作への敬意と創作への情熱から生まれたものです。
