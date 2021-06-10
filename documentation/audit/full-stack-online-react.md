
# React Fundamentals

Materials

## Article: NonTechnical Overview of React

### Recommendation

As a non-technical overview of React, I feel like this article assumes too much
prior knowledge and spends too much time comparing React to other technologies
that the student either won't know or care about. Given that, this article would
need to be rewritten or possibly just removed.

### Audit

A Brief History

"React has continued to grow in popularity since its release. It is now, along
with Angular _and Vue.js_, one of the most popular libraries for front-end
development."

Concepts

* This section assumes a lot of prior information
* If the intention of this article is to give students a light introduction to
  React, this section should be rewritten to cover just the introductory
  concepts that a student needs some awareness of

Single Page App

* Change this to a generic description of SPAs
* Mention that while React can be used to create SPAs, React can also be used to
  create components that render just part of an HTML page

Diffing Algorithm

* There's a reference to O(n) time without any explanation of what that means

JSX

* This bit talks like students know what JSX is

Comparisons with other frameworks and libraries

* This entire section feels opinionated and outdated to me

jQuery

* States that jQuery is the most popular JavaScript library in use

Vue

* Heavily opinionated assessment of Vue

Angular

* Outdated assessment of Angular

Ember

* Remove this overview of Ember?

React Native

* Outdated overview of React Native

## Article: NPM

### Recommendation

We might need to move the Webpack npm script section to another article, but
other than that, this article can safely be removed from the React curriculum.

### Audit

* Mostly unnecessary review of NPM
* Includes a short section that shows the student how to add an npm script to
  run Webpack

## Article: Webpack

### Recommendation

Should this article give students an introduction to concepts like
transpilation, module loading, and bundling? If so, then this article will need
to be significantly expanded. If this article only needs to be an introduction
to Webpack configuration, then we just need to review and update (to ensure that
it's accurate with the latest version of Webpack) and rename the article to
"Webpack Configuration".

No mention of how to install Webpack (`webpack` and `webpack-cli`).

### Audit

* Starts with a mostly unnecessary reminder about `.gitignore` and the
  `node_modules` folder
* Starts immediately into how to configure Webpack without offering any
  explanation of what Webpack is and how it's used and why students need to
  learn how to use it

## Article: ES6 Syntax: Object Destructuring

### Recommendation

Maybe leave it in as a review?

### Audit

Overview of object destructuring in ES6.

## Article: ES6 Syntax: Import/Export

### Recommendation

We need a proper introduction to ES Modules (i.e. "Introduction to ES Modules")
and this article only provides part of that. Write a new article that includes
the examples from this article (rewritten for style and accuracy).

### Audit

* Jumps right into import/export syntax without any mention of ES Modules
* Shows an odd way of structuring CommonJS module exports
* Inaccurately describes default exports as the way to export from a module that
  only has one item to export
* A couple of odd resources linked at the bottom of the article (StackOverflow
  answer and Airbnb style guide)

## Article: React Developer Tools

### Recommendation

Instead of just telling students that debugging React is "hard", maybe we should
record a video that actually shows some of the challenges of debugging React?
Show what React components and elements look like in the standard developer
tools before installing the React Developer Tools? Then show students how to use
the React Developer Tools to inspect components and component state? Also,
unless the React Developer Tools are specifically used in the introductory
videos, maybe this article/video should a bit later in the curriculum, maybe
after all of the introductory videos but just before the project(s)?

### Audit

* Lightweight article that tells students that debugging React is hard and that
  they should install the React Developer Tools extension

## Link: Thinking in React

### Recommendation

This is a great external resource, but it's introduced way too early in the
curriculum. We also should have our own video (at some point) that talks through
the process of breaking a UI down into individual components and deciding how to
manage your application state.

### Audit

* Interesting walkthrough of the process of designing a React application
* The external article assumes that the reader is familiar with all of the core
  React concepts

## Video: Intro to React

### Recommendation

It might be possible to edit out the Rails and ERB references (might need to
leave in the jQuery references). Ideally, we replace this video that's a more
gradual introduction to React, but given our time constraints, I'm not sure
that's the best use of our time.

A lot is talked about before students see any code whatsoever. The initial
component example seems too complicated (i.e. a component with state and an
event handler). Makes me wonder how effective this video is at introducing
students to React.

Seems like an easier place to start is to show functional components with props.
Another approach to consider is to show a simple React component without having
to use Webpack. I've also introduced React to beginners by starting with the
Create React App tooling and asking them to ignore the surrounding project files
and focusing on just the App component (then demonstrating very simple
functional components with props).

### Audit

* Starts off with a mention of the other materials that are available
* References MVC (which students haven't been introduced to)
* Refers to React as a framework
* References the Single Responsibility Principle (not sure if students will know
  what that is) but the instructor does give a light introduction to what it is
* Shows an example of breaking an app into components but doesn't walk through
  the process, instead it just gives an overview of the final component diagram
* Also references the "Thinking in React" external resource as required reading
* Walks through a simple button click counter component
* The initial introduction to components immediately jumps into a discussion of
  props and state
  * During this part of the video, the slide content is cut off at the bottom of
    the frame
* Also introduces pure functional components as the way to write components that
  don't have state
* Gives a quick overview of ES Module import syntax and refers to the reading in
  the curriculum
* Shows an example of stateful component (no render method at this point)
* Introduces the `render` method and talks about not invoking the `render`
  method directly then segues into talking about what causes a component to
  rerender
* Discussion about `this.setState` method
* Introduces JSX but compares it to ERB
* ERB is referenced again when looking at JSX interpolation
* Mentions that a React component must have a single root element
  * While this is still generally true (at least for beginners) React not
    supports components without a single root element
* Introduces events and compares events in React to events in jQuery (students
  haven't been introduced to jQuery in the JS/Py curriculum)
* Code updates to the example component just appear instead of being typed in
  real time
  * This makes it more difficult to follow the process of building out a
    component step-by-step
* Clumsily discusses event handler binding by comparing element events to
  component lifecycle events even though students haven't been introduced to
  lifecycle events yet
* Discusses how to go from a file that contains a React component into the
  JavaScript that's running on an HTML page
  * The instructor gives an explanation of the application's root HTML element
    and how React attaches itself to it but then says "that's an explanation of
    what happens... maybe it didn't make any sense at all"
* Shows the example component now with the appropriate import and export
  statements (without any explanation) and a bundle file in the `index.html`
  page
* References Webpack as something that "you've seen before" but the Webpack
  article just walks through Webpack configuration without an overview or
  explanation of Webpack
* Quickly walks through the Webpack configuration file
* Introduces the entry point file
* Quickly enumerates the project's dependencies in the `package.json` file (some
  are skipped or ignored while others are mentioned but not explained)
* Shows how React is bound to the root element in the HTML page
  * Another quick mention of jQuery here even though vanilla JS
    `document.addEventListener` is used
* Light explanation of the `ReactDOM.render` method

## Video: Transpilation

### Recommendation

It might be possible to edit out the ERB references, though the first slide
would also need to be replaced (not sure what slide app the instructor is
using). Ideally, we replace this video that's a better introduction to Babel and
transpilation, but given our time constraints, I'm not sure that's the best use
of our time.

The conversion from JSX into `React.createElement` method calls feels a little
glossed over to me. Maybe some side-by-side comparisons would be helpful. It
might also help to show the transpiled output of a single JSX file so that it's
easier to see the effects of transpilation.

The Webpack configuration is not explained, just shown. That's okay I guess if
we just expect students to "copy and paste and use" (which is often done in the
beginning while learning React). Also, it's worth remembering that the Create
React App tooling obscures all of the Webpack configuration, which is helpful
when initially learning React so you don't have to learn too many things at
once.

### Audit

* Compares JSX to ERB as a way to explain how JSX is converted to HTML before it
  can be displayed in the browser
* Discusses how JSX elements are converted into `React.createElement` method
  calls
* Babel is introduced as the tool that handles the conversion from JSX to JS
  * The content on this slide is cut off on the bottom of the frame
* Enumerates the npm packages that are required to convert JSX to JS
* Reiterates that the `node_modules` folder shouldn't be committed to source
  control
  * Also mentions in passing the generated bundle files shouldn't be committed
    to source control (without much explanation)
* Walks through a prebuilt Webpack configuration file showing how to associate
  JSX files with the Babel loader module
  * Doesn't give any explanation of what Webpack loaders or presets actually do,
    just shows the references in the Webpack configuration
* Shows the generated bundle in the browser's developer tools
* Stumbles through trying to set a breakpoint in the bundle file (doesn't work)
* Switches gears and talks show the Webpack configuration option for generating
  sourcemaps
* Uses the developer tools to show the child HTML elements in the React root
  element as an example of how transpiling JSX into JS is enabling the rendering
  of the component to the DOM

## Video: Functional Components

### Recommendation

This is the best video so far in this series of React videos. Good demo of
refactoring part of a component's rendering into a separate child component.

In the video, the instructor consistently refers to function based components as
"purely functional components", which is unfortunate, because
`React.PureComponent` has special meaning in React.

Also, the previous state of the component is done in an unsafe way. To access
the previous state of a component, an anonymous function should be passed to the
`this.setState` method that defines a parameter for the previous state (and
optional a parameter for the component's props if props are needed to calculate
the next state).

### Audit

* Continues the click counter example by adding a reset button and a reset
  counter
* Live coding this time... adds a reset button with a click handler
* This breaks the app... shows the error in the browser console
  * Interesting that Webpack watch is configured but that's not covered anywhere
    in the videos
* Implements the `reset` method
* Extends the component state with a `previousCounts` array
* Updates the `reset` method to...
  * Get a reference to the `this.state.previousCounts` array and push the
    `this.state.count` value onto the array
  * Pass the updated array into the `this.setState` method call
* Updates the `render` method to map over the `this.state.previousCounts` array
  to render an unordered list
* Refactors the unordered list into a `Counts` child component
* Adds a new file for the `Counts` component...
  * Stubs out a new class-based component
  * Exports the component using a default export
* Imports the component into the ClickCounter component
  * Quickly shows that you don't need the file extension when importing a
    component into another component because of the Webpack `resolve`
    configuration option
* Adds `constructor` and `render` methods to the `Counts` component
* Passes the `this.state.previousCounts` property into the child component using
  props
* Highlights that the new `Counts` component doesn't have any state nor does it
  use lifecycle events (which haven't been discussed yet) so it should be a
  "purely functional component"
* Refactors the `Counts` class-based component into a simple `Counts` function
  that returns JSX
* Refactors the `Counts` function to use an implicit return
* Refactors the `Counts` function to use parameter destructuring
* Moved the `ClickCounter` and `Counts` component files into a new `frontend`
  folder
* Shows the unordered list item key warning that's displaying the browser's
  console
* Adds the `key` attribute to the unordered list item rendering

## Video: Lifecycle Methods

### Recommendation

Another good video! I like the way that the developer tools are used to demo the
component lifecycle methods.

Three of the lifecycle methods shown are now marked as "legacy" lifecycle
methods.

* `UNSAFE_componentWillMount()`
* `UNSAFE_componentWillReceiveProps()`
* `UNSAFE_componentWillUpdate()`

Perhaps we could add a short article after the video that discusses that these
lifecycle methods shouldn't be used (and why)?

### Audit

* Continues with the previous example
* Converts the `Counts` function component back to a class component
* Video starts with the lifecycle methods stubbed out in the class component
  version
  * `componentWillMount`
  * `componentDidMount`
  * `componentWillReceiveProps`
  * `componentWillUpdate`
  * `componentDidUpdate`
  * `componentWillUnmount`
* Mentions that the methods are called during the lifecycle of the component and
  shouldn't be called directly in code
* Uses the browser's developer tools to show the `debugger` statements getting
  hit as the component moves through its lifecycle
  * Also uses the console to evaluate the parameter values that are passed to
    the lifecycle methods
* Not able to show the `componentWillUnmount` lifecycle method because the
  current app design won't ever unload the component
* After mentioning that lifecycle methods don't need to be bound like event
  handlers, shows how to bind event handlers in the constructor
* Discusses some of the use cases of the lifecycle methods (e.g.
  `componentDidMount` to know when to make AJAX requests)

## Article: Props and State

### Recommendation

This article is mostly okay as it is, though it'd be easy enough to add an
example of passing in an anonymous function (to the `this.setState` method) to
handle the state update when you need to refer to the previous state or props to
calculate the new state.

### Audit

* Quick review of props
* Reminder that a component shouldn't change its own props
* Review of state
* Short discussion of when to use state
* Uses a simple example of an input element to show how to update state
* Reminder to always use `this.setState` to update state
* Interestingly shows that you can pass a second argument into the
  `this.setState` method to execute code after the state has been asynchronously
  updated
  * Misses the chance to show how to pass in an anonymous function to handle the
    state update when you need to refer to the previous state or props to
    calculate the new state

## Link: Click Counter Demo

### Recommendation

Probably okay as it is, unless we want to highlight and explain the differences
between the provided code and what's shown in the videos.

### Audit

* Download of the project shown in the videos
* Some of the lifecycle methods have been removed and new method,
  `getDerivedStateFromProps` has been added without any explanation

## Quiz: React Fundamentals

### Recommendation

Replace with new assessment assets.

### Audit

* The `className` attribute (vs using `class`) isn't discussed in the materials
  leading up to this quiz
* One of the questions suggests that every React component needs to have a
  `render` method
  * For clarification, maybe update this to read "every React class component"?


Additional Resources

## Article: Babel

### Recommendation

A very brief introduction to transpilation. Some before/after examples would be
helpful for students to understand what Babel is doing to their code. Also would
be helpful to clarify the relationship between Babel and Webpack. It's not clear
from this article that Babel can be used without Webpack for example.

### Audit

* The opening paragraph suggests that some JavaScript environments natively
  understand JSX which I don't think is actually a thing
  * "JavaScript development touches a lot of diverse environments: Node, Chrome,
    Safari, etc. These various environments have different levels of
    compatibility with advanced JavaScript features like JSX and ES6."

## Article: React

### Recommendation

The placement of this article in the curriculum is very odd. This article feels
like it should go at the very beginning of the curriculum and merge with the
"NonTechnical Overview of React" article.

### Audit

* Gives a high level introduction to React
  * Mentions that React isn't a frontend MVC framework but JS/Py students
    haven't been introduced to MVC yet
* Attempts to explain why you would need React
* Gives a high level explanation of how React works
* The article stops mid thought, almost as if the person who was writing it ran
  out of time

## Article: JSX

### Recommendation

Again, the placement of this article in the curriculum feels off to me. It would
also be helpful to include more examples in this article, showing students
common JSX coding patterns.

### Audit

* Light introduction to JSX
* Shows an example of JSX side by side with the corresponding
  `React.createElement` method call
  * While the article mentions that JSX must be transpiled it doesn't make it
    clear that JSX transpiles into `React.createElement` method calls

## Article: React Components

### Recommendation

This article needs to be rewritten to be a proper introduction to writing React
components. It could start with writing simple function components with props.
Another article could cover class components that make use of state.

### Audit

* Very brief overview of an example project that students are prompted to
  download
* The article mainly just highlights the various pieces of the example without
  any real explanation

## Article: Declaration

### Recommendation

Rewrite this article and combine it with the previous "React Components"
article.

### Audit

* Brief article that compares function and class components
* Refers to function components as "Purely Functional Components" which isn't
  correct
* Uses jQuery's `$.ajax` to make an AJAX call
* The first example of class component uses a lifecycle method without any
  explanation
* Provides a brief description of pure functions

## Article: Lifecycle Methods

### Recommendation

Rewrite this article to be an actual introduction to the lifecycle of a
component and the methods that React provides that allow you to write code that
correspond to the key component lifecycle events.

### Audit

* Brief introduction to component lifecycle methods
* Shows an example of using `componentDidMount` without actually explaining what
  the component's lifecycle actually is

## Article: Synthetic Events

### Recommendation

Rewrite this article to be a proper introduction to handling events in React.
Also take the time to explain that the React `SyntheticEvent` object wraps the
native browser events to normalize events across browser vendors. The end result
is that while you're writing code against the React `SyntheticEvent` object, you
almost never need to think about it because it's interface mirrors the native
browser event object.

### Audit

* Very brief overview of event handling in React
* Uses the term "synthetic events" without actually explaining what it means

## Link: Official React Documentation

### Recommendation

This is an excellent resource for students to be aware of, but it doesn't make
it clear to students as to what parts of the official docs they should read and
which parts are okay to ignore for now.

### Audit

* Links to the React "Getting Started" official docs

## Project: Redux Lite

### Recommendation

The inclusion of this project at this point in the curriculum feels like a
mistake.

### Audit

* Walkthrough of building your own Redux implementation


Homeworks
## Project: Getting Started with NPM

### Recommendation

Are we expecting students to know how to configure a React project from scratch
or will they be using the Create React App tooling? If students need to know how
to configure Webpack to support React development, then having a project that
gives them practice at doing that makes a lot of sense, otherwise I'd cut this
project.

### Audit

* Has the student using npm to install dependencies and configuring Webpack to
  support React development

## Project: React Calculator

### Recommendation

With some minor cleanup and tweaks to the instructions this project could be
left in to provide students with practice at creating a basic class component.

### Audit

* Project that has students creating a simple Calculator class component


Projects
## Project: CSS Friends (Phase 12)

### Recommendation

Remove this project (doesn't seem to be part of the React curriculum).

### Audit

N/A

## Project: Widgets

### Recommendation

With some minor cleanup and tweaks to the instructions this project could be
left in to provide students with practice at creating components. The React
transitions bonus phase should be removed or replaced with something more
appropriate.

### Audit

* Project that has students building four simple widgets
* Mentions that jQuery shouldn't be used
* Bonus phase uses React transitions

## Project: Minesweeper

### Recommendation

With some minor cleanup and tweaks to the instructions this project could be
left in to provide students with practice at creating React components. Not sure
if the last phase that has students creating a modal is something that students
will need more guidance on or not.

### Audit

* Project that has students building a Minesweeper game
* Game logic is provided so students can focus on implementing the UI

# Redux Fundamentals

## Article: Advanced Containers

### Recommendation

Moved from the React Router lesson into the Redux lesson.

### Audit

TODO

# Middleware and Thunks
# Redux and the Rails API
# Frontend Routing with React

Materials

## Article: Intro to React Router

### Questions

* Should we explain the difference between `BrowserRouter` and `HashRouter`?
* Would it be worthwhile to focus on `BrowserRouter` and show how to configure
  Express to properly handle frontend routes?

### Recommendation

Some updates to this article would make it more approachable for beginners. The
overall approach of introducing React Router object types and listing their
properties before showing an example isn't very conducive to learning.

### Audit

* Compares browser location state to Redux which students haven't learned about
  yet if we move the React Router lesson ahead of the Redux lesson(s)
* Uses `HashRouter` instead of `BrowserRouter`
* References `Provider` which students haven't learned about yet if this lesson
  follows the React Fundamentals lesson

## Article: <Link>

### Recommendation

Maybe incorporate this content into the main React Router article?

### Audit

* Introduces the `Link` and `NavLink` components

## Article: <Switch>

### Recommendation

Maybe incorporate this content into the main React Router article?

### Audit

* Introduces the `Switch` component

## Article: withRouter

### Recommendation

We should consider removing this article, unless the student really needs to
know about the `withRouter` function at this time.

If we're going to teach students about the `withRouter` function, then we'll
need to teach students about higher order components before this article. Also,
we'd ideally come up with an example for this article that shows why the
`withRouter` function is interesting and useful (the React Router docs uses
`withRouter` to wrap a simple component that renders the user's current path).

### Audit

* Compares the `withRouter` function to the `connect` function from
  `react-redux`
* Students haven't learned about higher order components yet

## Article: <Redirect>

### Recommendation

Maybe incorporate this content into the main React Router article?

### Audit

* Introduces the `Redirect` component

## Article: Advanced Containers

### Recommendation

Move from the React Router lesson into the Redux lesson.

### Audit

N/A

## Quiz: Frontend Routing with React Quiz

### Recommendation

Consider updating the question type on the matching route paths so they don't
telegraph the expected answer.

### Audit

* The questions about the matching route paths telegraphs the correct answer by
  the answer type (multiple answers vs single answer)


Additional Resources
## Link: React Router Docs

### Recommendation

This is an excellent resource for students to be aware of, but it doesn't make
it clear to students as to what parts of the docs they should read and which
parts are okay to ignore for now.

### Audit

* Links to the React Router docs


Homeworks

## Project: Rainbow Routes

### Recommendation

Maybe review instructions and make minor tweaks, but other than that this
project seems good to go. Definitely not long enough to fill an entire day in
class.

### Audit

* Project that has students defining routes to display colors of the rainbow
* Students also add `Link` and `NavLink` components to render navigation to the
  available colors


Projects

## Project: Pokedex (Part 2)

### Recommendation

Move from the React Router lesson into the Redux lesson.

### Audit

* Part 2 of a 3-part project
* Part 1 is part of the "Redux and the Rails API" lesson

## Project: Pokedex (Part 3)

### Recommendation

Move from the React Router lesson into the Redux lesson.

### Audit

* Part 3 of a 3-part project
* Part 1 is part of the "Redux and the Rails API" lesson
* This part of the project is just the bonus phases

# Frontend Auth
# Completing Bench BnB
