# `bonita:2025.1-u0`

## Docker Metadata

- Image ID: `sha256:9bb88ba891f1d087a1908a91261b3ef4559ae3a66c545052d32f9d94967d088f`
- Created: `2025-11-08T18:40:22.331573805Z`
- Virtual Size: ~ 347.24 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["/__cacert_entrypoint.sh","/opt/files/startup.sh"]`
- Command: `["/opt/bonita/server/bin/catalina.sh","run"]`
- Environment:
  - `PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `JAVA_HOME=/opt/java/openjdk`
  - `LANG=en_US.UTF-8`
  - `LANGUAGE=en_US:en`
  - `LC_ALL=en_US.UTF-8`
  - `JAVA_VERSION=jdk-21.0.9+10`
  - `BONITA_VERSION=10.3.0`
  - `BRANDING_VERSION=2025.1-u0`
  - `BONITA_SHA256=44c078fad0ffeec0afac2bf512040be16af4b722369039fe3daef1c091594637`
  - `ZIP_FILE=BonitaCommunity-2025.1-u0.zip`
  - `BASE_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat`
  - `BONITA_URL=https://search.maven.org/remotecontent?filepath=org/bonitasoft/distrib/bundle-tomcat/10.3.0/bundle-tomcat-10.3.0.zip`
  - `HTTP_API=false`
  - `HTTP_API_USERNAME=http-api`
  - `HTTP_API_PASSWORD=`
  - `MONITORING_USERNAME=monitoring`
  - `MONITORING_PASSWORD=mon1tor1ng_adm1n`
  - `JMX_REMOTE_ACCESS=false`
  - `REMOTE_IP_VALVE_ENABLED=false`
  - `ACCESSLOGS_STDOUT_ENABLED=false`
  - `ACCESSLOGS_FILES_ENABLED=false`
  - `ACCESSLOGS_PATH=/opt/bonita/logs`
  - `ACCESSLOGS_PATH_APPEND_HOSTNAME=false`
  - `ACCESSLOGS_MAX_DAYS=30`
  - `HTTP_MAX_THREADS=20`
- Labels:
  - `maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>`

## `apk` (`.apk`-based packages)

### `apk` package: `acl-libs`

```console
acl-libs-2.3.2-r1 description:
Access control list utilities (libraries)

acl-libs-2.3.2-r1 webpage:
https://savannah.nongnu.org/projects/acl

acl-libs-2.3.2-r1 installed size:
33 KiB

acl-libs-2.3.2-r1 license:
LGPL-2.1-or-later AND GPL-2.0-or-later

```

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
alpine-release-3.21.5-r0 description:
Alpine release data

alpine-release-3.21.5-r0 webpage:
https://alpinelinux.org

alpine-release-3.21.5-r0 installed size:
346 B

alpine-release-3.21.5-r0 license:
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

### `apk` package: `bash`

```console
bash-5.2.37-r0 description:
The GNU Bourne Again shell

bash-5.2.37-r0 webpage:
https://www.gnu.org/software/bash/bash.html

bash-5.2.37-r0 installed size:
1243 KiB

bash-5.2.37-r0 license:
GPL-3.0-or-later

```

### `apk` package: `brotli-libs`

```console
brotli-libs-1.1.0-r2 description:
Generic lossless compressor (libraries)

brotli-libs-1.1.0-r2 webpage:
https://github.com/google/brotli

brotli-libs-1.1.0-r2 installed size:
913 KiB

brotli-libs-1.1.0-r2 license:
MIT

```

### `apk` package: `busybox`

```console
busybox-1.37.0-r13 description:
Size optimized toolbox of many common UNIX utilities

busybox-1.37.0-r13 webpage:
https://busybox.net/

busybox-1.37.0-r13 installed size:
798 KiB

busybox-1.37.0-r13 license:
GPL-2.0-only

```

### `apk` package: `busybox-binsh`

```console
busybox-binsh-1.37.0-r13 description:
busybox ash /bin/sh

busybox-binsh-1.37.0-r13 webpage:
https://busybox.net/

busybox-binsh-1.37.0-r13 installed size:
1 B

busybox-binsh-1.37.0-r13 license:
GPL-2.0-only

```

### `apk` package: `c-ares`

```console
c-ares-1.34.5-r0 description:
Asynchronous DNS/names resolver library

c-ares-1.34.5-r0 webpage:
https://c-ares.org/

c-ares-1.34.5-r0 installed size:
233 KiB

c-ares-1.34.5-r0 license:
MIT

```

### `apk` package: `ca-certificates`

```console
ca-certificates-20250911-r0 description:
Common CA certificates PEM files from Mozilla

ca-certificates-20250911-r0 webpage:
https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/

ca-certificates-20250911-r0 installed size:
248 KiB

ca-certificates-20250911-r0 license:
MPL-2.0 AND MIT

```

### `apk` package: `ca-certificates-bundle`

```console
ca-certificates-bundle-20250911-r0 description:
Pre generated bundle of Mozilla certificates

ca-certificates-bundle-20250911-r0 webpage:
https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/

ca-certificates-bundle-20250911-r0 installed size:
214 KiB

ca-certificates-bundle-20250911-r0 license:
MPL-2.0 AND MIT

```

### `apk` package: `coreutils`

```console
coreutils-9.5-r2 description:
The basic file, shell and text manipulation utilities

coreutils-9.5-r2 webpage:
https://www.gnu.org/software/coreutils/

coreutils-9.5-r2 installed size:
1006 KiB

coreutils-9.5-r2 license:
GPL-3.0-or-later

```

### `apk` package: `coreutils-env`

```console
coreutils-env-9.5-r2 description:
The basic file, shell and text manipulation utilities

coreutils-env-9.5-r2 webpage:
https://www.gnu.org/software/coreutils/

coreutils-env-9.5-r2 installed size:
46 KiB

coreutils-env-9.5-r2 license:
GPL-3.0-or-later

```

### `apk` package: `coreutils-fmt`

```console
coreutils-fmt-9.5-r2 description:
The basic file, shell and text manipulation utilities

coreutils-fmt-9.5-r2 webpage:
https://www.gnu.org/software/coreutils/

coreutils-fmt-9.5-r2 installed size:
42 KiB

coreutils-fmt-9.5-r2 license:
GPL-3.0-or-later

```

### `apk` package: `coreutils-sha512sum`

```console
coreutils-sha512sum-9.5-r2 description:
The basic file, shell and text manipulation utilities

coreutils-sha512sum-9.5-r2 webpage:
https://www.gnu.org/software/coreutils/

coreutils-sha512sum-9.5-r2 installed size:
46 KiB

coreutils-sha512sum-9.5-r2 license:
GPL-3.0-or-later

```

### `apk` package: `curl`

```console
curl-8.14.1-r2 description:
URL retrival utility and library

curl-8.14.1-r2 webpage:
https://curl.se/

curl-8.14.1-r2 installed size:
260 KiB

curl-8.14.1-r2 license:
curl

```

### `apk` package: `encodings`

```console
encodings-1.0.7-r1 description:
X.org font encoding files

encodings-1.0.7-r1 webpage:
https://xorg.freedesktop.org/

encodings-1.0.7-r1 installed size:
630 KiB

encodings-1.0.7-r1 license:
Public Domain

```

### `apk` package: `font-dejavu`

```console
font-dejavu-2.37-r5 description:
Font family based on the Bitstream Vera Fonts with a wider range of characters

font-dejavu-2.37-r5 webpage:
https://dejavu-fonts.github.io/

font-dejavu-2.37-r5 installed size:
9990 KiB

font-dejavu-2.37-r5 license:
Bitstream-Vera

```

### `apk` package: `fontconfig`

```console
fontconfig-2.15.0-r1 description:
Library for configuring and customizing font access

fontconfig-2.15.0-r1 webpage:
https://www.freedesktop.org/wiki/Software/fontconfig

fontconfig-2.15.0-r1 installed size:
515 KiB

fontconfig-2.15.0-r1 license:
MIT

```

### `apk` package: `freetype`

```console
freetype-2.13.3-r0 description:
TrueType font rendering library

freetype-2.13.3-r0 webpage:
https://www.freetype.org/

freetype-2.13.3-r0 installed size:
646 KiB

freetype-2.13.3-r0 license:
FTL OR GPL-2.0-or-later

```

### `apk` package: `gdbm`

```console
gdbm-1.24-r0 description:
GNU dbm is a set of database routines that use extensible hashing

gdbm-1.24-r0 webpage:
https://www.gnu.org/software/gdbm/

gdbm-1.24-r0 installed size:
67 KiB

gdbm-1.24-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gmp`

```console
gmp-6.3.0-r2 description:
free library for arbitrary precision arithmetic

gmp-6.3.0-r2 webpage:
https://gmplib.org/

gmp-6.3.0-r2 installed size:
417 KiB

gmp-6.3.0-r2 license:
LGPL-3.0-or-later OR GPL-2.0-or-later

```

### `apk` package: `gnupg`

```console
gnupg-2.4.7-r0 description:
GNU Privacy Guard 2 - meta package for full GnuPG suite

gnupg-2.4.7-r0 webpage:
https://www.gnupg.org/

gnupg-2.4.7-r0 installed size:
0 B

gnupg-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gnupg-dirmngr`

```console
gnupg-dirmngr-2.4.7-r0 description:
GNU Privacy Guard 2 - network certificate management service

gnupg-dirmngr-2.4.7-r0 webpage:
https://www.gnupg.org/

gnupg-dirmngr-2.4.7-r0 installed size:
629 KiB

gnupg-dirmngr-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gnupg-gpgconf`

```console
gnupg-gpgconf-2.4.7-r0 description:
GNU Privacy Guard 2 - core configuration utilities

gnupg-gpgconf-2.4.7-r0 webpage:
https://www.gnupg.org/

gnupg-gpgconf-2.4.7-r0 installed size:
237 KiB

gnupg-gpgconf-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gnupg-keyboxd`

```console
gnupg-keyboxd-2.4.7-r0 description:
GNU Privacy Guard 2 - keyboxd manager

gnupg-keyboxd-2.4.7-r0 webpage:
https://www.gnupg.org/

gnupg-keyboxd-2.4.7-r0 installed size:
223 KiB

gnupg-keyboxd-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gnupg-utils`

```console
gnupg-utils-2.4.7-r0 description:
GNU Privacy Guard 2 - utility programs

gnupg-utils-2.4.7-r0 webpage:
https://www.gnupg.org/

gnupg-utils-2.4.7-r0 installed size:
832 KiB

gnupg-utils-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gnupg-wks-client`

```console
gnupg-wks-client-2.4.7-r0 description:
GNU Privacy Guard 2 - Web Key Service client

gnupg-wks-client-2.4.7-r0 webpage:
https://www.gnupg.org/

gnupg-wks-client-2.4.7-r0 installed size:
167 KiB

gnupg-wks-client-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gnutls`

```console
gnutls-3.8.8-r0 description:
TLS protocol implementation

gnutls-3.8.8-r0 webpage:
https://www.gnutls.org/

gnutls-3.8.8-r0 installed size:
1865 KiB

gnutls-3.8.8-r0 license:
LGPL-2.1-or-later

```

### `apk` package: `gpg`

```console
gpg-2.4.7-r0 description:
GNU Privacy Guard 2 - public key operations only

gpg-2.4.7-r0 webpage:
https://www.gnupg.org/

gpg-2.4.7-r0 installed size:
929 KiB

gpg-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gpg-agent`

```console
gpg-agent-2.4.7-r0 description:
GNU Privacy Guard 2 - cryptographic agent

gpg-agent-2.4.7-r0 webpage:
https://www.gnupg.org/

gpg-agent-2.4.7-r0 installed size:
642 KiB

gpg-agent-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gpg-wks-server`

```console
gpg-wks-server-2.4.7-r0 description:
GNU Privacy Guard 2 - Web Key Service server

gpg-wks-server-2.4.7-r0 webpage:
https://www.gnupg.org/

gpg-wks-server-2.4.7-r0 installed size:
150 KiB

gpg-wks-server-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gpgsm`

```console
gpgsm-2.4.7-r0 description:
GNU Privacy Guard 2 - S/MIME version

gpgsm-2.4.7-r0 webpage:
https://www.gnupg.org/

gpgsm-2.4.7-r0 installed size:
481 KiB

gpgsm-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `gpgv`

```console
gpgv-2.4.7-r0 description:
GNU Privacy Guard 2 - signature verification only

gpgv-2.4.7-r0 webpage:
https://www.gnupg.org/

gpgv-2.4.7-r0 installed size:
428 KiB

gpgv-2.4.7-r0 license:
GPL-3.0-or-later

```

### `apk` package: `jattach`

```console
jattach-2.1-r0 description:
JVM dynamic attach utility

jattach-2.1-r0 webpage:
https://github.com/apangin/jattach

jattach-2.1-r0 installed size:
21 KiB

jattach-2.1-r0 license:
Apache-2.0

```

### `apk` package: `libassuan`

```console
libassuan-2.5.7-r0 description:
IPC library used by some GnuPG related software

libassuan-2.5.7-r0 webpage:
https://www.gnupg.org/software/libassuan/index.html

libassuan-2.5.7-r0 installed size:
66 KiB

libassuan-2.5.7-r0 license:
LGPL-2.1-or-later

```

### `apk` package: `libattr`

```console
libattr-2.5.2-r2 description:
utilities for managing filesystem extended attributes (libraries)

libattr-2.5.2-r2 webpage:
https://savannah.nongnu.org/projects/attr

libattr-2.5.2-r2 installed size:
21 KiB

libattr-2.5.2-r2 license:
LGPL-2.1-or-later

```

### `apk` package: `libbz2`

```console
libbz2-1.0.8-r6 description:
Shared library for bz2

libbz2-1.0.8-r6 webpage:
https://sourceware.org/bzip2/

libbz2-1.0.8-r6 installed size:
72 KiB

libbz2-1.0.8-r6 license:
bzip2-1.0.6

```

### `apk` package: `libcrypto3`

```console
libcrypto3-3.3.5-r0 description:
Crypto library from openssl

libcrypto3-3.3.5-r0 webpage:
https://www.openssl.org/

libcrypto3-3.3.5-r0 installed size:
4607 KiB

libcrypto3-3.3.5-r0 license:
Apache-2.0

```

### `apk` package: `libcurl`

```console
libcurl-8.14.1-r2 description:
The multiprotocol file transfer library

libcurl-8.14.1-r2 webpage:
https://curl.se/

libcurl-8.14.1-r2 installed size:
669 KiB

libcurl-8.14.1-r2 license:
curl

```

### `apk` package: `libexpat`

```console
libexpat-2.7.3-r0 description:
XML Parser library written in C (libraries)

libexpat-2.7.3-r0 webpage:
https://libexpat.github.io/

libexpat-2.7.3-r0 installed size:
133 KiB

libexpat-2.7.3-r0 license:
MIT

```

### `apk` package: `libffi`

```console
libffi-3.4.7-r0 description:
portable, high level programming interface to various calling conventions.

libffi-3.4.7-r0 webpage:
https://sourceware.org/libffi/

libffi-3.4.7-r0 installed size:
38 KiB

libffi-3.4.7-r0 license:
MIT

```

### `apk` package: `libfontenc`

```console
libfontenc-1.1.8-r0 description:
X11 font encoding library

libfontenc-1.1.8-r0 webpage:
https://xorg.freedesktop.org/

libfontenc-1.1.8-r0 installed size:
25 KiB

libfontenc-1.1.8-r0 license:
MIT

```

### `apk` package: `libgcrypt`

```console
libgcrypt-1.10.3-r1 description:
General purpose crypto library based on the code used in GnuPG

libgcrypt-1.10.3-r1 webpage:
https://www.gnupg.org/

libgcrypt-1.10.3-r1 installed size:
1157 KiB

libgcrypt-1.10.3-r1 license:
LGPL-2.1-or-later AND GPL-2.0-or-later

```

### `apk` package: `libgpg-error`

```console
libgpg-error-1.51-r0 description:
Support library for libgcrypt

libgpg-error-1.51-r0 webpage:
https://www.gnupg.org/

libgpg-error-1.51-r0 installed size:
160 KiB

libgpg-error-1.51-r0 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `libidn2`

```console
libidn2-2.3.7-r0 description:
Encode/Decode library for internationalized domain names

libidn2-2.3.7-r0 webpage:
https://www.gnu.org/software/libidn#libidn2

libidn2-2.3.7-r0 installed size:
193 KiB

libidn2-2.3.7-r0 license:
GPL-2.0-or-later OR LGPL-3.0-or-later

```

### `apk` package: `libintl`

```console
libintl-0.22.5-r0 description:
GNU gettext runtime library

libintl-0.22.5-r0 webpage:
https://www.gnu.org/software/gettext/gettext.html

libintl-0.22.5-r0 installed size:
65 KiB

libintl-0.22.5-r0 license:
LGPL-2.1-or-later

```

### `apk` package: `libksba`

```console
libksba-1.6.7-r0 description:
Libksba is a CMS and X.509 access library

libksba-1.6.7-r0 webpage:
https://www.gnupg.org/software/libksba/index.html

libksba-1.6.7-r0 installed size:
205 KiB

libksba-1.6.7-r0 license:
LGPL-3.0-only AND GPL-2.0-only AND GPL-3.0-only

```

### `apk` package: `libldap`

```console
libldap-2.6.8-r0 description:
OpenLDAP libraries

libldap-2.6.8-r0 webpage:
https://www.openldap.org/

libldap-2.6.8-r0 installed size:
365 KiB

libldap-2.6.8-r0 license:
OLDAP-2.8

```

### `apk` package: `libncursesw`

```console
libncursesw-6.5_p20241006-r3 description:
Console display library (libncursesw)

libncursesw-6.5_p20241006-r3 webpage:
https://invisible-island.net/ncurses/

libncursesw-6.5_p20241006-r3 installed size:
334 KiB

libncursesw-6.5_p20241006-r3 license:
X11

```

### `apk` package: `libpng`

```console
libpng-1.6.47-r0 description:
Portable Network Graphics library

libpng-1.6.47-r0 webpage:
http://www.libpng.org

libpng-1.6.47-r0 installed size:
181 KiB

libpng-1.6.47-r0 license:
Libpng

```

### `apk` package: `libpsl`

```console
libpsl-0.21.5-r3 description:
C library for the Publix Suffix List

libpsl-0.21.5-r3 webpage:
https://rockdaboot.github.io/libpsl

libpsl-0.21.5-r3 installed size:
73 KiB

libpsl-0.21.5-r3 license:
MIT

```

### `apk` package: `libsasl`

```console
libsasl-2.1.28-r8 description:
Cyrus Simple Authentication and Security Layer (SASL) library

libsasl-2.1.28-r8 webpage:
https://www.cyrusimap.org/sasl/

libsasl-2.1.28-r8 installed size:
163 KiB

libsasl-2.1.28-r8 license:
BSD-3-Clause-Attribution AND BSD-4-Clause

```

### `apk` package: `libssl3`

```console
libssl3-3.3.5-r0 description:
SSL shared libraries

libssl3-3.3.5-r0 webpage:
https://www.openssl.org/

libssl3-3.3.5-r0 installed size:
779 KiB

libssl3-3.3.5-r0 license:
Apache-2.0

```

### `apk` package: `libtasn1`

```console
libtasn1-4.20.0-r0 description:
The ASN.1 library used in GNUTLS

libtasn1-4.20.0-r0 webpage:
https://www.gnu.org/software/gnutls/

libtasn1-4.20.0-r0 installed size:
65 KiB

libtasn1-4.20.0-r0 license:
LGPL-2.1-or-later

```

### `apk` package: `libunistring`

```console
libunistring-1.2-r0 description:
Library for manipulating Unicode strings and C strings

libunistring-1.2-r0 webpage:
https://www.gnu.org/software/libunistring/

libunistring-1.2-r0 installed size:
1673 KiB

libunistring-1.2-r0 license:
GPL-2.0-or-later OR LGPL-3.0-or-later

```

### `apk` package: `mkfontscale`

```console
mkfontscale-1.2.3-r1 description:
Scalable font index generator for X

mkfontscale-1.2.3-r1 webpage:
https://xorg.freedesktop.org/

mkfontscale-1.2.3-r1 installed size:
34 KiB

mkfontscale-1.2.3-r1 license:
MIT

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

### `apk` package: `musl-locales`

```console
musl-locales-0.1.0-r1 description:
Locales support for musl

musl-locales-0.1.0-r1 webpage:
https://git.adelielinux.org/adelie/musl-locales/-/wikis/home

musl-locales-0.1.0-r1 installed size:
150 KiB

musl-locales-0.1.0-r1 license:
LGPL-3.0-only

```

### `apk` package: `musl-locales-lang`

```console
musl-locales-lang-0.1.0-r1 description:
Languages for package musl-locales

musl-locales-lang-0.1.0-r1 webpage:
https://git.adelielinux.org/adelie/musl-locales/-/wikis/home

musl-locales-lang-0.1.0-r1 installed size:
36 KiB

musl-locales-lang-0.1.0-r1 license:
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

### `apk` package: `ncurses-terminfo-base`

```console
ncurses-terminfo-base-6.5_p20241006-r3 description:
Descriptions of common terminals

ncurses-terminfo-base-6.5_p20241006-r3 webpage:
https://invisible-island.net/ncurses/

ncurses-terminfo-base-6.5_p20241006-r3 installed size:
95 KiB

ncurses-terminfo-base-6.5_p20241006-r3 license:
X11

```

### `apk` package: `nettle`

```console
nettle-3.10-r1 description:
Low-level cryptographic library

nettle-3.10-r1 webpage:
https://www.lysator.liu.se/~nisse/nettle/

nettle-3.10-r1 installed size:
587 KiB

nettle-3.10-r1 license:
GPL-2.0-or-later OR LGPL-3.0-or-later

```

### `apk` package: `nghttp2-libs`

```console
nghttp2-libs-1.64.0-r0 description:
HTTP/2 C client, server and proxy (libraries)

nghttp2-libs-1.64.0-r0 webpage:
https://nghttp2.org

nghttp2-libs-1.64.0-r0 installed size:
137 KiB

nghttp2-libs-1.64.0-r0 license:
MIT

```

### `apk` package: `npth`

```console
npth-1.6-r4 description:
The New GNU Portable Threads library

npth-1.6-r4 webpage:
https://gnupg.org/related_software/npth/

npth-1.6-r4 installed size:
17 KiB

npth-1.6-r4 license:
LGPL-2.0-or-later

```

### `apk` package: `openssl`

```console
openssl-3.3.5-r0 description:
Toolkit for Transport Layer Security (TLS)

openssl-3.3.5-r0 webpage:
https://www.openssl.org/

openssl-3.3.5-r0 installed size:
765 KiB

openssl-3.3.5-r0 license:
Apache-2.0

```

### `apk` package: `p11-kit`

```console
p11-kit-0.25.5-r2 description:
Library for loading and sharing PKCS#11 modules

p11-kit-0.25.5-r2 webpage:
https://p11-glue.freedesktop.org/

p11-kit-0.25.5-r2 installed size:
1362 KiB

p11-kit-0.25.5-r2 license:
BSD-3-Clause

```

### `apk` package: `p11-kit-trust`

```console
p11-kit-trust-0.25.5-r2 description:
System trust module from p11-kit

p11-kit-trust-0.25.5-r2 webpage:
https://p11-glue.freedesktop.org/

p11-kit-trust-0.25.5-r2 installed size:
329 KiB

p11-kit-trust-0.25.5-r2 license:
BSD-3-Clause

```

### `apk` package: `pinentry`

```console
pinentry-1.3.1-r0 description:
Collection of simple PIN or passphrase entry dialogs which utilize the Assuan protocol

pinentry-1.3.1-r0 webpage:
https://www.gnupg.org/aegypten2/

pinentry-1.3.1-r0 installed size:
66 KiB

pinentry-1.3.1-r0 license:
GPL-2.0-or-later

```

### `apk` package: `readline`

```console
readline-8.2.13-r0 description:
GNU readline library

readline-8.2.13-r0 webpage:
https://tiswww.cwru.edu/php/chet/readline/rltop.html

readline-8.2.13-r0 installed size:
280 KiB

readline-8.2.13-r0 license:
GPL-3.0-or-later

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

### `apk` package: `skalibs-libs`

```console
skalibs-libs-2.14.3.0-r0 description:
Set of general-purpose C programming libraries for skarnet.org software. (libraries)

skalibs-libs-2.14.3.0-r0 webpage:
https://skarnet.org/software/skalibs/

skalibs-libs-2.14.3.0-r0 installed size:
191 KiB

skalibs-libs-2.14.3.0-r0 license:
ISC

```

### `apk` package: `sqlite-libs`

```console
sqlite-libs-3.48.0-r4 description:
C library that implements an SQL database engine (libraries)

sqlite-libs-3.48.0-r4 webpage:
https://www.sqlite.org/

sqlite-libs-3.48.0-r4 installed size:
1549 KiB

sqlite-libs-3.48.0-r4 license:
blessing

```

### `apk` package: `ssl_client`

```console
ssl_client-1.37.0-r13 description:
External ssl_client for busybox wget

ssl_client-1.37.0-r13 webpage:
https://busybox.net/

ssl_client-1.37.0-r13 installed size:
14 KiB

ssl_client-1.37.0-r13 license:
GPL-2.0-only

```

### `apk` package: `su-exec`

```console
su-exec-0.2-r3 description:
switch user and group id, setgroups and exec

su-exec-0.2-r3 webpage:
https://github.com/ncopa/su-exec

su-exec-0.2-r3 installed size:
13 KiB

su-exec-0.2-r3 license:
MIT

```

### `apk` package: `tzdata`

```console
tzdata-2025b-r0 description:
Timezone data

tzdata-2025b-r0 webpage:
https://www.iana.org/time-zones

tzdata-2025b-r0 installed size:
435 KiB

tzdata-2025b-r0 license:
Public-Domain

```

### `apk` package: `unzip`

```console
unzip-6.0-r15 description:
Extract PKZIP-compatible .zip files

unzip-6.0-r15 webpage:
http://www.info-zip.org/UnZip.html

unzip-6.0-r15 installed size:
240 KiB

unzip-6.0-r15 license:
custom

```

### `apk` package: `utmps-libs`

```console
utmps-libs-0.1.2.3-r2 description:
A secure utmp/wtmp implementation (libraries)

utmps-libs-0.1.2.3-r2 webpage:
https://skarnet.org/software/utmps/

utmps-libs-0.1.2.3-r2 installed size:
13 KiB

utmps-libs-0.1.2.3-r2 license:
ISC

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

### `apk` package: `zstd-libs`

```console
zstd-libs-1.5.6-r2 description:
Zstandard - Fast real-time compression algorithm (libraries)

zstd-libs-1.5.6-r2 webpage:
https://facebook.github.io/zstd/

zstd-libs-1.5.6-r2 installed size:
697 KiB

zstd-libs-1.5.6-r2 license:
BSD-3-Clause OR GPL-2.0-or-later

```
