# flat35hd99

- [flat35hd99](#flat35hd99)
- [ポートフォリオ](#ポートフォリオ)
  - [TEDxNagoyaUのウェブページリプレイス](#tedxnagoyauのウェブページリプレイス)
  - [cache-make](#cache-make)
  - [openscad-actions](#openscad-actions)
  - [生物学的構造単位生成器](#生物学的構造単位生成器)
  - [その他成果物や公開しているもの](#その他成果物や公開しているもの)
- [Education](#education)

# ポートフォリオ

## TEDxNagoyaUのウェブページリプレイス

以前所属していたサークルのウェブページを完全リプレイスしました。

- リポジトリ([tedxnagoyau/website](https://github.com/tedxnagoyau/website))
- デモ
  - [現在現役生によって運用されているウェブサイト](https://tedxnagoyau.com/)
  - [デモサイト](demo-tedxnagoya-u.wataru.app)(flat35hd99の最終コミット時点)
    - [予備リンク](https://fir-tedxnu.web.app/)
- 開発期間: 6ヶ月
- 開発人数：2人（当時）
- 使用技術：Nuxt, Nuxt Content, Vuetify, Firebase, GitHub Actions

当時はWordPressによって運用されていましたが、数年メンテナンスがされておらず、以下のような課題を抱えていました。

- WordPress, PHPともにバージョンが古く、多数の脆弱性がそのままになっていた
- 使用していたテーマのサポートが過去のバージョンアップ作業によって切れてしまい、管理できなくなっていた
- 毎月VM維持の費用がかかる
- 更新一つ一つがビッグバンアップデートになり、更新の心理的ハードルが高い

これらの課題を解決するため、当時比較的新しい技術であった、[Nuxt](https://github.com/nuxt/nuxt.js)と[Nuxt Content](https://github.com/nuxt/content)を用いた静的ウェブサイトによって、置き換えました。

技術選定においては、上記課題を解決しつつ、以下の項目についても考慮しました。

- イベント運営のサークルであるため、技術に強い人間が毎年来る・育成に成功するとは限らないこと
  - 対立候補の[Gatsby](https://github.com/gatsbyjs/gatsby)や[Next](https://github.com/vercel/next.js)はReactで書くため、学習コストを勘案して除外
- 開発・運用が、携わった人のキャリアにプラスにはたらくこと
- 秋からの開発に際し、夏のイベントの告知を新ウェブページで行えること

## cache-make

GNU makeはビルド対象物とそのソースファイルのタイムスタンプを比較して、再ビルドが必要か判別します。しかし、GitHub Actionsで利用する場合には、通常の[actions/cache](https://github.com/actions/cache)を使うだけではタイムスタンプ情報が失われてしまうため、全てビルドし直すことになってしまいます。

本actionはgitのlogからタイムスタンプ情報を復元し、必要最低限のビルドだけで済むようにできるようにします。

- [解説記事](https://qiita.com/flat35hd99/items/b0b8931f8dfcb00891cb)
  - なぜ作ったのかはこの記事が詳しいです。
- [リポジトリ](https://github.com/flat35hd99/cache-make)
- 開発期間：1週間程度
- 開発人数：1人
- 使用技術：シェルスクリプト, Git

## openscad-actions

OpenSCADはスクリプト言語によってオブジェクトを記述できるCADです。必然的にGitとの親和性が高く、CI/CDしたいと思ったため、GitHub Actionsによる自動ビルドを簡単にできるactionsを作成しました。これまで3回fork,1回PRされている、ニッチなところに刺さるactionsです。

- [リポジトリ](https://github.com/flat35hd99/openscad-actions)

## 生物学的構造単位生成器

JPHACKS 2021というハッカソンで、研究上の課題を解決するために作成しました。

- [リポジトリ](https://github.com/jphacks/d_2110)

## その他成果物や公開しているもの

- [flat35hd99 - GitHub](https://github.com/flat35hd99)
- [Qiita](https://qiita.com/flat35hd99)
- [Computational Study on the Thermal Conductivity of a Protein](https://doi.org/10.1021/acs.jpcb.2c00958)

# Education

- 名古屋大学理学部物理学科
- 名古屋大学大学院理学研究科 <- Here
