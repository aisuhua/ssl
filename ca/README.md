# CA 根证书

创建根证书，只需要执行一次，创建了就不需要再执行

```sh
../bin/cfssl genkey -initca ca-csr.json | cfssljson -bare ca
```
