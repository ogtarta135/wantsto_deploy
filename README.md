# wantsto_deploy
test用

## draw.io MCP サーバー連携

リポジトリ直下の `.mcp.json` で公式の draw.io MCP サーバー（[`@drawio/mcp`](https://github.com/jgraph/drawio-mcp)）を登録しています。
Claude Code でこのリポジトリを開くと `drawio` サーバーが読み込まれます（初回は承認プロンプトが出ます）。

- 必要なもの: Node.js（`npx` が使えること）
- `DRAWIO_BROWSER=off` のため、ブラウザは自動で開かず、draw.io エディタの URL だけを返します（クラウド/SSH 環境向け）。ローカルでブラウザを自動で開きたい場合はこの行を削除してください。

主なツール:

| ツール | 用途 |
|---|---|
| `open_drawio_mermaid` | Mermaid から draw.io 図を作成 |
| `open_drawio_xml` | draw.io XML から図を作成（ELK 自動レイアウト可） |
| `open_drawio_csv` | CSV から図（組織図など）を作成 |
| `search_shapes` | AWS / Azure / GCP などのアイコン検索 |
| `list_pages` / `get_page` / `set_page` | ローカルの `.drawio` ファイルをページ単位で読み書き |
| `get_drawio_reference` | 図作成用リファレンスの取得 |

使い方の例: 「このリポジトリの構成図を draw.io で描いて」
