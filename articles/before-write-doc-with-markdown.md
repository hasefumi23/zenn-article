---
title: "Markdown でドキュメントを書くその前に"
emoji: "🐕"
type: "tech"
topics: ["markdown", "document"]
published: true
---

:::message
この記事は諸事情合って突貫で書いたので、結構至らない点があると思います😅
その辺に関しては後日修正予定です。
:::

IT に携わるエンジニアにとって最も一般的な記法といえば Markdown ですよね。GitHub や GitLab、Backlog などの仕事で使うサービスでも Markdown 記法がよく使われています。ちょっと前から、自分は手元のメモなどにも Markdown を使うようにしました。元々記法を覚えるのが面倒だったり、プレビューするのが面倒だったりと、何かと面倒だと思ってましたが、慣れればとても便利なものだということに気づきました。

- プレビューせずとも、目を凝らせばドキュメントの構造がパットわかる視認性の良さ
- Markdown さえ覚えていれば大体どのチケット管理系のサービスでも対応しているという、ポータビリティの高さ
- すべてをテキストで表現するので、git との相性もとても良い

そうやって Markdown を日々書く中で、自分の Markdown 環境をコツコツとカイゼンして来ました。この記事では、Markdown でドキュメントを書くその前に、整えておくと便利な設定やツールなどを紹介します。

大前提として、エディタには VS Code を使っています。

- [VS Code Extension](#vs-code-extension)
    - [Markdown All in One](#markdown-all-in-one)
    - [markdownlint](#markdownlint)
    - [Paste Image](#paste-image)
    - [Table Formatter](#table-formatter)
    - [Markdown Emoji](#markdown-emoji)
    - [Excel to Markdown table](#excel-to-markdown-table)
- [Chrome Extension](#chrome-extension)
    - [Create Link](#create-link)
    - [cocopy](#cocopy)
- [Font](#font)
    - [UDEV Gothic](#udev-gothic)
- [オススメの記事](#オススメの記事)
- [Tips](#tips)

## VS Code Extension

まずは VS Code の Extension を入れましょう。以下がそのリストです。

### Markdown All in One

https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one

- とりあえず入れておきましょう
- 機能がありすぎて把握できてませんが、便利にしてくれているはずです

### markdownlint

https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint

- Markdown 用の linter です
- 統一感のある見た目に整えてくれます

### Paste Image

https://marketplace.visualstudio.com/items?itemName=mushan.vscode-paste-image

- 画像をいい感じに処理してくれる Extension です
- クリップボードの画像を開いているエディタのディレクトリに保存して、そのファイルのパスを書き込んでくれます
- こんな感じの動作です
    - ![](/images/vscode-paste-image.gif)

### Table Formatter

https://marketplace.visualstudio.com/items?itemName=shuworks.vscode-table-formatter

- いい感じにテーブルをフォーマットしてくれます
- テーブルに日本語が入っていてもきれいに整形してくれる
- 以下の Extension もテーブルをフォーマットしてくれますが、日本語が入ってたりすると若干崩れてしまうため、今は使ってません
    - [Markdown Table Prettifier](https://marketplace.visualstudio.com/items?itemName=darkriszty.markdown-table-prettify)

### Markdown Emoji

https://marketplace.visualstudio.com/items?itemName=bierner.markdown-emoji

- emoji は当然必要ですよね
- `:`に続けて絵文字の名前を入力したら、いい感じにサジェストしてくれます

### Excel to Markdown table

https://marketplace.visualstudio.com/items?itemName=csholmq.excel-to-markdown-table

- Markdown の弱点のひとつであるテーブルを書くときに良い働きをしてくれる Extension です
- Excel もしくはスプレッドシートからコピペすると、表形式をいい感じにテーブル記法に変換してくれます
    - こんな感じに動作します
        - ![](/images/vscode-extension-excel-to-table.gif)

## Chrome Extension

記事を書くときは、参考にしたサイトなどの URL をコピペすることが頻繁にあると思います。以下の 2 つの Extension は、URL を簡単に Markdown 形式でコピーすることができる Extension です

### Create Link

https://chrome.google.com/webstore/detail/create-link/gcmghdmnkfdbncmnmlkkglmnnhagajbm

- マウスを使っているときは、こっちを使います

### cocopy

https://chrome.google.com/webstore/detail/cocopy/ihnfodlbkhgjnbheemjhkjfkfglgbdgc

- キーボードだけで操作したいときはこっちを使います
- こちらはカスタムすることでリッチテキストとしてコピーすることもできるので便利です
    - カスタムの方法については以下の記事を参照してください
        - [Slack や Google Docs にページへのリンクを共有するなら圧倒的に cocopy が楽 - 詩と創作・思索のひろば](https://motemen.hatenablog.com/entry/2022/02/cocopy-rich-text)
- あとロゴがかわいい

## Font

### UDEV Gothic

フォントは、UDEV Gothic を使っています。以前は PlemolJP や JetBrains Mono など試していましたが、これに落ち着きました。

https://github.com/yuru7/udev-gothic

- >UDEV Gothic は、ユニバーサルデザインフォントの BIZ UD ゴシック と、 開発者向けフォントの JetBrains Mono を合成した、プログラミング向けフォントです。
    - らしいです
- 個人的にメリットと感じるのは以下の点です
    - 全角スペースが可視化されている
        - ![](/images/2022-08-04-23-11-58.png)
        - ![](/images/2022-08-04-23-13-31.png)
        - Markdown は半角スペースを使うべき箇所に、全角スペースを使ったらうまくレンダリングされないので、地味に便利です
- 幅比率が 半角 1:全角 2
    - 半角文字と全角文字が混在しても、列がいい感じに揃っていてとてもいい
- 判別しづらい文字が判別し易い形になっている
    - UDEV Gothic を使えば SIer と Sler を間違えることもなくなる (きっと)
        - ![](/images/2022-08-04-23-18-26.png)

## オススメの記事

オススメの記事は、Markdown 記法についてではなく、ドキュメントを書く時の心構えなどについて書かれた記事を紹介します。個人的にこの 2 つの記事を読んでから箇条書きの便利さを知り、Markdown でドキュメントを書く時も箇条書きを多用するようになりました。

https://scrapbox.io/shokai/%E7%BE%8E%E6%96%87%E7%AB%A0%E6%BB%85%E3%81%99%E3%81%B9%E3%81%97

http://haya14busa.com/hatena-pepabo-kyoto/

Markdown で書くときも箇条書きを使って文章に構造を持たせると、書き手の頭も整理されやすいし、読み手の頭にもスッと入ってくる文章になると思っています。

## Tips

VS Code で Markdown を書く時に覚えておくとちょっとだけ便利な Tips を書きます。

- 箇条書きは `tab` でインデント可能
    ![](/images/markdown-tips1.gif)
- 箇条書きの中にコードブロックを書く場合、インデントさせる必要がある (空行はなくてもいいけど linter に怒られます)

    ```js
    console.log("hello, world!");
    ```

    - 実際には以下のように書いています
        - ![](/images/2022-08-04-23-42-18.png)
- `- [ ]` でチェックボックスを作れる
    - [ ] こんな感じでチェックボックスを作れます
    - サービスによっては、文章を直接編集せずにクリックするだけでチェックすることも可能です

---

以上、Markdownを書く環境の紹介でした。少しでも読んでくれた人の役に立てたら嬉しいです😁
皆さんもMarkdown関連のオススメExtensionなどがあったら教えて下さい🙏
それではHappy writing✨
