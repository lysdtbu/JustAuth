<p align="center">
	<a href="https://www.justauth.cn/"><img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/logo.png" width="400"></a>
</p>
<p align="center">
	<strong>Login, so easy.</strong>
</p>
<p align="center">
	<a target="_blank" href="https://search.maven.org/search?q=g:%22me.zhyd%22%20AND%20a:%22JustAuth%22">
		<img src="https://img.shields.io/badge/Maven Central-1.0.0-blue.svg" ></img>
	</a>
	<a target="_blank" href="https://gitee.com/yadong.zhang/JustAuth/blob/master/LICENSE">
		<img src="https://img.shields.io/badge/License-GPL%20v3-yellow.svg" ></img>
	</a>
	<a target="_blank" href="https://www.oracle.com/technetwork/java/javase/downloads/index.html">
		<img src="https://img.shields.io/badge/JDK-1.8+-green.svg" ></img>
	</a>
</p>

<center>
    <table>
        <thead>
            <tr>
                <td align="center" width="200"><a href="https://gitee.com/"><img src="https://gitee.com/logo_icon.png" width="30"></a></td>
                <td align="center" width="200"><a href="https://github.com"><img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/github.png" width="30"></a></td>
                <td align="center" width="200"><a href="https://weibo.com"><img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/weibo.png" width="30"></a></td>
                <td align="center" width="200"><a href="https://www.csdn.net/"><img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/csdn.png" width="30"></a></td>
                <td align="center" width="200"><a href="https://www.dingtalk.com"><img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/dingding.png" width="30"></a></td>
                <td align="center" width="200"><a href="https://connect.qq.com/devuser.html#/"><img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/qq.png" width="30"></a></td>
                <td align="center" width="200"><a href="https://mp.weixin.qq.com/cgi-bin/loginpage?t=wxm2-login&lang=zh_CN"><img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/wechats.png" width="30"></a></td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td align="center" width="200"><a href="#Gitee">Gitee</a></td>
                <td align="center" width="200"><a href="#Github">Github</a></td>
                <td align="center" width="200"><a href="#Weibo">Weibo</a></td>
                <td align="center" width="200"><a href="#CSDN">CSDN</a></td>
                <td align="center" width="200"><a href="#钉钉">钉钉</a></td>
                <td align="center" width="200"><a href="#QQ">QQ</a></td>
                <td align="center" width="200"><a href="#微信">微信</a></td>
            </tr>
        </tbody>
    </table>
</center>
-------------------------------------------------------------------------------



JustAuth，如你所见，它仅仅是一个**第三方授权登录**的**工具类库**，它可以让我们脱离繁琐的第三方登录SDK，让登录变得**So easy!**

## 快速使用
- 引入依赖
```xml
<dependency>
    <groupId>me.zhyd.oauth</groupId>
    <artifactId>JustAuth</artifactId>
    <version>1.0.0</version>
</dependency>
```
- 调用api
```java
AuthRequest authRequest = new AuthGiteeRequest(AuthConfig.builder()
        .clientId("clientId")
        .clientSecret("clientSecret")
        .redirectUri("redirectUri")
        .build());
// 自动跳转到授权页面
authRequest.authorize(response);
// 返回授权页面，可自行调整
authRequest.authorize();
```

#### API列表
|  :computer: 平台  |  :coffee: API类  |  :page_facing_up: SDK  |
|:------:|:-------:|:-------:|
|  <img src="https://gitee.com/logo_icon.png" width="20">  |  [AuthGiteeRequest](https://gitee.com/yadong.zhang/JustAuth/blob/master/src/main/java/me/zhyd/oauth/request/AuthGiteeRequest.java)  | [https://github.com/settings/developers](https://github.com/settings/developers) |
|  <img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/github.png" width="20">  |  [AuthGithubRequest](https://gitee.com/yadong.zhang/JustAuth/blob/master/src/main/java/me/zhyd/oauth/request/AuthGiteeRequest.java)  | [https://gitee.com/api/v5/oauth_doc#list_1](https://gitee.com/api/v5/oauth_doc#list_1)  |
|  <img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/weibo.png" width="20">  |  [AuthWeiboRequest](https://gitee.com/yadong.zhang/JustAuth/blob/master/src/main/java/me/zhyd/oauth/request/AuthGiteeRequest.java)  |  [https://open.weibo.com/apps](https://open.weibo.com/apps)  |
|  <img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/csdn.png" width="20">  |  AuthCsdnRequest  |  [https://connect.qq.com/](https://connect.qq.com/)  |
|  <img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/dingding.png" width="20">  |  AuthDingTalkRequest  |  待续  |
|  <img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/qq.png" width="20">  |  AuthQqRequest  |  待续  |
|  <img src="https://gitee.com/yadong.zhang/static/raw/master/JustAuth/wechats.png" width="20">  |  AuthWechatRequest  |  待续  |
