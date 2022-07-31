# 概要

markuplintのテストリポジトリ。  
前提：windowsユーザーです。(改行コードがCRLF)

## .markuplintrc

デフォルト設定からの変更点

### attr-spacing
rule.attr-spacingをfalseにしています。

### indentation
rule.indentationを"tab"にしています。

### character-reference
rule.character-referenceを教えていただいた通りfalseにしています。

### parser
parserに@markuplint/svelte-parserを指定しています。

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

## チェック結果

```
> test-markuplint@0.0.1 markuplint
> markuplint ./src/**/*.svelte

<markuplint> error: The #text is invalid element (15:7): Broke mapping nodes. (parse-error) D:\develop\test-markuplint\src\components\Navigation.svelte:15:7
  14: →   →   </li>
  15: →   </ul>
                                                                                    
  16: </nav>
<markuplint> error: The #text is invalid element (15:7): Broke mapping nodes. (parse-error) D:\develop\test-markuplint\src\components\Navigation.svelte:15:7
  14: →   →   </li>
  15: →   </ul>
                                                                                    
  16: </nav>
<markuplint> passed D:\develop\test-markuplint\src\routes\index.svelte
```
