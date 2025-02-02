# nuxt-bugsnag

[![npm version][npm-version-src]][npm-version-href]
[![npm downloads][npm-downloads-src]][npm-downloads-href]
[![CircleCI][circle-ci-src]][circle-ci-href]
[![Codecov][codecov-src]][codecov-href]
[![License][license-src]][license-href]

>

[📖 **Release Notes**](./CHANGELOG.md)

This is a module from the [bugsnag demo project](https://github.com/bugsnag/bugsnag-js/tree/master/examples/nuxtjs)

## Setup

1. Add `nuxt-bugsnag` dependency to your project

```bash
npm install nuxt-bugsnag
```

2. Add `nuxt-bugsnag` to the `modules` section of `nuxt.config.js`
Bugsnag recommends creating two projects in your dashboard, one for the server errors and one for the browser errors.

```js
{
  modules: [
    // Simple usage
    'nuxt-bugsnag',

    // With options
    ['nuxt-bugsnag', {
      clientConfig: {
        apiKey: 'YOUR_BROWSER_API_KEY'
      },
      serverConfig: {
        apiKey: 'YOUR_SERVER_API_KEY'
      }
    }]
  ]
}
```

If you don't want to use two API keys just use the apiKey property

```js
{
  modules: [
    ['nuxt-bugsnag', {
      apiKey: 'Your_API_KEY'
    }]
  ]
}
```

You can pass every bugsnag [options](https://docs.bugsnag.com/platforms/javascript/configuration-options/) in the options object


```js
{
  modules: [
    // Simple usage
    'nuxt-bugsnag',

    // With options
    ['nuxt-bugsnag', {
      clientConfig: {
        apiKey: 'YOUR_BROWSER_API_KEY'
      },
      serverConfig: {
        apiKey: 'YOUR_SERVER_API_KEY'
      }
      config: {
        notifyReleaseStages: ['staging', 'production'],
      }
    }]
  ]
}
```

if you want to split them for the server and client again, you can do this aswell.

```js
{
  modules: [
    // Simple usage
    'nuxt-bugsnag',

    // With options
    ['nuxt-bugsnag', {
      apiKey: 'YOUR_API_KEY',
      clientConfig: {
        appType: 'browser',
      },
      serverConfig: {
        appType: 'server'
      }
    }]
  ]
}
```


# Source Maps

You can upload sourcemaps by adding the option `publishRelease`.

```js
{
  modules: [
    // Simple usage
    'nuxt-bugsnag',

    // With options
    ['nuxt-bugsnag', {
      apiKey: 'YOUR_API_KEY',
      publishRelease: true,
    }]
  ]
}
```

## Development

1. Clone this repository
2. Install dependencies using `yarn install` or `npm install`
3. Start development server using `npm run dev`

## License

[MIT License](./LICENSE)

Copyright (c) Julian Martin <julian.martin@russmedia.com>

<!-- Badges -->
[npm-version-src]: https://img.shields.io/npm/v/nuxt-bugsnag/latest.svg?style=flat-square
[npm-version-href]: https://npmjs.com/package/nuxt-bugsnag

[npm-downloads-src]: https://img.shields.io/npm/dt/nuxt-bugsnag.svg?style=flat-square
[npm-downloads-href]: https://npmjs.com/package/nuxt-bugsnag

[circle-ci-src]: https://circleci.com/gh/JulianMar/nuxt-bugsnag/tree/master.svg?style=shield
[circle-ci-href]: https://circleci.com/gh/julianmar/nuxt-bugsnag

[codecov-src]: https://img.shields.io/codecov/c/github/julianmar/nuxt-bugsnag.svg?style=flat-square
[codecov-href]: https://codecov.io/gh/julianmar/nuxt-bugsnag

[license-src]: https://img.shields.io/npm/l/nuxt-bugsnag.svg?style=flat-square
[license-href]: https://npmjs.com/package/nuxt-bugsnag
