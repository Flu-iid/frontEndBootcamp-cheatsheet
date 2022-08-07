# Prime number 1-1000 solution
## solution-1
```js
var counter = 0
number.forEach(function(item)) {
    for (i=1; i<=item; i++) {
        if (item==1){
            continue;
        }
        if (item%i) {
            counter++;
        }
    }
    if (counter==2){
        primes.push(item);
        counter=0;
    }
    counter=0;
```
## solution-2
```js
var counter = 0
number.forEach(function(item)) {
    for (i=2; i<=item; i++) {
        if (item%i==0){
         break;
        }
    }
    if (item==i){
        primes.push(item);
    }
}
```
## solution-3
```js
//solution-3
var primeNumbers=numbers.filter(function(item){
    if(item==1){
        return false;
    }
    for (i=2; i<item;i++){
        if(item%i==0){
            return false
        }
    }
    return true
})

//solution-3.1
var primeNumbers=numbers.filter(function(item){
    for (i=2; i<item;i++){
        if(item%i==0){
            return false
        }
    }
    return item>1
})
```
## solution-4 Sieve of Eratosthenes
```js
var eratosthenes = function(n) {
    var array = [], upperLimit = Math.sqrt(n), output = [];
    for (var i = 0; i<n; i++){
        array.push(true);
    }

    for (var i = 2; i<= upperLimit; i++) {
        if (array[i]) {
            for (var j = i * i; j < n; j+=i){
                array[j] = false;
            }
        }
    }

    for (var i = 2; i < n; i++) {
        if (array[i]) {
            output.push(i);
        }
    }
    return output;
};

```
# ternary nested conditions
> think ternary from inside conditions first
```js
if(number > 15){
    if(number< 35){
        "a"
    }else if(number > 35){
        "b"
    }
}else if (number < 15){
    "c"
}

number > 15 ?
(number < 35 ? "a"
:number > 35 && "b")
:number < 10 && "c"

```
# Flag
```js
var flag;
var number = 15;

if (number%2==0) {
    flag=true;
}else{
    flag=false;
}

if (flag){
    "a"
}else{
    "b"
}

```
> used a lot for loading screens

# Obj properties and methods
```js
Math.round() // 0.5 => 1
.ceil()
.floor()
.trunc() => return int
.sign() // -1 0 1

.pow()
.sqrt()
.abs()
.min() .max() // u can use "spread / rest" for arrays
//.min(...[1,2,3,4,5])

.random()
```
```js
str.slice(start, end)
.substring(start, end) // if start end are (< 0) they will be consider 0
.substr(start, length)

.replace() //only first match
(/aaaa/i) //insensitive
(/aaaa/g)  //global

.toUpperCase()
.toLowerCase()

.concat(seperator, "string") //concatenating strings

.trim() //removing space

.padStart(n, "x")
.padEnd()

.charAt(index) 
.charCodeAt(index) //ascii for H is 72
//UTF-16 for H is U+0048

```
>`typeof` is an operator
## turn str to num
```js
Number() //turn to number

parsFloat()
parsInt() //returns the number if first index is number
//"3.2fdkfdfdfd" => 

+"32" //unary operator
```
## turn num to str
```js
String()
242+""
(234).toString() //needs to be in parentheses or be var
.toFixed(x)  //x can be used to add decimal value
```
## turn array to str
```js
.join()
.toString()
JSON.stringify() //turn obj to str
```
## turn obj to array
```js
v = {}
Object.keys(v) //keys
Object.values(v) //values
Object.enteries(v) //puts each key,value into an array and all in obj
```

## [Date()](https://www.w3schools.com/js/js_dates.asp)

## [REGEX](https://www.w3schools.com/js/js_regexp.asp)

# while and do while

# loop on strings for search
```js
str.indexOf(smallStr, n) // can have second parameter of n declares which index start searching from

str.search() //can accept regex value
str.include() //return bool
str.startsWith() //return bool
str.endsWith() //return bool

```
[.match()]()
[.find()]()

# Script in html
> `<noscript></noscript>` for scripts in restricted mode browser

```js
var text = document.getElementById("myText")
console.log(text) => p#myText
console.log(text.textContent)

.querySelector("#myText")
.querySelector("p")


screen //screen details
navigator //

.style.color // for readying style from document / html

.innerText //only includes and shows text
.innerHTML //can include tags and show them

const element = document.querySelector('.element')
const style = getComputedStyle(element)//get computed style
```
> [Adruino IoT](https://create.arduino.cc/projecthub/products/arduino-iot-cloud)

## `setInterval()`
```js
var text = document.querySelector(".show");

var sec = 0;
var min = 0;
var hour = 0;
var flag = true;
var time;
function Start() {
    if (flag) {
        time = setInterval(function () {
            sec++;
            if (sec == 60) {
                sec = 0;
                min++;
            }
            if (min == 60) {
                min = 0;
                hour++;
            }
            if (hour == 24) {
                sec = 0;
                min = 0;
                hour = 0;
            }
            text.textContent = `${hour < 10 ? "0" + hour : hour
            }:${min < 10 ? "0" + min : min
            }:${sec < 10 ? "0" + sec : sec}`;
        }, 200);
    }
}

function Pause() {
    clearInterval(time);
}

function Reset() {
    clearInterval(time);
    sec = 0;
    min = 0;
    hour = 0;
}
```
## `setTimeout()`
```js
function change() {
    setTimeout(function () {
        text.textContent = "change";
    }, 5000)
}
```

# AJAX => `async javascript xml`
> `xmlHTTPrequest` old requests
> `fetch()` (form of `Promise`)
>> 500 server | 400 | 200 success
>> GET POST PUT DELETE
```js
.then() // if successful
.catch() // error
```
>`fetch` gets executed last of all functions
> [jsonplaceholder]()

```js
function getData() {
    fetch("")
    .then(function (response) {
        return response.json();
    })
    .then(function (json) {
        console.log(json);
        text.textContent = json.title;
    })
    .try()
    .catch()
    // later on in Axios
}
```
> [openweather]()








