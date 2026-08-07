# my twitter 🕊️

自分だけのタイムライン。読者は専属AI秘書1名。

- 投稿すると `naganoyoh/secretary`（プライベート）の `ネタメモ/` にmdファイルが1枚増える
- 秘書が毎朝それを読んで、SNSポストの下書きに変換する
- 「📮 秘書からの納品」欄で、最新のSNSストック10本をタップコピーできる

## 構成

`index.html` 1枚だけの静的ページ。ビルド不要。

- 合鍵（GitHub PAT）は端末のlocalStorageにのみ保存。送信先はGitHub API（api.github.com）のみ
- 圏外・失敗時は下書きをlocalStorageに退避し、次回復元する

## デプロイ（Cloudflare Pages）

1. Cloudflareダッシュボード → Workers & Pages → Create → Pages → Connect to Git
2. このリポジトリ `naganoyoh/my-twitter` を選択
3. ビルド設定はすべて空欄のまま（Framework preset: None）でデプロイ
4. できたURLをiPhoneのSafariで開き、共有 → **ホーム画面に追加**
5. 初回のみ ⚙️ から合鍵（`github_pat_…`）を保存
