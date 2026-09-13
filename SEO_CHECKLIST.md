# SEO改善チェックリスト

正式URL: https://toms-thinking.github.io/

## 実装と検証

- [x] title: 物知りトムさん｜公式ホームページ
- [x] description: 下記の自然な日本語130文字を設定
- [x] canonical: https://toms-thinking.github.io/
- [x] h1: 既存の「物知りトムさんの大冒険」を1つ維持。各セクションh2、カード見出しh3
- [x] 本文: 既存紹介の冒頭に正式名称を使用。画面上部に公式ホームページと明示
- [x] alt: 全7画像に説明。トムさん、町の集合絵、ピップの説明を改善
- [x] OGP: title / description / type / url / image / site_name / locale、画像寸法・alt
- [x] X: summary_large_image、title / description / image / image:alt
- [x] 構造化データ: WebSiteのJSON-LD。法人・レビュー等を追加していません
- [x] robots.txt: 全クローラー許可、サイトマップを指定
- [x] sitemap.xml: 実在するトップページのみ。ページ内アンカーと外部noteは含めていません
- [x] favicon: 既存tom.pngを縮小した48px PNG、180px Apple Touch Icon
- [x] 画像軽量化: 元PNGを保持し表示用WebPを追加。7画像合計8,160,725→1,169,742バイト（約86%削減）
- [x] 下部画像6枚にlazy loading、最初の世界観画像はeager、全画像に寸法とasync decoding
- [x] viewport設定維持。Chromeの320 / 375 / 390 / 768 / 1440pxで横はみ出し・画像読込を検証
- [x] ページ内リンク、画像、favicon、OGP画像、robots.txt、sitemap.xmlをローカルHTTPで検証
- [x] 第2話・第3話の仮リンクを、公式note一覧で確認した実在記事URLに修正
- [x] 外部リンク9件すべてHTTP 200（note 6件、YouTube、X、TikTok）。ログインや地域差による表示は別途確認が必要
- [x] CSS / JavaScriptは既存のHTML内配置を維持。ブラウザーのJavaScriptエラーなし
- [x] JavaScript無効時も本文表示。通常時のフェード演出は維持
- [x] 既存の外側sectionの閉じタグを補完し、背景色・余白・レイアウトを維持
- [x] Google確認用HTMLファイルをルートに追加可能。架空の確認コードなし
- [ ] 実機iPhone Safariで最終表示確認（Chromeでの幅別確認は実施済み）
- [ ] Google Search Console登録待ち

## 最終description

物知りトムさんの公式ホームページ。親子で読める、やさしいなぞとき物語の世界をご紹介しています。19世紀ヨーロッパ風の町リンドルを舞台に、トムさんと仲間たちのキャラクター紹介や、身近なふしぎを解き明かすお話、noteで読めるエピソードへのリンクを掲載しています。

## sitemap.xmlの登録ページ

- https://toms-thinking.github.io/

## robots.txt

```text
User-agent: *
Allow: /

Sitemap: https://toms-thinking.github.io/sitemap.xml
```

## JSON-LD

```json
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "name": "物知りトムさん",
  "alternateName": "物知りトムさんの大冒険",
  "url": "https://toms-thinking.github.io/",
  "description": "物知りトムさんの公式ホームページ。親子で読める、やさしいなぞとき物語の世界をご紹介しています。19世紀ヨーロッパ風の町リンドルを舞台に、トムさんと仲間たちのキャラクター紹介や、身近なふしぎを解き明かすお話、noteで読めるエピソードへのリンクを掲載しています。",
  "inLanguage": "ja"
}
```

## 変更ファイル

- 変更: index.html
- 新規: robots.txt、sitemap.xml、SEO_CHECKLIST.md、favicon.png、apple-touch-icon.png
- 新規画像: images/ogp.jpg、images/title2.webp、images/7spring.webp、images/tom.webp、images/pip.webp、images/meg.webp、images/gaff.webp、images/gilbert.webp
- 元のPNG画像は変更していません。OGPはtitle2.pngの全体を1200×630に収め、余白だけ追加しています

## Search Consoleで人間が行う作業

1. URLプレフィックスのプロパティとして https://toms-thinking.github.io/ を追加します
2. HTMLファイルによる確認を選び、Googleが発行した確認ファイルをダウンロードします
3. ファイル名と内容を変えずにリポジトリルートへ追加し、GitHub Pagesへ公開します
4. Google指定URLでファイルが取得できることを確認し、Search Consoleの「確認」を実行します。確認ファイルはその後も保持します
5. サイトマップに https://toms-thinking.github.io/sitemap.xml を送信します
6. URL検査でトップページを確認し、インデックス登録をリクエストします
7. ページのインデックス登録と検索パフォーマンスを継続確認します。設定だけで検索順位や掲載時期は保証されません

## 今後の改善

- note・Xのプロフィール等から「物知りトムさん 公式ホームページ」の自然なリンクを設定します
- 作品の公開状況を更新します。第1話リンク先のnoteタイトルは「トムさんとしゃべる犬」、サイトの紹介タイトルは「はじまりの栗の木」と異なるため、意図を確認してから統一します（今回の掲載内容は維持）
- 実測のCore Web Vitalsを確認し、必要ならフォントや画像の配信サイズを追加調整します
- Search Consoleの検索語を参考に、必要な作品紹介を少しずつ充実させます。SEOだけを目的とした大量ページは作成しません
- /index.htmlのcanonicalはルートに統一しています。GitHub Pagesにはサーバー側リダイレクトを追加していません
