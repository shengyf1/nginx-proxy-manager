![Nginx Proxy Manager](https://public.jc21.com/nginx-proxy-manager/github.png "Nginx Proxy Manager")

# Nginx代理管理器

![Version](https://img.shields.io/badge/version-2.0.14-green.svg?style=for-the-badge)
![Stars](https://img.shields.io/docker/stars/jc21/nginx-proxy-manager.svg?style=for-the-badge)
![Pulls](https://img.shields.io/docker/pulls/jc21/nginx-proxy-manager.svg?style=for-the-badge)

该项目是一个预先构建的docker映像，使您可以轻松转发到在家中或其他情况下运行的网站，包括免费的SSL，而无需对Nginx或Letsencrypt有所了解。


## 项目目标

我创建此项目是为了满足个人需要，即为用户提供一种轻松的方法来完成具有SSL终止的反向代理主机，并且它必须非常容易，猴子才能做到。 这个目标没有改变。
尽管可能有高级选项，但它们是可选的，并且项目应尽可能简单，以使进入此处的障碍很小。

<a href="https://www.buymeacoffee.com/jc21" target="_blank"><img src="http://public.jc21.com/github/by-me-a-coffee.png" alt="Buy Me A Coffee" style="height: 51px !important;width: 217px !important;" ></a>


## 特点

- 基于[Tabler]（https://tabler.github.io/）的美观且安全的管理界面
- 无需了解Nginx即可轻松创建转发域，重定向，流和404主机
- 使用“让我们加密”或提供您自己的自定义SSL证书的免费SSL
- 主机的访问列表和基本HTTP身份验证
- 高级Nginx配置可供超级用户使用
- 用户管理，权限和审核日志


## 截图

[![Login](https://public.jc21.com/nginx-proxy-manager/v2/small/login.jpg "Login")](https://public.jc21.com/nginx-proxy-manager/v2/large/login.jpg)
[![Dashboard](https://public.jc21.com/nginx-proxy-manager/v2/small/dashboard.jpg "Dashboard")](https://public.jc21.com/nginx-proxy-manager/v2/large/dashboard.jpg)
[![Proxy Hosts](https://public.jc21.com/nginx-proxy-manager/v2/small/proxy-hosts.jpg "Proxy Hosts")](https://public.jc21.com/nginx-proxy-manager/v2/large/proxy-hosts.jpg)
[![Proxy Host Settings](https://public.jc21.com/nginx-proxy-manager/v2/small/proxy-hosts-new1.jpg "Proxy Host Settings")](https://public.jc21.com/nginx-proxy-manager/v2/large/proxy-hosts-new1.jpg)
[![Proxy Host SSL](https://public.jc21.com/nginx-proxy-manager/v2/small/proxy-hosts-new2.jpg "Proxy Host SSL")](https://public.jc21.com/nginx-proxy-manager/v2/large/proxy-hosts-new2.jpg)
[![Redirection Hosts](https://public.jc21.com/nginx-proxy-manager/v2/small/redirection-hosts.jpg "Redirection Hosts")](https://public.jc21.com/nginx-proxy-manager/v2/large/redirection-hosts.jpg)
[![Redirection Host Settings](https://public.jc21.com/nginx-proxy-manager/v2/small/redirection-hosts-new1.jpg "Redirection Host Settings")](https://public.jc21.com/nginx-proxy-manager/v2/large/redirection-hosts-new1.jpg)
[![Streams](https://public.jc21.com/nginx-proxy-manager/v2/small/streams.jpg "Streams")](https://public.jc21.com/nginx-proxy-manager/v2/large/streams.jpg)
[![Stream Settings](https://public.jc21.com/nginx-proxy-manager/v2/small/streams-new1.jpg "Stream Settings")](https://public.jc21.com/nginx-proxy-manager/v2/large/streams-new1.jpg)
[![404 Hosts](https://public.jc21.com/nginx-proxy-manager/v2/small/dead-hosts.jpg "404 Hosts")](https://public.jc21.com/nginx-proxy-manager/v2/large/dead-hosts.jpg)
[![404 Host Settings](https://public.jc21.com/nginx-proxy-manager/v2/small/dead-hosts-new1.jpg "404 Host Settings")](https://public.jc21.com/nginx-proxy-manager/v2/large/dead-hosts-new1.jpg)
[![Certificates](https://public.jc21.com/nginx-proxy-manager/v2/small/certificates.jpg "Certificates")](https://public.jc21.com/nginx-proxy-manager/v2/large/certificates.jpg)
[![Lets Encrypt Certificates](https://public.jc21.com/nginx-proxy-manager/v2/small/certificates-new1.jpg "Lets Encrypt Certificates")](https://public.jc21.com/nginx-proxy-manager/v2/large/certificates-new1.jpg)
[![Custom Certificates](https://public.jc21.com/nginx-proxy-manager/v2/small/certificates-new2.jpg "Custom Certificates")](https://public.jc21.com/nginx-proxy-manager/v2/large/certificates-new2.jpg)
[![Access Lists](https://public.jc21.com/nginx-proxy-manager/v2/small/access-lists.jpg "Access Lists")](https://public.jc21.com/nginx-proxy-manager/v2/large/access-lists.jpg)
[![Access List Users](https://public.jc21.com/nginx-proxy-manager/v2/small/access-lists-new1.jpg "Access List Users")](https://public.jc21.com/nginx-proxy-manager/v2/large/access-lists-new1.jpg)
[![Users](https://public.jc21.com/nginx-proxy-manager/v2/small/users.jpg "Users")](https://public.jc21.com/nginx-proxy-manager/v2/large/users.jpg)
[![User Permissions](https://public.jc21.com/nginx-proxy-manager/v2/small/users-permissions.jpg "User Permissions")](https://public.jc21.com/nginx-proxy-manager/v2/large/users-permissions.jpg)
[![Audit Log](https://public.jc21.com/nginx-proxy-manager/v2/small/audit-log.jpg "Audit Log")](https://public.jc21.com/nginx-proxy-manager/v2/large/audit-log.jpg)


## 开始

请查阅[安装说明]（doc/INSTALL.md）以获得完整的指南，
或者，如果您只想以最快的速度启动并运行，请抓取`doc/example/`文件夹中的所有文件并运行`docker-compose up -d`


## 管理

当docker容器已经运行，连接到`81`端口来访问管理界面.

[http://localhost:81](http://localhost:81)

注意：请求SSL证书只有从外部访问才能生效，如下所述。


### 默认管理用户

```
Email:    admin@example.com
Password: changeme
```

使用该默认用户登录后，将立即要求您修改详细信息并更改密码。


## 托管家庭网络

在这里，我将不做过多介绍，仅对自管理服务器的新手做个基本介绍。

1. 您的家用路由器将在某处具有“端口转发”部分。 登录并找到它
2. 将端口80和443的端口转发添加到托管该项目的服务器
3. 使用静态IP或DuckDNS之类的服务，将您的域名详细信息配置为指向您的家庭网络
4. 使用此处的Nginx代理管理器作为网关，以转发到其他基于Web的服务


## Nginx管理服务器 Proxy Manager in the wild

随着该软件的普及，通常会看到它与其他平台集成在一起。 请注意，除非这些集成的文档中特别提及，否则我将*不支持*它们，即使看起来像这些集成页面上的任何捐赠链接也不会出现。

Known integrations:

- [HomeAssistant Hass.io plugin](https://github.com/hassio-addons/addon-nginx-proxy-manager)
- [UnRaid / Synology](https://github.com/jlesage/docker-nginx-proxy-manager)
