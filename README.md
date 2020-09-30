# customize-cra-eslint
customize eslint config for customize-cra.

## Install
```bash
npm i customize-cra-eslint -D
```

## Usage
- Add and edit configuration file `config-overrides.js` at the root of your project.
- Add or update customize-cra config content as following:
```js
const { override } = require('customize-cra');
const eslintConfigOverrides = require('customize-cra-eslint');

module.exports = override(
  eslintConfigOverrides(),
);
```

`customize-cra-eslint` use `root/.eslintrc.js` for default rules.  

You can also customize your eslint rules for `customize-cra-eslint`, for example:
```js
const { override } = require('customize-cra');
const eslintConfigOverrides = require('customize-cra-eslint');
const eslintConfig = require('./.eslintrc.js');

module.exports = override(
  eslintConfigOverrides(eslintConfig),
);
```

inspired by https://github.com/arackaf/customize-cra/issues/175#issuecomment-610023655
