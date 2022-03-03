---
title: "実際に開発してみよう"
weight: 11
---

何となく基礎についてわかってきたところで、実際に世の中に公開されているサービスを修正して git で反映させてみましょう。

皆さんが修正するのは、この資料です。
URL: https://github.com/mikan-project/git_study

この資料は不完全で、資料の充実をさせていくだけでなく、typo ミスなど、改善点が多くあります。

---

何かプロジェクトを修正して反映させようとすると、以下がよくある流れだと思います。

1. issue を発行する
   - どんなバグがあるか、あるいはどんな課題を解決したいのか、どんな機能を追加したいのか、など（粒度はチームによって様々だし、いろんな使い方があります。）
2. ローカルが最新状態であることを確認して、ブランチを切る
   - [これ](/section_2/branch/#checkout)です
   - ブランチを新しく生やすことを「ブランチを切る」と言ったりします。命名については後ほど。とりあえずなんでもいいと思います。
3. いろいろ修正する。
4. commit -> push する。
5. pull request を出す。
   - リモートリポジトリにて、とあるブランチの変更をあるブランチに反映させたい時は、pull request を送ります。
6. pull request が良ければマージ（反映）