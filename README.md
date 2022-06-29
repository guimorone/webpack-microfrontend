# Webpack and Micro Frontend

Webpack and Micro frontend course

## Webpack

[Tutorial](https://youtu.be/MpGLUVbqoYQ)

### Caveats about the video

- <span style="color:blue;">0:36:10</span> Had to use "devtool": false, instead of none due to a breaking change in the latest webpack.
- <span style="color:blue;">1:15:04</span> Latest webpack 5 package.json script: "start": "webpack serve --config webpack.dev.js --open",
- <span style="color:blue;">1:24:30</span> file-loader not needed in webpack 5: Add the following to your webpack.prod.js file:

  ```js
  module.exports = merge(common, {
    mode: 'production',
    output: {
      ...,
      assetModuleFilename: './imgs/[name].[hash].[ext]',
    },
  });

  ```

- <span style="color:blue;">1:42:05</span> **optimize-css-assets-webpack-plugin** not supporting webpack5, use **css-minimizer-webpack-plugin** instead per maintainers.<-- you don't need this however as webpack5 will minify for you.

### Running the project

```sh
  cd webpack/
  npm install
  npm start
```

## Micro Frontend

[Tutorial](https://youtu.be/lKKsjpH09dU)

### Full Site Federation eCommerce Example

An example eCommerce app Module Federation in a Full Site Federation configuration, using [react-router-dom](https://www.npmjs.com/package/react-router-dom) to manage the routing.

### Installation

In these five directories; `addtocart`, `cart`, `home`, `pdp` and `server` run these commands:

```sh
yarn && yarn start
```

In a different terminal window for each app.

The visit the [home page](http://localhost:3000/).
