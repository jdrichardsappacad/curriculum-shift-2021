
# React-Redux Curriculum Updates

## Proposed Schedule

See the [Proposed React Schedule] Google Sheet for a detailed breakdown of the
proposed schedule.

### Week 1

* Day 1 - Off / Intro to React Homework (Concepts, React.createElement, ES
  Modules)
* Day 2 - Intro to React (React.createElement, JSX, Create React App)
* Day 3 - Class Components (State, Event Handling, Forms, Component Lifecycle)
* Day 4 - React Router, React Builds
* Day 5 - Context

### Week 2

* Day 1 - Intro to Redux (Using Redux without React, Store, Reducers, Actions)
* Day 2 - Redux + React (Using Redux with React without React-Redux library)
* Day 3 - Intermediate Redux (React-Redux library, Containers, Middleware,
  Thunks, Auth)
* Day 4 - Hooks
* Day 5 - WebSockets, Project Planning

## Recommendations

### Schedule Updates

* Assign students homework on their day off (day 1)
  * This will give us a jump start on a long week of new content

* Shorten the time spent on `React.createElement` on day 2 so that students can
  start using JSX sooner

* Reduce the scope of the material that's covered on day 3
  * Move the Introduction to JSX content to day 2

* Move React Builds to day 4 so that day 5 can be focused on Context

* Spread the Redux material over two and a half days
  * Introduce the basics of Redux (Store, Reducers, Actions) without React on
    the afternoon of week 2 day 1
  * Cover using Redux with React without the React-Redux library on week 2 day 2
  * Cover intermediate Redux (React-Redux library, Containers, Middleware,
    Thunks, Auth) on week 2 day 3

### Project Updates

#### Higher Priority

* Create new `React.createElement` project (based on phase 1 of the existing
  `React.createElement` project)

* Remove the Widgets Router project to make room for the React Builds project on
  week 1 day 4

* Create new Context project to give students practice with using Context
  without the complexities of working with authentication

* Update the existing Tweets Revisited Context related project
  * Provide more of the non-Context related solution to reduce the overall scope
    of the project

* Create new Redux project to give students practice at implementing Redux
  without React
  * Focus on actions, reducers, and the store
  * Write imperative code to exercise the Redux implementation
  * Use Node.js to run the application
  * For a preview of the solution for this project see the [`app.js`] and
    [`reduxStoreActionReducer.js`] files in the [New Intro to Redux Projects PR]

* Create new Redux + React project to give students practice at using Redux
  within a React application
  * Hold off on using the React-Redux library to keep things as simple as
    possible conceptually
  * Reuse the application theme from the first Redux-only project

* Update the Pokedex Hooks project to give students practice at refactoring
  class components to function components and Hooks
  * Starter project includes Redux to give students additional exposure to Redux
  * Initial phases will have students refactoring using `useState` and
    `useEffect`
  * Later phase will have students refactoring components to use Redux Hooks
  * Include a bonus phase to refactor to replace Redux with Context (and the
    `useContext` Hook) 

#### Lower Priority

* Create a version of the Giphy project that uses class components + Redux to
  give students additional practice with Redux

### Content Updates

#### Higher Priority

* Update the Redux objectives so that they're split across 2 days

* Update the Redux Explained article to explain why you'd want to use Redux
  instead of Context

* Update the Store, Reducers, and Actions articles to remove any references to
  React

* Create new Implementing Redux coding demo video to walk through implementing
  Redux (sans React)
  * Highlight the Redux flow by setting `debugger` statements and prompting the
    student to predict what the next step in the flow will be

* Write new article(s) to introduce students to using Redux within a React
  application (without using the React-Redux library) 

* Create new Intro to Redux + React lecture video to conceptually introduce
  using Redux within a React application (without using the React-Redux library)

* Create new Redux + React Coding Demo video(s) to walk through using Redux
  within a React application (without using the React-Redux library)
  * See the Calculator project within the [New Intro to Redux Projects PR] for
    an example application of using Redux with React without using the
    React-Redux library
  * Highlight the Redux flow by setting `debugger` statements and prompting the
    student to predict what the next step in the flow will be

* Create new Redux Flow video that uses `debugger` statements to highlight the
  Redux flow and prompts students to predict what the next step will be

* Update the Redux Provider, React Redux Connect, Container Components,
  Selectors, More About Containers, Middleware, and Thunks Middleware articles
  to fit within the new Redux learning progression

* Write new React Router Hooks article to introduce students to using React
  Router Hooks

* Write new Redux Hooks article to introduce students to using Redux Hooks

* Create new React Router Hooks video to introduce students to using React
  Router Hooks

* Create new Redux Hooks video to introduce students to using Redux Hooks
  * Base on Bart's Redux Hooks video:
    https://drive.google.com/open?id=1pMLgiVwu0QoWaebdPr4A9Op0ex6KkUzw

#### Lower Priority

* Write new React State Management article that conceptually introduces state
  management before students learn about Context and Redux

* Write new Introduction to ES Modules article (introduce ES modules, introduce
  the syntax, and compare them to CommonJS modules)

* Write new WebSockets Intro and Using WebSockets on the Server and Client
  articles
  * Base these new articles on the existing WebSockets overview article

## Observations

### Monday (Day 1)

No class... holiday :)

### Tuesday (Day 2)

* There was a lot of material and concepts presented before students really saw
  what a simple React function component looks like in code
* We talk about ES modules in the `React.createElement` video before we teach
  students about them
* Chat with instructors...
  * Too much time spent on `React.createElement`
  * Worthwhile to show `React.createElement` before showing JSX, but too much
    time is spent on it

### Wednesday (Day 3)

* It'd be ideal if students could work through the JSX content _before_ they
  learn about class components (and state, event handling, and lifecycle
  methods)
  * Shortening the `React.createElement` content would help give time for
    learning and practicing JSX on the previous day
* Chat with instructors...
  * Too much, too soon (day 3's homework includes Intro to JSX, class
    components, event handling, forms, and lifecycle methods)
  * Breaking up the day (i.e. lecture(s), project, lecture(s), project) is
    challenging because of individual paces
  * Students enjoy having bonus phases available though it'd be helpful if
    solutions were provided for all of the available bonus phases

### Thursday (Day 4)

* Content balancing
  * Noticeably lighter day compared to the previous day and a half
  * Neither React Router project has bonus phases
  * Students were encouraged to review the week's material with the extra time
    if they finish early
  * No one finished the Widgets project from the previous day (some students
    didn't even start it)
  * Moving the Introduction to JSX content to day 2 will give students more time
    to work on the class components projects
* Chat with instructors...
  * Instructors felt like students had a good amount of experience with JSX from
    the first two projects on day 3, but neither of them implement lifecycle
    methods (those are only present in a couple of the components in the Widgets
    project)
* Slack chat (later in the day)...
  * Question about Monday's assessment led me to review Friday's projects
  * Suggested that the projects could be swapped which would allow more
    emphasis to be placed on the Context project

### Friday (Day 5)

* A student had a question about how to define a component that can accept
  children
* Chat with instructors...
  * Instructors felt like there's a missing overview video that gives students
    an introduction to front end builds
  * Discussed an idea about having a project where we'd provide students with an
    existing larger React project and have students make a change (i.e. add a
    simple feature or fix a bug)

### Monday (Week 2, Day 1)

* Assessment in the morning
* To allow more time for the large amount of Redux homework, the instructors had
  the students (in pairs) review the solution code for the state-based app
  project in the afternoon instead of taking the time to build it themselves

### Tuesday (Week 2, Day 2)

* The original Redux articles have received an initial review and update but
  they could still use a more thorough review and update to bring them to the
  new standards
* A student asked a question today about why you don't any parameters to the
  `mapStateToProps` function when calling the `react-redux` `connect` method
  * Student had some confusion around passing a function by reference vs calling
    it yourself
* Chat with instructors...
  * Feeling that Redux thunks and auth are too much to add in right away
  * Suggestion to move the Pokedex state-based version of the app to end of the
    previous week so that Redux could be taught over two days (instead of a
    single day)
  * Introduce the basics of Redux on Monday afternoon
  * Suggestion to use the Redux version of Pokedex for the Hooks project
  * Look for opportunities to use Redux in future projects to reinforce learning
    (example: the WebSockets project)
  * Discussed the merits of organizing Redux code into a single `store` folder
    vs organizing Redux code into separate folders (folder per type approach)

### Wednesday (Week 2, Day 3)

* Add an `Intro to State Management` article introducing Context and Redux
  together before the Context project on Day 5
* Expand more days for Context and Redux
  * 2 days of Context, instead of 1 day (and introduce Context with a simpler
    project not connected to user auth)
  * 3 days of Redux, instead of 1 day
* Student was confused about what the Redux store was and what Reducers were
  * I showed him and his partner how to use the `redux-logger` middleware
    instead of just using the React developer tools
  * Students are familiar with using the normal developer tools and logging
    middleware from Express, so introducing Redux with `redux-logger` instead of
    jumping straight into the React developer tools could help
* Officially switch order of projects:
  1. Giphy Hooks (actually a Redux-focused project)
  2. Pokedex state-based Hooks
  3. Pokedex context-based Hooks
* Personal brainstorm: create diagram that compares `componentDidMount`,
  `componentDidUpdate`, and `componentWillUnmount` to `useEffect` hook
  * Personal observation from lecture question: add a walk-through article that
    clarifies the `cleanup` in `useEffect` (i.e. clock demo with `clearInterval`
    used in a `cleanup` function in the `useEffect` hook

### Thursday (Week 2, Day 4)

* Should we move the Hooks content ahead of Redux so that we can use Hooks when
  teaching Redux?
  * Is it necessary for students to know how to use Redux with class components?
  * Are students primarily using Hooks once they learn about it?
* Chat with the instructors...
  * One pair still hadn't gotten to the Hooks material yet
  * If some pairs don't get through the WebSockets material this week, the
    project is guided enough that students could do it on their own

[Proposed React Schedule]: https://docs.google.com/spreadsheets/d/1m3WFTbkOQ_n-mNSumfZn6h08fv_OmNSIbm-Z0wAfM_0/edit#gid=0

[New Intro to Redux Projects PR]: https://github.com/appacademy/Modular-Curriculum/pull/299

[`app.js`]: https://github.com/appacademy/Modular-Curriculum/blob/c645c9f3d1a91e7ed44c0695c2fc607486deab17/content/react-redux/topics/redux/projects/redux-task-list/app.js

[`reduxStoreActionReducer.js`]: https://github.com/appacademy/Modular-Curriculum/blob/c645c9f3d1a91e7ed44c0695c2fc607486deab17/content/react-redux/topics/redux/projects/redux-task-list/reduxStoreActionReducer.js
