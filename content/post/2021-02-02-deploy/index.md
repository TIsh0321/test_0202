---
title: Deploy
author: TomokiIshikawa
date: '2021-02-02'
slug: deploy
categories: []
tags: []
---

##Deployの方法

Blogdownの公式Documentationでは
- github
- Netlify
の２種類の方法を提案しているが、[Netlify](https://app.netlify.com) を使用する方法を推奨している。


0. `config.TOML`(私の場合は何故かTOMLではYAMLファイルになっている)の`baseURL`にgithubのレポジトリを入力
**初期設定で忘れそうなので、忘れないように**

```{Rmarkdown}
1. blogdown::new_post() で記事を書く。/content/post/ディレクトリに格納されている。
2. blogdown::build_site() を実行
3. blogdown::serve_site() を実行
4. GitでCommitしてPushする
5. Netlifyにログインし、”new site from git”から設定を行う
(URLは無料だと設定できない)
```

