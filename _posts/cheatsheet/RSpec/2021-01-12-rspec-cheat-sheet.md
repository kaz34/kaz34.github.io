---
layout: post
title:  "RSpecのエラー解決"
categories: cheatsheet
permalink: /rspec-bookmarks
excerpt_separator: <!--more-->
tags: rspec
---

![image here](/assets/img/thumbnail/13.jpeg)

<!--more-->

## Migrations are pending. To resolve this issue, run: bin/rails db:migrate RAILS_ENV=testYou have 27 pending migrations:

```
rails db:migrate:reset
```

↓

## `require': cannot load such file — rails_helper (LoadError)

原因は、このエラーに限らず、そもそもテスト用のDBが作られていなかった。

<br>

```
rails db:test:prepare
```

チートシート
rspecのメソッドをmodule化するファイルを作成する方法
https://breakthrough-tech.yuta-u.com/rspec/how-to-make-spec-support/


**click_linkがiconの場合。**

通常は、

```ruby
click_link "ログイン"
```

iconの場合。

view

```ruby
<button type="button" class="btn btn-light">
 <%= link_to logout_path,　title: "logout", class: "nav-link active text-black", method: :delete do %>
 <i class="fas fa-sign-out-alt"></i>
 <% end %>
 </button>
```

rspec

```ruby
click_link "logout"#titleを追加。
```

