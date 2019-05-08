tslint-sf-react
------------

Lint rules related to React & JSX for [TSLint](https://github.com/palantir/tslint/).

## Usage

tslint-sf-react has peer dependencies on TSLint and TypeScript.

To use these lint rules with the default preset, use configuration inheritance via the `extends` keyword.
Here's a sample configuration where `tslint.json` lives adjacent to your `node_modules` folder:

```js
{
  "extends": [ "tslint-sf-react"],
  "rules": {
    // override tslint-sf-react rules here
    "jsx-wrap-multiline": false
  }
}
```

## Rules

  [detail rules](https://github.com/SFTC/tslint-sf-react/blob/master/RULES.md)
