# switch case

+ switch === case

# for loop

`break;`   
`continue;`

# method and property

+ they are object values

```js
var myObject = {show:function(){
    console.log("show")
}}

myObject.show()
```


# arrayMethod
```js
.pop()
.shift()
// return item

.push(n)
.unshift(n)
// return new **length** 

.reverse() //return new array


.splice(start, length) // drops from index start to the appointed length
//return new array
```
> changing array
<hr>

```js
.slice(index_n,index_m) // drops from index_n to  the end of index_m-1
//return new array

.concat() // concatenating arrays 

.indexOf(n) // if nothing --> -1  

.includes(n) // boolean return

.join(seperater) // obj -->str

```
> doesn't change original array
<hr>

## callback methods
```js
.sort() //return sorted array
//**remember still sorts old array**
// sorts numbers like char (1000,2)
/*
array.sort(myfn)
function myfn(x,y){
    return y-x  --> from big to small
    return x-y  --> from small to big
}
*/

.forEach(function(item, index, array){
     
})
// nop return

numbers.forEach(function(item,idex,array){
    number[index] = item * 2
})
//


.map()
// return new array
// good way to copy new array


.filter()
// return new array
// in function return needs bool


.reduce()

var num=numbers.reduce(function(x,y){
    return x+y
}, 0) >    0 1 2 3 4 5 6 7 8 .... if y is 1
```
### some examples
```
var numbers = [3, 4 ,21, 32, 35, 49, 76, 90, 140, 12, 64, 700, 20, 19]

var sum = numbers.reduce(function(x,y){
    if (y%7==0){
    return x+y
    }else {
        return x
    }
}, 0)

console.log(sum)
```
> needs return. without return sums with undefined and returns NaN

# ternary

> always has return

```js
var result = x>10 ? "x>10" : "x<10"

var result = x>10 ? "x>10" : x>5 ? "x>5" : "x,5";

var result = x>10 && "x>10" // no return (cause && compares two bool)
```

```
for (key in object) {

}
```
> for objects loops

<hr>

## string formatting && template litteral
```
`my ${age}`
```

> in react ES6 we use ternary instead of if and map/filter for loops



