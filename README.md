![](images/logo.png)
# NetDiscovery

[![@Tony沈哲 on weibo](https://img.shields.io/badge/weibo-%40Tony%E6%B2%88%E5%93%B2-blue.svg)](http://www.weibo.com/fengzhizi715)
[![License](https://img.shields.io/badge/license-Apache%202-lightgrey.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

# 最新版本

模块|netdiscovery-core|netdiscovery-extra|netdiscovery-selenium
---|:-------------:|:-------------:|:-------------:
最新版本| [ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-core/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-core/_latestVersion)| [ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-extra/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-extra/_latestVersion)|[ ![Download](https://api.bintray.com/packages/fengzhizi715/maven/netdiscovery-selenium/images/download.svg) ](https://bintray.com/fengzhizi715/maven/netdiscovery-selenium/_latestVersion)

NetDiscovery目前还是早期的版本，很多的细节需要不断地完善。

# NetDiscovery 功能点：
## 1.Spider功能
Spider可以单独使用，也可以添加到SpiderEngine中使用。

Spider中内置了很多组件。例如downloader就已经支持了好几种，可以热插拔随时替换，或者编写自己的downloader。

queue、parser、pipeline也都类似。

![](images/Spider.png)

在调试的时候，可以使用ConsolePipeline或者DebugPipeline

DebugPipeline的效果如下

![](images/DebugPipeline.jpg)

## 2.SpiderEngine功能
SpiderEngine可以管理引擎中的爬虫，包括爬虫的生命周期。
![](images/SpiderEngine.png)


### 2.1 获取某个爬虫的状态
http://localhost:{port}/netdiscovery/spider/{spiderName}

类型：GET

### 2.2 获取SpiderEngine中所有爬虫的状态
http://localhost:{port}/netdiscovery/spiders/

类型：GET

### 2.3 修改某个爬虫的状态
http://localhost:{port}/netdiscovery/spider/{spiderName}/status

类型：POST

参数说明：

```java
{
    "status":2   //让爬虫暂停
}
```

|status       | 作用        |
|:-------------|:-------------|
|2|让爬虫暂停|
|3|让爬虫从暂停中恢复|
|4|让爬虫停止|

## 3. admin模块
admin模块可以监控线上的爬虫运行情况，并进行管理。前端部分使用vue的elementUI框架进行开发。

下图是使用admin模块的例子

![](images/NetDiscovery-admin.jpeg)

# NetDiscovery 基本原理：
## 1.基本原理
![](images/basic_principle.png)

## 2.集群原理
![](images/cluster_principle.png)

# 案例:
* [user-agent-list](https://github.com/fengzhizi715/user-agent-list):抓取常用浏览器的user agent

# TODO:
1. 增加对登录验证码的识别
2. 增加elasticsearch的支持

# 联系方式:
QQ交流群：490882934
