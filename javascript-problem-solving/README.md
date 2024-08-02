<div align="center">
  <img height="60" src="https://img.icons8.com/color/344/javascript.png">
  <h1>JavaScript Questions : Problem Solving</h1>
</div>


<p align="center">
From basic to advanced: test how well you can write JavaScript, refresh your knowledge a bit or prepare for your coding interview!</p>

---

###### 1. Can you block the main thread for 3 seconds ?

<details><summary><b>Solution</b></summary>
<p>

```javascript
console.log("start")

function blockMainThread(ms){
    const start = Date.now();
    while(Date.now() - start < ms){

    }
}

blockMainThread(3000);

console.log("end")
```
</p>
</details>

---

###### 2. Create a polyfill for flat().

<details><summary><b>Solution</b></summary>
<p>

```javascript
Array.prototype.flat2 = function (){
    let fillArr = []
    for(let el of this){
        if(Array.isArray(el)){
            for(let e of el){
                fillArr.push(e)
            }
        }else{
            fillArr.push(el)
        }
    }
    return fillArr
}
```
</p>
</details>

---