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

const {name, age} = profile //const names arent important

//

const array = ["arsham", "mahdiun", 26. 9.75]

const[esm,,,score] = array //check later on
```

# React
## Positive facts
> SPA Single Page Application
and more in video

## Negative facts
`<div if="root"> side content  </div>`

vercel -> nextJS

ssr -> Server Side Rendering

ssg -> Server Side Generating

⠋

check react npm global install

check Map() for ES6

meta theme color


PWA

jEST MOCHA

redux routerdom


JSX

9.9.9 major minor patch









