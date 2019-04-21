<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [React学習まとめ](#react%E5%AD%A6%E7%BF%92%E3%81%BE%E3%81%A8%E3%82%81)
  - [Progageまとめ](#progage%E3%81%BE%E3%81%A8%E3%82%81)
    - [React始め方](#react%E5%A7%8B%E3%82%81%E6%96%B9)
    - [ボタン押下で表示する値を変える](#%E3%83%9C%E3%82%BF%E3%83%B3%E6%8A%BC%E4%B8%8B%E3%81%A7%E8%A1%A8%E7%A4%BA%E3%81%99%E3%82%8B%E5%80%A4%E3%82%92%E5%A4%89%E3%81%88%E3%82%8B)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# React学習まとめ
- progate

## Progageまとめ


### React始め方
- reactをimportする必要がある
- React.Componentを継承する必要がある
- renderメソッド内のreturn内にJSX形式で記述されたコードがブラウザに表示される
- JSX外で定義された変数はJSX内でブレースをつけて呼び出すと参照できる

```js
import React from 'react'

class App extends React.Component{
  render(){
    const name = '名前';
    return(
      <h1>{ name }</h1>
    )
  };
}

export default App;
```

### ボタン押下で表示する値を変える
- `<button onClick={()=>{ハンドラ}}`
- 処理に合わせて出力する値を変えたいときreactでは`state`というオブジェクトを`constructor`内で作成し、その値をイベントハンドラで変える
- `state`の値を変更する際は`this.setState()`を用いること
```js
constructor(props){
  super(props);
  this.state = { name: '太郎' };
}
render(){
  return{
    <div>
      <h1>こんにちは{this.state.name}さん</h1>
      <button onClick={()=>{this.setState({name: '太郎'})}}>太郎</button>
      <button onClick={()=>{this.setState({name:  '二郎'})}}>二郎</button>


    </div>
  }
}
```
