# webpack-fe-36

1. npm init -y

2. npm i webpack webpack-cli webpack-dev-server webpack-merge --save-dev

3. npm i babel-loader @babel/core @babel/plugin-proposal-class-properties @babel/preset-env --save-dev

4. .babelrc

```
{
  "presets": ["@babel/preset-env"],
  "plugins": ["@babel/plugin-proposal-class-properties"]
}
```

5. npm i eslint eslint-config-airbnb-base eslint-config-prettier eslint-import-resolver-webpack eslint-plugin-import eslint-plugin-prettier eslint-webpack-plugin --save-dev

6. .eslintrc

```
{
  "ignorePatterns": ["dist", "node_modules"],
  "rules": {
    "max-len": [
      "error",
      {
        "ignoreUrls": true,
        "code": 80
      }
    ],
    "prefer-template": "off",
    "indent": [1, 2],
    "object-curly-spacing": 1,
    "no-multiple-empty-lines": [
      1,
      {
        "max": 1,
        "maxEOF": 1
      }
    ],
    "no-var": 1,
    "camelcase": 1,
    "no-new-wrappers": 1,
    "no-nested-ternary": 1,
    "no-console": 1,
    "no-template-curly-in-string": 1,
    "no-self-compare": 1,
    "import/prefer-default-export": 0,
    "func-names": [1, "as-needed"],
    "arrow-body-style": 1,
    "semi": [1, "never"],
    "import/no-extraneous-dependencies": ["off", { "devDependencies": false }]
  },
  "env": {
    "browser": true,
    "es6": true
  },
  "extends": ["eslint:recommended", "airbnb-base", "prettier"],
  "globals": {
    "Atomics": "readonly",
    "SharedArrayBuffer": "readonly"
  },
  "parserOptions": {
    "ecmaVersion": 11,
    "sourceType": "module"
  },
  "plugins": ["prettier"],
  "settings": {
    "import/resolver": {
      "webpack": {
        "config": "config/webpack.common.js"
      }
    }
  }
}
```

7. npm i prettier prettier-webpack-plugin --save-dev

8. .prettierrc

```
{
  "trailingComma": "es5",
  "singleQuote": true,
  "tabWidth": 2,
  "printWidth": 80,
  "semi": false
}
```

9. npm i style-loader css-loader css-minimizer-webpack-plugin mini-css-extract-plugin node-sass sass-loader postcss-loader postcss-preset-env --save-dev

10. postcss.config.js

```
module.exports = {
  plugins: {
    'postcss-preset-env': {
      browsers: 'last 2 versions',
    },
  },
}

```

11. npm i html-webpack-plugin clean-webpack-plugin copy-webpack-plugin cross-env --save-dev

12. npm i handlebars handlebars-loader

13. npm install friendly-errors-webpack-plugin webpackbar --save-dev
