# dio_intercept_to_curl

[![pub package](https://img.shields.io/pub/v/dio_intercept_to_curl.svg)](https://pub.dartlang.org/packages/dio_intercept_to_curl)

A Flutter curl-command generator for Dio.

![dio_intercept_to_curl log output](https://github.com/OwnWeb/dio_intercept_to_curl/raw/main/example/assets/example.png?raw=true)

Easily test your Flutter-made requests in your favorite terminal or even in Postman or Insomnia.

## Why?

Sometimes you want to replay the HTTP requests made in your app, or you want to share it with your
beloved backend developer. Or you just love CURL.

Use your app as you want, and when the broken-request comes, look at your terminal, copy and paste
it, and enjoy replaying it easily!

## Features

* Simple GET/POST/DELETE/PUT requests logging
* With data when available
* Postman-ready

## Getting Started
```dart
_dio = Dio();

_dio.interceptors.add(DioInterceptToCurl());
```

Depending on your needs, you can also pass `printOnSuccess: true` to print all requests instead of
only errored ones.

By default, `convertFormData` is `true` and converts `FormData` to plain `Map` so we can get a CURL
representation even while using `FormData` (as for file uploads).
