# think-captcha
thinkphp5.1 验证码类库 前后端分利用

## 安装
> composer require ftkj/ftcaptcha


##使用
### 生成base64 验证码，
```php
$captcha = new FtCaptcha((array) Config::pull('captcha'));
return $captcha->entry();
```
返回：
```
{
    "id": "kb7noqgcglk47rnkj9vknoae51",
    "captcha_base64": "iVBO...=="
}
```

### 验证

```
$captcha = new FtCaptcha((array) Config::pull('captcha'));
return $captcha->check($code,$id);
```

返回：true / false
