# server.example.com

生成服务端 Server 证书

```sh
# -profile=server
../bin/cfssl gencert -ca=../ca/ca.pem -ca-key=../ca/ca-key.pem -config=../ca-config.json -profile=server csr.json | cfssljson -bare server.example.com
```
