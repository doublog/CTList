# 配置文件
## 无特殊需要,只需要填写账号密码
```
[
    {
        "UserName": "",                                 # Input Phone Number.
        "Password": "",                                 # Input Password.
        "CaptchaMode": "0",                             # Captcha Mode. 0: Auto Reject, 1: Manual Input, other: API URL. 
        "RefreshToken": "",                             # Token, Not modify.
        "RefreshTokenTime": "",                         # Log Token Time, Not modify.
        "SubPath": "/CTCloud",                          # Index Path 
        "RootPathId": "-11",                            # Default Root: -11
        "HideItemId": "Num01|Num02",                    # Allow Folder and File.
        "RefreshURL": 1800,                             # Max: 1800; Allow Max: 2329
        "RefreshInterval": 900,                         # Max: Null, Min Global Value
    }
]
```

# 刷新策略
```
Token(保活): 60 * 60 * 24 * 5
Cookie(授权): 60 * 30
URL(下载链接): 60 * 30 （配置文件可改 <RefreshURL>）
Folder(刷新目录): 60 * 15  （配置文件可改, 全局最小值生效 <RefreshInterval>）
```

# 天翼云网盘登陆验证码识别API(基于OCR)
```
# 目前只支持天翼云网盘登陆的验证码(其他类型根本识别不出来)
# 下载天翼云验证码需要添加请求头 "Referer: https://open.e.189.cn/"

# 接口: https://api.moeclub.org/SampleCode
# 方式: POST
# 参数: Base64=<IMAGE_BASE64_CODE>&Type=CTCloud
# 返回: 状态码:200, 显示识别结果. 状态码:404, 识别错误或结果不符合预设规则, 显示为空.
```
