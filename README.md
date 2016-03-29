# CSS variable loader

[![npm](https://img.shields.io/npm/v/css-variables-loader.svg)](https://www.npmjs.com/package/css-variables-loader)
[![Build Status](https://travis-ci.org/Dashlane/css-variables-loader.svg?branch=master)](https://travis-ci.org/Dashlane/css-variables-loader)
[![Dependency Status](https://gemnasium.com/Dashlane/css-variables-loader.svg)](https://gemnasium.com/Dashlane/css-variables-loader)

Import your CSS variables into JavaScript.

## Assumptions

This project assumes you use [W3C custom properties](https://www.w3.org/TR/css-variables/) for CSS variables. This is how they look:

```css
:root {
    --my-theme-color: hsl(121, 90%, 90%);
    --my-accent-color: hsl(60, 90%, 90%);
    --my-font-size: 18px;
}
```

Only the custom properties on the `:root` selector are currently supported.

This project also assumes you have a Webpack-like setup for building your application.

## Usage

Install the loader into your project with `npm install --save css-variables-loader`.

In your JavaScript, use `var variables = require('!css-variables!../path/to/variables.css')`.

Now `variables` is a map of variable names to values as strings.
