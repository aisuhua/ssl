# client.example.com

生成客户端 Client 证书

```sh
# -profiles=client
../bin/cfssl gencert -ca=../ca/ca.pem -ca-key=../ca/ca-key.pem -config=../ca-config.json -profile=client csr.json | cfssljson -bare client.example.com
```
