五感に訴える対象を短く表現するデータをシンボルとする。

それを適切に決める方針

命名　音楽　触覚　型　公準　など


## 目的

検索しやすく

短い情報で見つけたい人に解凍後の情報を正確に伝えられるように。


## 用語


### シンボル同士の意味の距離

静止視力（ランドルト環による測定）が弱い人でもわかるぐらい、シンボルとシンボルの定義を離す

シンボル同士の意味が接近しすぎると、シンボルへの認識力が弱い人はぼやけて違いが認識できない。


## 参照しているスコープとコンテキスト

俗に言う文脈

参照するスコープが小さい場合（専門的な話題）は、同じシンボルでも意味を分割して２つの単語として扱いたい場合もある。

逆に参照しているスコープが大きければ（世間話）、複数のシンボルを一つの意味として扱いたくなる。


## 情報の二重化を避ける

意味の重複を避ける

シンボルを設定する場所

格納するシンボルの種類が決められている


## 一意性

離れたところから認識しやすいものほどよい

できるだけ特定しやすいように

間違って特定したとしても、被害が少なくなるような間違い方になるシンボルが良い

一意性をもたせるために従うべき最低限のルールが識別子の付け方である。

[RFC 8820 - URI Design and Ownership](https://datatracker.ietf.org/doc/html/rfc8820)

RFCのURIの標準に従うべき。

[A Persistent Identifier (PID) policy for the European Open Science Cloud (EOSC) - Publications Office of the EU](https://op.europa.eu/en/publication-detail/-/publication/35c5ca10-1417-11eb-b57e-01aa75ed71a1/language-en)

EUの基準もあります。


## 物理名

機械に認識させて絶対的な一意性　一貫性を確保するためのシンボル

不変性を優先する

論理名

物理名と紐付いていれば可変

人間の感覚に近いシンボル


## マトリクス

名前以外の列に保存するべき情報を名前に載せない　情報の二重化の禁止原則より


## 木構造　ディレクトリのシンボル


### ディレクトリに情報をもたせるべきか？

背景知識が同一である人間が見る場合はディレクトリ（親が一つの樹形の情報構成）自体に情報をもたせる。

そうでない場合は、ファイル名に情報をもたせる。


### ディレクトリに情報を持たせない場合

ディレクトリの間のファイル移動が頻繁にある。

\
ディレクトリ名に情報があっても、ファイル名にそれを重複して記載する。

ファイル名が３０文字を超える場合は、ルートノード側のディレクトリ名と重複する情報から削る。


### ディレクトリ命名規則

ディレクトリはそこまで考えなくていい。　検索さえできれば問題ありません。


## ドメインモデルとの一致

ドメイン駆動設計で全て動く \
ユビキタス言語を使え


### 相対概念をできるだけ使うな



* 最終
* 最新

他のファイルによって変化する。相対概念はソート列によって実現。

相対概念は検索の条件として使う


# 個別ルール


### ファイル命名規則

作成日時や最終更新日時など、ファイルシステム自身がファイル名以外の情報に保存する要素はファイル名に含めない。

バージョン名はファイル名に含めずファイル管理ソフトのバージョン管理機能のみを使う。 \
ファイル名をソートに利用しない。ソート機能は別列で行う。関係性データベースで扱うものとして設計する。


## バージョニング

[https://semver.org/lang/ja/](https://semver.org/lang/ja/)
