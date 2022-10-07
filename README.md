# React JS Best Practices

making react js easier a bit with best practice.

- [requirement](#requirement)
  - [installation](#installation)
  - [jsx](#jsx)
  - [elements rendering](#elements-rendering)
- [styling](#styling)
  - [css](#css)
  - [styled components](#styled-components)
- [import and exports](#import-and-exports)
  - [components](#components)
  - [files and links ](#files-and-links)
  - [through array maping ](#through-maping-array)
- [destructuring](#destructuring)
  - [destructuring props](#destructuring-props)
- [tips and tricks](#tips-and-tricks)

## requirement

although react js is Javascript frontend libarary. there are some pre requirement for learning libarary like basics of `html`, `css`, `dom`,`es6`, `node` and `npm`.you don't need to master them all.

### installation

react js takes some time for installation so you can use [vite](https://vitejs.dev/guide/) instead of installing react. it will save your time and provide more features too.

```js
npm create vite@latest

```

### jsx

jsx is nothing just the combination of `javascript` and `xml`. react render the logic in jsx to show/load the elements.

```js
const name = "Josh Perez";
const element = <h1>Hello, {name}</h1>;
```

### elements rendering

we can render element/function or piece of javascript code any where in jsx using `{}`.

```js
const name = "Josh Perez";
const element = <h1>Hello, {name}</h1>;
```

## styling

react built to design interfaces and provide many ways to style its components.

### css

there are many ways to add css in react js.

- inline style
- styles through variable
- css file
- cdn links

each type will be covered here but all type are not recommended
we can achieve it through many ways.

### inline styles

we can add inline css to style element. it is not react recomended way of using style.

```js
return (
  <header>
    <h1
      style={{
        fontSize: "6rem",
        fontWeight: "600",
        marginBottom: "2rem",
      }}
    >
      todos
    </h1>
  </header>
);
```

### css through variable

we can add the css through variable.

```js
//storing in variable
const headerStyle = {
  padding: "20px 0",
  lineHeight: "1.5em",
}
//usage
<header style={headerStyle}>

```

### adding the style css file

we can add css file in react and use `className` instead of `class` as in css because `class` is reserve keyword for Javascript `classes`.

```js
import React from "react";
import ReactDOM from "react-dom";
import App from "./";

//stylesheet
import "./App.css";

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById("root")
);
```

### cdn links

you can use cdn links through html file `<head>` Tag as:

```js
<link href='https://cdn.jsdelivr.net/gh/engsiraj/
designsource@master/style.css' rel="stylesheet">
```

### styled components

styled components will be there in next few updates(would not take much time).

## import and exports

imports and export are JavaScript concept its came in use in es6 update.

### components

we have to create file `index.js/ts/jsx` to add exports in components folder.

```js
//export your component as index.js/ts/jsx file.

export { default as ChannelCard } from "./ChannelCard";
export { default as VideoCard } from "./VideoCard";
export { default as ChannelDetail } from "./ChannelDetail";
export { default as Feed } from "./Feed";

//import from your component as index.js/ts/jsx file.

import { ChannelCard, VideoCard, ChannelDetail, Feed } from "./";
```

### files and links

we have to create file `utils/constant.js/ts/jsx` to export components.

```js
// mui components
import MusicNoteIcon from "@mui/icons-material/MusicNote";
import HomeIcon from "@mui/icons-material/Home";
import CodeIcon from "@mui/icons-material/Code";
import OndemandVideoIcon from "@mui/icons-material/OndemandVideo";
import SportsEsportsIcon from "@mui/icons-material/SportsEsports";
//logo.png link
export const logo = "https://i.ibb.co/s9Qys2j/logo.png";
//react icons
export const categories = [
  { name: "New", icon: <HomeIcon /> },
  { name: "JS Mastery", icon: <CodeIcon /> },
  { name: "Coding", icon: <CodeIcon /> },
  { name: "ReactJS", icon: <CodeIcon /> },
  { name: "NextJS", icon: <CodeIcon /> },
];
// links url
export const demoThumbnailUrl = "https://i.ibb.co/G2L2Gwp/API-Course.png";
export const demoChannelUrl = "/channel/UCmXmlB4-HJytD7wek0Uo97A";
export const demoVideoUrl = "/video/GDa8kZLNhJ4";

//import from your component as utils/constant.js/ts/jsx file.

import {
  demoThumbnailUrl,
  demoVideoUrl,
  demoVideoTitle,
  demoChannelUrl,
  demoChannelTitle,
} from "../utils/constant";
```

### maping through array

```js
// importing images
import post1 from "assets/post1.png";
import post2 from "assets/post2.png";
import post3 from "assets/post3.png";
import post4 from "assets/post4.png";
import post5 from "assets/post5.png";
import post6 from "assets/post6.png";
// adding to the array
const posts = [post1,post2,post3,post4,post5,post6,];
// maping array in the  div
posts.map((post, index) => <div key={`post-${index}`} src={post} />

```

## destructuring

### destructuring props

there are many ways to destructure props in JavaScript. we will explore few of them.

1 - props without destructuring.

```js
//Props without destructuring - function recieve props as parameter.
function Product(props) {
  return (
    <div>
      <img src={props.img} alt="products" />
      <h4>{props.name}</h4>
      <p>{props.description}</p>
      <h4>{props.price}</h4>
    </div>
  );
}
export default Product;
```

2 - function recieve props as parameter

```js
function Product = (props) => {
//destructuring props in the body of function.
    const { img, name, desc, price} = props;
    return (
      <div>
      // props usage.
      <img src={img} alt="products"/>
        <h4>{name}</h4>
        <p>{description}</p>
        <h4>{price}</h4>
      </div>
    );
}
export default Product
```

3 - function recieve props to destructure

```javascript
//destructuring in function's parameter
function Product = ({ img, name, desc, price}) => {
    return (
      <div>
      // props usage.
      <img src={img} alt="products" />
        <h4>{name}</h4>
        <p>{description}</p>
        <h4>{price}</h4>
      </div>
    );
}
export default Product
```

usage of props from product functuion

```js
<Product
img="https://ng.jumia.is/unsafe/fit-in/300x300/filters:fill(white)/product/82/6142201/1.jpg?2933"
name="Cyxus"
desc="Non-Slip Fitness Leisure Running Sneakers"
price="$29"
/>
<Product
img="https://ng.jumia.is/unsafe/fit-in/300x300/filters:fill(white)/product/01/241417/1.jpg?6747"
name="Vitike"
desc="Latest Men Sneakers -Black"
price="$100"
/>
<Product
img="https://ng.jumia.is/unsafe/fit-in/300x300/filters:fill(white)/product/06/4410121/1.jpg?4437"
name="Aomei"
desc="Men's Trend Casual Sports Shoe"
price="$40"
/>
```

### pro tips

- create a good folder-structure.
- keep your key prop unique across the whole app.
- don't use inline-styles.
- use functional components (like arrow-functions).
- maintain a proper import structure (third-party imports first --> internal imports below).
- Maintain a structured import order.
- format your code before committing.

### author

errors are expected if you find one report it to the [author](https://twitter.com/engsiraj_).
