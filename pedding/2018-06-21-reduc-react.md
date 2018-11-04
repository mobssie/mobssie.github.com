---
layout: post
title:  "redux와 react 같이 사용하는 방"
date:   2018-06-21 00:18:23 +0700
categories: [jquery]
---

리액트와 리덕스 같이 사용하기
시작하는법

```javascript
npm i -S redux react-redux
```
```javascript
import MembershipLeverType from '../enums/MembershipLeverType';
const ini
function membershiplevelReducer(state, action){
    return state;
}
```
```javascript
// index.js
import {createStore, CombineReducers} from 'redux';
import {provider} from 'react-redux';

const store = createStore(
    combineReducers({
    MembershipLeverReducer: membershipLevelReducer
    }),
    __REDUX_DEVTOOLS_EXTENSION__ && __REDEX_DEVTOOLS_EXTENSION__()
);

reactDom.render(
    <provider store={store}>
        <MembershipHome/>
    <provider/>
    ,
    document.getElementById('app');
);

```