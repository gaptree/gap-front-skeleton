# gap-front-skeleton

```
cp ../gap-front-skeleton/. ./ -nvR
```


```
yarn init
```


```
yarn link eslint jest babel-core babel-jest babel-preset-env regenerator-runtime
yarn add eslint jest babel-core babel-jest babel-preset-env regenerator-runtime --dev

```

.babelrc

```
{
    "presets": [
        "env"
    ]
}
```


.eslintignore
```
jest.config.js
```


.eslintrc.js
```
module.exports = {
    "env": {
        "browser": true,
        "es6": true,
        "jest": true
    },
    "extends": "eslint:recommended",
    "parserOptions": {
        "sourceType": "module"
    },
    "rules": {
        "indent": [
            "error",
            4
        ],
        "linebreak-style": [
            "error",
            "unix"
        ],
        "quotes": [
            "error",
            "single"
        ],
        "semi": [
            "error",
            "always"
        ]
    },
    "parserOptions": {
        "ecmaVersion": 2017,
        "sourceType": "module"
    }
};
```


.sass-lint.yml
```yml
files:
    include: 'front/scss/**/*.scss'
rules:
    extends-before-mixins: 2
    extends-before-declarations: 2
    placeholder-in-extend: 2
    mixins-before-declarations:
        - 2
        -
            exclude:
                - breakpoint
                - mq

    no-warn: 1
    no-debug: 1
    no-ids: 2
    no-important: 2

    indentation:
        - 4
        -
            size: 4

    variable-for-property:
        - 1
        -
            'properties':
            - 'margin'
            - 'content'
```


package.json

```
  "scripts": {
    "test": "npm run jest && npm run eslint",
    "jest": "jest",
    "eslint": "eslint ."
  },
```

.travis.yml

```
sudo: false

language: node_js
node_js:
  - "8"
  - "7"

cache:
  directories:
    - "node_modules"
```
