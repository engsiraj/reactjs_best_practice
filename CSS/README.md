## React CSS - How?

many ways to add css in react js.

- inline style
- styles through variable
- css file
- cdn links

each type will be covered here but all type are not recommended
we can achieve it through many ways.

1 - inline styles

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

2 - css through variable

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

3 - adding the style css file

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

4 - cdn links

you can use cdn links through html file `<head>` Tag as:

```js
<link href='https://cdn.jsdelivr.net/gh/engsiraj/
designsource@master/style.css' rel="stylesheet">
```
