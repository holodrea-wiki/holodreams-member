# ホロドリ 非公式データベース & Webツール群

ファン向けポータルサイトおよび、演出・確率計算ロジックを搭載したWebアプリケーション群です。

🔗 **Site Top:** [https://holodrea-wiki.github.io/holodreams-member/index.html](https://holodrea-wiki.github.io/holodreams-member/index.html)  
🎰 **Gacha Simulator:** [https://holodrea-wiki.github.io/holodreams-member/gacha.html](https://holodrea-wiki.github.io/holodreams-member/gacha.html)

---

## 📌 プロジェクト概要
大量のキャラクター・楽曲データの閲覧性を高める「インタラクティブなデータベース」と、実機さながらの体験を提供する「ガチャシミュレーター」をフロントエンド単体で実装したWebアプリケーションです。

---

## 🛠 実装機能と技術的工夫

### 1. 攻略データベース（Database / Portal）
- **非同期データバインディング**: 外部データソースから非同期（Fetch API）でデータを取得・描画
- **多軸フィルター & リアルタイム検索**: メンバー所属・属性・楽曲条件などによる複合絞り込み
- **モーダルUI**: 画面遷移を挟まずに詳細情報を確認できるSPAライクな設計

### 2. ガチャシミュレーター（Interactive Tool）
- **確率計算ロジック**: 排出確率・レアリティ判定・天井/確定枠のシミュレーション処理
- **演出・アニメーション制御**: CSS AnimationsとJavaScriptによるカード排出演出・スキップ機能
- **データ管理**: 実行回数集計、所持・未所持ステータス管理、排出履歴のトラッキング

---

## 💻 使用技術（Tech Stack）
- **Languages**: HTML5, CSS3, JavaScript (Vanilla JS / ES6+)
- **Architecture**: Single Page Application (SPA) 設計, 非同期通信 (Promise / Async-Await)
- **Hosting**: GitHub Pages

---

## 💡 技術的なこだわり
- **軽量・高速な動作**: 外部の重いフレームワークに依存せず、Vanilla JavaScriptで記述することで高速な初期ロードと軽快なインタラクションを実現
- **UXを意識したレイアウト**: モバイル操作時でも指が届きやすいUI設計と、世界観に合わせたビジュアルデザイン
