# Code along: "different types of testing for people who do or do not know JS"

1. Bootstrap a CRA project with [Create React App](https://github.com/facebook/create-react-app).

```bash
npx create-react-app your-app-name 
```

> npx will run Node without any global installs

2. Navigate to your new CRA project and open it in [VSCode](https://vscode.dev/):

```bash
cd your-app-name
code .
```

>[yarn](https://classic.yarnpkg.com/en/) is better. But if you do not have yarn you can npm everything. Watch out for some syntax variations

## To run your CRA app locally

```bash
yarn start
```

## To test your CRA app locally

```bash
yarn test
```

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

3. Clean the boilerplate (legit React speak): remove the logo most of CSS and leave the following in your App.js:

```js
import './App.css';

function App() {
  return (
    <div className="App">
      <h1>Fa-la-la-la-la-la-la-la🎄🎄🎄🎄</h1>
    </div>
  );
}

export default App;
```

If your app is still running (btw *_CNTL+C_* to stop it) it should be singing fa-la-la
