---
title: "1つのlabel要素に複数のinput要素を関連付ける"
emoji: "🍢"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [HTML, HTML5, アクセシビリティ]
published: false
---

作りたい画面のイメージはこんな感じ

![検索条件のイメージ](/images/f5c4ffe50e6ff2/image1.png)

label要素「出版年代」を
2つの入力要素と関連づけたい


参考にしたのは以下の記事
https://zenn.dev/uhyo/articles/aria-label-and-labelledby

以下のようなコードになった。

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
