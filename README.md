# Custom Hooks

## Creating & Using Custom React Hooks

- Repetition: Rules of Hooks
- Why Custom Hooks?
- Creating Custom Hooks
- Using Custom Hooks

# Steps

## 0. Starting Project

1. run `cd backend/`, then `npm install`, then `node app.js` to launch the server
2. run `npm install`, then `npm run dev` to run the frontend
3. run `npx eslint --init`, then configure the `.eslintrc.cjs` file
4. create a `README.md` file

## 1. Creating a Custom Hook

1. create a new folder named `hooks` inside of the `src` folder
2. inside of it, create a new file named `useFetch.js`
3. inside of it, create a hook by defining a function named `useFetch`
4. outsource the `useEffect` code from `App.jsx` by copying it and pasting it inside of this `useFetch` custom hook
5. get rid of the `useEffect` code from `App.jsx` & call this `useFetch` custom hook instead

## 2. Custom Hook: Managing State & Returning State Values

1. manage some state in `useFetch.js` to make this `useFetch` custom hook functional
2. add a `isFetching`, `error` & `fetchedData` state
3. add a `fetchFn` function as a parameter of the `useFetch` hook to make it usable with all kind of fetch functions
4. execute this `fetchFn` function inside of the `useFetch` hook
5. replace the name of the `fetchPlaces` function with `fetchData`
6. add `fetchFn` as a dependency of the `useEffect` hook
7. return the states to make them available outside of the hook
8. export the `useFetch` custom hook to make it available in components
9. call the `useFetch` hook in `App.jsx` and pass the `fetchUserPlaces` to it as an argument
10. get the returned state snapshots from the `useFetch` hook as a result of calling `useFetch` with help of object destructuring
11. add `intialValue` prop to the `useFetch` hook to make some state more configurable

## 3. Exposing Nested Functions From The Custom Hook

1. make the updating function `setFetchedData` available by returning it in the `useFetch` hook
2. in `App.jsx`, extract this `setFetchedData` updating function
3. for completeness sake, and to get rid of the eslint warning, add `setUserPlaces` as a dependency of the `useCallback` hook in `App.jsx`
   It technically won't make a difference though because it does refer to a state updating function and those are guaranteed by React to never change.
