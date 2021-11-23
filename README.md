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

8. Run the tests, push your test to GitHub

9. Find your `App.test.js` (comes shipped with CRA). Make it fail, e.g., by setting `screen.getByTestId('counter-butt')`. You can read [RTL docs](https://testing-library.com/docs/react-testing-library/intro/) for ideas on what your UI elements might be and how to test for them.

10. Make your `App.test.js` pass.

11. Experiment with [Snapshots](https://jestjs.io/docs/snapshot-testing).

First, you will need to install a snapshot renderer:

```bash
yarn add react-test-renderer
```

Then you can write your first snapshot test, e.g.,

```js
import React from 'react';
import renderer from 'react-test-renderer';

import App from './App';

test("that DOM renders consistently", () => {
    const tree = renderer.create(<App/>).toJSON();
    expect(tree).toMatchSnapshot();
})
```

Make changes to your `App.js`. Run tests. If you want to fix the tests press `u`. If, on the other hand you did something wrong to the DOM you can fix your code.

12. Making a Component. Create a folder called `components`. Make a `Counter.js` component. You can find the code in the repo or make your own to start with.

13. Check `Counter.test.js` for to see how to fake a click. You can use the ideas from that test or write your own using [RTL docs](https://testing-library.com/docs/react-testing-library/intro/).

14. Sign up or Login to [Netlify](https://www.netlify.com/). Deploy the app.

15. Go to Actions and choose the Action build the pipeline. You may copy the yaml from this repo to set up an Action.