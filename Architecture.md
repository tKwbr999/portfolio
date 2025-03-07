# プロジェクトアーキテクチャ

## 技術スタック

- **フレームワーク**: Next.js 15.2.1
- **言語**: TypeScript 5.x
- **スタイリング**: Tailwind CSS
- **UIコンポーネント**: 
  - Lucide React (アイコン)
  - Class Variance Authority (コンポーネントのバリエーション管理)
  - Tailwind Merge (クラスのマージ)
  - Tailwind CSS Animate (アニメーション)

## プロジェクト構造

```
portfolio/
├── src/               # ソースコードのルート
│   ├── app/          # Next.js 13+のApp Router
│   │   └── ...       # ページとレイアウト
│   ├── components/   # UIコンポーネント
│   │   └── ui/      # 基本的なUIコンポーネント
│   │       └── button.tsx
│   └── lib/          # ユーティリティと共有ロジック
│       └── utils.ts  # 一般的なユーティリティ関数
├── public/           # 静的アセット
├── components.json   # コンポーネントの設定
├── next.config.ts    # Next.jsの設定
├── tsconfig.json     # TypeScriptの設定
├── eslint.config.mjs  # ESLintの設定
└── postcss.config.mjs # PostCSSの設定
```

## UIコンポーネント

### Buttonコンポーネント
- **場所**: `src/components/ui/button.tsx`
- **特徴**:
  - Radix UIのSlotコンポーネントを使用
  - Class Variance Authorityでバリエーション管理
  - レスポンシブデザイン対応
  - アクセシビリティ考慮
  - ホバー、フォーカス、ディスエーブル状態のスタイリング

### 利用可能なバリエーション
- `variant`: default, destructive, outline, secondary, ghost, link
- `size`: default, sm, lg, icon

## 開発環境

- **開発サーバー**: `npm run dev` (Turbopackを使用)
- **ビルド**: `npm run build`
- **起動**: `npm run start`
- **Lint**: `npm run lint`

## 特徴

- TypeScriptによる型安全性
- Tailwind CSSによる効率的なスタイリング
- Next.jsのApp Routerによるモダンなルーティング
- モダンな依存関係管理 (React 19, Next.js 15)
