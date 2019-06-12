<p align="center">
  <a href="https://sweetalert2.github.io/">
    <img src="/assets/swal2-logo.png" alt="SweetAlert2">
  </a>
</p>

<p align="center">
  A beautiful, responsive, customizable, accessible (WAI-ARIA) replacement for JavaScript's popup boxes. Zero dependencies.
</p>

<p align="center">
  <a href="https://sweetalert2.github.io/">
    <img src="https://raw.github.com/sweetalert2/sweetalert2/master/assets/sweetalert2.gif" width="562"><br>
    See SweetAlert2 in action ↗
  </a>
</p>

<p align="center">
  <a href="https://travis-ci.org/sweetalert2/sweetalert2"><img alt="Build Status: Linux" src="https://travis-ci.org/sweetalert2/sweetalert2.svg?branch=master"></a>
  <a href="https://ci.appveyor.com/project/limonte/sweetalert2/branch/master"><img alt="Build Status: Windows" src="https://ci.appveyor.com/api/projects/status/paqdtx0snu53w5c1/branch/master?svg=true"></a>
  <a href="https://coveralls.io/github/sweetalert2/sweetalert2?branch=master"><img src="https://coveralls.io/repos/github/sweetalert2/sweetalert2/badge.svg?branch=master&" alt="Coverage Status"></a>
  <a href="https://www.npmjs.com/package/sweetalert2"><img alt="Version" src="https://img.shields.io/npm/v/sweetalert2.svg"></a>
  <a href="https://www.jsdelivr.com/package/npm/sweetalert2"><img alt="jsdelivr" src="https://data.jsdelivr.com/v1/package/npm/sweetalert2/badge?style=rounded"></a>
  <a href="#support-and-donations"><img alt="Support Donate" src="http://ionicabizau.github.io/badges/paypal.svg"></a>
</p>

---

:raised_hands: :raised_hands: :raised_hands: Help wanted!
---------------------------------------------------------

We just started the [`sweetalert2-themes`](https://github.com/sweetalert2/sweetalert2-themes) project, for now 3 themes are available: [`dark`](https://github.com/sweetalert2/sweetalert2-themes/tree/master/dark), [`minimal`](https://github.com/sweetalert2/sweetalert2-themes/tree/master/minimal), and [`borderless`](https://github.com/sweetalert2/sweetalert2-themes/tree/master/borderless). Please help us with [other themes](https://github.com/sweetalert2/sweetalert2-themes/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22), I would be happy to donate some :moneybag: for all active contributors. The quick-start contributing guide is [here](#contributing).

Thank you :heart:

---

:point_right: **Upgrading from v7.x to v8.x?** [Read the release notes!](https://github.com/sweetalert2/sweetalert2/releases/tag/v8.0.0)
<br>If you're upgrading from v6.x, please [upgrade from v6 to v7](https://github.com/sweetalert2/sweetalert2/releases/tag/v7.0.0) first!

:point_right: **Migrating from [SweetAlert](https://github.com/t4t5/sweetalert)?** [SweetAlert 1.x to SweetAlert2 migration guide](https://github.com/sweetalert2/sweetalert2/wiki/Migration-from-SweetAlert-to-SweetAlert2)

---

Installation
------------

```sh
npm install --save sweetalert2
```

Or grab from [jsdelivr CDN](https://www.jsdelivr.com/package/npm/sweetalert2)
:

```html
<script src="https://cdn.jsdelivr.net/npm/sweetalert2@8"></script>
```


Usage
-----

```html
<script src="sweetalert2/dist/sweetalert2.all.min.js"></script>

<!-- Include a polyfill for ES6 Promises (optional) for IE11 -->
<script src="https://cdn.jsdelivr.net/npm/promise-polyfill@8/dist/polyfill.js"></script>
```

You can also include the stylesheet separately if desired:

```html
<script src="sweetalert2/dist/sweetalert2.min.js"></script>
<link rel="stylesheet" href="sweetalert2/dist/sweetalert2.min.css">
```

Or:

```js
// ES6 Modules or TypeScript
import Swal from 'sweetalert2'

// CommonJS
const Swal = require('sweetalert2')
```

It's possible to import JS and CSS separately, e.g. if you need to customize styles:

```js
import Swal from 'sweetalert2/dist/sweetalert2.js'

import 'sweetalert2/src/sweetalert2.scss'
```

Please note that [TypeScript is well-supported](https://github.com/sweetalert2/sweetalert2/blob/master/sweetalert2.d.ts), so you don't have to install a third-party declaration file.


Examples
--------

The most basic message:

```js
Swal.fire('Hello world!')
```

A message signaling an error:

```js
Swal.fire('Oops...', 'Something went wrong!', 'error')
```

Handling the result of SweetAlert2 modal:

```js
Swal.fire({
  title: 'Are you sure?',
  text: 'You will not be able to recover this imaginary file!',
  type: 'warning',
  showCancelButton: true,
  confirmButtonText: 'Yes, delete it!',
  cancelButtonText: 'No, keep it'
}).then((result) => {
  if (result.value) {
    Swal.fire(
      'Deleted!',
      'Your imaginary file has been deleted.',
      'success'
    )
  // For more information about handling dismissals please visit
  // https://sweetalert2.github.io/#handling-dismissals
  } else if (result.dismiss === Swal.DismissReason.cancel) {
    Swal.fire(
      'Cancelled',
      'Your imaginary file is safe :)',
      'error'
    )
  }
})
```

## [Go here to see the docs and more examples ↗](https://sweetalert2.github.io/)


Browser compatibility
---------------------

 IE11* | Edge | Chrome | Firefox | Safari | Opera | UC Browser
-------|------|--------|---------|--------|-------|------------
:heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |

\* ES6 Promise polyfill should be included, see [usage example](#usage).

Note that SweetAlert2 **does not** and **will not** provide support or functionality of any kind on IE10 and lower.


Related projects
-------------------------

- [ngx-sweetalert2](https://github.com/sweetalert2/ngx-sweetalert2) - Angular 4+ integration
- [sweetalert2-react-content](https://github.com/sweetalert2/sweetalert2-react-content) - React integration
- [sweetalert2-webpack-demo](https://github.com/sweetalert2/sweetalert2-webpack-demo) - webpack demo
- [sweetalert2-parcel-demo](https://github.com/sweetalert2/sweetalert2-parcel-demo) - overriding SCSS variables demo


Related community projects
-------------------------

- [avil13/vue-sweetalert2](https://github.com/avil13/vue-sweetalert2) - Vue.js wrapper
- [realrashid/sweet-alert](https://github.com/realrashid/sweet-alert) - Laravel 5 Package


