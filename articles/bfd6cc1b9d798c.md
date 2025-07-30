---
title: "デジタル名刺をDIYする"
emoji: "🚀"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [個人開発, Astro]
published: true
---

# デジタル名刺とは
これ
https://prairie.cards/

# アウトプット
プロフィールページ
https://nkzwsh00.github.io/portfolio/
この公開ページURLをカードに書き込みます。

プロフィールページのリポジトリ
https://github.com/nkzwsh00/portfolio

# この記事で「つくる」もの
1. プロフィールページを作成し、
2. デプロイし、
3. NFCタグが埋め込まれたカードにURL情報を書き込む

# プロフィールページを作成する
究極何でもいいですが、ここでは Astro を使いました。
https://docs.astro.build/ja/install-and-setup/
公式ドキュメントの手順に沿ってプロジェクトを作成。

プロフィールページの中身は自由。
今回は、claudecodeに指示してプロフィールページとしてそれっぽい体裁を整えさせました。

# デプロイする
ここも、究極ページが公開できれば何でもいいです。
今回は Github Pages を使います。
https://docs.astro.build/ja/guides/deploy/github/
公式ドキュメントの手順に従って、。
以降、変更をプッシュすると勝手にデプロイされます。

# カードにURL情報を書き込む
NFCタグを購入します。
形や規格にいろいろ種類があるらしい。
自分は以下のものを購入。
https://www.amazon.co.jp/dp/B08WRV4NHM/
カード型のほかに、コイン型、シールなどもあります。
規格はよく見ずに買いましたが、動きました。
人のスマホで読み込んでもらうことを考えると、広く使われてそうなものを選ぶのが丸いのかもしれません。

URL情報の書き込みにはNFCライターアプリを使用します。
自分は NFC Tools というスマホアプリを使いました。（iOS、android両対応）

PCから書き込みたい場合は、NFCライター端末が必要になります。

# 完成

URL情報を書き込んだら、動作確認をして完成です。
無地でさみしいので、ネットプリントでアイコンをシールにして貼りました。

![完成したデジタル名刺のイメージ](/images/bfd6cc1b9d798c/image.jpg)

このあたりは完全に好みで。
交流会で、NFC非対応のスマホを持つ方がいる可能性もあるので、QRコードなどを貼っておいてもいいかもしれません。

# 余談：技術選定について
## Astro
軽くてプロフィールページや静的コンテンツを扱うのに向いている。
React と得意分野が真逆なので、2番目にさわる JavaScript フレームワークとして都合がよかった。

関連:
Astro の細かい特徴については、大岡さんのスライドがわかりやすい。
https://speakerdeck.com/oukayuka/react-haci-no10nian-wosheng-kican-reruka-3tunotorendokarakao-eru?slide=27

## github pages
無料でお手軽✌️