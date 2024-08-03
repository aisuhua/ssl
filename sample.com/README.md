# sample.com

给域名 sample.com 生成一个服务端 Server 证书

```sh
../bin/cfssl gencert -ca=../ca/ca.pem -ca-key=../ca/ca-key.pem -config=../ca-config.json --profile=server csr.json | cfssljson -bare sample.com
```
