# laravel-district

中国行政区划数据，访问高德在线数据获取最新区划数据

中国行政区划数据，根据高德[行政区划浏览](https://lbs.amap.com/api/javascript-api/reference-amap-ui/geo/district-explorer)说明，访问[高德区划API](https://webapi.amap.com/ui/1.0/ui/geo/DistrictExplorer/assets/d_v1/country_tree.json)生成最新区划数据，支持动态更新最新区划数据。

# 安装说明

```php
$ composer require liufhai/laravel-district
```

# 使用说明

生成migrations。
```php
$ php artisan vendor:publish --provider="Liufhai\DistrictExplorer\ServiceProvider"
```

执行migrate。

```php
$ php artisan migrate
```

加载Seeder。
```php
$ composer dump-autoload
```

生成最新区划数据（数据表在生成时会自动清空之前数据）。
```php
$ php artisan db:seed --class=DistrictsSeeder
```
