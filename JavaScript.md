# JavaScript基礎
## importとexport
```js script
//module.js
const funcB = () => {
  console.log("funcB output");
};
//ファイルに一つだけしか設定できない
export default funcB;

//まとめて後述してもいい
//export { funcB }
```
```js script
//main.js
//{}がなくてもいい。名前も違うのでもいい
import functionB, { hello, User } from "./module.js";
functionB();
```

## コールバック関数（引数に関数を入れる）
``` js script
function  print(fn){
  //引数を渡す
  const result = fun(2)
  console.log(result)
}
//初期値を設定することができる
function fn(number = 3){
  return number * 2;
}
```
```js script
//e = Eventという意味
btnEl.addEventListener('click',(e)=>{
  console.log(e.target);
  //<button>テキスト</button>
  console.log(e.target.textContent);
  //テキスト
})
```
## mapとfilter
```js script
const arry = [10, 20, 30, 40]
const newArry = []
for (let i = 0; i < arry.length; i++) {
    newArry.push(arry[i] * 2);
}
```
```js script
//上を書き換える
const newArry2 = arry.map(val => val * 2)

//iインデックス arry配列がそのままわたってくる
// const newArray = array.map((val,i,arry) =>{
//     console.log(val)
//     return val *3
// })
```
```js script
//50以上だけを追加する
//trueであれば追加される
const newArry3 = newArry2.filter(val=> val > 50)
```
```js script
//一つにまとめることができる
const newArry2 = arry.map(val => val * 2).filter(val=> val > 50)
```
## 分割代入




