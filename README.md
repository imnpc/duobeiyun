Duobeiyun
======

基于 [多贝云](http://docs.duobeiyun.com/download/) 官方SDK,当前版本基于 duobeiyun_php_sdk_20180606。


## 安装

使用 Composer 安装:

```
composer require "imnpc/duobeiyun"
```

## 使用

```php
use Imnpc\Duobeiyun\DuobeiyunApi;

$client = new DuobeiyunApi();
echo $client->createRoom(
    "测试多贝云01",                  // title
    strtotime("2014/12/8 15:40"),   // startTime
    3,                              // duration
    DuobeiyunApi::$ROOM_HAS_VIDEO,  // video
    DuobeiyunApi::$ROOM_TYPE_1vN    // roomType
  );
```

## 参考

- [官方PHP-SDK](http://docs.duobeiyun.com/php)

# License

MIT
