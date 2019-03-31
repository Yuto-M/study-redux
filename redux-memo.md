- action
    - stateを変更するにはactionを発行する
    - actionのtypeを設定する定数を別ファイルに定義するとプログラムの見通しがよくなる。
    　ただ小さいプロジェクトの場合は、別ファイルに分けて定義しない方が簡単かもしれない。
- reducer
    - actionとstateを受けとり、新しいstateを発行する
    - 大きなreducerは分割して小さなreducerにまとめる
    - 分割したreducerはcombineReducers()を使って一つのreducerにまとめる
https://redux.js.org/introduction/prior-art
    - 初回時のstateをreduxが要求する際はstateがundefinedなので、用意した初期状態のstateを返却するようにする
- reactと連携させる場合
    - react側では、受け取ったデータの表示のみを行うようにする
    - `prop-types`はreactコンポーネントのpropsのvalidationチェック機能
https://qiita.com/sfatsfc/items/d32b28ccd10e04bc87ae
    - 最初にpresentational componentを作る。その後、container componentを作る

- 補足
    - stateを更新する際にimmutableなstateの作り方がわからないときは、immutable.jsのようなライブラリを使用するのもあり
```
https://immutable-js.github.io/immutable-js/
```