# React JS Best Practices

making react js easier with best practice at one place. 


- [first requirement](#first-requirement)
- [installation](#installation)
- [tips and tricks](#tips-and-tricks)
- [import and exports components](#import-and-exports-components)
- [import and exports files and links ](#import-and-exports-files-and-links)
- [import and exports maping through array ](#import-and-exports-maping-through-array)
- [destructuring props in react](#destructuring-props-in-react)


## first requirement

Although react js is Javascript based frontend libarary you have to learn the logic and structure of js. but there are some pre requirement for the libarary to learn these are includes only basics of `html`, `css`, `dom`,`es6`, `node` and `npm`. although these are requirements you should have basic understanding of them and not to be master them all at once.

## installation 

Although react js need some time for installation so you can use [vite](https://vitejs.dev/guide/) instead of installing react directly. it will save lot of your time and provide more feature along with.

```js
npm create vite@latest

```
## tips and tricks

- Create a good folder-structure
- Keep your key prop unique across your whole app
- don't use inline-styles
- use functional components (like arrow-functions)
- maintain a proper import structure (third-party imports first --> internal imports below)
- Maintain a structured import order
- format your code before committing

## import and exports components

First we will create file for adding what we want to export `index.js/ts/jsx` in components folder.

```javascript
//export your component as index.js/ts/jsx file.

export { default as ChannelCard } from "./ChannelCard";
export { default as VideoCard } from "./VideoCard";
export { default as ChannelDetail } from "./ChannelDetail";
export { default as Feed } from "./Feed";

//import from your component as index.js/ts/jsx file.

import { ChannelCard, VideoCard, ChannelDetail, Feed } from "./";
```

## import and exports files and links

First we will create file for adding what we want to export `utils/contant.js/ts/jsx` for components.

```javascript
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

## import and exports maping through array

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

## destructuring props in react

there are many ways for destructuring props in react js we will explore only few usefull methods thats easy to understand/deal with.

```javascript

//Props without destructuring - function recieve props as parameter 

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

```
1 - destructuring within the body of the function - function recieve props as parameter

```javascript

export default Product

//Destructuring within the body of the function - function recieve props as parameter

function Product = (props) => {
//First Step: Destructuring within the body of the function
    const { img, name, desc, price} = props;
    return (
      <div>
      <img src={img} alt="products" />
        <h4>{name}</h4>
        <p>{description}</p>
        <h4>{price}</h4>
      </div>
    );
}

export default Product
```
2 - destructuring within function's parameter

```javascript
//First Step: Destructuring within function's parameter
function Product = ({ img, name, desc, price}) => {
    return (
      <div>
      <img src={img} alt="products" />
        <h4>{name}</h4>
        <p>{description}</p>
        <h4>{price}</h4>
      </div>
    );
}

export default Product
```
using props values from product functuion

```javascript
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






## author

errors are expected if you find one report it to the [author](https://twitter.com/engsiraj_).