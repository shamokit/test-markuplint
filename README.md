# 概要

Svelte使用時のmarkuplintのテストリポジトリ。  
OS：windows(改行コードがCRLF)

## vite.config.js

localhost:3000で見たいので

```bash
	server: {
		port: 3000,
		host: true
	},
```

を追記しています。  
そのほかのsvelteの設定などはデフォルトのままです。

## npm scripts

ローカルサーバーの起動
```bash
npm run dev
```

markuplintのチェック
```bash
npm run markuplint
```
