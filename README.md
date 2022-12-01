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

# isNegativeInteger

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Test if a finite [double-precision floating-point number][ieee754] is a negative integer.



<section class="usage">

## Usage

To use in Observable,

```javascript
isNegativeInteger = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-assert-is-negative-integer@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var isNegativeInteger = require( 'path/to/vendor/umd/math-base-assert-is-negative-integer/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/math-base-assert-is-negative-integer@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.isNegativeInteger;
})();
</script>
```

#### isNegativeInteger( x )

Tests if a finite [double-precision floating-point number][ieee754] is a negative `integer`.

```javascript
var bool = isNegativeInteger( -1.0 );
// returns true

bool = isNegativeInteger( 0.0 );
// returns false

bool = isNegativeInteger( 10.0 );
// returns false
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   The function assumes a **finite** `number`. If provided negative `infinity`, the function will return `true`, when, in fact, the result is undefined. If `x` can be `infinite`, wrap the implementation as follows:

    ```javascript
    function check( x ) {
        return (
            x > -Infinity &&
            isNegativeInteger( x )
        );
    }

    var bool = check( -Infinity );
    // returns false
    ```

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/math-base-assert-is-negative-integer@umd/browser.js"></script>
<script type="text/javascript">
(function () {

var bool = isNegativeInteger( -5.0 );
// returns true

bool = isNegativeInteger( 0.0 );
// returns false

bool = isNegativeInteger( 1.0 );
// returns false

bool = isNegativeInteger( -3.14 );
// returns false

bool = isNegativeInteger( NaN );
// returns false

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math/base/assert/is-integer`][@stdlib/math/base/assert/is-integer]</span><span class="delimiter">: </span><span class="description">test if a finite double-precision floating-point number is an integer.</span>
-   <span class="package-name">[`@stdlib/math/base/assert/is-nonnegative-integer`][@stdlib/math/base/assert/is-nonnegative-integer]</span><span class="delimiter">: </span><span class="description">test if a finite double-precision floating-point number is a nonnegative integer.</span>
-   <span class="package-name">[`@stdlib/math/base/assert/is-nonpositive-integer`][@stdlib/math/base/assert/is-nonpositive-integer]</span><span class="delimiter">: </span><span class="description">test if a finite double-precision floating-point number is a nonpositive integer.</span>
-   <span class="package-name">[`@stdlib/math/base/assert/is-positive-integer`][@stdlib/math/base/assert/is-positive-integer]</span><span class="delimiter">: </span><span class="description">test if a finite double-precision floating-point number is a positive integer.</span>

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

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-assert-is-negative-integer.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-assert-is-negative-integer

[test-image]: https://github.com/stdlib-js/math-base-assert-is-negative-integer/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/math-base-assert-is-negative-integer/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-assert-is-negative-integer/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-assert-is-negative-integer?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-assert-is-negative-integer.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-assert-is-negative-integer/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-assert-is-negative-integer/tree/deno
[umd-url]: https://github.com/stdlib-js/math-base-assert-is-negative-integer/tree/umd
[esm-url]: https://github.com/stdlib-js/math-base-assert-is-negative-integer/tree/esm
[branches-url]: https://github.com/stdlib-js/math-base-assert-is-negative-integer/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-assert-is-negative-integer/main/LICENSE

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985

<!-- <related-links> -->

[@stdlib/math/base/assert/is-integer]: https://github.com/stdlib-js/math-base-assert-is-integer/tree/umd

[@stdlib/math/base/assert/is-nonnegative-integer]: https://github.com/stdlib-js/math-base-assert-is-nonnegative-integer/tree/umd

[@stdlib/math/base/assert/is-nonpositive-integer]: https://github.com/stdlib-js/math-base-assert-is-nonpositive-integer/tree/umd

[@stdlib/math/base/assert/is-positive-integer]: https://github.com/stdlib-js/math-base-assert-is-positive-integer/tree/umd

<!-- </related-links> -->

</section>

<!-- /.links -->
