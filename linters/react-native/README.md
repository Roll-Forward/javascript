# Packages

These Node.js packages are required for the recommended React Native ESLint setup:

```Bash
yarn add eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react eslint-watch babel-core babel-eslint babel-preset-airbnb babel-preset-react-native -D
```

# Scripts

Add these scripts to the `package.json` file:

```JSON
"scripts": {
    "android": "node node_modules/react-native/local-cli/cli.js run-android",
    "ios": "node node_modules/react-native/local-cli/cli.js run-ios",
    "lint": "yarn run lint:jsx",
    "lint:jsx": "eslint --ext .js,.jsx src",
    "lint-fix": "yarn run lint:jsx --fix",
    "lint-watch": "esw -w --changed src/**",
    "start": "node node_modules/react-native/local-cli/cli.js start",
    "start:android": "react-native run-android && yarn run lint-watch",
    "start:ios": "react-native run-ios && yarn run lint-watch",
    "test": "jest"
}
```
