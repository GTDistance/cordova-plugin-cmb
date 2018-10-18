# tff-plugin-cmb
cmb cordova plugin


#### install

```
ionic cordova plugin add https://github.com/GTDistance/cordova-plugin-cmb.git --variable PRIVATE_KEY=[value]

android 还需要修改 res -> values -> cmbkb_strings.xml 里的 cmbkb_publickey 值为 PRIVATE_KEY, 后续打算使用hook或者配置实现

```

#### use

````
//success支付成功，fail支付失败，none没有支付
window.TffCMB.pay({
    url: [招行一网通h5支付页面地址, 字符串],
    jsonRequestData: [需要传的参数, json对象]
}, function(msg){
    if(msg === "success"){
        // do something
    }
}, function(err){
    if(err === "fail"){
        // do something
    }
});
````
