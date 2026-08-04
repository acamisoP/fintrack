# fintrack

家計簿システム「kakeibo」の閲覧専用PWA(GitHub Pages配信用・Public)。

- 明細DB(Notion)をホーム/取引/分析の3画面で見る。**編集機能なし**
- カメラ版(`kakeibo-pwa` リポジトリ)とは**別リポジトリ**。同一オリジンの別パスに分けることで
  PWAのscope衝突(カメラ版のscope内にネストすると1つのアプリに統合されてしまう)を回避している
- GAS WebアプリURLは**このリポジトリに含めない**。`?gas=<WebアプリURL>` で一度開くと
  localStorageに保存される。カメラ版設定済みの端末なら同一オリジンのため設定不要
- 本体(GAS・設計書)は別リポジトリ `kakeibo`(Private)で管理

## スマホへの導入手順

1. Chromeで `https://<pages-url>/fintrack/` を開く(カメラ版設定済みなら `?gas=` 不要)
2. メニュー →「ホーム画面に追加」
3. 起動すると今月のサマリーが即表示される
