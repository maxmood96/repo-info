# `haproxy:2.1.2-alpine`

## Docker Metadata

- Image ID: `sha256:c4d28fe3a5325f64a518bb8fcdde7910b955b503ff5504e3f197554cb880fdc8`
- Created: `2019-12-23T17:22:40.483237341Z`
- Virtual Size: ~ 22.49 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/docker-entrypoint.sh"]`
- Command: `["haproxy","-f","/usr/local/etc/haproxy/haproxy.cfg"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `HAPROXY_VERSION=2.1.2`
  - `HAPROXY_URL=https://www.haproxy.org/download/2.1/src/haproxy-2.1.2.tar.gz`
  - `HAPROXY_SHA256=6079b08a8905ade5a9a2835ead8963ee10a855d8508a85efb7181eea2d310b77`

## `apk` (`.apk`-based packages)

### `apk` package: `alpine-baselayout`

```console
alpine-baselayout-3.1.2-r0 description:
Alpine base dir structure and init scripts

alpine-baselayout-3.1.2-r0 webpage:
https://git.alpinelinux.org/cgit/aports/tree/main/alpine-baselayout

alpine-baselayout-3.1.2-r0 installed size:
405504

alpine-baselayout-3.1.2-r0 license:
GPL-2.0-only

```

### `apk` package: `alpine-keys`

```console
alpine-keys-2.1-r2 description:
Public keys for Alpine Linux packages

alpine-keys-2.1-r2 webpage:
https://alpinelinux.org

alpine-keys-2.1-r2 installed size:
98304

alpine-keys-2.1-r2 license:
MIT

```

### `apk` package: `apk-tools`

```console
apk-tools-2.10.4-r2 description:
Alpine Package Keeper - package manager for alpine

apk-tools-2.10.4-r2 webpage:
https://git.alpinelinux.org/cgit/apk-tools/

apk-tools-2.10.4-r2 installed size:
262144

apk-tools-2.10.4-r2 license:
GPL2

```

### `apk` package: `busybox`

```console
busybox-1.30.1-r2 description:
Size optimized toolbox of many common UNIX utilities

busybox-1.30.1-r2 webpage:
https://busybox.net/

busybox-1.30.1-r2 installed size:
942080

busybox-1.30.1-r2 license:
GPL-2.0

```

### `apk` package: `ca-certificates-cacert`

```console
ca-certificates-cacert-20190108-r0 description:
Mozilla bundled certificates

ca-certificates-cacert-20190108-r0 webpage:
https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/

ca-certificates-cacert-20190108-r0 installed size:
245760

ca-certificates-cacert-20190108-r0 license:
MPL-2.0 GPL-2.0-or-later

```

### `apk` package: `libc-utils`

```console
libc-utils-0.7.1-r0 description:
Meta package to pull in correct libc

libc-utils-0.7.1-r0 webpage:
http://alpinelinux.org

libc-utils-0.7.1-r0 installed size:
4096

libc-utils-0.7.1-r0 license:
BSD

```

### `apk` package: `libcrypto1.1`

```console
libcrypto1.1-1.1.1d-r0 description:
Crypto library from openssl

libcrypto1.1-1.1.1d-r0 webpage:
https://www.openssl.org

libcrypto1.1-1.1.1d-r0 installed size:
2736128

libcrypto1.1-1.1.1d-r0 license:
OpenSSL

```

### `apk` package: `libssl1.1`

```console
libssl1.1-1.1.1d-r0 description:
SSL shared libraries

libssl1.1-1.1.1d-r0 webpage:
https://www.openssl.org

libssl1.1-1.1.1d-r0 installed size:
532480

libssl1.1-1.1.1d-r0 license:
OpenSSL

```

### `apk` package: `libtls-standalone`

```console
libtls-standalone-2.9.1-r0 description:
libtls extricated from libressl sources

libtls-standalone-2.9.1-r0 webpage:
https://www.libressl.org/

libtls-standalone-2.9.1-r0 installed size:
110592

libtls-standalone-2.9.1-r0 license:
ISC

```

### `apk` package: `lua5.3-libs`

```console
lua5.3-libs-5.3.5-r2 description:
Lua dynamic library runtime

lua5.3-libs-5.3.5-r2 webpage:
https://www.lua.org/

lua5.3-libs-5.3.5-r2 installed size:
221184

lua5.3-libs-5.3.5-r2 license:
MIT

```

### `apk` package: `musl`

```console
musl-1.1.22-r3 description:
the musl c library (libc) implementation

musl-1.1.22-r3 webpage:
http://www.musl-libc.org/

musl-1.1.22-r3 installed size:
598016

musl-1.1.22-r3 license:
MIT

```

### `apk` package: `musl-utils`

```console
musl-utils-1.1.22-r3 description:
the musl c library (libc) implementation

musl-utils-1.1.22-r3 webpage:
http://www.musl-libc.org/

musl-utils-1.1.22-r3 installed size:
147456

musl-utils-1.1.22-r3 license:
MIT BSD GPL2+

```

### `apk` package: `pcre2`

```console
pcre2-10.33-r0 description:
Perl-compatible regular expression library

pcre2-10.33-r0 webpage:
https://pcre.org/

pcre2-10.33-r0 installed size:
655360

pcre2-10.33-r0 license:
BSD-3-Clause

```

### `apk` package: `scanelf`

```console
scanelf-1.2.3-r0 description:
Scan ELF binaries for stuff

scanelf-1.2.3-r0 webpage:
https://wiki.gentoo.org/wiki/Hardened/PaX_Utilities

scanelf-1.2.3-r0 installed size:
98304

scanelf-1.2.3-r0 license:
GPL-2.0

```

### `apk` package: `ssl_client`

```console
ssl_client-1.30.1-r2 description:
EXternal ssl_client for busybox wget

ssl_client-1.30.1-r2 webpage:
https://busybox.net/

ssl_client-1.30.1-r2 installed size:
28672

ssl_client-1.30.1-r2 license:
GPL-2.0

```

### `apk` package: `zlib`

```console
zlib-1.2.11-r1 description:
A compression/decompression Library

zlib-1.2.11-r1 webpage:
http://zlib.net

zlib-1.2.11-r1 installed size:
110592

zlib-1.2.11-r1 license:
zlib

```
