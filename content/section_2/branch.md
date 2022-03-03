---
title: "ブランチについて理解しよう"
weight: 9
---

Git を使えるようになるにあたって、`branch`は最も重要な仕組みの 1 つです。

ブランチというのは、レポジトリの変更を分岐しながら残していくためのものです。

複数人が同時並行で開発する時、ある人の変更と自分の変更が被ったりしたらよく分からなくなってしまいます。

ブランチを分岐しながら開発していき、その後メインのブランチに反映させることで、そのような課題をなくすことができます。

<img src="/branch.png" width="500" />

(引用: https://cloudsmith.co.jp/blog/efficient/2020/08/1534208.html)

新しくリポジトリを作成した時、メインのリポジトリは`main`という名前になっています。ここから、とある作業を行いたい時は別のブランチに行って作業を行い、そのままリモートのリポジトリにそれを伝えます。

その後、あなたの作業が承認されたら、`main`にあなたの変更を反映する、といった流れで開発することで、一番メインの状態が安全に担保される形になります。

## コマンドを理解しよう

### checkout

別のブランチに移動するコマンドです。例えば、`main`ブランチにいる際に違う作業をするブランチに移動したかったら

```
> git checkout [ブランチ名]
```

とすることで移動できます。

ここから新しくブランチを作って移動したい、ということがあれば

```
> git checkout -b [新しいブランチ名]
```

としてください。

### merge

**ローカルリポジトリにて**、別のブランチの状態を今のブランチに反映させたい際には、今のブランチにいる状態で

```
> git merge [別ブランチ名]
```

とすれば反映されます。

### pull

リモートリポジトリのあるブランチの状態が誰かによって変更されて、自分のローカルリポジトリと状態が異なっている場合、

```
> git pull origin [ブランチ名]
```

とすることで、そのブランチの最新状態（リモートリポジトリの状態）を取り込むことができます。