# Project: 0x02. ES6 classes

![ES6-Classes](./main_files/ES6-Classes.jpeg)

## Resources

### Read or watch:-

- [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- [Metaprogramming](https://www.keithcirkel.co.uk/metaprogramming-in-es6-symbols/#symbolspecies)

## Project Setup

## Install NodeJS 12.11.x

```bash
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
```

### Verify NodeJS and npm versions:-

```bash
nodejs -v
npm -v
```

## Install Jest, Babel, and ESLint

Run the following command in your project directory to install `Jest`, `Babel`, and `ESLint`:

```bash
npm install
```

## Configuration Files

Add the files below to your project directory

### `package.json`

<details>
<summary>Click to show/hide file contents</summary>

```bash
{
  "scripts": {
    "lint": "./node_modules/.bin/eslint",
    "check-lint": "lint [0-9]*.js",
    "dev": "npx babel-node",
    "test": "jest",
    "full-test": "./node_modules/.bin/eslint [0-9]*.js && jest"
  },
  "devDependencies": {
    "@babel/core": "^7.6.0",
    "@babel/node": "^7.8.0",
    "@babel/preset-env": "^7.6.0",
    "eslint": "^6.4.0",
    "eslint-config-airbnb-base": "^14.0.0",
    "eslint-plugin-import": "^2.18.2",
    "eslint-plugin-jest": "^22.17.0",
    "jest": "^24.9.0"
  }
}
```

</details>

### `babel.config.js`

<details>
<summary>Click to show/hide file contents</summary>

```bash
module.exports = {
  presets: [
    [
      '@babel/preset-env',
      {
        targets: {
          node: 'current',
        },
      },
    ],
  ],
};
```

</details>

### `.eslintrc.js`

<details>
<summary>Click to show/hide file contents</summary>

```bash
module.exports = {
  env: {
    browser: false,
    es6: true,
    jest: true,
  },
  extends: [
    'airbnb-base',
    'plugin:jest/all',
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parserOptions: {
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  plugins: ['jest'],
  rules: {
    'no-console': 'off',
    'no-shadow': 'off',
    'no-restricted-syntax': [
      'error',
      'LabeledStatement',
      'WithStatement',
    ],
  },
  overrides:[
    {
      files: ['*.js'],
      excludedFiles: 'babel.config.js',
    }
  ]
};
```

</details>

- Don't forget to run npm install to install the dependencies specified in package.json.

* **0. You used to attend a place like this at some point** - Implement a class named `ClassRoom` with the given attributes. - `0-classroom.js`.
* **1. Let's make some classrooms** - Import `ClassRoom` from `0-classroom.js`. Implement a function named `initializeRooms`. It should return an array of 3 `ClassRoom` objects with the sizes 19, 20, and 34 (in this order). - `1-make_classrooms.js`.
* **2. A Course, Getters, and Setters** - Implement a class named `HolbertonCourse` with the given attributes and requirements. - `2-hbtn_course.js`.
* **3. Methods, static methods, computed methods names..... MONEY** - Implement a class named `Currency` with the given attributes and requirements. - `3-currency.js`.
* **4. Pricing** - Import `Currency` from `3-currency.js`. Implement a class named `Pricing` with the given attributes and requirements. - `4-pricing.js`.
* **5. A Building** - Implement a class named `Building` with the given attributes and requirements. - `5-building.js`.
* **6. Inheritance** - Import `Building` from `5-building.js.`. Implement a class named `SkyHighBuilding` that extends from `Building` with the given attributes and requirements. - `6-sky_high.js`.
* **7. Airport** - Implement a class named `Airport` with the given attributes. - `7-airport.js`.
* **8. Primitive - Holberton Class** - Implement a class named `HolbertonClass` with the given attributes. - `8-hbtn_class.js`.
* **9. Hoisting** - Fix the given code and make it work. - `9-hoisting.js`.
* **10. Vroom** - Implement a class named `Car` with the given attributes. - `10-car.js`.
* **11. EVCar** - Import `Car` from `10-car.js.` Implement a class named `EVCar` that extends from `Car` with the given attributes and requirements. - `100-evcar.js`.
