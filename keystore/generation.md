# Generation

## Creating a Store

The JDK includes a tool for creating KeyStores.

```bash
keytool -keystore storeName.jks -genkey -alias someAlias
```

### Defining Type

```bash
keytool -keystore storeName.jks -genkey -alias someAlias -Dkeystore.type=pkcs12
```

