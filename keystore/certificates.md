# Certificates

## Creation

Once the store has been created it can be used to generate a certificate.

```bash
keytool -certreq -keystore storeName.jks -alias someAlias -file test.csr
```

## Importing

```text
keytool -import -keystore storeName.jks -alias someAlias -file test.cer
```

