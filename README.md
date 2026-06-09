# 鳩居ぼたん案内所

GitHub Pagesで公開する静的Webサイトです。

## 推奨ディレクトリ構成

```text
hatoi-botan-guide/
├── index.html
├── profile.html
├── services.html
├── works.html
├── links.html
├── assets/
│   ├── css/
│   │   └── style.css
│   └── images/
│       ├── .gitkeep
│       └── README.md
├── .nojekyll
└── README.md
```

## サイト設計概要

「なんでもやってるお宿のお姉さん」をコンセプトに、トップページを総合受付、下層ページを各案内板として設計しています。

- `index.html`: 初見の訪問者向けの総合案内。受付中サービス、作品・企画、SNS、お問い合わせへの導線を配置。
- `profile.html`: 何をしている人なのかを伝える自己紹介、現在の活動、活動履歴。
- `services.html`: 占い、相談サポート、イラスト、衣装デザイン、グッズ販売のメニュー。
- `works.html`: お言葉、12星座メイド、アトリエくろにかの企画紹介。
- `links.html`: SNS、販売サイト、依頼窓口、その他リンク。

## デザイン方針

桜色、白、若草色を中心にした、団子の三色を思わせる配色です。和風に寄せすぎず、宿屋の案内所らしい読みやすさと個人サイトの温かみを優先しています。

画像を追加する場合は `assets/images/` に保存し、HTML内の `.image-slot` 部分を `img` 要素に差し替えてください。

## GitHub Pages公開手順

1. このフォルダの中身をGitHubリポジトリへ追加します。
2. GitHubで対象リポジトリを開きます。
3. `Settings` → `Pages` を開きます。
4. `Build and deployment` の `Source` で `Deploy from a branch` を選びます。
5. `Branch` で `main`、公開フォルダで `/root` を選び、保存します。
6. 数分待つと、GitHub PagesのURLが表示されます。

リポジトリのサブフォルダで公開する場合は、公開したいフォルダだけをリポジトリ直下に置くか、GitHub Pagesの公開対象を調整してください。

## WordPressへ移行しやすくするための注意点

- 1ページ1テーマに分けているので、固定ページ化しやすい構成です。
- 共通ナビゲーション、本文、カード、リンク集をCSSクラスで分けています。
- 本文はHTML内に直接書いているため、WordPress移行時は各ページ本文へコピーしやすいです。
- 画像は `assets/images/` に集約する想定なので、WordPressのメディアライブラリへ移しやすくなっています。
- JavaScriptや外部ライブラリに依存していないため、テーマ化したときの崩れが少ない構成です。
- 将来の移行を考える場合、見出し階層を変えすぎず、サービスやリンクはまとまり単位で管理してください。

<!-- Reflesh -->