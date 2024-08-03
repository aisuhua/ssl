# *.example.com

生成泛域名证书

```sh
../bin/cfssl gencert -ca=../ca/ca.pem -ca-key=../ca/ca-key.pem -config=../ca-config.json csr.json | cfssljson -bare wildcard.example.com
```
