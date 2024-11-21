# `mediawiki:1.39.10-fpm-alpine`

## Docker Metadata

- Image ID: `sha256:e05ee3e2dec4111d5be22e5b8b8b4004d3de299f7696a9d2f4675119758d6150`
- Created: `2024-10-10T17:52:24Z`
- Virtual Size: ~ 405.95 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Entrypoint: `["docker-php-entrypoint"]`
- Command: `["php-fpm"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`
  - `PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c`
  - `PHP_INI_DIR=/usr/local/etc/php`
  - `PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64`
  - `PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64`
  - `PHP_LDFLAGS=-Wl,-O1 -pie`
  - `GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD`
  - `PHP_VERSION=8.1.31`
  - `PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz`
  - `PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc`
  - `PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca`
  - `MEDIAWIKI_MAJOR_VERSION=1.39`
  - `MEDIAWIKI_VERSION=1.39.10`

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

### `apk` package: `argon2-libs`

```console
argon2-libs-20190702-r5 description:
The password hash Argon2, winner of PHC (libraries)

argon2-libs-20190702-r5 webpage:
https://github.com/P-H-C/phc-winner-argon2

argon2-libs-20190702-r5 installed size:
52 KiB

argon2-libs-20190702-r5 license:
Apache-2.0 OR CC0-1.0

```

### `apk` package: `brotli-libs`

```console
brotli-libs-1.1.0-r2 description:
Generic lossless compressor (libraries)

brotli-libs-1.1.0-r2 webpage:
https://github.com/google/brotli

brotli-libs-1.1.0-r2 installed size:
932 KiB

brotli-libs-1.1.0-r2 license:
MIT

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

### `apk` package: `c-ares`

```console
c-ares-1.33.1-r0 description:
Asynchronous DNS/names resolver library

c-ares-1.33.1-r0 webpage:
https://c-ares.org/

c-ares-1.33.1-r0 installed size:
168 KiB

c-ares-1.33.1-r0 license:
MIT

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

### `apk` package: `curl`

```console
curl-8.11.0-r2 description:
URL retrival utility and library

curl-8.11.0-r2 webpage:
https://curl.se/

curl-8.11.0-r2 installed size:
256 KiB

curl-8.11.0-r2 license:
curl

```

### `apk` package: `fftw-double-libs`

```console
fftw-double-libs-3.3.10-r5 description:
Discrete Fourier transform (DFT) library

fftw-double-libs-3.3.10-r5 webpage:
http://www.fftw.org/

fftw-double-libs-3.3.10-r5 installed size:
2028 KiB

fftw-double-libs-3.3.10-r5 license:
GPL-2.0-or-later

```

### `apk` package: `fontconfig`

```console
fontconfig-2.15.0-r1 description:
Library for configuring and customizing font access

fontconfig-2.15.0-r1 webpage:
https://www.freedesktop.org/wiki/Software/fontconfig

fontconfig-2.15.0-r1 installed size:
756 KiB

fontconfig-2.15.0-r1 license:
MIT

```

### `apk` package: `freetype`

```console
freetype-2.13.2-r0 description:
TrueType font rendering library

freetype-2.13.2-r0 webpage:
https://www.freetype.org/

freetype-2.13.2-r0 installed size:
664 KiB

freetype-2.13.2-r0 license:
FTL OR GPL-2.0-or-later

```

### `apk` package: `gdbm`

```console
gdbm-1.23-r1 description:
GNU dbm is a set of database routines that use extensible hashing

gdbm-1.23-r1 webpage:
https://www.gnu.org/software/gdbm/

gdbm-1.23-r1 installed size:
84 KiB

gdbm-1.23-r1 license:
GPL-3.0-or-later

```

### `apk` package: `git`

```console
git-2.45.2-r0 description:
Distributed version control system

git-2.45.2-r0 webpage:
https://www.git-scm.com/

git-2.45.2-r0 installed size:
6468 KiB

git-2.45.2-r0 license:
GPL-2.0-only

```

### `apk` package: `git-init-template`

```console
git-init-template-2.45.2-r0 description:
Git init template directory

git-init-template-2.45.2-r0 webpage:
https://www.git-scm.com/

git-init-template-2.45.2-r0 installed size:
96 KiB

git-init-template-2.45.2-r0 license:
GPL-2.0-only

```

### `apk` package: `gnu-libiconv-libs`

```console
gnu-libiconv-libs-1.17-r2 description:
GNU charset conversion library for libc which doesn't implement it (libraries)

gnu-libiconv-libs-1.17-r2 webpage:
https://www.gnu.org/software/libiconv

gnu-libiconv-libs-1.17-r2 installed size:
1064 KiB

gnu-libiconv-libs-1.17-r2 license:
LGPL-2.1-or-later

```

### `apk` package: `icu-data-en`

```console
icu-data-en-74.2-r0 description:
Stripped down ICU data with only en_US/GB locale and no legacy charset converters

icu-data-en-74.2-r0 webpage:
https://icu.unicode.org/

icu-data-en-74.2-r0 installed size:
2756 KiB

icu-data-en-74.2-r0 license:
ICU

```

### `apk` package: `icu-libs`

```console
icu-libs-74.2-r0 description:
International Components for Unicode library (libraries)

icu-libs-74.2-r0 webpage:
https://icu.unicode.org/

icu-libs-74.2-r0 installed size:
4408 KiB

icu-libs-74.2-r0 license:
ICU

```

### `apk` package: `imagemagick`

```console
imagemagick-7.1.1.32-r2 description:
Collection of tools and libraries for many image formats

imagemagick-7.1.1.32-r2 webpage:
https://imagemagick.org/

imagemagick-7.1.1.32-r2 installed size:
4340 KiB

imagemagick-7.1.1.32-r2 license:
ImageMagick

```

### `apk` package: `imagemagick-libs`

```console
imagemagick-libs-7.1.1.32-r2 description:
Collection of tools and libraries for many image formats (libraries)

imagemagick-libs-7.1.1.32-r2 webpage:
https://imagemagick.org/

imagemagick-libs-7.1.1.32-r2 installed size:
4168 KiB

imagemagick-libs-7.1.1.32-r2 license:
ImageMagick

```

### `apk` package: `lcms2`

```console
lcms2-2.16-r0 description:
Color Management Engine

lcms2-2.16-r0 webpage:
https://www.littlecms.com

lcms2-2.16-r0 installed size:
344 KiB

lcms2-2.16-r0 license:
MIT

```

### `apk` package: `libacl`

```console
libacl-2.3.2-r0 description:
Dynamic library for access control list support

libacl-2.3.2-r0 webpage:
https://savannah.nongnu.org/projects/acl

libacl-2.3.2-r0 installed size:
44 KiB

libacl-2.3.2-r0 license:
LGPL-2.1-or-later AND GPL-2.0-or-later

```

### `apk` package: `libbsd`

```console
libbsd-0.12.2-r0 description:
commonly-used BSD functions not implemented by all libcs

libbsd-0.12.2-r0 webpage:
https://libbsd.freedesktop.org/

libbsd-0.12.2-r0 installed size:
76 KiB

libbsd-0.12.2-r0 license:
BSD-3-Clause

```

### `apk` package: `libbz2`

```console
libbz2-1.0.8-r6 description:
Shared library for bz2

libbz2-1.0.8-r6 webpage:
https://sourceware.org/bzip2/

libbz2-1.0.8-r6 installed size:
88 KiB

libbz2-1.0.8-r6 license:
bzip2-1.0.6

```

### `apk` package: `libcrypto3`

```console
libcrypto3-3.3.2-r1 description:
Crypto library from openssl

libcrypto3-3.3.2-r1 webpage:
https://www.openssl.org/

libcrypto3-3.3.2-r1 installed size:
4660 KiB

libcrypto3-3.3.2-r1 license:
Apache-2.0

```

### `apk` package: `libcurl`

```console
libcurl-8.11.0-r2 description:
The multiprotocol file transfer library

libcurl-8.11.0-r2 webpage:
https://curl.se/

libcurl-8.11.0-r2 installed size:
636 KiB

libcurl-8.11.0-r2 license:
curl

```

### `apk` package: `libexpat`

```console
libexpat-2.6.4-r0 description:
XML Parser library written in C (libraries)

libexpat-2.6.4-r0 webpage:
https://libexpat.github.io/

libexpat-2.6.4-r0 installed size:
144 KiB

libexpat-2.6.4-r0 license:
MIT

```

### `apk` package: `libffi`

```console
libffi-3.4.6-r0 description:
portable, high level programming interface to various calling conventions.

libffi-3.4.6-r0 webpage:
https://sourceware.org/libffi/

libffi-3.4.6-r0 installed size:
52 KiB

libffi-3.4.6-r0 license:
MIT

```

### `apk` package: `libgcc`

```console
libgcc-13.2.1_git20240309-r0 description:
GNU C compiler runtime libraries

libgcc-13.2.1_git20240309-r0 webpage:
https://gcc.gnu.org

libgcc-13.2.1_git20240309-r0 installed size:
152 KiB

libgcc-13.2.1_git20240309-r0 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `libgomp`

```console
libgomp-13.2.1_git20240309-r0 description:
GCC shared-memory parallel programming API library

libgomp-13.2.1_git20240309-r0 webpage:
https://gcc.gnu.org

libgomp-13.2.1_git20240309-r0 installed size:
324 KiB

libgomp-13.2.1_git20240309-r0 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `libidn2`

```console
libidn2-2.3.7-r0 description:
Encode/Decode library for internationalized domain names

libidn2-2.3.7-r0 webpage:
https://www.gnu.org/software/libidn#libidn2

libidn2-2.3.7-r0 installed size:
208 KiB

libidn2-2.3.7-r0 license:
GPL-2.0-or-later OR LGPL-3.0-or-later

```

### `apk` package: `libltdl`

```console
libltdl-2.4.7-r3 description:
Runtime libraries for GNU Libtool Dynamic Module Loader

libltdl-2.4.7-r3 webpage:
https://www.gnu.org/software/libtool

libltdl-2.4.7-r3 installed size:
52 KiB

libltdl-2.4.7-r3 license:
LGPL-2.0-or-later AND GPL-2.0-or-later

```

### `apk` package: `libmd`

```console
libmd-1.1.0-r0 description:
Message Digest functions from BSD systems

libmd-1.1.0-r0 webpage:
https://www.hadrons.org/software/libmd/

libmd-1.1.0-r0 installed size:
64 KiB

libmd-1.1.0-r0 license:
BSD-3-Clause AND BSD-2-Clause AND ISC AND Beerware AND Public Domain

```

### `apk` package: `libncursesw`

```console
libncursesw-6.4_p20240420-r2 description:
Console display library (libncursesw)

libncursesw-6.4_p20240420-r2 webpage:
https://invisible-island.net/ncurses/

libncursesw-6.4_p20240420-r2 installed size:
344 KiB

libncursesw-6.4_p20240420-r2 license:
X11

```

### `apk` package: `libpanelw`

```console
libpanelw-6.4_p20240420-r2 description:
Console display library (libpanelw)

libpanelw-6.4_p20240420-r2 webpage:
https://invisible-island.net/ncurses/

libpanelw-6.4_p20240420-r2 installed size:
32 KiB

libpanelw-6.4_p20240420-r2 license:
X11

```

### `apk` package: `libpng`

```console
libpng-1.6.44-r0 description:
Portable Network Graphics library

libpng-1.6.44-r0 webpage:
http://www.libpng.org

libpng-1.6.44-r0 installed size:
200 KiB

libpng-1.6.44-r0 license:
Libpng

```

### `apk` package: `libpsl`

```console
libpsl-0.21.5-r1 description:
C library for the Publix Suffix List

libpsl-0.21.5-r1 webpage:
https://rockdaboot.github.io/libpsl

libpsl-0.21.5-r1 installed size:
88 KiB

libpsl-0.21.5-r1 license:
MIT

```

### `apk` package: `libsodium`

```console
libsodium-1.0.19-r0 description:
P(ortable|ackageable) NaCl-based crypto library

libsodium-1.0.19-r0 webpage:
https://github.com/jedisct1/libsodium

libsodium-1.0.19-r0 installed size:
348 KiB

libsodium-1.0.19-r0 license:
ISC

```

### `apk` package: `libssl3`

```console
libssl3-3.3.2-r1 description:
SSL shared libraries

libssl3-3.3.2-r1 webpage:
https://www.openssl.org/

libssl3-3.3.2-r1 installed size:
796 KiB

libssl3-3.3.2-r1 license:
Apache-2.0

```

### `apk` package: `libstdc++`

```console
libstdc++-13.2.1_git20240309-r0 description:
GNU C++ standard runtime library

libstdc++-13.2.1_git20240309-r0 webpage:
https://gcc.gnu.org

libstdc++-13.2.1_git20240309-r0 installed size:
2652 KiB

libstdc++-13.2.1_git20240309-r0 license:
GPL-2.0-or-later AND LGPL-2.1-or-later

```

### `apk` package: `libunistring`

```console
libunistring-1.2-r0 description:
Library for manipulating Unicode strings and C strings

libunistring-1.2-r0 webpage:
https://www.gnu.org/software/libunistring/

libunistring-1.2-r0 installed size:
1692 KiB

libunistring-1.2-r0 license:
GPL-2.0-or-later OR LGPL-3.0-or-later

```

### `apk` package: `libx11`

```console
libx11-1.8.9-r1 description:
X11 client-side library

libx11-1.8.9-r1 webpage:
https://xorg.freedesktop.org/

libx11-1.8.9-r1 installed size:
3088 KiB

libx11-1.8.9-r1 license:
X11

```

### `apk` package: `libxau`

```console
libxau-1.0.11-r4 description:
X11 authorisation library

libxau-1.0.11-r4 webpage:
https://xorg.freedesktop.org/

libxau-1.0.11-r4 installed size:
28 KiB

libxau-1.0.11-r4 license:
MIT

```

### `apk` package: `libxcb`

```console
libxcb-1.16.1-r0 description:
X11 client-side library

libxcb-1.16.1-r0 webpage:
https://xcb.freedesktop.org/

libxcb-1.16.1-r0 installed size:
1012 KiB

libxcb-1.16.1-r0 license:
MIT

```

### `apk` package: `libxdmcp`

```console
libxdmcp-1.1.5-r1 description:
X11 Display Manager Control Protocol library

libxdmcp-1.1.5-r1 webpage:
https://xorg.freedesktop.org/

libxdmcp-1.1.5-r1 installed size:
40 KiB

libxdmcp-1.1.5-r1 license:
MIT

```

### `apk` package: `libxext`

```console
libxext-1.3.6-r2 description:
X11 miscellaneous extensions library

libxext-1.3.6-r2 webpage:
https://xorg.freedesktop.org/

libxext-1.3.6-r2 installed size:
80 KiB

libxext-1.3.6-r2 license:
MIT

```

### `apk` package: `libxml2`

```console
libxml2-2.12.7-r0 description:
XML parsing library, version 2

libxml2-2.12.7-r0 webpage:
https://gitlab.gnome.org/GNOME/libxml2

libxml2-2.12.7-r0 installed size:
1088 KiB

libxml2-2.12.7-r0 license:
MIT

```

### `apk` package: `lua5.1-libs`

```console
lua5.1-libs-5.1.5-r13 description:
Lua dynamic library runtime

lua5.1-libs-5.1.5-r13 webpage:
https://www.lua.org/

lua5.1-libs-5.1.5-r13 installed size:
168 KiB

lua5.1-libs-5.1.5-r13 license:
MIT

```

### `apk` package: `mpdecimal`

```console
mpdecimal-4.0.0-r0 description:
complete implementation of the General Decimal Arithmetic Specification

mpdecimal-4.0.0-r0 webpage:
https://www.bytereef.org/mpdecimal/index.html

mpdecimal-4.0.0-r0 installed size:
204 KiB

mpdecimal-4.0.0-r0 license:
BSD-2-Clause

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

### `apk` package: `ncurses-terminfo-base`

```console
ncurses-terminfo-base-6.4_p20240420-r2 description:
Descriptions of common terminals

ncurses-terminfo-base-6.4_p20240420-r2 webpage:
https://invisible-island.net/ncurses/

ncurses-terminfo-base-6.4_p20240420-r2 installed size:
212 KiB

ncurses-terminfo-base-6.4_p20240420-r2 license:
X11

```

### `apk` package: `nghttp2-libs`

```console
nghttp2-libs-1.62.1-r0 description:
HTTP/2 C client, server and proxy (libraries)

nghttp2-libs-1.62.1-r0 webpage:
https://nghttp2.org

nghttp2-libs-1.62.1-r0 installed size:
152 KiB

nghttp2-libs-1.62.1-r0 license:
MIT

```

### `apk` package: `oniguruma`

```console
oniguruma-6.9.9-r0 description:
a regular expressions library

oniguruma-6.9.9-r0 webpage:
https://github.com/kkos/oniguruma

oniguruma-6.9.9-r0 installed size:
552 KiB

oniguruma-6.9.9-r0 license:
BSD-2-Clause

```

### `apk` package: `openssl`

```console
openssl-3.3.2-r1 description:
Toolkit for Transport Layer Security (TLS)

openssl-3.3.2-r1 webpage:
https://www.openssl.org/

openssl-3.3.2-r1 installed size:
784 KiB

openssl-3.3.2-r1 license:
Apache-2.0

```

### `apk` package: `pcre2`

```console
pcre2-10.43-r0 description:
Perl-compatible regular expression library

pcre2-10.43-r0 webpage:
https://pcre.org/

pcre2-10.43-r0 installed size:
708 KiB

pcre2-10.43-r0 license:
BSD-3-Clause

```

### `apk` package: `pyc`

```console
pyc-3.12.7-r0 description:
Meta package for pulling in all -pyc packages

pyc-3.12.7-r0 webpage:
https://www.python.org/

pyc-3.12.7-r0 installed size:
4096 B

pyc-3.12.7-r0 license:
PSF-2.0

```

### `apk` package: `python3`

```console
python3-3.12.7-r0 description:
High-level scripting language

python3-3.12.7-r0 webpage:
https://www.python.org/

python3-3.12.7-r0 installed size:
24 MiB

python3-3.12.7-r0 license:
PSF-2.0

```

### `apk` package: `python3-pyc`

```console
python3-pyc-3.12.7-r0 description:
High-level scripting language (install .pyc cache files)

python3-pyc-3.12.7-r0 webpage:
https://www.python.org/

python3-pyc-3.12.7-r0 installed size:
4096 B

python3-pyc-3.12.7-r0 license:
PSF-2.0

```

### `apk` package: `python3-pycache-pyc0`

```console
python3-pycache-pyc0-3.12.7-r0 description:
High-level scripting language (.pyc pycache files)

python3-pycache-pyc0-3.12.7-r0 webpage:
https://www.python.org/

python3-pycache-pyc0-3.12.7-r0 installed size:
11 MiB

python3-pycache-pyc0-3.12.7-r0 license:
PSF-2.0

```

### `apk` package: `readline`

```console
readline-8.2.10-r0 description:
GNU readline library

readline-8.2.10-r0 webpage:
https://tiswww.cwru.edu/php/chet/readline/rltop.html

readline-8.2.10-r0 installed size:
300 KiB

readline-8.2.10-r0 license:
GPL-3.0-or-later

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

### `apk` package: `sqlite-libs`

```console
sqlite-libs-3.45.3-r1 description:
C library that implements an SQL database engine (libraries)

sqlite-libs-3.45.3-r1 webpage:
https://www.sqlite.org/

sqlite-libs-3.45.3-r1 installed size:
1428 KiB

sqlite-libs-3.45.3-r1 license:
blessing

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

### `apk` package: `tar`

```console
tar-1.35-r2 description:
Utility used to store, backup, and transport files

tar-1.35-r2 webpage:
https://www.gnu.org/software/tar/

tar-1.35-r2 installed size:
428 KiB

tar-1.35-r2 license:
GPL-3.0-or-later

```

### `apk` package: `xz`

```console
xz-5.6.2-r0 description:
Library and CLI tools for XZ and LZMA compressed files

xz-5.6.2-r0 webpage:
https://tukaani.org/xz/

xz-5.6.2-r0 installed size:
184 KiB

xz-5.6.2-r0 license:
GPL-2.0-or-later AND 0BSD AND Public-Domain AND LGPL-2.1-or-later

```

### `apk` package: `xz-libs`

```console
xz-libs-5.6.2-r0 description:
Library and CLI tools for XZ and LZMA compressed files (libraries)

xz-libs-5.6.2-r0 webpage:
https://tukaani.org/xz/

xz-libs-5.6.2-r0 installed size:
236 KiB

xz-libs-5.6.2-r0 license:
GPL-2.0-or-later AND 0BSD AND Public-Domain AND LGPL-2.1-or-later

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

### `apk` package: `zstd-libs`

```console
zstd-libs-1.5.6-r0 description:
Zstandard - Fast real-time compression algorithm (libraries)

zstd-libs-1.5.6-r0 webpage:
https://www.zstd.net/

zstd-libs-1.5.6-r0 installed size:
716 KiB

zstd-libs-1.5.6-r0 license:
BSD-3-Clause OR GPL-2.0-or-later

```
