## scss sass



1- install sass using npm.

```
npm i sass --save
```

2 - create file and folder as `css/style.scss`.

3 - import file `style.scss` in `App.jsx` components.

```js
import "./css/styles.scss";
```

4 - operators
this is how we can use operators `+/-*` in sass,

```css
font-size: 3rem + 3rem;
```

5 - variables

```css
$bg-color: orange;
```

6 - nested

```scss
.main_header {
  display: grid;
  h1 {
    font-size: 50rem;
    // for hover
    &:hover {
      color: red;
    }
    // pseudo css
    &::before,
    &::after {
      color: blue;
    }
  }
}
```

7 - mixin

```scss
mixin space_between {
  display: flex;
  justify-content: space-between;
}
//usage
.main-header {
  @include space_between;
  color: $primary;
}
```

8 - parameters
if you want to pass more than 1 parameter you have to just remember the sequence of the parameters you just passed to the mixin.

```scss
mixin space_between($font_size) {
  display: flex;
  justify-content: space-between;
  font-size: $font_size;
}
//usage
.main-header {
  @include space_between(20px);
  color: $primary;
}
```

9 - partials

- file `_underscore.scss` for example: `_mixin.scss` or `_vars.scss`
- now we just import file in another file where we want to use the scss as:

```scss
@import "mixin";
@import "vars";
```

- yes! we don't need underscore `_` or `.scss` file extension while importing the file.

errors are expected if you find one report it to the [author](https://twitter.com/engsiraj_).