# Generation

## Creating a Store

The JDK includes a tool for creating KeyStores.

```bash
keytool -keystore storeName.jks -genkey -alias storeAlias
```

### Defining Type

```bash
keytool -keystore storeName.jks -genkey -alias storeAlias -Dkeystore.type=pkcs12
```

