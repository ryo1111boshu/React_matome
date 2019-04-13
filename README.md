# React学習まとめ
- progate

4/13

reactをimportする必要がある
React.Componentを継承する必要がある
renderメソッド内のreturn内にJSX形式で記述されたコードがブラウザに表示される
JSX外で定義された変数はJSX内でブレースをつけて呼び出すと参照できる

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


---
