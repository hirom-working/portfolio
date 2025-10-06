# Hiromtoon's Portfolio

システムエンジニアとしてのポートフォリオサイトです。オンプレミスKubernetesクラスター構築、LLMファインチューニング、自動化システム開発など、実践的なプロジェクトを紹介しています。

## 🌐 サイトURL

GitHub Pages: `https://hiromtoon.github.io/portfolio/`

## 📁 プロジェクト構成

```
portfolio/
├── index.html                          # トップページ
├── css/
│   └── style.css                      # メインスタイルシート
├── images/
│   ├── architecture.svg               # システム構成図
│   └── screenshots/                   # スクリーンショット
├── projects/
│   ├── homelab-infrastructure.html    # Kubernetes インフラ
│   ├── hiromtoon-llm.html            # LLMファインチューニング
│   └── twitter-automation.html        # Twitter Bot
└── README.md                          # このファイル
```

## 🚀 ローカルでの確認方法

### 1. シンプルなHTTPサーバー起動

```bash
# Python 3 を使用
cd /home/hirom/Projects/portfolio
python3 -m http.server 8000

# ブラウザで確認
http://localhost:8000
```

### 2. VS Code Live Server（推奨）

1. VS Code で `portfolio` ディレクトリを開く
2. Live Server 拡張機能をインストール
3. `index.html` を右クリック → "Open with Live Server"

## 📤 GitHub Pages へのデプロイ

### 初回デプロイ

```bash
cd /home/hirom/Projects/portfolio

# Gitリポジトリ初期化
git init
git add .
git commit -m "Initial commit: Portfolio site"

# GitHubリポジトリ作成（GitHub上で作成済みの場合はスキップ）
# https://github.com/new でリポジトリ作成

# リモートリポジトリ追加
git remote add origin https://github.com/hiromtoon/portfolio.git

# メインブランチにプッシュ
git branch -M main
git push -u origin main

# GitHub Pages用ブランチ作成
git checkout -b gh-pages
git push -u origin gh-pages
```

### GitHub Pages 設定

1. GitHub リポジトリページへ移動
2. **Settings** → **Pages** を開く
3. **Source** で `gh-pages` ブランチを選択
4. **Save** をクリック
5. 数分後、`https://hiromtoon.github.io/portfolio/` でアクセス可能

### 更新時のデプロイ

```bash
# メインブランチで更新
git add .
git commit -m "Update portfolio content"
git push origin main

# gh-pagesブランチにマージ
git checkout gh-pages
git merge main
git push origin gh-pages

# メインブランチに戻る
git checkout main
```

## 🎨 カスタマイズ

### 色の変更

`css/style.css` の `:root` セクションで色を変更できます:

```css
:root {
    --bg-primary: #0a0e27;        /* 背景色（ダーク） */
    --accent-primary: #3b82f6;    /* アクセントカラー（ブルー） */
    --accent-secondary: #8b5cf6;  /* アクセントカラー（パープル） */
}
```

### コンテンツの更新

- **トップページ**: `index.html` を編集
- **プロジェクト詳細**: `projects/*.html` を編集
- **構成図**: `images/architecture.svg` を編集

## 📊 含まれているプロジェクト

### 1. Homelab Kubernetes Infrastructure
- 3ノードHAクラスター（MicroK8s）
- GitOps（ArgoCD）による自動デプロイ
- Harbor プライベートコンテナレジストリ
- Prometheus & Grafana モニタリング

### 2. Hiromtoon LLM
- Twitter データ19,320件から学習
- QLoRA ファインチューニング（Gemma3-27B）
- 自宅GPU環境（RTX 5060 Ti × 2）で実現
- メモリ最適化により32GB VRAMで学習成功

### 3. AI-Powered Twitter Bot
- ローカルLLM（Ollama gemma2:27b）統合
- Kubernetes CronJob での自動実行
- インテリジェントなリツイート＆いいね機能
- 完全セルフホスティング（外部API不使用）

## 🔧 技術スタック

- **Frontend**: HTML5, CSS3（カスタムデザイン）
- **Hosting**: GitHub Pages
- **Design**: ダークモード、レスポンシブデザイン
- **Icons**: SVG

## 📝 ライセンス

© 2025 Hiromtoon. All rights reserved.

## 📧 連絡先

- **GitHub**: https://github.com/hiromtoon
- **Twitter**: https://twitter.com/hiromtoon

---

**更新履歴**
- 2025-10-06: 初版作成
