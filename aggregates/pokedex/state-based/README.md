# State-Based Pokedex

This project challenges you to build a slightly more than non-trivial
application using class-based components that have state in them. You do this so
that you can compare and contrast this method with other state-management
methods like Redux and Context+Hooks.

## Getting started

You'll need the backend for the Pokedex application. Clone it from
https://github.com/appacademy-starters/pokedex-backend. Follow the instructions
in that repository's README to get it set up.

The API for the backend is also documented in that README.

Once you have that up and running, create a new React application using
Create React App and the App Academy **simple** template.

```
npx create-react-app state-based-pokedex --template @appacademy/simple
```

Now, install **react-router-dom**.

```
npm install react-router-dom
```

## Explore the reference application

Go to https://aa-state-pokedex.herokuapp.com to see what you should build. It is
an application that uses the backend located at
https://aa-pokedex-backend.herokuapp.com.

That's your goal. Create something like that application using your local
backend that you just cloned and the React application that you just created.

In the implementation that you see on line, there are the following components

* `App`: Does that browser routing and top-level fetches of data to draw the
  data
* `LoginPanel`: Shows the login panel
* `PokemonBrowser`: The browser that draws the list on the left after logging in
   and has a route to the `PokemonDetail` when the route matches "/pokemon/:id"
* `PokemonDetail`: Makes a fetch to the API on mount and update to load the
   details of the selected Pokemon

## Try it on your own

This will be tough because it'll be the first React app from scratch that you've
done. Don't worry, though. You can do it. You've done a whole bunch of these in
various ways. You can do this. Just get one piece working at a time. For
example, you could:

1. Make the login form component and get it to make a fetch for a token
2. Make the app component aware of the new token through a callback passed
   through props
3. Have the app component render the Pokemon browser after getting a token
4. Have the app component save the token to the local storage and read it on
   refresh and not show the login form if one exists
5. When someone clicks on a Pokemon in the list, have it show the details of the
   Pokemon

Or, you could do something similar to those previous steps but use a `Context`.
This is your project. You can make this work.

Remember, Create React App will let your React application use environment
variables that start with `REACT_APP_`, so use that to your advantage for
specifying the URL of the backend.

Go ahead and look at the solution code if you want a direction to move because
you don't know where to start. That's ok. Take a peek. Study it. Then, put it
away and do it yourself. Make it better!
