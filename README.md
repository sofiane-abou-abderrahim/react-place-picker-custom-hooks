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
