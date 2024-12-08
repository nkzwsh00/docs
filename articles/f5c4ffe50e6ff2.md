---
title: "1つのlabel要素に複数のinput要素を関連付ける"
emoji: "🍢"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [HTML, HTML5, アクセシビリティ]
published: true
---

# つくりたいもの

![検索条件のイメージ](/images/f5c4ffe50e6ff2/image1.png)

label要素「出版年代」を
2つの入力要素と関連づけたい

# 実装したもの

```html
<h3>検索条件</h3>
<label id="published" for="start">出版年代</label>
<p>
  <input
    id="start"
    type="text"
    aria-label="始点"
    aria-labelledby="published start"
  />
  〜
  <input
    id="end"
    type="text"
    aria-label="終点"
    aria-labelledby="published end"
  />
</p>
```

アクセシビリティも以下の通り付与されている。
![付与されたアクセシビリティのイメージ](/images/f5c4ffe50e6ff2/image2.png)

# 解説

表題のような疑問に対して、テックリードから提示されたのが以下の記事。

https://zenn.dev/uhyo/articles/aria-label-and-labelledby


この表題の問いについて、関連付けというふわっとして言葉を使ってますね。
この問いをテックリードに投げた時点で自分には課題が分割できておらず、正確には以下の2つを分解して考えるべきでした。
- labelをクリックしたときinput要素がアクティブになる。
- input要素とlabel要素の関係をアクセシビリティ観点でわかる状態にする。

1つ目についてはlabelクリック時に1つ目のinput要素が活性化すればよく、
2つ目についてはaria-labelのベタ書きでも達成できます。

例として以下のようにaria-labelledbyのハックを使わなくても課題を達成できますね。

```html
<h3>検索条件</h3>
<label id="published" for="start">出版年代</label>
<p>
  <input
    id="start"
    type="text"
    aria-label="出版年代 始点"
  />
  〜
  <input
    id="end"
    type="text"
    aria-label="出版年代 終点"
  />
</p>
```
