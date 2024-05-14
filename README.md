# Learning-React
All tutorials I'm following while learning react

### npx create-react-app app-name
Creates a react app (basic template) in current directory

### npm start
Starts the development server

# Tips
1. Identifying if a piece of data is state
    1. Does it remain unchanged over time? If so, it isn’t state.
    2. Is it passed in from a parent via props? If so, it isn’t state.
    3. Can you compute it based on existing state or props in your component? If so, it definitely isn’t state!
What’s left is probably state.

2. Identifying where a state should live
    For each piece of state in your application:

    1. Identify every component that renders something based on that state.
    2. Find their closest common parent component—a component above them all in the hierarchy.
    3. Decide where the state should live:
        1. Often, you can put the state directly into their common parent.
        2. You can also put the state into some component above their common parent.
        3. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common parent component.