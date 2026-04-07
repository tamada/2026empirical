# 2026年度 エンピリカルソフトウェア工学

## 目的

- 実際のソフトウェア開発でどのようなことが行われているかを実践する．
  - そのために，何らかのアプリケーション（CLIアプリケーション）の開発を行い，ソフトウェア開発の流れを学ぶ．

授業に先立ち，以下のことをお願いします。

- [この Google Form](https://forms.gle/NJvFb8eChxA4k9TN7)から事前調査アンケートへの回答してください。
- [GitHub](https://github.com/)アカウントを作成しておいてください。
  - [GitHub Student Developer Pack](https://education.github.com/pack)へ登録しておいてください。

## 利用する技術

- 開発
  - git/[GitHub](https://github.com/), [GitLab](https://gitlab.com/)
    - [Conventional Commits](https://www.conventionalcommits.org/ja/v1.0.0/)
  - ビルドツール
    - [Gradle](https://gradle.org/)
    - [Pants](https://www.pantsbuild.org/)
    - [Bazel](https://bazel.build/)
    - [Buck](https://buck.build/)
    - [Please](https://please.build/)
    - [Blade](https://github.com/chen3feng/blade-build)）
  - リリース管理
    - [Semantic Versioning](https://semver.org/lang/ja/)
    - [DOI（Digital Object Identifier）](https://www.doi.org)
  - Web API
    - REST, [GraphQL](https://graphql.org)
- テスト
  - UnitTestツール
  - 各種サービス
    - [codebeat](https://codebeat.co/)
    - [Codacy](https://www.codacy.com/)
    - [Coveralls](https://coveralls.io/) など）
- デプロイ
  - CI/CD
  - [Homebrew](https://brew.sh/index_ja), [Chocolatey](https://community.chocolatey.org/) など
  - [Docker](https://docker.com/), [Podman](https://podman.io/), [Finch](https://github.com/runfinch)
- ドキュメント
  - README, badge
    - [Markdown](https://daringfireball.net/projects/markdown/)
  - ソフトウェアライセンス
    - [MIT](https://opensource.org/license/mit)
    - [GNU GPL](https://www.gnu.org/licenses/gpl-3.0.html)
    - [Apache License](https://www.apache.org/licenses/)など．
  - 静的サイトジェネレータ
    - [Jekyll](http://jekyllrb-ja.github.io/)
    - [Hugo](https://gohugo.io/)
    - [gatsbyjs](https://www.gatsbyjs.com/)など
  - 設定記述言語
    - Toml, Yaml, JSON, XML
  
### 利用する言語の候補

- [Zig](https://ziglang.org)
  - [他言語習得者がとりあえず使えるようになるZig](https://zenn.dev/drumato/books/learn-zig-to-be-a-beginner/viewer/introduction)
- [TypeScript](https://www.typescriptlang.org/)
  - [deno](https://deno.land/)
    - [Effective Deno](https://zenn.dev/uki00a/books/effective-deno)
    - [Deno での TypeScript の概要](https://deno-ja.vercel.app/manual@v1.9.1/typescript/overview)
  - [Bun](https://bun.com)
- [WebAssembly](https://webassembly.org)
  - [Wasmer](https://wasmer.io)
  - [Text Format](https://webassembly.github.io/spec/core/text/index.html)
  - [WebAssemblyの歩き方](https://zenn.dev/canary_techblog/articles/47af6331b4ecfb)
  - [入門WebAssembly](https://www.amazon.co.jp/dp/4798173592/)
- [Rust](https://www.rust-lang.org/ja)
  - https://rust-cli.github.io/book/index.html
  - [Command Line Apps in Rust](https://rust-cli.github.io/book/index.html#command-line-apps-in-rust)
  - [Command Line Rust](https://www.oreilly.com/library/view/command-line-rust/9781098109424/)
  - [プログラミング言語Rust](https://doc.rust-jp.rs/book-ja/)
- [Go](https://go.dev/)
- [Kotlin](https://kotlinlang.org/)
- Java（モダンな書き方）
  - [All Loops Are a Code Smell](https://medium.com/swlh/all-loops-are-a-code-smell-6416ac4865d6)
  - [GraalVM](https://www.graalvm.org/) で native code にする．

## 開発候補

### lsの再発明

以下のような機能を盛り込もう。
全て盛り込む必要はない。以下に挙げていない機能を盛り込むのもあり。

- `-l` フォーマットの時に、以下のようにする。
  - ファイルサイズを 1.2GB など human readable (humanize) する。
  - ディレクトリ内に README.md があれば、tagline を表示する。
  - pdf はPDF内のタイトルを表示する。
- `.gitignore`、`.dockerignore` などを考慮して表示する。
- 作成日時が24時間以内であれば、🆕 を付ける。
- ソート順をファイルサイズ、最終更新日時、ファイル名などを選択できる。
- 。。。

## 進め方

- 第１講（2026-04-10）
  - 言語を決める．
- 第２講（2026-04-17）〜第12講（2026-07-03）
  - 各種知識の授業．
  - 開発．
  - なお，プログラム言語自体に関する授業はあまり行いません．
- 第13講（2026-07-10），第14講（2026-07-17）
  - 発表

## 参考資料

- [Command Line Interface Guidelines](https://clig.dev)
  - CLIアプリはどうあるべきかが書かれたサイト．
- [tamada/developing_flows](https://github.com/tamada/developing_flows)
  - ソフトウェア開発でプログラムを書き始める前に行わなければならないことを中心に書いた手引き書．
- [シェルスクリプトを学ぶ人のための「新しいUNIX哲学」 〜 ソフトウェアツールという考え方](https://qiita.com/ko1nksm/items/c55d067b55bbd561df11)
  - これまでに出版されている4つのUNIX哲学を踏まえて，現代のUNIX哲学について解説している．
- [図解でわかる! 理工系のためのよい文章の書き方 論文・レポートを自力で書けるようになる方法](https://www.amazon.co.jp/dp/4798158895)
- [イラストでわかるDockerとKubernetes](https://www.amazon.co.jp/dp/4297118378/)（[改訂版](https://www.amazon.co.jp/dp/4297140551) 2024-03-04 発売）
