# example.com

生成可同时用于服务器 Server 和客户端 Client 双向认证的证书

```sh
../bin/cfssl gencert -ca=../ca/ca.pem -ca-key=../ca/ca-key.pem -config=../ca-config.json csr.json | cfssljson -bare example.com
```
