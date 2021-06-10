# React Fundamentals (W10D2)

Please audit these resources

---

## Article: Non-technical overview of React

Notes:

- I think we can just revise and keep most of this!
- In the revision suggestions below, I shortened the "A Brief History" section
  and added it to the "React" section.

Revision suggestions:

# React [TODO: EDIT]

React came out of a [project at Facebook] to develop a version of PHP that could
defend against Cross Site Scripting (XSS) attacks. This version of PHP could
properly escape malicious code and had the ability to condense PHP elements into
single, HTML-like tags to be re-used in the codebase. There was just one
problem: the performance of DOM manipulation was terrible.

One engineer had the idea of using PHP's syntax and use of tags in a Javascript
library. In order to improve the performance of DOM manipulation, lifecycle
methods and a differential algorithm to identify what needed to be updated were
introduced. Thus React was born.

React was first used in Facebook's newsfeed in 2011 and Instagram.com in 2012.
React has continued to grow in popularity since its release. It is now, along
with Angular, one of the most popular libraries for front-end development. In
addition to Facebook, React is used by Uber, Airbnb, Netflix, Yahoo, Pinterest,
Feedly, Coursera, Product Hunt, and OpenTable.

## Concepts [TODO: KEEP]

### Single Page App

### Virtual DOM

### React Life Cycle [Joanna's suggestion to add a brief overview/diagram]

[Diagram](http://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/) linked
in React docs

### Diffing Algorithm

### JSX

### Enzyme and Jest

## Comparisons with other frameworks and libraries [TODO: REMOVE/EDIT]

I think we can shorten or remove this section, as this is already a long
introductory overview to React.

## Thinking in React [TODO: ADD]

This [resource](https://reactjs.org/docs/thinking-in-react.html) was taken from
the "Thinking in React" reading

---

## Article: Webpack

Notes:

- I think we can keep and add to this!
- In the suggested revision below, I just took out the `.gitignore` section and
  one sentence about Rails.

Revision suggestions::

# Webpack Configuration

Add introduction to what Webpack is (I was already using it for like 2 full
weeks before realizing that it was bundling all of my project's JavaScript into
one JavaScript file).

Just like with NPM, you can use a configuration file to set up your webpack
options. You'll have to create this file by hand. It should live in your
project's root directory, be named `webpack.config.js`, and export a single
object.

## Specifying entry and output files

The `webpack.config.js` file allows you to specify your entry file, and the name
and location of your output file. See the example below:

```js
const path = require("path");

module.exports = {
  entry: "./frontend/my_app.jsx",
  output: {
    path: path.resolve(__dirname, "app", "assets", "javascripts"),
    filename: "bundle.js",
  },
  // CODE SHORTENED FOR BREVITY
};
```

## The `devtool` key and `source-map` [TODO: EDIT (add screenshot of devtools sources/bundle.js tab vs sources/entry.jsx tab)]

The `webpack.config.js` file accepts a `devtool` key that can be used to enable
useful tools, particularly `source-map`. A source map makes it possible for you
to see the line numbers of your original source code when errors are raised.
This is generally not possible because your `bundle.js` does not maintain the
line numbers from the files it is bundling.

```js
module.exports = {
  // CODE SHORTENED FOR BREVITY
  devtool: "source-map",
  // CODE SHORTENED FOR BREVITY
};
```

## Resolving extensions

The `webpack.config.js` file also accepts a `resolve` key, which lets you
specify what file `extensions` to process without explicitly naming them. Note
that you must include the star matcher `'*'` to be able to include files with an
explicit extension. Otherwise `require('file_name.js')` will cause webpack to
look for `file_name.js.js`.

```js
module.exports = {
  // CODE SHORTENED FOR BREVITY
  resolve: {
    extensions: [".js", ".jsx", "*"],
  },
  // CODE SHORTENED FOR BREVITY
};
```

## Sample `webpack.config.js`

```js
// webpack.config.js
const path = require("path");

module.exports = {
  entry: "./frontend/entry.jsx",
  output: {
    filename: "./bundle.js",
  },
  module: {
    rules: [
      {
        test: [/\.jsx?$/],
        exclude: /(node_modules)/,
        use: {
          loader: "babel-loader",
          query: {
            presets: ["@babel/env", "@babel/react"],
          },
        },
      },
    ],
  },
  devtool: "source-map",
  resolve: {
    extensions: [".js", ".jsx", "*"],
  },
};
```

---

## Article: React Developer Tools

Notes:

- We can use this if we splice out 0:00-1:35!

---

## Video: React: Intro

- We can splice 0:00-1:35 (speaker mentions Rails)
- Video outline:
  - Brief React overview
  - Thinking in React components introduction
  - Anatomy / physiology of components: props, state, & jsx
  - Click Counter demo
    - Demonstrates class component
    - Demonstrates `super()` vs `super(props)` to pass props

---

## Video: React: Transpilation

- We can use this if we splice out 0:00-2:01 (speaker has a slide that connects
  erb to JSX)

---

## Video: React: Functional Components

- I think we can use this!
- Video outline:
  - Extends click counter demo
  - Creates `Counts` component as ES6 functional component

---

## Video: React: Lifecycle Methods

- Video outline:
  - Quickly refactors `Counts` component as a class component
  - Great demo that walks through the component life cycle methods with
    debuggers:
    - componentWillMount
    - componentDidMount
    - componentWillReceiveProps
    - componentWillUpdate
    - componentDidUpdate
    - componentWillUnmount

---

## Article: React: Component Attributes [Joanna's suggestion to add]

# React: Component Attributes

Brief intro connecting HTML to JSX

## Synthetic events

### `onClick`

We can outline the differences between `onClick={this.handleClick}` and
`onClick={() = this.handleClick(e)}`

### `onChange`

## `className`

## Props

---

## Article: Props and State

- I think we can use this!

---

## Demo: Click Counter Code Demo [Joanna's suggestion to move this right after React videos]

- Currently is a to a zip file for the Click Counter demo from the videos (we
  can update this to a repo link).

---

## Quiz: React Fundamentals Quiz [TODO: KEEP]

---

## Article: React Components [Joanna's suggestion to move this article before React Fundamentals Quiz]

- This article definitely feels very slim.

---

## Article: Life Cycle Methods [Joanna's suggestion to move this article before React videos]

- This article also feels very slim.

Revision suggestions:

- Add to current intro: Components sometimes need to call certain functions or
  run other bits of code at various points during their lifecycle. For example,
  a component might need to fetch new data from the server once it has been
  mounted to the DOM. Code for these actions live in a component's lifecycle
  methods.
- Bring back
  [diagram](http://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/)
  linked in React docs (suggested addition to React intro)
- Explain the use case for each of the common life cycle methods:
  - componentDidMount
  - componentDidUpdate
- Talk about deprecated "legacy" methods (as noted in the [React
  docs](https://reactjs.org/docs/react-component.html))
- Introduce Hooks and how they connect to the life cycle methods

---

## Project: React Calculator

- Works off of a skeleton linked
  [here](https://open.appacademy.io/learn/full-stack-online/react/getting-started-with-npm).
- This project teaches students about `state` and is the introduction to
  rendering JSX.

Revised Learning Objectives:

- This project can be a simple data rendering project to introduce `props` and
  rendering in JSX.
- Students could be given a `data.js` file with a POJO to simulate data fetched
  from an API.
- Students could be given a diagram that outlines "React thinking" with an
  example of how to plan components based on the given `data.js` file.
- Students can import the `data.js` file and thread it's attributes as `props`.

## Project: Widgets

- [Widgets project live](https://appacademy.github.io/curriculum/widgets/)
- We could add project set-up instructions about webpack configuration and using
  [create-react-app](https://create-react-app.dev/docs/getting-started/). If
  they have questions about set-up, they can refer to the original React
  Calculator skeleton they received.
- Project uses `componentWillUnmount` (Do we want this? I actually don't know.
  -Joanna)
- Project uses `XMLHttpRequest` to fetch from the [open weather
  API](https://openweathermap.org/current) (Do we want to use Fetch API?)

Current Project Outline:

- Phase 1: Create a `clock.jsx` component
  - Use `setState` and `setInterval` to write a `tick` function
  - Create a JavaScript Date object
  - Render date with Date methods
- Phase 2: Add google font and `index.css` stylesheet to `index.html` head
  [TODO: REMOVE?]
- Phase 3: Create tabs for a folder
- Phase 4: Use `navigator.geolocation` in fetch call to open weather API (brief
  note about API keys but no note on suggestions to secure them)
- Phase 5: Create `Autocomplete` component that filters a list of names by the
  user's input.
- Bonus: Implement [React-Transitions](https://reactjs.org/docs/animation.html)
  - It definitely feels too soon to introduce this.
