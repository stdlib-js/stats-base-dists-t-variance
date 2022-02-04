<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Variance

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Student's t][t-distribution] distribution [variance][variance].

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

The [variance][variance] for a [Student's t][t-distribution] random variable with degrees of freedom `ν` is

<!-- <equation class="equation" label="eq:t_variance" align="center" raw="\operatorname{Var}\left( X \right) = \begin{cases} \frac{\nu }{\nu-2} & \text{ for } \nu > 2 \\ \infty & \text{ for } 1 < \nu \le 2 \end{cases}" alt="Variance for a Student's t distribution."> -->

<div class="equation" align="center" data-raw-text="\operatorname{Var}\left( X \right) = \begin{cases} \frac{\nu }{\nu-2} &amp; \text{ for } \nu &gt; 2 \\ \infty &amp; \text{ for } 1 &lt; \nu \le 2 \end{cases}" data-equation="eq:t_variance">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@51534079fef45e990850102147e8945fb023d1d0/lib/node_modules/@stdlib/stats/base/dists/t/variance/docs/img/equation_t_variance.svg" alt="Variance for a Student's t distribution.">
    <br>
</div>

<!-- </equation> -->

For `ν` smaller than one, the variance is not defined.

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/stats-base-dists-t-variance
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm` branch][esm-url].
-   If you are using Deno, visit the [`deno` branch][deno-url].
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd` branch][umd-url].

</section>

<section class="usage">

## Usage

```javascript
var variance = require( '@stdlib/stats-base-dists-t-variance' );
```

#### variance( v )

Returns the [variance][variance] of a [Student's t][t-distribution] distribution with degrees of freedom `v`.

```javascript
var y = variance( 9.0 );
// returns ~1.286

y = variance( 3.5 );
// returns ~2.333
```

If provided `1 < v <= 2`, the function returns `infinity`.

```javascript
var y = variance( 1.5 );
// returns Infinity

y = variance( 2.0 );
// returns Infinity
```

If provided `v <= 1`, the function returns `NaN`.

```javascript
var y = variance( -1.0 );
// returns NaN

y = variance( 0.8 );
// returns NaN
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var round = require( '@stdlib/math-base-special-round' );
var variance = require( '@stdlib/stats-base-dists-t-variance' );

var v;
var y;
var i;

for ( i = 0; i < 10; i++ ) {
    v = randu() * 20.0;
    y = variance( v );
    console.log( 'v: %d, Var(X,v): %d', v.toFixed( 4 ), y.toFixed( 4 ) );
}
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-t-variance.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-t-variance

[test-image]: https://github.com/stdlib-js/stats-base-dists-t-variance/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/stats-base-dists-t-variance/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-t-variance/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-t-variance?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-t-variance.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-t-variance/main

-->

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-t-variance/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-base-dists-t-variance/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-base-dists-t-variance/tree/esm

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-t-variance/main/LICENSE

[t-distribution]: https://en.wikipedia.org/wiki/Student%27s_t-distribution

[variance]: https://en.wikipedia.org/wiki/Variance

</section>

<!-- /.links -->
