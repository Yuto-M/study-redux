# study-redux
# 概要
Redux勉強用

## Goal
- reduxのtutorialをやる

## tips
- action
    - stateを変更するにはactionを発行する
- reducer
    - actionとstateを受けとり、新しいstateを発行する
    - 大きなreducerは分割して小さなreducerにまとめる
    - 分割したreducerはcombineReducers()を使って一つのreducerにまとめる
https://redux.js.org/introduction/prior-art
