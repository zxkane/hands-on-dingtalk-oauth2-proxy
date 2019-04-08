## Kubernetes中使用基于[钉钉认证][dingtalk-auth]的[oauth2 proxy][oauth2-proxy]为Web站点实现认证及授权

### 模块简介

- [Nginx Ingress Controller][nginx-ingress]为K8S集群内Web应用提供反向代理，以及为站点实现外部认证。
- 简单的Web站点，基于[Nginx docker容器][docker-nginx]。该站点默认没有认证及授权功能，使用外部[钉钉][dingtalk-auth]应用作为认证及授权。
- [OAuth2 Proxy on Dingtalk][dingtalk-oauth2-proxy]提供基于[钉钉][dingtalk-auth]应用的扫码认证及授权，只有认证且授权的用户才可以访问上面的Web站点。

完整部署步骤，查看[这里][blog-post]。

[dingtalk-auth]: https://open-doc.dingtalk.com/microapp/serverapi2/kymkv6
[oauth2-proxy]: https://github.com/bitly/oauth2_proxy
[nginx-ingress]: https://github.com/kubernetes/ingress-nginx
[docker-nginx]: https://hub.docker.com/_/nginx
[dingtalk-oauth2-proxy]: https://github.com/zxkane/oauth2_proxy
[blog-post]: https://kane.mx/posts/effective-cloud-computing/oauth2-proxy-on-kubernetes/part2/
