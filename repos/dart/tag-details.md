<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10.0-290.4.beta`](#dart3100-2904beta)
-	[`dart:3.10.0-290.4.beta-sdk`](#dart3100-2904beta-sdk)
-	[`dart:3.9`](#dart39)
-	[`dart:3.9-sdk`](#dart39-sdk)
-	[`dart:3.9.4`](#dart394)
-	[`dart:3.9.4-sdk`](#dart394-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:b8495dc2a2a7a3658951e9949a4dddbaf43dc26e896b1af4e1a77147ab998528
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:b8495dc2a2a7a3658951e9949a4dddbaf43dc26e896b1af4e1a77147ab998528
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-290.4.beta`

```console
$ docker pull dart@sha256:b89dcfb284a254c1bc54d512ed76d51dbc32dbb3af7b44c95be7ab6a9f558fa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:3.10.0-290.4.beta` - linux; amd64

```console
$ docker pull dart@sha256:f9ed657c4d5e3f97d67880f0d9113b6eee1af4ecade72ab64da34e4c3dfbaf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ec2ca095326c5b20be3fc8678f533dc1ff8f50ccdd815f58e92754a2b831cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:45 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f19f01a509086c8b7b03d33d103893495c703e087cc2b892a82bb2fce8d727`  
		Last Modified: Tue, 04 Nov 2025 04:15:36 GMT  
		Size: 42.5 MB (42493599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff32e16829208b3d18b7627a966036fcfbd68caba5e7ef596cf0a97a54d0063`  
		Last Modified: Tue, 04 Nov 2025 04:15:33 GMT  
		Size: 1.9 MB (1873623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf2357c8330c81ae8a419b2685e2c78b5b509d4415911abdc1fc2dadb0637bc`  
		Last Modified: Tue, 04 Nov 2025 10:08:04 GMT  
		Size: 213.1 MB (213123103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-290.4.beta` - unknown; unknown

```console
$ docker pull dart@sha256:5e837a27769d8052ed7f7de634e7e8b72201e3960e01601fd7a4cf7bca6d401e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667cdf9a7921e7ebf3f3978342063805e802fd33f137f7ac9081c1968c869a96`

```dockerfile
```

-	Layers:
	-	`sha256:7417f79ae0c5aee79b610d323a3f47a7a0c63b8295758b292b85061a94cfdef3`  
		Last Modified: Tue, 04 Nov 2025 09:53:43 GMT  
		Size: 18.9 KB (18922 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-290.4.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:9d03b710f66b5487b6bf50ad1323c8d7c4d5f1b3aea7a20074b567638265c1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219901041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3b95b872f7897e3e680ee83772d0db5fc9aa647e45a3dff42f0f127de9a08d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:29 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:29 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9e2ec3da8bf845c0305beb77b1005cf6412f8ebcb0cfce2a89899c4e023bb`  
		Last Modified: Tue, 04 Nov 2025 02:20:10 GMT  
		Size: 37.5 MB (37498778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dc5ff7b6a37478b04b16f01331b0d5f0bd8f01702f3eec3662731f062e6b72`  
		Last Modified: Tue, 04 Nov 2025 02:20:06 GMT  
		Size: 1.3 MB (1275115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b6df820bad278266f680463046cdc57a0ad3375727f29ed0258e450955934`  
		Last Modified: Tue, 04 Nov 2025 10:10:04 GMT  
		Size: 154.9 MB (154914077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-290.4.beta` - unknown; unknown

```console
$ docker pull dart@sha256:009106f8521484ed850022143f01d96fc277b1b6898941a9a6ee4ddbf818dd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b235791ad1144406c4ed82426acd1b44437499b083d29999f523939687dfe`

```dockerfile
```

-	Layers:
	-	`sha256:245c0c64f0c2235bd62a3b73fa893830227a0d6496bce9a028aa749e1aff6808`  
		Last Modified: Tue, 04 Nov 2025 09:53:46 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-290.4.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7c6d63097c566fa94e034c9e515d075610eecf14f0b3322edcc4d82ee0af0be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286355447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980b01fbb755da9928701c924fd83523b42df094d512630cf552508f7f3b5048`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:05 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a58e8c8f200cd1433fa21a373e968459d45ea0733a81b582347b54f088fde`  
		Last Modified: Tue, 04 Nov 2025 01:30:57 GMT  
		Size: 42.3 MB (42292994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b56a40b0401a2a36dadc42cebc7ec0ebc25aa21aebd10e07a3ed59a5015f0f`  
		Last Modified: Tue, 04 Nov 2025 01:30:54 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c207aa7e535b085aebd309c2aa1a07bcfe4cb04729fef8251d13b7c6ecc1432f`  
		Last Modified: Tue, 04 Nov 2025 10:10:00 GMT  
		Size: 212.4 MB (212353478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-290.4.beta` - unknown; unknown

```console
$ docker pull dart@sha256:ebcf812d91de37b3654889739ca6de6541bc7c7e5e18074f3138a7c40967fab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be58ecc08316e3af52bb97320641930b11710352008f1b7b2b1e76148e80656`

```dockerfile
```

-	Layers:
	-	`sha256:aa5f20c23d8ed3f617d54b53f61947dab9183d029ce3616c30e73e0809f304a1`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-290.4.beta` - linux; riscv64

```console
$ docker pull dart@sha256:d83f21195b16b7cd9b67f07ead8b30415dcf81055a96ac649a5055f5842cde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232961681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68462cc545bd580d3e8fbe24c1209bac247e934f240f221d82343db44a396358`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:34:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Oct 2025 21:34:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Oct 2025 21:34:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 21:34:52 GMT
WORKDIR /root
# Thu, 30 Oct 2025 21:35:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec0f9e08b260538440cd52261c947e1bd83acefb176ac1a0096d41f24b2553b`  
		Last Modified: Thu, 30 Oct 2025 21:40:25 GMT  
		Size: 41.6 MB (41560987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3067dd0e062d97af724bda19fc00d8673cf75edef7a7ab8ab163f1a8cee2682f`  
		Last Modified: Thu, 30 Oct 2025 21:40:21 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa82dfc185344ee822867d21fb16c0682deb95a0f5562aa7963981b9e6327a4c`  
		Last Modified: Thu, 30 Oct 2025 23:54:07 GMT  
		Size: 161.6 MB (161557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-290.4.beta` - unknown; unknown

```console
$ docker pull dart@sha256:76dfa4756e99a65edd24feebf4e7435084fbca9c8ce9fce7699408b7eb660205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b3d09cff17dcc547f3851f2b82c847bdd1f111a7af821bc384278b37b2fa17`

```dockerfile
```

-	Layers:
	-	`sha256:ced6e766ba285ee13814cf16b9e925bee4cad326ee81dc73a9b87a38184a294c`  
		Last Modified: Thu, 30 Oct 2025 23:53:32 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-290.4.beta-sdk`

```console
$ docker pull dart@sha256:b89dcfb284a254c1bc54d512ed76d51dbc32dbb3af7b44c95be7ab6a9f558fa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:3.10.0-290.4.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f9ed657c4d5e3f97d67880f0d9113b6eee1af4ecade72ab64da34e4c3dfbaf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ec2ca095326c5b20be3fc8678f533dc1ff8f50ccdd815f58e92754a2b831cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:45 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f19f01a509086c8b7b03d33d103893495c703e087cc2b892a82bb2fce8d727`  
		Last Modified: Tue, 04 Nov 2025 04:15:36 GMT  
		Size: 42.5 MB (42493599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff32e16829208b3d18b7627a966036fcfbd68caba5e7ef596cf0a97a54d0063`  
		Last Modified: Tue, 04 Nov 2025 04:15:33 GMT  
		Size: 1.9 MB (1873623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf2357c8330c81ae8a419b2685e2c78b5b509d4415911abdc1fc2dadb0637bc`  
		Last Modified: Tue, 04 Nov 2025 10:08:04 GMT  
		Size: 213.1 MB (213123103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-290.4.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5e837a27769d8052ed7f7de634e7e8b72201e3960e01601fd7a4cf7bca6d401e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667cdf9a7921e7ebf3f3978342063805e802fd33f137f7ac9081c1968c869a96`

```dockerfile
```

-	Layers:
	-	`sha256:7417f79ae0c5aee79b610d323a3f47a7a0c63b8295758b292b85061a94cfdef3`  
		Last Modified: Tue, 04 Nov 2025 09:53:43 GMT  
		Size: 18.9 KB (18922 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-290.4.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:9d03b710f66b5487b6bf50ad1323c8d7c4d5f1b3aea7a20074b567638265c1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219901041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3b95b872f7897e3e680ee83772d0db5fc9aa647e45a3dff42f0f127de9a08d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:29 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:29 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9e2ec3da8bf845c0305beb77b1005cf6412f8ebcb0cfce2a89899c4e023bb`  
		Last Modified: Tue, 04 Nov 2025 02:20:10 GMT  
		Size: 37.5 MB (37498778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dc5ff7b6a37478b04b16f01331b0d5f0bd8f01702f3eec3662731f062e6b72`  
		Last Modified: Tue, 04 Nov 2025 02:20:06 GMT  
		Size: 1.3 MB (1275115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b6df820bad278266f680463046cdc57a0ad3375727f29ed0258e450955934`  
		Last Modified: Tue, 04 Nov 2025 10:10:04 GMT  
		Size: 154.9 MB (154914077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-290.4.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:009106f8521484ed850022143f01d96fc277b1b6898941a9a6ee4ddbf818dd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b235791ad1144406c4ed82426acd1b44437499b083d29999f523939687dfe`

```dockerfile
```

-	Layers:
	-	`sha256:245c0c64f0c2235bd62a3b73fa893830227a0d6496bce9a028aa749e1aff6808`  
		Last Modified: Tue, 04 Nov 2025 09:53:46 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-290.4.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7c6d63097c566fa94e034c9e515d075610eecf14f0b3322edcc4d82ee0af0be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286355447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980b01fbb755da9928701c924fd83523b42df094d512630cf552508f7f3b5048`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:05 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a58e8c8f200cd1433fa21a373e968459d45ea0733a81b582347b54f088fde`  
		Last Modified: Tue, 04 Nov 2025 01:30:57 GMT  
		Size: 42.3 MB (42292994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b56a40b0401a2a36dadc42cebc7ec0ebc25aa21aebd10e07a3ed59a5015f0f`  
		Last Modified: Tue, 04 Nov 2025 01:30:54 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c207aa7e535b085aebd309c2aa1a07bcfe4cb04729fef8251d13b7c6ecc1432f`  
		Last Modified: Tue, 04 Nov 2025 10:10:00 GMT  
		Size: 212.4 MB (212353478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-290.4.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ebcf812d91de37b3654889739ca6de6541bc7c7e5e18074f3138a7c40967fab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be58ecc08316e3af52bb97320641930b11710352008f1b7b2b1e76148e80656`

```dockerfile
```

-	Layers:
	-	`sha256:aa5f20c23d8ed3f617d54b53f61947dab9183d029ce3616c30e73e0809f304a1`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-290.4.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:d83f21195b16b7cd9b67f07ead8b30415dcf81055a96ac649a5055f5842cde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232961681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68462cc545bd580d3e8fbe24c1209bac247e934f240f221d82343db44a396358`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:34:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Oct 2025 21:34:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Oct 2025 21:34:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 21:34:52 GMT
WORKDIR /root
# Thu, 30 Oct 2025 21:35:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec0f9e08b260538440cd52261c947e1bd83acefb176ac1a0096d41f24b2553b`  
		Last Modified: Thu, 30 Oct 2025 21:40:25 GMT  
		Size: 41.6 MB (41560987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3067dd0e062d97af724bda19fc00d8673cf75edef7a7ab8ab163f1a8cee2682f`  
		Last Modified: Thu, 30 Oct 2025 21:40:21 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa82dfc185344ee822867d21fb16c0682deb95a0f5562aa7963981b9e6327a4c`  
		Last Modified: Thu, 30 Oct 2025 23:54:07 GMT  
		Size: 161.6 MB (161557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-290.4.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:76dfa4756e99a65edd24feebf4e7435084fbca9c8ce9fce7699408b7eb660205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b3d09cff17dcc547f3851f2b82c847bdd1f111a7af821bc384278b37b2fa17`

```dockerfile
```

-	Layers:
	-	`sha256:ced6e766ba285ee13814cf16b9e925bee4cad326ee81dc73a9b87a38184a294c`  
		Last Modified: Thu, 30 Oct 2025 23:53:32 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9`

```console
$ docker pull dart@sha256:89c1ecd039165a2abf664922d066684fc63ee582a6a4eb256831498515da1cc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:3.9` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9-sdk`

```console
$ docker pull dart@sha256:89c1ecd039165a2abf664922d066684fc63ee582a6a4eb256831498515da1cc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:3.9-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.4`

```console
$ docker pull dart@sha256:89c1ecd039165a2abf664922d066684fc63ee582a6a4eb256831498515da1cc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:3.9.4` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.4-sdk`

```console
$ docker pull dart@sha256:89c1ecd039165a2abf664922d066684fc63ee582a6a4eb256831498515da1cc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:3.9.4-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:b89dcfb284a254c1bc54d512ed76d51dbc32dbb3af7b44c95be7ab6a9f558fa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:f9ed657c4d5e3f97d67880f0d9113b6eee1af4ecade72ab64da34e4c3dfbaf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ec2ca095326c5b20be3fc8678f533dc1ff8f50ccdd815f58e92754a2b831cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:45 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f19f01a509086c8b7b03d33d103893495c703e087cc2b892a82bb2fce8d727`  
		Last Modified: Tue, 04 Nov 2025 04:15:36 GMT  
		Size: 42.5 MB (42493599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff32e16829208b3d18b7627a966036fcfbd68caba5e7ef596cf0a97a54d0063`  
		Last Modified: Tue, 04 Nov 2025 04:15:33 GMT  
		Size: 1.9 MB (1873623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf2357c8330c81ae8a419b2685e2c78b5b509d4415911abdc1fc2dadb0637bc`  
		Last Modified: Tue, 04 Nov 2025 10:08:04 GMT  
		Size: 213.1 MB (213123103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:5e837a27769d8052ed7f7de634e7e8b72201e3960e01601fd7a4cf7bca6d401e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667cdf9a7921e7ebf3f3978342063805e802fd33f137f7ac9081c1968c869a96`

```dockerfile
```

-	Layers:
	-	`sha256:7417f79ae0c5aee79b610d323a3f47a7a0c63b8295758b292b85061a94cfdef3`  
		Last Modified: Tue, 04 Nov 2025 09:53:43 GMT  
		Size: 18.9 KB (18922 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:9d03b710f66b5487b6bf50ad1323c8d7c4d5f1b3aea7a20074b567638265c1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219901041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3b95b872f7897e3e680ee83772d0db5fc9aa647e45a3dff42f0f127de9a08d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:29 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:29 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9e2ec3da8bf845c0305beb77b1005cf6412f8ebcb0cfce2a89899c4e023bb`  
		Last Modified: Tue, 04 Nov 2025 02:20:10 GMT  
		Size: 37.5 MB (37498778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dc5ff7b6a37478b04b16f01331b0d5f0bd8f01702f3eec3662731f062e6b72`  
		Last Modified: Tue, 04 Nov 2025 02:20:06 GMT  
		Size: 1.3 MB (1275115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b6df820bad278266f680463046cdc57a0ad3375727f29ed0258e450955934`  
		Last Modified: Tue, 04 Nov 2025 10:10:04 GMT  
		Size: 154.9 MB (154914077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:009106f8521484ed850022143f01d96fc277b1b6898941a9a6ee4ddbf818dd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b235791ad1144406c4ed82426acd1b44437499b083d29999f523939687dfe`

```dockerfile
```

-	Layers:
	-	`sha256:245c0c64f0c2235bd62a3b73fa893830227a0d6496bce9a028aa749e1aff6808`  
		Last Modified: Tue, 04 Nov 2025 09:53:46 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7c6d63097c566fa94e034c9e515d075610eecf14f0b3322edcc4d82ee0af0be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286355447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980b01fbb755da9928701c924fd83523b42df094d512630cf552508f7f3b5048`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:05 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a58e8c8f200cd1433fa21a373e968459d45ea0733a81b582347b54f088fde`  
		Last Modified: Tue, 04 Nov 2025 01:30:57 GMT  
		Size: 42.3 MB (42292994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b56a40b0401a2a36dadc42cebc7ec0ebc25aa21aebd10e07a3ed59a5015f0f`  
		Last Modified: Tue, 04 Nov 2025 01:30:54 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c207aa7e535b085aebd309c2aa1a07bcfe4cb04729fef8251d13b7c6ecc1432f`  
		Last Modified: Tue, 04 Nov 2025 10:10:00 GMT  
		Size: 212.4 MB (212353478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:ebcf812d91de37b3654889739ca6de6541bc7c7e5e18074f3138a7c40967fab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be58ecc08316e3af52bb97320641930b11710352008f1b7b2b1e76148e80656`

```dockerfile
```

-	Layers:
	-	`sha256:aa5f20c23d8ed3f617d54b53f61947dab9183d029ce3616c30e73e0809f304a1`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:d83f21195b16b7cd9b67f07ead8b30415dcf81055a96ac649a5055f5842cde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232961681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68462cc545bd580d3e8fbe24c1209bac247e934f240f221d82343db44a396358`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:34:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Oct 2025 21:34:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Oct 2025 21:34:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 21:34:52 GMT
WORKDIR /root
# Thu, 30 Oct 2025 21:35:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec0f9e08b260538440cd52261c947e1bd83acefb176ac1a0096d41f24b2553b`  
		Last Modified: Thu, 30 Oct 2025 21:40:25 GMT  
		Size: 41.6 MB (41560987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3067dd0e062d97af724bda19fc00d8673cf75edef7a7ab8ab163f1a8cee2682f`  
		Last Modified: Thu, 30 Oct 2025 21:40:21 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa82dfc185344ee822867d21fb16c0682deb95a0f5562aa7963981b9e6327a4c`  
		Last Modified: Thu, 30 Oct 2025 23:54:07 GMT  
		Size: 161.6 MB (161557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:76dfa4756e99a65edd24feebf4e7435084fbca9c8ce9fce7699408b7eb660205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b3d09cff17dcc547f3851f2b82c847bdd1f111a7af821bc384278b37b2fa17`

```dockerfile
```

-	Layers:
	-	`sha256:ced6e766ba285ee13814cf16b9e925bee4cad326ee81dc73a9b87a38184a294c`  
		Last Modified: Thu, 30 Oct 2025 23:53:32 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:b89dcfb284a254c1bc54d512ed76d51dbc32dbb3af7b44c95be7ab6a9f558fa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f9ed657c4d5e3f97d67880f0d9113b6eee1af4ecade72ab64da34e4c3dfbaf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287268461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ec2ca095326c5b20be3fc8678f533dc1ff8f50ccdd815f58e92754a2b831cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:45 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f19f01a509086c8b7b03d33d103893495c703e087cc2b892a82bb2fce8d727`  
		Last Modified: Tue, 04 Nov 2025 04:15:36 GMT  
		Size: 42.5 MB (42493599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff32e16829208b3d18b7627a966036fcfbd68caba5e7ef596cf0a97a54d0063`  
		Last Modified: Tue, 04 Nov 2025 04:15:33 GMT  
		Size: 1.9 MB (1873623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf2357c8330c81ae8a419b2685e2c78b5b509d4415911abdc1fc2dadb0637bc`  
		Last Modified: Tue, 04 Nov 2025 10:08:04 GMT  
		Size: 213.1 MB (213123103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5e837a27769d8052ed7f7de634e7e8b72201e3960e01601fd7a4cf7bca6d401e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667cdf9a7921e7ebf3f3978342063805e802fd33f137f7ac9081c1968c869a96`

```dockerfile
```

-	Layers:
	-	`sha256:7417f79ae0c5aee79b610d323a3f47a7a0c63b8295758b292b85061a94cfdef3`  
		Last Modified: Tue, 04 Nov 2025 09:53:43 GMT  
		Size: 18.9 KB (18922 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:9d03b710f66b5487b6bf50ad1323c8d7c4d5f1b3aea7a20074b567638265c1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219901041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3b95b872f7897e3e680ee83772d0db5fc9aa647e45a3dff42f0f127de9a08d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:29 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:29 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9e2ec3da8bf845c0305beb77b1005cf6412f8ebcb0cfce2a89899c4e023bb`  
		Last Modified: Tue, 04 Nov 2025 02:20:10 GMT  
		Size: 37.5 MB (37498778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dc5ff7b6a37478b04b16f01331b0d5f0bd8f01702f3eec3662731f062e6b72`  
		Last Modified: Tue, 04 Nov 2025 02:20:06 GMT  
		Size: 1.3 MB (1275115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b6df820bad278266f680463046cdc57a0ad3375727f29ed0258e450955934`  
		Last Modified: Tue, 04 Nov 2025 10:10:04 GMT  
		Size: 154.9 MB (154914077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:009106f8521484ed850022143f01d96fc277b1b6898941a9a6ee4ddbf818dd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b235791ad1144406c4ed82426acd1b44437499b083d29999f523939687dfe`

```dockerfile
```

-	Layers:
	-	`sha256:245c0c64f0c2235bd62a3b73fa893830227a0d6496bce9a028aa749e1aff6808`  
		Last Modified: Tue, 04 Nov 2025 09:53:46 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:7c6d63097c566fa94e034c9e515d075610eecf14f0b3322edcc4d82ee0af0be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286355447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980b01fbb755da9928701c924fd83523b42df094d512630cf552508f7f3b5048`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:05 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a58e8c8f200cd1433fa21a373e968459d45ea0733a81b582347b54f088fde`  
		Last Modified: Tue, 04 Nov 2025 01:30:57 GMT  
		Size: 42.3 MB (42292994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b56a40b0401a2a36dadc42cebc7ec0ebc25aa21aebd10e07a3ed59a5015f0f`  
		Last Modified: Tue, 04 Nov 2025 01:30:54 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c207aa7e535b085aebd309c2aa1a07bcfe4cb04729fef8251d13b7c6ecc1432f`  
		Last Modified: Tue, 04 Nov 2025 10:10:00 GMT  
		Size: 212.4 MB (212353478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ebcf812d91de37b3654889739ca6de6541bc7c7e5e18074f3138a7c40967fab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be58ecc08316e3af52bb97320641930b11710352008f1b7b2b1e76148e80656`

```dockerfile
```

-	Layers:
	-	`sha256:aa5f20c23d8ed3f617d54b53f61947dab9183d029ce3616c30e73e0809f304a1`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:d83f21195b16b7cd9b67f07ead8b30415dcf81055a96ac649a5055f5842cde19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232961681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68462cc545bd580d3e8fbe24c1209bac247e934f240f221d82343db44a396358`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Thu, 30 Oct 2025 21:34:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Oct 2025 21:34:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Oct 2025 21:34:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Oct 2025 21:34:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 21:34:52 GMT
WORKDIR /root
# Thu, 30 Oct 2025 21:35:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=40132ac8b651895e76011d54d5703cc5a2e126cd396f75a0d9f24729b4f9c79d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bbc36ed5076a95609cccbc6f76f7b077f998acdd4b7f6a22ff66e32412fd5dcf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b440bb5f329c07161ab0396bbc8f739d9c547067cb98b9882932a048bebff62c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=bdc460714c5cefc2984fd0f8fe2c83a907cd15c44d35f43ba8dff3e40a7eb60c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec0f9e08b260538440cd52261c947e1bd83acefb176ac1a0096d41f24b2553b`  
		Last Modified: Thu, 30 Oct 2025 21:40:25 GMT  
		Size: 41.6 MB (41560987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3067dd0e062d97af724bda19fc00d8673cf75edef7a7ab8ab163f1a8cee2682f`  
		Last Modified: Thu, 30 Oct 2025 21:40:21 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa82dfc185344ee822867d21fb16c0682deb95a0f5562aa7963981b9e6327a4c`  
		Last Modified: Thu, 30 Oct 2025 23:54:07 GMT  
		Size: 161.6 MB (161557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:76dfa4756e99a65edd24feebf4e7435084fbca9c8ce9fce7699408b7eb660205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b3d09cff17dcc547f3851f2b82c847bdd1f111a7af821bc384278b37b2fa17`

```dockerfile
```

-	Layers:
	-	`sha256:ced6e766ba285ee13814cf16b9e925bee4cad326ee81dc73a9b87a38184a294c`  
		Last Modified: Thu, 30 Oct 2025 23:53:32 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:89c1ecd039165a2abf664922d066684fc63ee582a6a4eb256831498515da1cc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:b8495dc2a2a7a3658951e9949a4dddbaf43dc26e896b1af4e1a77147ab998528
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:89c1ecd039165a2abf664922d066684fc63ee582a6a4eb256831498515da1cc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:89c1ecd039165a2abf664922d066684fc63ee582a6a4eb256831498515da1cc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a0796ee7c244e22ff51c26d8a622ddea811be59bb07c75650fe64bd41d760719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e7b5b82d6106167157b5b43c7da9305f82d72fb48a1f7be60b40c0122a7e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 04:14:38 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 04:14:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:14:38 GMT
WORKDIR /root
# Tue, 04 Nov 2025 04:14:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf1c275b302982dc816f16843ecbad83fd1bf3e0c5b3c44d25d0cb480721625`  
		Last Modified: Tue, 04 Nov 2025 04:15:30 GMT  
		Size: 42.5 MB (42493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5a187a1cf07d9d457f1f7d57dcaa296189a13d431a763f6929bde20629e87`  
		Last Modified: Tue, 04 Nov 2025 04:15:26 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327997589d047267c1960427fe4a00bd60e7af9094134ebec1d94ca5c2a6461`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 221.2 MB (221247103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1fa460f5432375888e09da4c7640c1558da40b989b41013f200c73a6999919ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0381db9e62d57e66f21da5054dedec9c2a93576082edbfb18c58e321b08ec62`

```dockerfile
```

-	Layers:
	-	`sha256:078527592501e104a4e6109829f7e3064d24c77b910c73ee107cb8563a955de3`  
		Last Modified: Tue, 04 Nov 2025 09:53:24 GMT  
		Size: 20.6 KB (20607 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3d7653f55c597471ae903174696a981b0ab1ee2e2de0d4f0e69cb528f466e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d5bc4ce00a55faf398116c82fc9a8147620734a7cd23014c28cbe12dfb5d99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:19:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 02:19:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 02:19:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:19:13 GMT
WORKDIR /root
# Tue, 04 Nov 2025 02:19:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13f91f4b89054049bdd6bebf2e56ac6de531eb65ff496c94fb4c7867c8b346`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 37.5 MB (37498636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3082cc05a6b1a52facff5438a8263c46bb8eef386f5d339208d1c48a7e668a`  
		Last Modified: Tue, 04 Nov 2025 02:19:51 GMT  
		Size: 1.3 MB (1275126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdca7c7bb09b0bfe0a233d6573f60eb594eacc3271a76d7947fa8939ed1208`  
		Last Modified: Tue, 04 Nov 2025 09:54:08 GMT  
		Size: 155.8 MB (155805190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d37d16d9d86759ea21543a6136ceeae2f469d06e3eff2f7881a770ad9b4912e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9b9336873120bbce88cd63549aab84d9a0eea5df1462e4d6c8c09f800e4ef2`

```dockerfile
```

-	Layers:
	-	`sha256:1c40b4cdc8a3257b9b779d46529d0f757333944b4e6ed4b2e0839be8f8b0c2f9`  
		Last Modified: Tue, 04 Nov 2025 09:53:30 GMT  
		Size: 20.8 KB (20761 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json
