---
title: GithubActions を使い始めた
date: 2020-02-24T17:53:05+09:00
draft: false
categories: ['til']
tags: ['github-actions', 'CI']
---

最近、仕事でGithubを使い始めた。

使い始めて便利だったものや、今後使ってみたいものをメモしていく

※ [awsome](https://github.com/sdras/awesome-actions) みればいいじゃんって言われたら存在意義がなくなるので目をつむってくださいｗ


言語に依存するものはいくらでもあるので今回はLint系に絞っていく.




- [snow-actions/eclint@v1.0.1](https://github.com/snow-actions/eclint)

これは何かと言うと EditorConfig に従っているかどうかをチェックする GithubAction.
例えば、チーム開発でWindowsとMacのメンバーが混在している状況では特に効果が高い.

自分は自宅ではWindowsがメインで仕事ではMacが多いのでとても助かっている
（普段使いのエディタならEditorConfig勝手に読み込んでくれるんだけど、コンフリクト解消時にVimとか使ってしまうと一気に改行文字が変わってしまう事故がある）

git-hook でいいいじゃんと思う人もいると思うが、ローカルで設定が要らないのは大事

- [WIP](https://github.com/wip/action)

WIPのものがマージされる事故が発生したので導入した。
あってはならないがあったのだ。

- [ReviewDog](https://github.com/reviewdog/reviewdog#github-actions)

PRにコメントしてくれる犬。
マージ止めるほどじゃないけど、Lintエラーしてほしい物に対して使っている。

人がやるとその人にヘイトがたまるので良くないが犬なら許してくれる（笑）

- [ssh-agent](https://github.com/webfactory/ssh-agent)

まだ使ってないけど、他のPrivate Repository参照したいとき使う事になりそう。


- [assignee-to-reviewer-action] (https://github.com/pullreminders/assignee-to-reviewer-action)

バイク小屋対策


- [lighthouse-action ] (https://github.com/jakejarvis/lighthouse-action)

実行するの忘れてるヤツを自動で動かしてくれる。文明の利器

---

ちなみにCircleCIのようにローカルで動かしてくれるものは無いらしい。