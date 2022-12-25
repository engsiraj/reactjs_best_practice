### React CSS - How?

react is ui libarary, support alomost all kind of css preprocessor and framework 

many ways to add css in react js.

- [inline style](#inline-styles)
- [css through variable](#css-through-variable)
- [css file](#css-file)
- [cdn links](#cdn-links)

each type will be covered here but all type are not recommended

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

### css file

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

errors are expected if you find one report it to the [author](https://twitter.com/engsiraj_).
