# Youzan Golang SDK


## 通过App Id 和 App Secret来调用 
``` go
client := YZClient{appID: "<AppID>", appSecret: "<AppSecret>"}
	ret := client.Invoke("kdt.shop.basic.get", "1.0.0", "GET", map[string]string{}, map[string]string{})
	println(ret)
```

## 通过OAuth 的access token 来调用
```go
    client := YZClient{isOAuth: true, accessToken: "<accessToken>"}
	ret := client.Invoke("kdt.shop.basic.get", "1.0.0", "GET", map[string]string{}, map[string]string{})
	println(ret)
```

## Go Test 

### 在shell中设置 YZAppID和 YZAppSecret 变量

```
export YZAppID=<Your App ID>
export YZAppSecret=<Your App Secret>
```

### Test

```go
go test
```