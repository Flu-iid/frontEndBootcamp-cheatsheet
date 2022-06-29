# Sass
.styles/scss/style.css  
.styles/css/
> sass --watch  styles\scss:styles\css

```scss
$color: #eee; // adding variable
```
## @mixin
```scss
@mixin name { //can have parameters as well
    color: red;
}

div {
    @include name;
}
```
> can have _mixin.scss and _variables.scss
```scss
@import "mixins"; // if its in _mixin.scss
@import "variables"; // if its in _variables.scss
```

```scss
@mixin name($color1, $color2) {
    color: $color1;
    background-color: $color2;
    @content;  // to add values in style.scss extra than mixin
}
```
```scss
@mixin query($width) {
    @media (max-width:$width) {
        @content;
    }
}
// for simpler media query
@if; // inside for different widths
```
```scss
@extend; //for copying other tags styles
```
## loops
```scss
@for $item from 1 through 5 {
    .container#{$item}{ //if item changed
        background-color: blue;
        height: 20px * $item;
    }
}
//
$item: 0;
@while ($item < 6) {
    .container#{$item}{
        background-color: blue;
        height: 20px * $item;
    }
    $item: $item + 1 
}
//
@each $element, $color in (container1: blue, container2: red, container3: green) {
    .#{$element}{
        color: $color;
    }
}

```
> colorlib.com

# JS

> jsbin.com

> remember js is dynamic so dont wory if sometimes doesnt make sense as others

>>>>>_** objects are pointers to memory**_








