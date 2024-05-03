# geo-area-calculator

Calculation of polygon area in WGS'84 coordinates. Port of the Python algorithm to PHP and JS.

# Install
In the project root folder:
```sh
.../geo-area-calculator$ composer install
```
If js tests needed:
```sh
.../geo-area-calculator$ npm install
```
# Tests
PHP
-----
```sh
.../geo-area-calculator$ phpunit
```

JavaScript
-----
```sh
.../geo-area-calculator$ npm test
```

# Examples

JavaScript
-----
```js
alert( ffGeo.getGeoPolygonArea(
			[
				[ -10.812317, 18 ],
				[ 10.812317, -18 ],
				[ 26.565051,  18 ],
				[ 52.622632, -18 ],
				[ 52.622632,  54 ],
				[ 10.812317,  54 ],
				[ -10.812317, 18 ],
			]
) );
```

PHP
-----
```php
use siddthartha\geo\area\helpers\GeoAreaCalculator;

echo GeoAreaCalculator::getArea(
        [
                [ -10.812317, 18 ],
                [ 10.812317, -18 ],
                [ 26.565051,  18 ],
                [ 52.622632, -18 ],
                [ 52.622632,  54 ],
                [ 10.812317,  54 ],
                [ -10.812317, 18 ],
        ]
);
// 33953235824742.51 (sq.meters)
```
