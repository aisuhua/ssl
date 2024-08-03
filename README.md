# ssl

用简单的方式管理证书

## 适用

- 测试环境
- 在安全性要求不高的内网环境，简化证书管理

## 特点

- 证书有效期 100 年
- 使用 cfssl 生成证书，即可通过配置（csr.json）管理证书
- 可结合 git 做版本管理

## 介绍

- bin 是 cfssl 命令行工具存放位置
- ca 目录是根证书存放位置
- ca-config.json 签发证书时的全局配置
- 每个证书一个目录，如 example.com 存放着给域名 example.com 签发的证书，签发步骤看 README.md 文件

## 查看证书内容

```sh
openssl x509 -in example.com/example.com.pem -text
```
