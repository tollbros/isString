# isString package

Is the string a string?

```
const isString = require('isstring')

console.log('isString', isString(3))
console.log('isString', isString([3]))
console.log('isString', isString('test'))
```
 
## How was this package created?
1. Created the `isString` project on Github as an empty repo for the `tollbros` Github org.
2. Locally created a `packages` directory.
3. Checked out the `isString` repo in the `packages` directory.
4. Within the `packages/isString` directory, run `npm init --scope=tollbrothers` and chose all the defaults.
5. Created the `index.js` file in `packages/isString`, this matches the default `package.json` (see `main` key).

## How was this package tested locally?
1. Within the `packages/isString` directory, run `npm link`. This created the `package-lock.json` file.
2. Went back to the `packages` directory and created a `isStringTEST` directory.
3. Created the `script.js` file in `packages/isStringTEST`.
4. Within the `packages/isStringTEST` directory, run `npm link isstring`. This linked the `isString` package to the test script.
5. Run the script via `node script.js`

## How do we publish changes?
1. Login first via `npm login`
2. Run `npm publish --access=public`

## Things to consider
- You can publish code without commiting it. Not sure why you would but there are no guards to prevent you from doing so.
- On github, the org is `tollbros`
- On npm, the org is `tollbrothers`

## Semantic Release Workflow
Basically, follow the commit message format below. Then when the commit is posted on the `main` branch semantic-release will do its thing and publish a new version on `merge to main` or a direct commit to `main`.
* [Commit message format](https://github.com/semantic-release/semantic-release#commit-message-format)