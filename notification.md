# 通知

コールバック（ある条件が成就したら〜〜を呼び出してほしい）全般に関してのルール

フェッチ型の情報取得ではなくプッシュ型の情報通知を優先する。ほしいほうが聞きに行くのではなく、欲しい情報の条件を宣言しておき、条件に合致する情報を発信側が選択して送信する。


## 目的

受信者がほしい通知のみを受信者に届けたい。

関係のない通知が届くと、通知を見ても見ている人にとって利益がないので、無視するようになってしまう。


# 既読となる条件

受信者から送信者に既読フラグが返された瞬間


## 使用方針

期待する応答速度に応じてチャンネルを使い分ける。

送信側がチャンネルを分けられない場合は、即時反応を期待しないメッセージと見做す。

受信側の責任でがチャンネルを見分けられない場合は、すべて即時反応を期待するメッセージと見做す。


### 送信者側のチャンネルを区別する義務

即時応答が期待されていない受信者に即時応答を期待するチャンネルで情報を送信してはならない。


#### 具体例

即時反応を期待するメッセージで通知が来ても、労働契約で決まった稼働時間でなければ、応答する義務はない。


### 具体例

情報が通知されることで人を騒がせると思う場合には通知をオフにすることで受けて側で制御できるようにする. 受け手側で通知を制御できない場合発信者が発信を制限しなくてはならない。


## 受け取る態度

受信者の責任範囲に通知が飛ばなければ、送信者がメッセージを送達したとみなさない。

例

相手がインターネットに接続できない場合で、こちらはプッシュ通知サーバーへメッセージを配信済みの場合でなおかつ、プッシュ通知サーバーに接続する義務が受信者側にあるとすると、プッシュ通知サーバーへ配信した時点で発信者の送達義務は履行済みとする。

通知が飛んでいるかどうかは、モバイル版のプッシュ通知の受信設定が受信可能な最小範囲での設定であった場合に飛んでいるかどうかで判定する。

例

チャンネル内の全てのメッセージに関して通知が飛ぶ設定と、自分に対するメンションのみが通知される設定があった場合、自分に対するメンションのみが通知される設定が最小範囲での通知の受信設定である。したがって、チャンネル内で@を付けずに発言した場合、通知が届かない。したがってメッセージが伝達されたとみなさない。