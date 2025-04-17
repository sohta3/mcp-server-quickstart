# mcp-server-quickstart

[Zenn記事「MCPサーバー自作入門」](https://zenn.dev/zaki_yama/articles/mcp-server-getting-started)の実装例です。

## 概要

National Weather Service (NWS) APIを使用して、米国の気象情報を取得するMCPサーバーです。

## 機能

- 緯度経度を指定して天気予報を取得
- 米国内の地域のみサポート

## 使用方法

1. インストール

```bash
npm install
```

2. ビルド

```bash
npm run build
```

3. Cursorの設定

`.cursor/mcp.json`に以下の設定を追加：

```json
{
    "mcpServers": {
      "weather-forecast": {
        "command": "node",
        "args": [
          "./build/index.js"
        ]
      }
    }
}
```

## ライセンス

ISC
