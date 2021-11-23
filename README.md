# Code along: "different types of testing for people who do or do not know JS"

## General React commands and things

### To run your CRA app locally

```bash
yarn start
```

### To test your CRA app locally

```bash
yarn test
```

>[yarn](https://classic.yarnpkg.com/en/) is better. But if you do not have yarn you can npm everything. Watch out for some syntax variations

### Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

## Code along steps

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

If your app is still running (btw *CNTL+C* to stop it) it should be singing fa-la-la

4. Create a remote repository without a `readme`, `.gitignore` or license.

5. Follow the GitHub instructions to change origin of your React app.

6. Add, commit and push your React App

7. Write your first test and call it `smoke.test.js`

```js
describe("checks that tests are testing", () => {
    it("should do basic maths", () => {
        expect(1+1).toBe(2);
    })
})
```