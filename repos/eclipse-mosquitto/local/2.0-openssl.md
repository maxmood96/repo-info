# `eclipse-mosquitto:2.0.21`

## Docker Metadata

- Image ID: `sha256:35f50ba5c1109692c2b87b0bb401df076f4595e37a5284d23aad3f0caa257c77`
- Created: `2025-03-06T16:26:36Z`
- Virtual Size: ~ 9.89 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/docker-entrypoint.sh"]`
- Command: `["/usr/sbin/mosquitto","-c","/mosquitto/config/mosquitto.conf"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `VERSION=2.0.21`
  - `DOWNLOAD_SHA256=7ad5e84caeb8d2bb6ed0c04614b2a7042def961af82d87f688ba33db857b899d`
  - `GPG_KEYS=A0D6EEA1DCAE49A635A3B2F0779B22DFB3E717B7`
  - `LWS_VERSION=4.2.1`
  - `LWS_SHA256=842da21f73ccba2be59e680de10a8cce7928313048750eb6ad73b6fa50763c51`
- Labels:
  - `description=Eclipse Mosquitto MQTT Broker`
  - `maintainer=Roger Light <roger@atchoo.org>`

## `apk` (`.apk`-based packages)

### `apk` package: `alpine-baselayout`

```console
alpine-baselayout-3.6.8-r1 description:
Alpine base dir structure and init scripts

alpine-baselayout-3.6.8-r1 webpage:
https://git.alpinelinux.org/cgit/aports/tree/main/alpine-baselayout

alpine-baselayout-3.6.8-r1 installed size:
6532 B

alpine-baselayout-3.6.8-r1 license:
GPL-2.0-only

```

### `apk` package: `alpine-baselayout-data`

```console
alpine-baselayout-data-3.6.8-r1 description:
Alpine base dir structure and init scripts

alpine-baselayout-data-3.6.8-r1 webpage:
https://git.alpinelinux.org/cgit/aports/tree/main/alpine-baselayout

alpine-baselayout-data-3.6.8-r1 installed size:
18 KiB

alpine-baselayout-data-3.6.8-r1 license:
GPL-2.0-only

```

### `apk` package: `alpine-keys`

```console
alpine-keys-2.5-r0 description:
Public keys for Alpine Linux packages

alpine-keys-2.5-r0 webpage:
https://alpinelinux.org

alpine-keys-2.5-r0 installed size:
13 KiB

alpine-keys-2.5-r0 license:
MIT

```

### `apk` package: `alpine-release`

```console
alpine-release-3.21.3-r0 description:
Alpine release data

alpine-release-3.21.3-r0 webpage:
https://alpinelinux.org

alpine-release-3.21.3-r0 installed size:
346 B

alpine-release-3.21.3-r0 license:
MIT

```

### `apk` package: `apk-tools`

```console
apk-tools-2.14.6-r3 description:
Alpine Package Keeper - package manager for alpine

apk-tools-2.14.6-r3 webpage:
https://gitlab.alpinelinux.org/alpine/apk-tools

apk-tools-2.14.6-r3 installed size:
247 KiB

apk-tools-2.14.6-r3 license:
GPL-2.0-only

```

### `apk` package: `busybox`

```console
busybox-1.37.0-r12 description:
Size optimized toolbox of many common UNIX utilities

busybox-1.37.0-r12 webpage:
https://busybox.net/

busybox-1.37.0-r12 installed size:
798 KiB

busybox-1.37.0-r12 license:
GPL-2.0-only

```

### `apk` package: `busybox-binsh`

```console
busybox-binsh-1.37.0-r12 description:
busybox ash /bin/sh

busybox-binsh-1.37.0-r12 webpage:
https://busybox.net/

busybox-binsh-1.37.0-r12 installed size:
1 B

busybox-binsh-1.37.0-r12 license:
GPL-2.0-only

```

### `apk` package: `ca-certificates`

```console
ca-certificates-20241121-r1 description:
Common CA certificates PEM files from Mozilla

ca-certificates-20241121-r1 webpage:
https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/

ca-certificates-20241121-r1 installed size:
251 KiB

ca-certificates-20241121-r1 license:
MPL-2.0 AND MIT

```

### `apk` package: `ca-certificates-bundle`

```console
ca-certificates-bundle-20241121-r1 description:
Pre generated bundle of Mozilla certificates

ca-certificates-bundle-20241121-r1 webpage:
https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/

ca-certificates-bundle-20241121-r1 installed size:
217 KiB

ca-certificates-bundle-20241121-r1 license:
MPL-2.0 AND MIT

```

### `apk` package: `cjson`

```console
cjson-1.7.18-r0 description:
Lighweight JSON parser in C

cjson-1.7.18-r0 webpage:
https://github.com/DaveGamble/cJSON

cjson-1.7.18-r0 installed size:
29 KiB

cjson-1.7.18-r0 license:
MIT

```

### `apk` package: `libcrypto3`

```console
libcrypto3-3.3.3-r0 description:
Crypto library from openssl

libcrypto3-3.3.3-r0 webpage:
https://www.openssl.org/

libcrypto3-3.3.3-r0 installed size:
4607 KiB

libcrypto3-3.3.3-r0 license:
Apache-2.0

```

### `apk` package: `libssl3`

```console
libssl3-3.3.3-r0 description:
SSL shared libraries

libssl3-3.3.3-r0 webpage:
https://www.openssl.org/

libssl3-3.3.3-r0 installed size:
779 KiB

libssl3-3.3.3-r0 license:
Apache-2.0

```

### `apk` package: `musl`

```console
musl-1.2.5-r9 description:
the musl c library (libc) implementation

musl-1.2.5-r9 webpage:
https://musl.libc.org/

musl-1.2.5-r9 installed size:
646 KiB

musl-1.2.5-r9 license:
MIT

```

### `apk` package: `musl-utils`

```console
musl-utils-1.2.5-r9 description:
the musl c library (libc) implementation

musl-utils-1.2.5-r9 webpage:
https://musl.libc.org/

musl-utils-1.2.5-r9 installed size:
102 KiB

musl-utils-1.2.5-r9 license:
MIT AND BSD-2-Clause AND GPL-2.0-or-later

```

### `apk` package: `scanelf`

```console
scanelf-1.3.8-r1 description:
Scan ELF binaries for stuff

scanelf-1.3.8-r1 webpage:
https://wiki.gentoo.org/wiki/Hardened/PaX_Utilities

scanelf-1.3.8-r1 installed size:
65 KiB

scanelf-1.3.8-r1 license:
GPL-2.0-only

```

### `apk` package: `ssl_client`

```console
ssl_client-1.37.0-r12 description:
External ssl_client for busybox wget

ssl_client-1.37.0-r12 webpage:
https://busybox.net/

ssl_client-1.37.0-r12 installed size:
14 KiB

ssl_client-1.37.0-r12 license:
GPL-2.0-only

```

### `apk` package: `tzdata`

```console
tzdata-2025a-r0 description:
Timezone data

tzdata-2025a-r0 webpage:
https://www.iana.org/time-zones

tzdata-2025a-r0 installed size:
433 KiB

tzdata-2025a-r0 license:
Public-Domain

```

### `apk` package: `zlib`

```console
zlib-1.3.1-r2 description:
A compression/decompression Library

zlib-1.3.1-r2 webpage:
https://zlib.net/

zlib-1.3.1-r2 installed size:
101 KiB

zlib-1.3.1-r2 license:
Zlib

```
