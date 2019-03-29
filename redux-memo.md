- action
    - stateを変更するにはactionを発行する
- reducer
    - actionとstateを受けとり、新しいstateを発行する
    - 大きなreducerは分割して小さなreducerにまとめる
    - 分割したreducerはcombineReducers()を使って一つのreducerにまとめる
https://redux.js.org/introduction/prior-art
- reactと連携させる場合
    - react側では、受け取ったデータの表示のみを行うようにする
    - `prop-types`はreactコンポーネントのpropsのvalidationチェック機能
https://qiita.com/sfatsfc/items/d32b28ccd10e04bc87ae
    - 最初にpresentational componentを作る。その後、container componentを作る