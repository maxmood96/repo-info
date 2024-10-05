# `eclipse-mosquitto:2.0.19`

## Docker Metadata

- Image ID: `sha256:e7a8ea2ac6f8f42d38e36b5adbbb2c72b03edf051cb0fc27c41d2e1654978fd8`
- Created: `2024-10-02T10:16:48Z`
- Virtual Size: ~ 9.37 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/docker-entrypoint.sh"]`
- Command: `["/usr/sbin/mosquitto","-c","/mosquitto/config/mosquitto.conf"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `VERSION=2.0.19`
  - `DOWNLOAD_SHA256=33af3637f119a61c509c01d2f8f6cc3d8be76f49e850132f2860af142abf82a9`
  - `GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7`
  - `LWS_VERSION=4.2.1`
  - `LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51`
- Labels:
  - `description=Eclipse Mosquitto MQTT Broker`
  - `maintainer=Roger Light <roger@atchoo.org>`

## `apk` (`.apk`-based packages)

### `apk` package: `alpine-baselayout`

```console
alpine-baselayout-3.6.5-r0 description:
Alpine base dir structure and init scripts

alpine-baselayout-3.6.5-r0 webpage:
https://git.alpinelinux.org/cgit/aports/tree/main/alpine-baselayout

alpine-baselayout-3.6.5-r0 installed size:
308 KiB

alpine-baselayout-3.6.5-r0 license:
GPL-2.0-only

```

### `apk` package: `alpine-baselayout-data`

```console
alpine-baselayout-data-3.6.5-r0 description:
Alpine base dir structure and init scripts

alpine-baselayout-data-3.6.5-r0 webpage:
https://git.alpinelinux.org/cgit/aports/tree/main/alpine-baselayout

alpine-baselayout-data-3.6.5-r0 installed size:
76 KiB

alpine-baselayout-data-3.6.5-r0 license:
GPL-2.0-only

```

### `apk` package: `alpine-keys`

```console
alpine-keys-2.4-r1 description:
Public keys for Alpine Linux packages

alpine-keys-2.4-r1 webpage:
https://alpinelinux.org

alpine-keys-2.4-r1 installed size:
156 KiB

alpine-keys-2.4-r1 license:
MIT

```

### `apk` package: `apk-tools`

```console
apk-tools-2.14.4-r0 description:
Alpine Package Keeper - package manager for alpine

apk-tools-2.14.4-r0 webpage:
https://gitlab.alpinelinux.org/alpine/apk-tools

apk-tools-2.14.4-r0 installed size:
296 KiB

apk-tools-2.14.4-r0 license:
GPL-2.0-only

```

### `apk` package: `busybox`

```console
busybox-1.36.1-r29 description:
Size optimized toolbox of many common UNIX utilities

busybox-1.36.1-r29 webpage:
https://busybox.net/

busybox-1.36.1-r29 installed size:
908 KiB

busybox-1.36.1-r29 license:
GPL-2.0-only

```

### `apk` package: `busybox-binsh`

```console
busybox-binsh-1.36.1-r29 description:
busybox ash /bin/sh

busybox-binsh-1.36.1-r29 webpage:
https://busybox.net/

busybox-binsh-1.36.1-r29 installed size:
8192 B

busybox-binsh-1.36.1-r29 license:
GPL-2.0-only

```

### `apk` package: `ca-certificates`

```console
ca-certificates-20240705-r0 description:
Common CA certificates PEM files from Mozilla

ca-certificates-20240705-r0 webpage:
https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/

ca-certificates-20240705-r0 installed size:
712 KiB

ca-certificates-20240705-r0 license:
MPL-2.0 AND MIT

```

### `apk` package: `ca-certificates-bundle`

```console
ca-certificates-bundle-20240705-r0 description:
Pre generated bundle of Mozilla certificates

ca-certificates-bundle-20240705-r0 webpage:
https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/

ca-certificates-bundle-20240705-r0 installed size:
236 KiB

ca-certificates-bundle-20240705-r0 license:
MPL-2.0 AND MIT

```

### `apk` package: `cjson`

```console
cjson-1.7.18-r0 description:
Lighweight JSON parser in C

cjson-1.7.18-r0 webpage:
https://github.com/DaveGamble/cJSON

cjson-1.7.18-r0 installed size:
44 KiB

cjson-1.7.18-r0 license:
MIT

```

### `apk` package: `libcrypto3`

```console
libcrypto3-3.3.2-r0 description:
Crypto library from openssl

libcrypto3-3.3.2-r0 webpage:
https://www.openssl.org/

libcrypto3-3.3.2-r0 installed size:
4660 KiB

libcrypto3-3.3.2-r0 license:
Apache-2.0

```

### `apk` package: `libssl3`

```console
libssl3-3.3.2-r0 description:
SSL shared libraries

libssl3-3.3.2-r0 webpage:
https://www.openssl.org/

libssl3-3.3.2-r0 installed size:
796 KiB

libssl3-3.3.2-r0 license:
Apache-2.0

```

### `apk` package: `musl`

```console
musl-1.2.5-r0 description:
the musl c library (libc) implementation

musl-1.2.5-r0 webpage:
https://musl.libc.org/

musl-1.2.5-r0 installed size:
652 KiB

musl-1.2.5-r0 license:
MIT

```

### `apk` package: `musl-utils`

```console
musl-utils-1.2.5-r0 description:
the musl c library (libc) implementation

musl-utils-1.2.5-r0 webpage:
https://musl.libc.org/

musl-utils-1.2.5-r0 installed size:
128 KiB

musl-utils-1.2.5-r0 license:
MIT AND BSD-2-Clause AND GPL-2.0-or-later

```

### `apk` package: `scanelf`

```console
scanelf-1.3.7-r2 description:
Scan ELF binaries for stuff

scanelf-1.3.7-r2 webpage:
https://wiki.gentoo.org/wiki/Hardened/PaX_Utilities

scanelf-1.3.7-r2 installed size:
80 KiB

scanelf-1.3.7-r2 license:
GPL-2.0-only

```

### `apk` package: `ssl_client`

```console
ssl_client-1.36.1-r29 description:
EXternal ssl_client for busybox wget

ssl_client-1.36.1-r29 webpage:
https://busybox.net/

ssl_client-1.36.1-r29 installed size:
28 KiB

ssl_client-1.36.1-r29 license:
GPL-2.0-only

```

### `apk` package: `zlib`

```console
zlib-1.3.1-r1 description:
A compression/decompression Library

zlib-1.3.1-r1 webpage:
https://zlib.net/

zlib-1.3.1-r1 installed size:
108 KiB

zlib-1.3.1-r1 license:
Zlib

```
