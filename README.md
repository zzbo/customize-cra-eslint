# customize-cra-eslint
use eslint config for customize-cra

## Install
```bash
npm i customize-cra-eslint
```

## Usage
- add configuration file `config-overrides.js` at the root of your project.
- add customize-cra config content as following:
```js
const { override } = require('customize-cra');
const eslintConfigOverrides = require('customize-cra-eslint');

module.exports = override(
  eslintConfigOverrides(),
);
```

customize-cra-eslint use `root/.eslintrc.js` for default config.
customize your eslint rules:
```
const { override } = require('customize-cra');
const eslintConfigOverrides = require('customize-cra-eslint');
const eslintConfig = require('./.eslintrc.js');

module.exports = override(
  eslintConfigOverrides(eslintConfig),
);
```

inspired by https://github.com/arackaf/customize-cra/issues/175#issuecomment-610023655
