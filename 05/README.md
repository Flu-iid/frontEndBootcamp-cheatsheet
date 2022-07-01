# ES6
`var => let, const`
> var can be accessed after (for) and (if), if it was declared in (for) and (if)
> let and const aren't declare tolerant
<hr>

```js
function fn() {
    code
    return result
}

const fn = () => {
    code
    return result
} 

function fn() { return result}

const fn = () => result //with arrow function with 1 argument u can put parentheses or not
```
> for array and Obj use `const`

```js
//spread / rest operator
const array = [1,2,3,4]
const clone = [...array] // clone array
const clone = [...array, "ali"] // to add extra item to cloned array

//Obj
//same as array


//
const profile = {name: "arsham", family:"mahdiun", age:26, score:9.75}

profile.name --> "arsham"

const {name, age} = profile //const names are important
const { name: a1, age: b1 } = profile;

// destructuring array
const array = ["arsham", "mahdiun", 26. 9.75]

const[esm,,,score] = array

// * .keys()
const arr = ['a', , 'c'];
const sparseKeys = Object.keys(arr);
const denseKeys = [...arr.keys()];
console.log(sparseKeys); // ['0', '2']
console.log(denseKeys);  // [0, 1, 2]


//* array 1 to 10
Array.from({length: 10}, (element, index) => ++index
Array.from(arrayLike, (element) => { /* ... */ } )
// array-like objects (objects with a length property and indexed elements).
```

# React ⠋
## Positive facts
> SPA Single Page Application
and more in video

> Virtual DOM
better rendering (1-99 + 100 example)

## Negative facts
> `<div if="root"> side content  </div>` SEO Problem

**to solve it**
vercel Co. (pronounces ver-sel) -> NEXT.js framework (renders codes on server-side)

ssr -> Server Side Rendering

ssg -> Server Side Generating (generate html)

## react setup for project

> `npx create-react-app app-name` (execute npm in local)
> `cd app-name`
> `npm start` (`run build` `test`)

## react files

### package.json
> version control of react project packages

> `npm i` when u have package.json to get react packages (node_modules)

9.9.9 major minor patch  
~ latest patch  
^ latest minor

>> Map()
```js
const a = new Map();
a.set(1, 2);
console.log(a);
```
> `"script"` is for `npm run`

### other meta
```html
<meta name="theme-color" content="#000000">
<!-- for browser tab color -->
```
### manifest link 
```html
<link rel="manifest" href="./manifest.json">
<!-- for PWA (Progressive Web App) -->
```
### (to test js)
> jEST MOCHA

### src/index.js
> is the main file

doesnt change much (except for redux routerDOM)

### src/App.js
> in App() is App component
> export default app; (to use in index.js)
_**JSX = javaScriptXML**_
> only 1 parent tag as return

## Functional component

```js
import React from "react";

const Mycomponent = () => {
    return <p>Mycomponent</p>;
};

export default Mycomponent;
// export {Mycomponent} ; --> import {Mycomponent as Mycomp}
```
> Components must start with upperCase

## Fragments

+ better for adding multiple elements
- but can't add className without proper element name

> `React.Fragment`
> empty fragment
<> </>

## Adding variables

```js
array = [1,2,3,4]  -> renders unstylable elements (later on do it with list rendering)

object = {name: "ali"} -> only values are showable
```

## List Rendering

```js
[1,2,3,4].map((item) => <span>{item}</span>;);
```
> react key
```js
[1,2,3,4].map((item) => <span key={}>{item}</span>;);
```
##
> React 18+ renders component 2 times

> on function calls in react different from HTML, function has to call without parenthesis -> {fn} or {() => fn()}

## State
> to tell react to change variables on events

```js
import React, {useState} from "react";

const [num, setNum] = useState(0);

const plus = () => {
    setNum((Last)=>Last+1);
};
```
> React renders after the function declaration ends (after })

```js
function App() {
    const [num, setNum] = useState(0);

    console.log("first" + num);

    const plus = ( => {
        setNum((Last) => Last +1);
        console.log("second" + num);
    });
    // React first does the function then stores the value in State. so second is 1 number behind first.
}
```
# Example

```js
function App() {
    const [num, setNum] = useState(0);

    const changeNumber = (x) => {
        setNum((Last) => Last + x);
    };

    return (
        <div className="App">
            <p>{num}</p>
            <button onClick={()=>changeNumber(+5)}>+5</button>
            <button onClick={()=>changeNumber(+10)}>+10</button>
            <button onClick={()=>changeNumber(-5)}>-5</button>
            <button onClick={()=>changeNumber(-10)}>-10</button>
        </div>
    );
}

export default App;
```
```js
function App() {
    const [num, setNum] = useState([0]);

    const addNumber = () => {
        setNum((Last) => [...Last, Last[Last.length - 1] + 1]);
    };

    return (
        <div className="App">
            <button onClick={addNumber}>add</button>
            <p>{num}</p>
        </div>
    );
}

export default App;
```
# CSS React
> if css is imported in one component, it will be global in all components. (unless you restrict it).

**react-motion**  
**swiper**

> React inline style -> style{{ color:"red" }}

## Restricted css
>test.**module**.css   
>`import style from ""`

## Dynamic style
> Solution 1
```js
style={{background-color: item%2 ? "red" : "blue"}}
```
>Solution 2
```js
className={item%2 ? "red" : "blue"}
```
# onChange event
```js
function App() {
    const [text, setText] = useState("");
    const [show, setShow] = useState("");

    return (
        <div className="App">
            <input
            value={text}
            type="text"
            onChange={(event) => setText(event.target.value)}>
            <button
            onClick={() => {
                setShow(text);
                setText("");
            }}>add</button>
            <p>{show}</p>
        </div>
    );
}
```
> **react motion**  
> **swiper**





