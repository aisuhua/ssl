# *.wildcard.net

生成一个支持双向认证的泛域名证书，可用于在内网部署时简化证书管理。

```sh
../bin/cfssl gencert -ca=../ca/ca.pem -ca-key=../ca/ca-key.pem -config=../ca-config.json csr.json | cfssljson -bare wildcard.net
```
