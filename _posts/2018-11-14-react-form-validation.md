---
layout: post
title:  "React 폼(Form) 유효성 검사 하기"
date:   2018-11-14 00:18:23 +0700
categories: [React, Validation]
---
<br/><br/><br/><br/>

React는 선언형이기때문에 입력이 동적으로 이루어져야 한다.
뷰 상태와 동기화 되어야 한다.  
```javascript
handleChange(event){
    this.setState({title: event.target.value})
}
render(){
    return <input type="text" name="title" value={this.state.title} onChange = {this.handleChange.bind(this)}
}
```
<br/>
`입력 > 이벤트핸들러감지(event.tartget.value > 상태에 새로운값 저장 > 뷰갱신`<br/><br/>
**React에서 폼과 이벤트 정의**<br/>
- onChange : 폼의 입력 요소에 변경이 생기면 발생<br/>
- onInput : < textarea >< input > 요소의 값이 변경될 때 발생 (React 팀은 이 이벤트 사용 X)<br/>
- onSubmit : 폼 제출시 발생<br/>
<br/><br/>
```javascript
const Form = ({value, onChange, onCreate, onKeyPress}) => {
  return (
    <div className="form">
      <input value={value} onChange={onChange} onKeyPress={onKeyPress}/>
      <div className="create-button" onClick={onCreate}>
        추가
      </div>
    </div>
  );
};
```
이 컴포넌트는 총 4가지의 **props** 를 받아옵니다.<br/><br/>

**value**: 인풋의 내용<br/>
**onCreate**: 버튼이 클릭 될 때 실행 될 함수<br/>
**onChange**: 인풋 내용이 변경 될 때 실행되는 함수<br/>
**onKeyPress**: 인풋에서 키를 입력 할 때 실행되는 함수. 이 함수는 나중에 Enter 가 눌렸을 때 onCreate 를 한 것과 동일한 작업을 하기 위해서 사용합니다.<br/><br/><br/>



** 참고 사이트 : https://yazzya.blog.me/221362860933
<br/><br/><br/>