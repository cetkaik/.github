# 開発者向け情報

## 概要

cetkaik のアプリについての開発者向け情報を蓄積するためのドキュメントです。

# 構成図

[構成図](v1/architecture.md)のページを見てください。

# TODOと issue の管理

個別の repository に属さない cetkaik アプリ全体の TODO や issue、ロードマップは様々な場所で相談されていますが、大体を [hsjoihs](https://github.com/sozysozbot) が一人で書く体制で何年もやってきたせいで、あんまり上手く管理されていません

オープンで公開されているものとしては、cetkaik に限らないリポジトリだと[AIL-MO-LETI-CEP/issues](https://github.com/AIL-MO-LETI-CEP/issues/issues) に一応置いてありますが、[cerke_online_alpha/issues](https://github.com/jurliyuuri/cerke_online_alpha/issues) に委任して管理している部分が多いかなぁ。一応 [cetkaik_programming_issues/issues](https://github.com/cetkaik/cetkaik_programming_issues/issues) ってのも用意しておいたので、

- 「cerke_online およびそれをサポートするための TypeScript コード資産」に関しては [cerke_online_alpha/issues](https://github.com/jurliyuuri/cerke_online_alpha/issues)
- それ以外に関しては  [cetkaik_programming_issues/issues](https://github.com/cetkaik/cetkaik_programming_issues/issues) 

としてもらうといいのかなぁ。

# 備考

現在稼働中なのは V1 アプリ群です。

- そもそもフロントエンドの全てを生 DOM の操作で行ってしまっており、機能追加がコード負債の追加と同義になってしまっている（React への移行により強制的に解決させるか？ cf. [cerke_online_alpha#152](https://github.com/jurliyuuri/cerke_online_alpha/issues/152) ）
- 盤面の保持・更新がserverとclientで重複しており、 single source of trust になっていない（cf. [cerke_online_alpha#212](https://github.com/jurliyuuri/cerke_online_alpha/issues/212)）

の理由で、V2 アプリ群の開発を**行いたいなという夢が抱かれている**最中です。

机戦にまつわるコード資産はは、 2022 年 12 月現在、主に以下の 3 つに分けられます。

- cerke_online およびそれをサポートするための TypeScript コード資産（上述の「V1 アプリ群」がこれに相当）
- それ以外の小規模な Web サービスをサポートするための JavaScript コード資産 
- 高速に動くことで実用的な速度のゲーム AI を提供できることが期待される Rust コード資産

現状、これらの間の連携はそんなに上手くいっていません。
