## 創成期

2010年3月　ひっそりと産声をあげる

- 非エンジニアである弊社代表が一人で WordPress をレンタルサーバに設置しサイトを開設
- 適当な無料の WordPress テーマ

---

## この頃のシステム構成

- レンタルサーバ 2500円/月
    - PHP(CGIモード)
- WordPress + いくつかのプラグイン 
- non programing

![wordpress](img/wordpress-logo-stacked-rgb.png)

---

## ブログ期

![blog-site](img/screen.png)

---

## ブログ期

- ユーザが求めているであろう情報を投稿していった。
- 次第にユーザが増えてきた

---

## ちょっとデザインをととのえる

![early-site-2](img/early-site-2.png)

---

# 会員登録できるようにしよう

---

## 最初の壁 

エンジニアがいない!

---

## この頃

- エンジニア 0.2名 / 他でフルタイム勤務
- デザイナー 0.5名 / 岐阜県からリモート

---

## 2010年9月　会員制立ち上げ期

- 開発期間1ヶ月
<!-- .element: class="fragment" data-fragment-index="1" -->

- メインプログラマは、昨日まで Web デザイナー
<!-- .element: class="fragment" data-fragment-index="2" -->

- セキュリティ怖い
<!-- .element: class="fragment" data-fragment-index="3" -->

- ユーザ管理/認証まわりは、WordPress のユーザ管理機構にのっかることに
<!-- .element: class="fragment" data-fragment-index="4" -->

---

## 手法

- WordPress 固定ページを作成し、各ページにテンプレートファイルを関連付け
- テンプレートファイルに、ベタりとPHPで記述
    - (例) mypage.php
- 使いまわす関数は function.php に

---

## レンタルサーバ プラン変更

- 会員登録機能/ログインのため、独自SSL が必要に
- 2500円/月 -> 4500円/月

---

## なんとか完成し、リリース！

- 順調に登録されているのをみてほっと胸をなでおろす
- 会員登録するとできること
<!-- .element: class="fragment" data-fragment-index="1" -->

    - マイページだけ
<!-- .element: class="fragment" data-fragment-index="2" -->

- 日々増えていく会員登録
<!-- .element: class="fragment" data-fragment-index="3" -->

- これまでのリピーターからの期待は高かった！
<!-- .element: class="fragment" data-fragment-index="4" -->

- ユーザに使ってもらえるものをはやく提供しなければ
<!-- .element: class="fragment" data-fragment-index="5" -->

---

## この頃の開発環境

- 開発環境: レンタルサーバ上に staging 環境
<!-- .element: class="fragment" data-fragment-index="1" -->

    - http://xxx.xxx.jp/staging/
<!-- .element: class="fragment" data-fragment-index="2" -->

- デプロイ
<!-- .element: class="fragment" data-fragment-index="3" -->

    - SCP でファイルアップロード
<!-- .element: class="fragment" data-fragment-index="4" -->

- テスト
<!-- .element: class="fragment" data-fragment-index="5" -->

    - 目視で動作かくにん！よかった
<!-- .element: class="fragment" data-fragment-index="6" -->

- ソースコード管理
<!-- .element: class="fragment" data-fragment-index="7" -->

    - (お察しください)
<!-- .element: class="fragment" data-fragment-index="8" -->

- DBの日次バックアップだけはとっていた
<!-- .element: class="fragment" data-fragment-index="9" -->

---

## 方針

サービスが当たるかどうかもわからない。

- アプリケーション
    - 動作する機能をとにかく実装、リリースしていく
- インフラ
    - 管理対象を必要最低限に保ち、極力増やさない
    - 最悪を避ける

---

# ユーザを集め、順調にPVが増え、レンタルサーバではパフォーマンスが低下してきた

---

## 2011年1月　共有レンタルサーバからVPS へ移行

- VPS (メモリ512G) へ移行
- nginx + php-fpm

---

# WordPress には詳しくなったが...

---

# WordPress のカスタマイズを続けることに限界を感じ始める

---

# デザインとロジックが分離されていない

---

# MVCフレームワークを使いたい

---

## 2011年3月

- まずは、社内向けの管理画面で CakePHP を試験導入してみる
- いくつかの機能を実装してみて、感触をつかむ

