<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10`](#dart310)
-	[`dart:3.10-sdk`](#dart310-sdk)
-	[`dart:3.10.8`](#dart3108)
-	[`dart:3.10.8-sdk`](#dart3108-sdk)
-	[`dart:3.11.0-296.4.beta`](#dart3110-2964beta)
-	[`dart:3.11.0-296.4.beta-sdk`](#dart3110-2964beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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

### `dart:3.10` - linux; amd64

```console
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10-sdk`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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

### `dart:3.10-sdk` - linux; amd64

```console
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.8`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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

### `dart:3.10.8` - linux; amd64

```console
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.8` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.8` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.8` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.8` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.8` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.8` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.8` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.8-sdk`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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

### `dart:3.10.8-sdk` - linux; amd64

```console
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.8-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.8-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.8-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-296.4.beta`

```console
$ docker pull dart@sha256:20f444d971837be8e3298d42b9589c5be49e751d1835ca5e772549cc0edecebc
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

### `dart:3.11.0-296.4.beta` - linux; amd64

```console
$ docker pull dart@sha256:63c61d42b0d8b16b4fa952a18dd8d028bd8dd6cab83d7d91fa5a6d5f2c13aa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307101993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67c4be388967bca2b45926fb2850a06a44f4edbfc369bc5b9f02ec909967539`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:42 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659501e0a35cd3b11d85e1b7a4661d685c1d04f5bf8dc3b2886cfe0d8bc6db6`  
		Last Modified: Tue, 20 Jan 2026 18:10:20 GMT  
		Size: 42.5 MB (42496214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d47aa19a27256935710f4d4e3a49712f6b58d5cb08c70f3dc767ff69fdebc`  
		Last Modified: Tue, 20 Jan 2026 18:10:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3401e8783703add6be754e3b67281c5309ff3df6a71854a0886ca9e2f07741d1`  
		Last Modified: Tue, 20 Jan 2026 18:10:25 GMT  
		Size: 233.0 MB (232961890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.4.beta` - unknown; unknown

```console
$ docker pull dart@sha256:3acc4321de5943ca014c813d2ca46d0d98d49a0585f0518871a317e7ab2bbc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5f2c5549786ab24161000fffe5253d8e723c3bdc8921a4ff46188804b54176`

```dockerfile
```

-	Layers:
	-	`sha256:b20f552f6fb1c0ec3f1b5caa2fd8c7d35ac389fbfe58c42e4b5d370a5e8de39d`  
		Last Modified: Tue, 20 Jan 2026 18:10:18 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.4.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:5edf53cec1cd6f1193267123c069dc86b53c0799606e95af83ff2eecfbb4c899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222900933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b476a95dcf8565b3b4b3df66887589379f7bc13d1257b47e52ba9609fe466a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:06 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:06 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3636bc42ce317d5dd8e95e038f7016a40b3309c32275d350d2b7bc506abc84`  
		Last Modified: Tue, 20 Jan 2026 18:09:36 GMT  
		Size: 37.5 MB (37497718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19f84b01f4d452e08ccfd7797c9dbd4c123b52c7dcb47d9580780d43036ea21`  
		Last Modified: Tue, 20 Jan 2026 18:09:34 GMT  
		Size: 1.3 MB (1273158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0ba39269f6478b64b6e800d223925e2986b58b3a511ffd889bad678f39f01e`  
		Last Modified: Tue, 20 Jan 2026 18:09:38 GMT  
		Size: 157.9 MB (157921447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.4.beta` - unknown; unknown

```console
$ docker pull dart@sha256:bfadbbcf2da4d475882f2ad2a7ea5c0cba37d5fde89fcca8999a4b7fbd3fb252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa109ae992193312d69739212cb823d9a941acb1098e97610127b9fe05856aa4`

```dockerfile
```

-	Layers:
	-	`sha256:c950e29e5ddea6f15b64366510e46b0b1a3c987967073da69e5538d8d489ee58`  
		Last Modified: Tue, 20 Jan 2026 18:09:34 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.4.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:38a86704ef99a9dd0110a6ad863621000ac1ab7ab93cc830548e5cb65d949e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305438026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ede9a32c4685279e163cc0eb990796739ab50bf860eb8455f0bb0658c8d3fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:19 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:19 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:19 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4674896fcb2d13ba80c1c105983c79691468622107884db9f42cf6fe95f49dd9`  
		Last Modified: Tue, 20 Jan 2026 18:10:04 GMT  
		Size: 42.3 MB (42292112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84bf5525cfe2f657e6a04fc41e0118e1c0ae9b91a828ee1837b238d9c95c16d`  
		Last Modified: Tue, 20 Jan 2026 18:10:03 GMT  
		Size: 1.6 MB (1564522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6a03d68923f454ca27775b44fde0c58034fecab06b22fe756ba9dd49efa134`  
		Last Modified: Tue, 20 Jan 2026 18:10:08 GMT  
		Size: 231.4 MB (231447318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.4.beta` - unknown; unknown

```console
$ docker pull dart@sha256:6373e01f928856e4523833f0b27790f673aa6f854ab9dd06833e7318e02e841f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bcc4e2158fe9526be9398894d751e7ba1c03e1362c44defb5859046c936849`

```dockerfile
```

-	Layers:
	-	`sha256:f0f5cdd102a4a74cf77fc275736eacbf551ed1c628352678846685cfa593b42c`  
		Last Modified: Tue, 20 Jan 2026 18:10:03 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.4.beta` - linux; riscv64

```console
$ docker pull dart@sha256:21b0280198017b02f30e648d88004010f7600e759f3e9cf9ae1e687fbab94972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251882011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453ee3791c857759be9f9511d851ae92b39357e45a774c9e324135b20c726c75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 06:09:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 22 Jan 2026 06:09:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 06:09:03 GMT
WORKDIR /root
# Thu, 22 Jan 2026 06:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd964154fd69474bb760acc185c93887153305690d52ca95e5344f66cfc9735f`  
		Last Modified: Thu, 22 Jan 2026 06:14:10 GMT  
		Size: 41.6 MB (41560975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1a3e2e2795c7ed75e644f823196653ca7d26369e21df079bc51ff3212f1e11`  
		Last Modified: Thu, 22 Jan 2026 06:13:59 GMT  
		Size: 1.6 MB (1564661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716b12846ec2225948bdd9736fafb7b5d522aa5651e218eece0d7284456441e5`  
		Last Modified: Thu, 22 Jan 2026 06:14:32 GMT  
		Size: 180.5 MB (180484656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.4.beta` - unknown; unknown

```console
$ docker pull dart@sha256:0dc8585dae936299ac8e380b29c78108e2b3df7d81edfa19fbada47b742132e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfc0b09c9d9da734b208364407804d31d4996b034b7a84e6e097ae66b429794`

```dockerfile
```

-	Layers:
	-	`sha256:29bffaca319258079f9b4a77c56b8c29e5bb2093679f9d7c57d88c8c5913c250`  
		Last Modified: Thu, 22 Jan 2026 06:13:58 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-296.4.beta-sdk`

```console
$ docker pull dart@sha256:20f444d971837be8e3298d42b9589c5be49e751d1835ca5e772549cc0edecebc
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

### `dart:3.11.0-296.4.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:63c61d42b0d8b16b4fa952a18dd8d028bd8dd6cab83d7d91fa5a6d5f2c13aa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307101993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67c4be388967bca2b45926fb2850a06a44f4edbfc369bc5b9f02ec909967539`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:42 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659501e0a35cd3b11d85e1b7a4661d685c1d04f5bf8dc3b2886cfe0d8bc6db6`  
		Last Modified: Tue, 20 Jan 2026 18:10:20 GMT  
		Size: 42.5 MB (42496214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d47aa19a27256935710f4d4e3a49712f6b58d5cb08c70f3dc767ff69fdebc`  
		Last Modified: Tue, 20 Jan 2026 18:10:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3401e8783703add6be754e3b67281c5309ff3df6a71854a0886ca9e2f07741d1`  
		Last Modified: Tue, 20 Jan 2026 18:10:25 GMT  
		Size: 233.0 MB (232961890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.4.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3acc4321de5943ca014c813d2ca46d0d98d49a0585f0518871a317e7ab2bbc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5f2c5549786ab24161000fffe5253d8e723c3bdc8921a4ff46188804b54176`

```dockerfile
```

-	Layers:
	-	`sha256:b20f552f6fb1c0ec3f1b5caa2fd8c7d35ac389fbfe58c42e4b5d370a5e8de39d`  
		Last Modified: Tue, 20 Jan 2026 18:10:18 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.4.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:5edf53cec1cd6f1193267123c069dc86b53c0799606e95af83ff2eecfbb4c899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222900933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b476a95dcf8565b3b4b3df66887589379f7bc13d1257b47e52ba9609fe466a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:06 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:06 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3636bc42ce317d5dd8e95e038f7016a40b3309c32275d350d2b7bc506abc84`  
		Last Modified: Tue, 20 Jan 2026 18:09:36 GMT  
		Size: 37.5 MB (37497718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19f84b01f4d452e08ccfd7797c9dbd4c123b52c7dcb47d9580780d43036ea21`  
		Last Modified: Tue, 20 Jan 2026 18:09:34 GMT  
		Size: 1.3 MB (1273158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0ba39269f6478b64b6e800d223925e2986b58b3a511ffd889bad678f39f01e`  
		Last Modified: Tue, 20 Jan 2026 18:09:38 GMT  
		Size: 157.9 MB (157921447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.4.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bfadbbcf2da4d475882f2ad2a7ea5c0cba37d5fde89fcca8999a4b7fbd3fb252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa109ae992193312d69739212cb823d9a941acb1098e97610127b9fe05856aa4`

```dockerfile
```

-	Layers:
	-	`sha256:c950e29e5ddea6f15b64366510e46b0b1a3c987967073da69e5538d8d489ee58`  
		Last Modified: Tue, 20 Jan 2026 18:09:34 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.4.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:38a86704ef99a9dd0110a6ad863621000ac1ab7ab93cc830548e5cb65d949e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305438026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ede9a32c4685279e163cc0eb990796739ab50bf860eb8455f0bb0658c8d3fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:19 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:19 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:19 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4674896fcb2d13ba80c1c105983c79691468622107884db9f42cf6fe95f49dd9`  
		Last Modified: Tue, 20 Jan 2026 18:10:04 GMT  
		Size: 42.3 MB (42292112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84bf5525cfe2f657e6a04fc41e0118e1c0ae9b91a828ee1837b238d9c95c16d`  
		Last Modified: Tue, 20 Jan 2026 18:10:03 GMT  
		Size: 1.6 MB (1564522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6a03d68923f454ca27775b44fde0c58034fecab06b22fe756ba9dd49efa134`  
		Last Modified: Tue, 20 Jan 2026 18:10:08 GMT  
		Size: 231.4 MB (231447318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.4.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6373e01f928856e4523833f0b27790f673aa6f854ab9dd06833e7318e02e841f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bcc4e2158fe9526be9398894d751e7ba1c03e1362c44defb5859046c936849`

```dockerfile
```

-	Layers:
	-	`sha256:f0f5cdd102a4a74cf77fc275736eacbf551ed1c628352678846685cfa593b42c`  
		Last Modified: Tue, 20 Jan 2026 18:10:03 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.4.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:21b0280198017b02f30e648d88004010f7600e759f3e9cf9ae1e687fbab94972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251882011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453ee3791c857759be9f9511d851ae92b39357e45a774c9e324135b20c726c75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 06:09:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 22 Jan 2026 06:09:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 06:09:03 GMT
WORKDIR /root
# Thu, 22 Jan 2026 06:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd964154fd69474bb760acc185c93887153305690d52ca95e5344f66cfc9735f`  
		Last Modified: Thu, 22 Jan 2026 06:14:10 GMT  
		Size: 41.6 MB (41560975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1a3e2e2795c7ed75e644f823196653ca7d26369e21df079bc51ff3212f1e11`  
		Last Modified: Thu, 22 Jan 2026 06:13:59 GMT  
		Size: 1.6 MB (1564661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716b12846ec2225948bdd9736fafb7b5d522aa5651e218eece0d7284456441e5`  
		Last Modified: Thu, 22 Jan 2026 06:14:32 GMT  
		Size: 180.5 MB (180484656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.4.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0dc8585dae936299ac8e380b29c78108e2b3df7d81edfa19fbada47b742132e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfc0b09c9d9da734b208364407804d31d4996b034b7a84e6e097ae66b429794`

```dockerfile
```

-	Layers:
	-	`sha256:29bffaca319258079f9b4a77c56b8c29e5bb2093679f9d7c57d88c8c5913c250`  
		Last Modified: Thu, 22 Jan 2026 06:13:58 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:20f444d971837be8e3298d42b9589c5be49e751d1835ca5e772549cc0edecebc
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
$ docker pull dart@sha256:63c61d42b0d8b16b4fa952a18dd8d028bd8dd6cab83d7d91fa5a6d5f2c13aa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307101993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67c4be388967bca2b45926fb2850a06a44f4edbfc369bc5b9f02ec909967539`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:42 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659501e0a35cd3b11d85e1b7a4661d685c1d04f5bf8dc3b2886cfe0d8bc6db6`  
		Last Modified: Tue, 20 Jan 2026 18:10:20 GMT  
		Size: 42.5 MB (42496214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d47aa19a27256935710f4d4e3a49712f6b58d5cb08c70f3dc767ff69fdebc`  
		Last Modified: Tue, 20 Jan 2026 18:10:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3401e8783703add6be754e3b67281c5309ff3df6a71854a0886ca9e2f07741d1`  
		Last Modified: Tue, 20 Jan 2026 18:10:25 GMT  
		Size: 233.0 MB (232961890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:3acc4321de5943ca014c813d2ca46d0d98d49a0585f0518871a317e7ab2bbc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5f2c5549786ab24161000fffe5253d8e723c3bdc8921a4ff46188804b54176`

```dockerfile
```

-	Layers:
	-	`sha256:b20f552f6fb1c0ec3f1b5caa2fd8c7d35ac389fbfe58c42e4b5d370a5e8de39d`  
		Last Modified: Tue, 20 Jan 2026 18:10:18 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:5edf53cec1cd6f1193267123c069dc86b53c0799606e95af83ff2eecfbb4c899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222900933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b476a95dcf8565b3b4b3df66887589379f7bc13d1257b47e52ba9609fe466a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:06 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:06 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3636bc42ce317d5dd8e95e038f7016a40b3309c32275d350d2b7bc506abc84`  
		Last Modified: Tue, 20 Jan 2026 18:09:36 GMT  
		Size: 37.5 MB (37497718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19f84b01f4d452e08ccfd7797c9dbd4c123b52c7dcb47d9580780d43036ea21`  
		Last Modified: Tue, 20 Jan 2026 18:09:34 GMT  
		Size: 1.3 MB (1273158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0ba39269f6478b64b6e800d223925e2986b58b3a511ffd889bad678f39f01e`  
		Last Modified: Tue, 20 Jan 2026 18:09:38 GMT  
		Size: 157.9 MB (157921447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:bfadbbcf2da4d475882f2ad2a7ea5c0cba37d5fde89fcca8999a4b7fbd3fb252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa109ae992193312d69739212cb823d9a941acb1098e97610127b9fe05856aa4`

```dockerfile
```

-	Layers:
	-	`sha256:c950e29e5ddea6f15b64366510e46b0b1a3c987967073da69e5538d8d489ee58`  
		Last Modified: Tue, 20 Jan 2026 18:09:34 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:38a86704ef99a9dd0110a6ad863621000ac1ab7ab93cc830548e5cb65d949e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305438026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ede9a32c4685279e163cc0eb990796739ab50bf860eb8455f0bb0658c8d3fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:19 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:19 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:19 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4674896fcb2d13ba80c1c105983c79691468622107884db9f42cf6fe95f49dd9`  
		Last Modified: Tue, 20 Jan 2026 18:10:04 GMT  
		Size: 42.3 MB (42292112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84bf5525cfe2f657e6a04fc41e0118e1c0ae9b91a828ee1837b238d9c95c16d`  
		Last Modified: Tue, 20 Jan 2026 18:10:03 GMT  
		Size: 1.6 MB (1564522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6a03d68923f454ca27775b44fde0c58034fecab06b22fe756ba9dd49efa134`  
		Last Modified: Tue, 20 Jan 2026 18:10:08 GMT  
		Size: 231.4 MB (231447318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:6373e01f928856e4523833f0b27790f673aa6f854ab9dd06833e7318e02e841f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bcc4e2158fe9526be9398894d751e7ba1c03e1362c44defb5859046c936849`

```dockerfile
```

-	Layers:
	-	`sha256:f0f5cdd102a4a74cf77fc275736eacbf551ed1c628352678846685cfa593b42c`  
		Last Modified: Tue, 20 Jan 2026 18:10:03 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:21b0280198017b02f30e648d88004010f7600e759f3e9cf9ae1e687fbab94972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251882011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453ee3791c857759be9f9511d851ae92b39357e45a774c9e324135b20c726c75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 06:09:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 22 Jan 2026 06:09:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 06:09:03 GMT
WORKDIR /root
# Thu, 22 Jan 2026 06:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd964154fd69474bb760acc185c93887153305690d52ca95e5344f66cfc9735f`  
		Last Modified: Thu, 22 Jan 2026 06:14:10 GMT  
		Size: 41.6 MB (41560975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1a3e2e2795c7ed75e644f823196653ca7d26369e21df079bc51ff3212f1e11`  
		Last Modified: Thu, 22 Jan 2026 06:13:59 GMT  
		Size: 1.6 MB (1564661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716b12846ec2225948bdd9736fafb7b5d522aa5651e218eece0d7284456441e5`  
		Last Modified: Thu, 22 Jan 2026 06:14:32 GMT  
		Size: 180.5 MB (180484656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:0dc8585dae936299ac8e380b29c78108e2b3df7d81edfa19fbada47b742132e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfc0b09c9d9da734b208364407804d31d4996b034b7a84e6e097ae66b429794`

```dockerfile
```

-	Layers:
	-	`sha256:29bffaca319258079f9b4a77c56b8c29e5bb2093679f9d7c57d88c8c5913c250`  
		Last Modified: Thu, 22 Jan 2026 06:13:58 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:20f444d971837be8e3298d42b9589c5be49e751d1835ca5e772549cc0edecebc
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
$ docker pull dart@sha256:63c61d42b0d8b16b4fa952a18dd8d028bd8dd6cab83d7d91fa5a6d5f2c13aa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307101993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67c4be388967bca2b45926fb2850a06a44f4edbfc369bc5b9f02ec909967539`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:42 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659501e0a35cd3b11d85e1b7a4661d685c1d04f5bf8dc3b2886cfe0d8bc6db6`  
		Last Modified: Tue, 20 Jan 2026 18:10:20 GMT  
		Size: 42.5 MB (42496214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d47aa19a27256935710f4d4e3a49712f6b58d5cb08c70f3dc767ff69fdebc`  
		Last Modified: Tue, 20 Jan 2026 18:10:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3401e8783703add6be754e3b67281c5309ff3df6a71854a0886ca9e2f07741d1`  
		Last Modified: Tue, 20 Jan 2026 18:10:25 GMT  
		Size: 233.0 MB (232961890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3acc4321de5943ca014c813d2ca46d0d98d49a0585f0518871a317e7ab2bbc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5f2c5549786ab24161000fffe5253d8e723c3bdc8921a4ff46188804b54176`

```dockerfile
```

-	Layers:
	-	`sha256:b20f552f6fb1c0ec3f1b5caa2fd8c7d35ac389fbfe58c42e4b5d370a5e8de39d`  
		Last Modified: Tue, 20 Jan 2026 18:10:18 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:5edf53cec1cd6f1193267123c069dc86b53c0799606e95af83ff2eecfbb4c899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222900933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b476a95dcf8565b3b4b3df66887589379f7bc13d1257b47e52ba9609fe466a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:06 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:06 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3636bc42ce317d5dd8e95e038f7016a40b3309c32275d350d2b7bc506abc84`  
		Last Modified: Tue, 20 Jan 2026 18:09:36 GMT  
		Size: 37.5 MB (37497718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19f84b01f4d452e08ccfd7797c9dbd4c123b52c7dcb47d9580780d43036ea21`  
		Last Modified: Tue, 20 Jan 2026 18:09:34 GMT  
		Size: 1.3 MB (1273158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0ba39269f6478b64b6e800d223925e2986b58b3a511ffd889bad678f39f01e`  
		Last Modified: Tue, 20 Jan 2026 18:09:38 GMT  
		Size: 157.9 MB (157921447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:bfadbbcf2da4d475882f2ad2a7ea5c0cba37d5fde89fcca8999a4b7fbd3fb252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa109ae992193312d69739212cb823d9a941acb1098e97610127b9fe05856aa4`

```dockerfile
```

-	Layers:
	-	`sha256:c950e29e5ddea6f15b64366510e46b0b1a3c987967073da69e5538d8d489ee58`  
		Last Modified: Tue, 20 Jan 2026 18:09:34 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:38a86704ef99a9dd0110a6ad863621000ac1ab7ab93cc830548e5cb65d949e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305438026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ede9a32c4685279e163cc0eb990796739ab50bf860eb8455f0bb0658c8d3fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 20 Jan 2026 18:09:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Jan 2026 18:09:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 Jan 2026 18:09:19 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 Jan 2026 18:09:19 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 18:09:19 GMT
WORKDIR /root
# Tue, 20 Jan 2026 18:09:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4674896fcb2d13ba80c1c105983c79691468622107884db9f42cf6fe95f49dd9`  
		Last Modified: Tue, 20 Jan 2026 18:10:04 GMT  
		Size: 42.3 MB (42292112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84bf5525cfe2f657e6a04fc41e0118e1c0ae9b91a828ee1837b238d9c95c16d`  
		Last Modified: Tue, 20 Jan 2026 18:10:03 GMT  
		Size: 1.6 MB (1564522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6a03d68923f454ca27775b44fde0c58034fecab06b22fe756ba9dd49efa134`  
		Last Modified: Tue, 20 Jan 2026 18:10:08 GMT  
		Size: 231.4 MB (231447318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6373e01f928856e4523833f0b27790f673aa6f854ab9dd06833e7318e02e841f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bcc4e2158fe9526be9398894d751e7ba1c03e1362c44defb5859046c936849`

```dockerfile
```

-	Layers:
	-	`sha256:f0f5cdd102a4a74cf77fc275736eacbf551ed1c628352678846685cfa593b42c`  
		Last Modified: Tue, 20 Jan 2026 18:10:03 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:21b0280198017b02f30e648d88004010f7600e759f3e9cf9ae1e687fbab94972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251882011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453ee3791c857759be9f9511d851ae92b39357e45a774c9e324135b20c726c75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 06:09:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 22 Jan 2026 06:09:03 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 22 Jan 2026 06:09:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 06:09:03 GMT
WORKDIR /root
# Thu, 22 Jan 2026 06:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9c33e9db6593e3ea9b06992a83d404099e1d3da4888651483a67d8c1debc6580;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4809981696ab4aa3898ca0e58f209d38df564d31b379c76312f23eda7efb9b44;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d6e641bbfadebb9ac490177f8e16978a01e964946adb592058fb27efbbbaf4c9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=36e5ebe20a6e8937ba85ead78dbf9335748175fbcf7c4ad6ae8dc84c02ecc91f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd964154fd69474bb760acc185c93887153305690d52ca95e5344f66cfc9735f`  
		Last Modified: Thu, 22 Jan 2026 06:14:10 GMT  
		Size: 41.6 MB (41560975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1a3e2e2795c7ed75e644f823196653ca7d26369e21df079bc51ff3212f1e11`  
		Last Modified: Thu, 22 Jan 2026 06:13:59 GMT  
		Size: 1.6 MB (1564661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716b12846ec2225948bdd9736fafb7b5d522aa5651e218eece0d7284456441e5`  
		Last Modified: Thu, 22 Jan 2026 06:14:32 GMT  
		Size: 180.5 MB (180484656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0dc8585dae936299ac8e380b29c78108e2b3df7d81edfa19fbada47b742132e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfc0b09c9d9da734b208364407804d31d4996b034b7a84e6e097ae66b429794`

```dockerfile
```

-	Layers:
	-	`sha256:29bffaca319258079f9b4a77c56b8c29e5bb2093679f9d7c57d88c8c5913c250`  
		Last Modified: Thu, 22 Jan 2026 06:13:58 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:538a59844eff5c6f6b8c761a974f1f035bb115f68710f6a90c32430af01c2241
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
$ docker pull dart@sha256:19587e256573910385797138af3ea103ef578ddc24693fbd35d11619f8b353b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290231030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6513881f6ef0d02dd7d7f349502d152406b4d0e05cd579e87ac219c095173953`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d04b2c857728e8f5b966145e9d50c495fa1af956174ff545af53dac7b33fbd`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 45.5 MB (45451196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa90025e3411e062e69c9bf47d193d8ae88b168d968075f999fc02c2269f20b`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be10fe465e83c57c60fb76f416a5bcb40f7d342c3e1058d0a802b6290b6c0e8`  
		Last Modified: Tue, 27 Jan 2026 19:55:20 GMT  
		Size: 213.1 MB (213135944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:52ff3ccbcc659b82f6c056f4924d18b99c410956ff47217d76fa1607a2b93f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781ee61cb492828d327ffaa04f395a0c611557075c77b71e2529a79306d8caf`

```dockerfile
```

-	Layers:
	-	`sha256:b70bfc1c0ac3f94a7b2e7a9ea4ecd07d791a86463062da73627fe1c47d4dd6c0`  
		Last Modified: Tue, 27 Jan 2026 19:55:15 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4b4f195237473547740f580c677f837bfe570fb9ddd8d75712a8625ef9063f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222102702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fb02e1d93d388760711e908aa99b9a9cd92a5229112e2de21c3286806ee552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:43 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:43 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a81d6fb184bd2d3df02167d4ff0609b19b9a84c42dcd372332687100f0844`  
		Last Modified: Tue, 27 Jan 2026 19:55:12 GMT  
		Size: 39.7 MB (39696325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f6d0c18f01458c8b2e67b877881acb680bc79a3230d0968ec4052819634cb`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82193abb766ef1eeaf61604bb7d023e2b588fb2b513929ed2c5291ef8b87b43e`  
		Last Modified: Tue, 27 Jan 2026 19:55:14 GMT  
		Size: 154.9 MB (154924611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6e7972329ac5719a4fe814475568b61fea654a264506c38fe12209bedd623ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6375de11caa8136d197ff41be881fd8e8ff1344f4ed9e21fe96c07d63e3c7263`

```dockerfile
```

-	Layers:
	-	`sha256:c3245579a83269566f5a90703cb5351ce3ab61777cd783b8b60f10879b6966f3`  
		Last Modified: Tue, 27 Jan 2026 19:55:10 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bfa70df9d741a981facd32d8eb6edaf8f114e5aafda02cf62c6fbcb2da3ead34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289658563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e49a10f041b74c391e733e2e9021a94656279886002729b1d24c5743c94876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:54:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:54:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:54:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:54:39 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:54:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb727b9fc8a5cb7da06bfdc13c37c8245ddb4fd2792ebbc4d00880c4d8a8b3`  
		Last Modified: Tue, 27 Jan 2026 19:55:18 GMT  
		Size: 45.6 MB (45601663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b0401c51dcf44b41e09ce2d9835c4de1002b6ab5616a17bceb2d59e369691`  
		Last Modified: Tue, 27 Jan 2026 19:55:17 GMT  
		Size: 1.6 MB (1564526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda122a3aa22844ee03b4b9e9f4bc8eb3c4bb21f071c11800a73f87ba01563c`  
		Last Modified: Tue, 27 Jan 2026 19:55:21 GMT  
		Size: 212.4 MB (212358300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dd0ca39c76927bfb4cf2b7b4b9ede16aee2b0589b31920ec9c8be2cebf256b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb27f60ab587f4d5bf45c2088d289b7092f760fd806d4f75634fe0682054b2`

```dockerfile
```

-	Layers:
	-	`sha256:b301ee0dc6c662cc18802c1fd1934d5808c10d03c1c69f72a8a33717b6246e10`  
		Last Modified: Tue, 27 Jan 2026 19:55:16 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:4a2776c565a9d507bea72a24de6f95690408a1e2adfc0e8a9769d6ef76a33a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235579903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3022f640f0031b6d7173b510b344f82da39f12b946be247433c58bc04f65fd4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Tue, 27 Jan 2026 19:56:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 27 Jan 2026 19:56:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 27 Jan 2026 19:56:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 19:56:52 GMT
WORKDIR /root
# Tue, 27 Jan 2026 19:57:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6712007d16203f8928b402800ded0e92357426b83b02417d1573db9cc88b75c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bf800929f939aa2e5278194b10e6f8abf8a29b72d13bdb49cb2460cb316178f8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=584eea4c53f64feda68eba5dc4b2b024275c21003dfccd85a79e934faaac0921;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=02f03a8fd0743342bbbcae3f8d9ccd720b140f8dddb074b968e1a7ac8454dcc8;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.8/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2551a70901ad7a263c4aba5bcc9d9533cb86c00d0ce87bb7adaeff0d3b9da53`  
		Last Modified: Tue, 27 Jan 2026 20:01:38 GMT  
		Size: 44.2 MB (44180524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cdd3dd7d58d14f37366fe77e320ec5dabfc435a4fde0542865d5ce4ef35ea2`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 1.6 MB (1564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b915b85787747729fceee934e2354d5369b88623a7433de7fc6c3aa644d1c6`  
		Last Modified: Tue, 27 Jan 2026 20:01:53 GMT  
		Size: 161.6 MB (161562995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:408c1a19902fe5dd649c0622810d799b5675802ad0992990e1bd43826b059eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f9d6ac9d9a5726c7922043a73c6b332da336cd03964d462d96dd532459c560`

```dockerfile
```

-	Layers:
	-	`sha256:dec564add6a31b9e50765818bba721ade4d6e2384dd382efb58f9c000f9c473d`  
		Last Modified: Tue, 27 Jan 2026 20:01:23 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json
