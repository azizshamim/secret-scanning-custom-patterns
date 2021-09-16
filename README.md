# demo-secrets-geekmasher

Custom Secret Scanning Repo - @GeekMasher


## Samples

### SSH (private keys)

```
--BEGIN OPENSSH PRIVATE KEY--+[a-zA-Z0-9+/=\s]+--+END OPENSSH PRIVATE KEY--
```

### GPG (private key)

```
--BEGIN PGP PRIVATE KEY BLOCK--+[a-zA-Z0-9+/=\s]+--+END PGP PRIVATE KEY BLOCK--
```

### URI Strings

```
[0-9A-Za-z]+
```

**Before Secret**

```
\A|(A-Za-z0-9)?://[^/?#:]*:
```

**After Secret**

```
\z|[@]
```

### SendGrid

```
SG\.[a-zA-Z0-9-]*\.[a-zA-Z0-9-]*
```
