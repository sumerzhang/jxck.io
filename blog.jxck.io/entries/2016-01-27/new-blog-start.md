# [web][blog] Blog を移転しました


## Intro

長いこと [はてな](https://jxck.hatenablog.com/) をメインにし、他にも [Qiita](https://qiita.com/jxck_) や [Tumblr](http://jxck.tumblr.com/) を使って色々書いて来たが、そろそろ自分のドメインに全部集約していこうかと思う。


## motivation

最近、メディア系は独自のサイトを持つよりも、 Medium などのサービス経由で流入してもらわないと辛いという話を良く聞くので、その意味では完全に逆行しているかもしれない。

しかし、別に PV を稼ぐためにブログを書いているわけでもないので、むしろ技術的にも自分で色々試せる自由な環境を持ち、特定のサービスに依存せずやってみるのも良いと考える。

むしろ、ドメイン自体は結構前に取っていたので、遅すぎるくらいなのだが、やっと重い腰を上げた。

まだ作り途中であり、一気に移行するのは難しいが、徐々に作りながらやっていこうと思う。


## test section

以降は、本サイトのマークアップやスタイルをテストするためのセクションである。

対応している記法を列挙し、挙動を確認する。


### headding section 3

ここは `<h3>` セクションである。


#### headding section 4

ここは `<h4>` セクションである。


### リストスタイル

リストスタイルは 2 つある

1. ordered list
2. un-ordered list

それぞれは使うタグが違う

- ここはリストスタイルである
- unordered list は `<ul>` を用いて表現する
- `<li>` の前には markdown と同じく `-` を表示する
  - 入れ子にも対応している
- しかし 2 段階以上の深さは使わないようにする


### 定義リスト

定義リストは `<dl>` を用いて表現する

定義リスト(description list)
: `<dl>` を用いる

定義(description term)
: `<dt>` を用いる

説明(description details)
: `<dd>` を用いる


### サンプルコード

インラインの場合は `<code>` タグを用いて表現する。

コードブロックの場合は `<pre>` と `<code>` を用いて表現する。


```js
if ('ServiceWorkerGlobalScope' in self && self instanceof ServiceWorkerGlobalScope) {
  ['install', 'activate', 'beforeevicted', 'evicted', 'fetch', 'message', 'push'].forEach((e) => {
    self.addEventListener(e, (ev) => {
      console.log(e, ev);
    });
  });

  self.addEventListener('install', (ev) => {
    ev.waitUntil(self.skipWaiting());
  });

  self.addEventListener('activate', (ev) => {
    ev.waitUntil(self.clients.claim());
    console.log('claimed');
  });
}
```

ファイルからコードを読むこともできる。


```js:sample.js
```


## 引用

引用は `<blockquote>` を用いて表現する。

> 他のサイトなどから引用する場合は `<blockquote>` を用いて表現する。
> 複数行あると `<p>` に展開される
> 引用元の URL は `<cite>` を用いてマークアップする
> --- <cite>[example.com](https://example.com)</cite>


## テーブル

テーブルは `<table>` タグを用いて表現する。

| 範囲             | 文字数 |
|:-----------------|-------:|
| 基本ラテン文字   | 94     |
| CJK 記号と句読点 | 11     |
| ひらがな         | 81     |
| カタカナ         | 83     |
| 半角形と全角形   | 0      |
| 常用漢字         | 2136   |
| 記号             | 1      |
| 不要文字         | - 23   |
| 追加更新         | 13     |
| 合計             | 2396   |


| file type | size  | ratio |
|:----------|------:|------:|
| .webp     |  9474 |  100% |
| .webp.gz  |  2609 |   28% |
| .webp.br  |  2544 |   27% |



## イメージ

イメージは `<img>` タグを用いて表現する。

![jxck](https://logo.jxck.io/jxck.png#256x256 'jxck logo')
