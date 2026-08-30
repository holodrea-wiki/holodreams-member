# ホロドリ 非公式データベース & Webアプリケーション群

ファン向け総合ポータルサイトおよび、実用ツール・演出シミュレーターをフロントエンド単体で実装したWebアプリケーション群です。

---

## 🔗 各種ページ・機能一覧（Live Demo）

| ページ名 / ツール名 | 概要 / 主な機能 | リンク |
| :--- | :--- | :--- |
| **ポータルTOP** | サイト全体の総合ポータル・更新情報・ナビゲーション | [サイトを開く](https://holodrea-wiki.github.io/holodreams-member/index.html) |
| **タレント一覧** | 期生別の多軸フィルター＆リアルタイム検索 | [一覧を見る](https://holodrea-wiki.github.io/holodreams-member/talent.html) |
| **メンバー一覧** | 所属・属性・期生別の多軸フィルター＆リアルタイム検索 | [一覧を見る](https://holodrea-wiki.github.io/holodreams-member/member.html) |
| **楽曲一覧データベース** | 楽曲検索、ソート機能、各種詳細データのモーダル表示 | [楽曲一覧を見る](https://holodrea-wiki.github.io/holodreams-member/music.html) |
| **ガチャシミュレーター** | 排出確率計算ロジック、カード演出、所持・未所持判定 | [ツールを試す](https://holodrea-wiki.github.io/holodreams-member/gacha.html) |
| **所有率チェッカー** | 所持率の自動計算、**結果のX（Twitter）シェア機能** | [チェッカーを開く](https://holodrea-wiki.github.io/holodreams-member/collecyion.html) |
| **サイトについて / お問い合わせ** | 二次創作ガイドライン準拠、免責事項、**権利者向け定型文付き問い合わせフォーム** | [確認する](https://holodrea-wiki.github.io/holodreams-member/about.html) |

---

## 📌 プロジェクト概要・開発の背景
大量のキャラクターデータ・楽曲データを快適に閲覧できる情報設計と、ファンが遊べるインタラクティブなツール群（ガチャ・チェッカー）を、外部サーバー費用をかけずにGitHub Pages単体で高速動作させることを目指して開発しました。

---

## 🛠 主な機能とフロントエンド実装の工夫

### 1. データベース & 検索・フィルタリング（タレント一覧・楽曲一覧）
- **非同期データバインディング**: JSON / 外部データソースから非同期（Fetch API）でデータを取得し、動的レンダリング
- **リアルタイム多軸検索**: 複数条件（所属・属性・フリーワードなど）を組み合わせた瞬時の絞り込み処理
- **モーダルUI / SPA設計**: 画面遷移による負荷を減らし、シームレスな詳細情報閲覧を実現

### 2. インタラクティブWebツール（ガチャシミュレーター・所有率チェッカー）
- **確率計算 & 状態管理**: 確率テーブルに基づいた排出判定ロジックと、累計実行回数・確率統計の集計
- **演出・アニメーション制御**: CSS AnimationsとJavaScriptによるカード排出演出とスキップ処理
- **ローカルデータ永続化**: LocalStorage等を活用した所持カード・チェック状態の保持機能
- **SNSシェア機能（X連携）**: チェック結果（所持率・対象データ）に応じた動的なシェア用URL・ハッシュタグ自動生成（Web Intent API）

### 3. 法的配慮・コンプライアンス（ガイドライン・問い合わせ設計）
- **二次創作ガイドライン準拠**: 公式ポリシーに則った運営方針・著作権表記（コピーライト）の徹底と免責事項の明記
- **権利者向け専用メールフォーム**: 件名・本文にテンプレート（連絡理由・対象箇所等の入力欄）が自動展開されるメールリンク（mailtoパラメータ制御）を実装し、スムーズな連絡窓口を確保

---

## 💻 使用技術（Tech Stack）
- **Languages**: HTML5, CSS3, JavaScript (Vanilla JS / ES6+)
- **Architecture**: Single Page Application (SPA) 設計, 非同期通信 (Fetch / JSON)
- **Data & Storage**: LocalStorage, JSONデータ管理
- **External Integration**: X (Twitter) Web Intent API, Mailto URL Schema
- **Hosting**: GitHub Pages

---

## 💡 技術的な強み・こだわり
- **フレームワーク非依存（軽量・高速）**: ReactやVueなどの重い外部ライブラリを使わず、Vanilla JSで軽量に実装することで初期表示速度と操作レスポンスを最大化
- **完全レスポンシブ**: スマートフォンでの片手操作・スワイプ・モーダル操作に配慮したUI設計
- **拡散導線と問い合わせUX**: SNS自動シェアによるバイラル設計と、定型文自動入力による権利者対応の摩擦低減
