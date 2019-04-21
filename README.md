# React学習まとめ
- progate

## Progageまとめ

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

## ボタン押下で表示する値を変える
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
