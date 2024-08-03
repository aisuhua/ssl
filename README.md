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

## 示例

给域名 sample.com 生成一个 https 证书

```sh
$ git clone git@github.com:aisuhua/ssl.git
$ cd ssl
$ mkdir sample.com
$ cd sample.com
$ vim csr.json
$ ../bin/cfssl gencert -ca=../ca/ca.pem -ca-key=../ca/ca-key.pem -config=../ca-config.json --profile=server csr.json | cfssljson -bare sample.com
$ ls
csr.json  sample.com.csr  sample.com-key.pem  sample.com.pem
```

详见 [sample.com](sample.com)

## 其他

查看证书内容

```sh
openssl x509 -in example.com/example.com.pem -text
```
