# 工藤の学習メモ

## リンク

- [1章 TypeScriptとは何か](https://chaploud.github.io/EffectiveTypeScript/kudo/chapter01/)
- [2章 TypeScriptの型システム](https://chaploud.github.io/EffectiveTypeScript/kudo/chapter02/)

## 実行環境

TypeScriptをそのまま実行できて便利なので `Bun` を使う

### インストール(Linux)

```bash
curl -fsSL https://bun.sh/install | bash
```

### 初期化

```bash
bun init # ローカル環境
```

### VSCode拡張機能

- [Code Runner](https://marketplace.visualstudio.com/items/?itemName=formulahendry.code-runner) をインストール
- [Bun for Visual Studio Code](https://marketplace.visualstudio.com/items/?itemName=oven.bun-vscode) をインストール
- settings.jsonに以下を設定

```json
{
  "code-runner.executorMap": {
    "javascript": "bun"
    "typescript": "bun"
  }
}
```

### 実行

- VSCode上で「Run Code」を実行する　か
- コマンドラインで `bun <ファイル>.ts` を実行する
