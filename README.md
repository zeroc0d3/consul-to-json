# consul-to-json

Consul KV-store backup and restore utility.

## Instalation
```bash
npm install -g consul-to-json
```

## Usage


```
  Usage: consul-to-json [options] [command]

  Commands:

    backup [options] [file]   backup consul keystory from specified key to JSON file
    restore [options] [file]  restore JSON dump of consul to specified key. Defaults to restoring to root of keystore
```

### Backup

```
  Usage: backup [options] [file]

  backup consul keystory from specified key to JSON file

  Options:

    -h, --help          output usage information
    -k, --key <key>     specify key to backup from
    -p, --preety-print  preety-print JSON
    --type-mapping      perform type-mapping of kv structure based on consul-kv-object flagmapping
    --host <host>       consul host to use, defaults to 127.0.0.1
    --port <port>       consul port to use, defaults to 8500
    --secure            use HTTPS to connect to consul
```

### Restore

```
  Usage: restore [options] [file]

  restore JSON dump of consul to specified key. Defaults to restoring to root of keystore

  Options:

    -h, --help       output usage information
    -k, --key <key>  specify key to backup to
    -d, --delete     delete consul kv under specified key
    --type-mapping   perform type-mapping of kv structure based on consul-kv-object flagmapping
    --host <host>    consul host to use, defaults to 127.0.0.1
    --port <port>    consul port to use, defaults to 8500
    --secure         use HTTPS to connect to consul
```

