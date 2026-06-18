# EC送料設計レポート：GitHub Pages公開用

このフォルダの `index.html` をGitHubへアップロードすると、GitHub Pagesで公開できます。

## 公開手順

1. GitHubで新しいPublicリポジトリを作る
2. このフォルダ内の `index.html` をアップロードする
3. リポジトリの `Settings` → `Pages` を開く
4. `Build and deployment` のSourceを `Deploy from a branch` にする
5. Branchを `main`、フォルダを `/(root)` にして保存する

公開URLの形：

`https://GitHubユーザー名.github.io/リポジトリ名/`

元の調査Markdownを変更した後は、ワークスペース直下で次を実行すると `index.html` も更新されます。

```powershell
node .\render_ec_shipping_report.mjs
```

GitHubとの初回接続が終わった後は、ワークスペース直下で次を実行すると、HTML作成・コミット・GitHubへの送信をまとめて実行できます。

```powershell
.\publish_github_pages.ps1
```
