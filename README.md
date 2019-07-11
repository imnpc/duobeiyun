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

$partnerId ="xxxx";
$appKey="xxxx";
$serverAddress = "https://api.duobeiyun.net";//官方目前拥有 api.duobeiyun.com  api.duobeiyun.net 2个接口  默认com的可不传递本参数

$client = new DuobeiyunApi($partnerId,$appKey,$serverAddress);
echo $client->createRoom(
    "测试多贝云",                  // title
    strtotime("2019/7/11 10:40"),   // startTime
    1,                              // duration
    DuobeiyunApi::$ROOM_HAS_VIDEO,  // video
    DuobeiyunApi::$ROOM_TYPE_1vN    // roomType
  );
```

## 接口参考

- [官方PHP-SDK](http://docs.duobeiyun.com/php)

# License

MIT