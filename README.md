# study-redux
# 概要
Redux勉強用

## Goal
- reduxのtutorialをやる

## tips
- action
    - stateを変更するにはactionを発行する
    - actionは必ずそのactionが何のアクションなのかを示すtypeプロパティを持つ
      - typeは通常文字列定数で、タイプのみを定義した別モジュールにすることも多い。
https://redux.js.org/basics/actions
    - Action Creatorsっていうactionを作成する関数を用意することも多い
    - 更にaction creatorsとdispatch()を紐付けるbound action creatorっていう関数を作ることも多い
      - bound action creatorを作ることにより、変更があった際にbound action creatorを呼んでactionが作られそれが、dispatchされるという流れが完成する
- reducer
    - actionとstateを受けとり、新しいstateを発行するのがreducer
    - 大きなreducerは分割して小さなreducerにまとめる
    - 分割したreducerはcombineReducers()を使って一つのreducerにまとめる
https://redux.js.org/introduction/prior-art
    - 作成しようとしているアプリ内で必要なstateの構造を検討してからreducerの検討に入る
    - reducerはpure functionでなければならない
      - pure functionとは
https://medium.freecodecamp.org/what-is-a-pure-function-in-javascript-acb887375dfe
    - 未定義のaction.typeが送られてきたらstateをそのまま返す
- store
  - 1アプリケーションにstoreは必ず1つのみ
- reactとreduxの併用
  - presentational componentとcontainer componentの違いを理解する