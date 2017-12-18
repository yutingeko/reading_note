```
for(let i = 0; 1<10; 1++) {
  let i = 10;
  console.log(i);
}```

以作用域來看可以看作...

```
{
  let i = 0; 
  {
    let i = 10;
  }
}
```

> 宣告2個let不會出現reference error，因為不同作用域

> const不能reassign, const a = {}, "="不是等於的意思, 是assign之意


### JSX ###
* className, htmlFor
* ref, key attributes
* React component 命名一定要大寫 <Testlist />
* eventListener 使用 camelCase //onClick={} ...
* all elements could be self-closing
* style is "object" //如下範例

```
  <div style={{color: red}}></div>
```

> component 無法trigger event //沒有tirgger 或是 emit

> arrow function 使用時function自動bind.(this)

```
function() {
  ......
}.bind(this);

// -------------

() => {

}
```

react components 之間的溝通透過props, 尚未提及redux

