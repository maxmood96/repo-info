<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.11`](#dart311)
-	[`dart:3.11-sdk`](#dart311-sdk)
-	[`dart:3.11.6`](#dart3116)
-	[`dart:3.11.6-sdk`](#dart3116-sdk)
-	[`dart:3.12.0-327.5.beta`](#dart3120-3275beta)
-	[`dart:3.12.0-327.5.beta-sdk`](#dart3120-3275beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:03b628160f6906098352a6d9c97a147afaa28cf4af97cb588aa33655d6ec3125
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
$ docker pull dart@sha256:6fca8ec81f19ea02852181bb6d6b6f2c8af40b5af71bd44a6f1c17b32726b5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307116306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e27e26babd3fb01528bcf25882ca53099d08b7566bd3072dcba2577811b18c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:20 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93913ed0cb8033f0570b8477e52b7ca740ac11a84df86fc7d5115d437f815459`  
		Last Modified: Wed, 22 Apr 2026 01:41:03 GMT  
		Size: 42.5 MB (42501924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298179b974d51e9ab711dc5b1a58114f2de7132948b19bdb6b0f78f6e313770d`  
		Last Modified: Wed, 22 Apr 2026 01:41:02 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92796381bb8f3ff78540804b0774964079e5601ffeface570828e91b3ba5fa93`  
		Last Modified: Wed, 22 Apr 2026 01:41:07 GMT  
		Size: 233.0 MB (232964605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:83aacecd80616b3300f4ed485be9e1c5513b6a2fd2420dc14640efca1068b6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777686a7b563cad133740613839400d9e851d2f80d9527c112ffabe4a1894d1e`

```dockerfile
```

-	Layers:
	-	`sha256:e28c195613233f34185d9068b372c250d7b95a2bf198299d996a825e1d153c5b`  
		Last Modified: Wed, 22 Apr 2026 01:41:01 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:4767ba45583365fa95d6258dd5c909f1752a6db5c54d638235d85f37a08d5b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222906186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801f2c955e11a50b48164a06274b9126fb0bcb358dee91a5e11dfd03a94defee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:21:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:45 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:21:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d49b850ba491a47364b9d1f7274134b5aa79824e7409ad7bfbcdfca67d6a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:14 GMT  
		Size: 37.5 MB (37495194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d467bfbe77b21ad22523c4aa1c34f73801ab9853380e987d04c386c512eb987`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 1.3 MB (1273180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf038da165c351b846c0060f19a944cc8c9199b30d2022ff2c7bbf2a210d86`  
		Last Modified: Wed, 22 Apr 2026 02:22:18 GMT  
		Size: 157.9 MB (157922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:c0ebe10efd94f3a8be9079a32430f3a68a193d6a6bccd5784c5993285e394992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b09d831f5b96622cf47089865cfc978481009726e41f6782d1798c3dd0192c8`

```dockerfile
```

-	Layers:
	-	`sha256:7884d97136c9700429a63bb44c80547a5aeb1adc101019d0f2b3484317515d3a`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4fa41deadb0cacbe0afe5ef582cc23f656c31a200e35ec63ff227ea4ef0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305460142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747ef0f73bf5a7abf89263e14cfbb790381a26dedfae3c37d8fa71a586fe13e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:03 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2c50602dbae22665348dc0af6960c74d19aca2d3dbdef96e5f831827b5198`  
		Last Modified: Wed, 22 Apr 2026 01:44:43 GMT  
		Size: 42.3 MB (42281614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dffb5391455222f4a4e357fcf3cb2587738e0675054707558cacc130e804c`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ebf1b4fe1896ea7e885a9223dccd0352421f4b266d5b7a546ff0d7a6ee1b9`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 231.5 MB (231470539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:c3e6eeef0c6fcfa350f67726ccbfcb1a162eb5bfe1b547ed8e36ffab5610f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456fef4c864ae0024d5e2343ec0b97f126cf907a83940047c1befe569ca5eef`

```dockerfile
```

-	Layers:
	-	`sha256:c9bc5bc5932727ad6dcff9aae57456f06e748d575dcb7074e2248060abe20667`  
		Last Modified: Wed, 22 Apr 2026 01:44:39 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:7e1e984e969661d0f4165b8de3d66de9e557b8970a0026d3ed9e7232f51a6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251916485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15831e6542b6172fd4674a62c460d8b6a6a06b20e991adfdfed65a6212d70ac4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:24:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
ENV DART_SDK=/usr/lib/dart
# Sun, 26 Apr 2026 15:24:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 15:24:52 GMT
WORKDIR /root
# Sun, 26 Apr 2026 15:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186575cfef57b9d2a3865344d97ada65508c6cde820183fbd72e566cafc5a63`  
		Last Modified: Sun, 26 Apr 2026 15:29:47 GMT  
		Size: 41.6 MB (41571661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8913bbf72e845e075c1a1f1151b56d506d9ff2c90283b3acff0a53050750963`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 1.6 MB (1564398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96e20e050fd7e0bb6868f3f9528987929fbbb6741b55b0d13207363c142032`  
		Last Modified: Sun, 26 Apr 2026 15:30:06 GMT  
		Size: 180.5 MB (180500199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:5306ad4ab4c1eb7ba5aee65db233278fa8d7203d7aaf29470537d048df6f4199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ac85e8fde0cc7ff25159f6d0b92a2150e860aff1501f14b48631f6b790c26`

```dockerfile
```

-	Layers:
	-	`sha256:1135525fb00f68b7f118eb068b3ad6f7236f30278e047f35329303513753e321`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:03b628160f6906098352a6d9c97a147afaa28cf4af97cb588aa33655d6ec3125
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
$ docker pull dart@sha256:6fca8ec81f19ea02852181bb6d6b6f2c8af40b5af71bd44a6f1c17b32726b5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307116306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e27e26babd3fb01528bcf25882ca53099d08b7566bd3072dcba2577811b18c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:20 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93913ed0cb8033f0570b8477e52b7ca740ac11a84df86fc7d5115d437f815459`  
		Last Modified: Wed, 22 Apr 2026 01:41:03 GMT  
		Size: 42.5 MB (42501924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298179b974d51e9ab711dc5b1a58114f2de7132948b19bdb6b0f78f6e313770d`  
		Last Modified: Wed, 22 Apr 2026 01:41:02 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92796381bb8f3ff78540804b0774964079e5601ffeface570828e91b3ba5fa93`  
		Last Modified: Wed, 22 Apr 2026 01:41:07 GMT  
		Size: 233.0 MB (232964605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:83aacecd80616b3300f4ed485be9e1c5513b6a2fd2420dc14640efca1068b6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777686a7b563cad133740613839400d9e851d2f80d9527c112ffabe4a1894d1e`

```dockerfile
```

-	Layers:
	-	`sha256:e28c195613233f34185d9068b372c250d7b95a2bf198299d996a825e1d153c5b`  
		Last Modified: Wed, 22 Apr 2026 01:41:01 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4767ba45583365fa95d6258dd5c909f1752a6db5c54d638235d85f37a08d5b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222906186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801f2c955e11a50b48164a06274b9126fb0bcb358dee91a5e11dfd03a94defee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:21:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:45 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:21:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d49b850ba491a47364b9d1f7274134b5aa79824e7409ad7bfbcdfca67d6a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:14 GMT  
		Size: 37.5 MB (37495194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d467bfbe77b21ad22523c4aa1c34f73801ab9853380e987d04c386c512eb987`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 1.3 MB (1273180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf038da165c351b846c0060f19a944cc8c9199b30d2022ff2c7bbf2a210d86`  
		Last Modified: Wed, 22 Apr 2026 02:22:18 GMT  
		Size: 157.9 MB (157922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c0ebe10efd94f3a8be9079a32430f3a68a193d6a6bccd5784c5993285e394992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b09d831f5b96622cf47089865cfc978481009726e41f6782d1798c3dd0192c8`

```dockerfile
```

-	Layers:
	-	`sha256:7884d97136c9700429a63bb44c80547a5aeb1adc101019d0f2b3484317515d3a`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4fa41deadb0cacbe0afe5ef582cc23f656c31a200e35ec63ff227ea4ef0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305460142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747ef0f73bf5a7abf89263e14cfbb790381a26dedfae3c37d8fa71a586fe13e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:03 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2c50602dbae22665348dc0af6960c74d19aca2d3dbdef96e5f831827b5198`  
		Last Modified: Wed, 22 Apr 2026 01:44:43 GMT  
		Size: 42.3 MB (42281614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dffb5391455222f4a4e357fcf3cb2587738e0675054707558cacc130e804c`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ebf1b4fe1896ea7e885a9223dccd0352421f4b266d5b7a546ff0d7a6ee1b9`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 231.5 MB (231470539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c3e6eeef0c6fcfa350f67726ccbfcb1a162eb5bfe1b547ed8e36ffab5610f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456fef4c864ae0024d5e2343ec0b97f126cf907a83940047c1befe569ca5eef`

```dockerfile
```

-	Layers:
	-	`sha256:c9bc5bc5932727ad6dcff9aae57456f06e748d575dcb7074e2248060abe20667`  
		Last Modified: Wed, 22 Apr 2026 01:44:39 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:7e1e984e969661d0f4165b8de3d66de9e557b8970a0026d3ed9e7232f51a6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251916485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15831e6542b6172fd4674a62c460d8b6a6a06b20e991adfdfed65a6212d70ac4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:24:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
ENV DART_SDK=/usr/lib/dart
# Sun, 26 Apr 2026 15:24:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 15:24:52 GMT
WORKDIR /root
# Sun, 26 Apr 2026 15:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186575cfef57b9d2a3865344d97ada65508c6cde820183fbd72e566cafc5a63`  
		Last Modified: Sun, 26 Apr 2026 15:29:47 GMT  
		Size: 41.6 MB (41571661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8913bbf72e845e075c1a1f1151b56d506d9ff2c90283b3acff0a53050750963`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 1.6 MB (1564398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96e20e050fd7e0bb6868f3f9528987929fbbb6741b55b0d13207363c142032`  
		Last Modified: Sun, 26 Apr 2026 15:30:06 GMT  
		Size: 180.5 MB (180500199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5306ad4ab4c1eb7ba5aee65db233278fa8d7203d7aaf29470537d048df6f4199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ac85e8fde0cc7ff25159f6d0b92a2150e860aff1501f14b48631f6b790c26`

```dockerfile
```

-	Layers:
	-	`sha256:1135525fb00f68b7f118eb068b3ad6f7236f30278e047f35329303513753e321`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11`

```console
$ docker pull dart@sha256:03b628160f6906098352a6d9c97a147afaa28cf4af97cb588aa33655d6ec3125
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

### `dart:3.11` - linux; amd64

```console
$ docker pull dart@sha256:6fca8ec81f19ea02852181bb6d6b6f2c8af40b5af71bd44a6f1c17b32726b5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307116306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e27e26babd3fb01528bcf25882ca53099d08b7566bd3072dcba2577811b18c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:20 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93913ed0cb8033f0570b8477e52b7ca740ac11a84df86fc7d5115d437f815459`  
		Last Modified: Wed, 22 Apr 2026 01:41:03 GMT  
		Size: 42.5 MB (42501924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298179b974d51e9ab711dc5b1a58114f2de7132948b19bdb6b0f78f6e313770d`  
		Last Modified: Wed, 22 Apr 2026 01:41:02 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92796381bb8f3ff78540804b0774964079e5601ffeface570828e91b3ba5fa93`  
		Last Modified: Wed, 22 Apr 2026 01:41:07 GMT  
		Size: 233.0 MB (232964605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:83aacecd80616b3300f4ed485be9e1c5513b6a2fd2420dc14640efca1068b6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777686a7b563cad133740613839400d9e851d2f80d9527c112ffabe4a1894d1e`

```dockerfile
```

-	Layers:
	-	`sha256:e28c195613233f34185d9068b372c250d7b95a2bf198299d996a825e1d153c5b`  
		Last Modified: Wed, 22 Apr 2026 01:41:01 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm variant v7

```console
$ docker pull dart@sha256:4767ba45583365fa95d6258dd5c909f1752a6db5c54d638235d85f37a08d5b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222906186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801f2c955e11a50b48164a06274b9126fb0bcb358dee91a5e11dfd03a94defee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:21:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:45 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:21:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d49b850ba491a47364b9d1f7274134b5aa79824e7409ad7bfbcdfca67d6a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:14 GMT  
		Size: 37.5 MB (37495194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d467bfbe77b21ad22523c4aa1c34f73801ab9853380e987d04c386c512eb987`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 1.3 MB (1273180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf038da165c351b846c0060f19a944cc8c9199b30d2022ff2c7bbf2a210d86`  
		Last Modified: Wed, 22 Apr 2026 02:22:18 GMT  
		Size: 157.9 MB (157922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:c0ebe10efd94f3a8be9079a32430f3a68a193d6a6bccd5784c5993285e394992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b09d831f5b96622cf47089865cfc978481009726e41f6782d1798c3dd0192c8`

```dockerfile
```

-	Layers:
	-	`sha256:7884d97136c9700429a63bb44c80547a5aeb1adc101019d0f2b3484317515d3a`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4fa41deadb0cacbe0afe5ef582cc23f656c31a200e35ec63ff227ea4ef0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305460142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747ef0f73bf5a7abf89263e14cfbb790381a26dedfae3c37d8fa71a586fe13e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:03 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2c50602dbae22665348dc0af6960c74d19aca2d3dbdef96e5f831827b5198`  
		Last Modified: Wed, 22 Apr 2026 01:44:43 GMT  
		Size: 42.3 MB (42281614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dffb5391455222f4a4e357fcf3cb2587738e0675054707558cacc130e804c`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ebf1b4fe1896ea7e885a9223dccd0352421f4b266d5b7a546ff0d7a6ee1b9`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 231.5 MB (231470539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:c3e6eeef0c6fcfa350f67726ccbfcb1a162eb5bfe1b547ed8e36ffab5610f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456fef4c864ae0024d5e2343ec0b97f126cf907a83940047c1befe569ca5eef`

```dockerfile
```

-	Layers:
	-	`sha256:c9bc5bc5932727ad6dcff9aae57456f06e748d575dcb7074e2248060abe20667`  
		Last Modified: Wed, 22 Apr 2026 01:44:39 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; riscv64

```console
$ docker pull dart@sha256:7e1e984e969661d0f4165b8de3d66de9e557b8970a0026d3ed9e7232f51a6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251916485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15831e6542b6172fd4674a62c460d8b6a6a06b20e991adfdfed65a6212d70ac4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:24:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
ENV DART_SDK=/usr/lib/dart
# Sun, 26 Apr 2026 15:24:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 15:24:52 GMT
WORKDIR /root
# Sun, 26 Apr 2026 15:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186575cfef57b9d2a3865344d97ada65508c6cde820183fbd72e566cafc5a63`  
		Last Modified: Sun, 26 Apr 2026 15:29:47 GMT  
		Size: 41.6 MB (41571661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8913bbf72e845e075c1a1f1151b56d506d9ff2c90283b3acff0a53050750963`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 1.6 MB (1564398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96e20e050fd7e0bb6868f3f9528987929fbbb6741b55b0d13207363c142032`  
		Last Modified: Sun, 26 Apr 2026 15:30:06 GMT  
		Size: 180.5 MB (180500199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:5306ad4ab4c1eb7ba5aee65db233278fa8d7203d7aaf29470537d048df6f4199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ac85e8fde0cc7ff25159f6d0b92a2150e860aff1501f14b48631f6b790c26`

```dockerfile
```

-	Layers:
	-	`sha256:1135525fb00f68b7f118eb068b3ad6f7236f30278e047f35329303513753e321`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11-sdk`

```console
$ docker pull dart@sha256:03b628160f6906098352a6d9c97a147afaa28cf4af97cb588aa33655d6ec3125
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

### `dart:3.11-sdk` - linux; amd64

```console
$ docker pull dart@sha256:6fca8ec81f19ea02852181bb6d6b6f2c8af40b5af71bd44a6f1c17b32726b5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307116306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e27e26babd3fb01528bcf25882ca53099d08b7566bd3072dcba2577811b18c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:20 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93913ed0cb8033f0570b8477e52b7ca740ac11a84df86fc7d5115d437f815459`  
		Last Modified: Wed, 22 Apr 2026 01:41:03 GMT  
		Size: 42.5 MB (42501924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298179b974d51e9ab711dc5b1a58114f2de7132948b19bdb6b0f78f6e313770d`  
		Last Modified: Wed, 22 Apr 2026 01:41:02 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92796381bb8f3ff78540804b0774964079e5601ffeface570828e91b3ba5fa93`  
		Last Modified: Wed, 22 Apr 2026 01:41:07 GMT  
		Size: 233.0 MB (232964605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:83aacecd80616b3300f4ed485be9e1c5513b6a2fd2420dc14640efca1068b6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777686a7b563cad133740613839400d9e851d2f80d9527c112ffabe4a1894d1e`

```dockerfile
```

-	Layers:
	-	`sha256:e28c195613233f34185d9068b372c250d7b95a2bf198299d996a825e1d153c5b`  
		Last Modified: Wed, 22 Apr 2026 01:41:01 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4767ba45583365fa95d6258dd5c909f1752a6db5c54d638235d85f37a08d5b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222906186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801f2c955e11a50b48164a06274b9126fb0bcb358dee91a5e11dfd03a94defee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:21:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:45 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:21:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d49b850ba491a47364b9d1f7274134b5aa79824e7409ad7bfbcdfca67d6a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:14 GMT  
		Size: 37.5 MB (37495194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d467bfbe77b21ad22523c4aa1c34f73801ab9853380e987d04c386c512eb987`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 1.3 MB (1273180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf038da165c351b846c0060f19a944cc8c9199b30d2022ff2c7bbf2a210d86`  
		Last Modified: Wed, 22 Apr 2026 02:22:18 GMT  
		Size: 157.9 MB (157922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c0ebe10efd94f3a8be9079a32430f3a68a193d6a6bccd5784c5993285e394992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b09d831f5b96622cf47089865cfc978481009726e41f6782d1798c3dd0192c8`

```dockerfile
```

-	Layers:
	-	`sha256:7884d97136c9700429a63bb44c80547a5aeb1adc101019d0f2b3484317515d3a`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4fa41deadb0cacbe0afe5ef582cc23f656c31a200e35ec63ff227ea4ef0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305460142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747ef0f73bf5a7abf89263e14cfbb790381a26dedfae3c37d8fa71a586fe13e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:03 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2c50602dbae22665348dc0af6960c74d19aca2d3dbdef96e5f831827b5198`  
		Last Modified: Wed, 22 Apr 2026 01:44:43 GMT  
		Size: 42.3 MB (42281614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dffb5391455222f4a4e357fcf3cb2587738e0675054707558cacc130e804c`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ebf1b4fe1896ea7e885a9223dccd0352421f4b266d5b7a546ff0d7a6ee1b9`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 231.5 MB (231470539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c3e6eeef0c6fcfa350f67726ccbfcb1a162eb5bfe1b547ed8e36ffab5610f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456fef4c864ae0024d5e2343ec0b97f126cf907a83940047c1befe569ca5eef`

```dockerfile
```

-	Layers:
	-	`sha256:c9bc5bc5932727ad6dcff9aae57456f06e748d575dcb7074e2248060abe20667`  
		Last Modified: Wed, 22 Apr 2026 01:44:39 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:7e1e984e969661d0f4165b8de3d66de9e557b8970a0026d3ed9e7232f51a6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251916485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15831e6542b6172fd4674a62c460d8b6a6a06b20e991adfdfed65a6212d70ac4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:24:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
ENV DART_SDK=/usr/lib/dart
# Sun, 26 Apr 2026 15:24:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 15:24:52 GMT
WORKDIR /root
# Sun, 26 Apr 2026 15:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186575cfef57b9d2a3865344d97ada65508c6cde820183fbd72e566cafc5a63`  
		Last Modified: Sun, 26 Apr 2026 15:29:47 GMT  
		Size: 41.6 MB (41571661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8913bbf72e845e075c1a1f1151b56d506d9ff2c90283b3acff0a53050750963`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 1.6 MB (1564398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96e20e050fd7e0bb6868f3f9528987929fbbb6741b55b0d13207363c142032`  
		Last Modified: Sun, 26 Apr 2026 15:30:06 GMT  
		Size: 180.5 MB (180500199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5306ad4ab4c1eb7ba5aee65db233278fa8d7203d7aaf29470537d048df6f4199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ac85e8fde0cc7ff25159f6d0b92a2150e860aff1501f14b48631f6b790c26`

```dockerfile
```

-	Layers:
	-	`sha256:1135525fb00f68b7f118eb068b3ad6f7236f30278e047f35329303513753e321`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.6`

**does not exist** (yet?)

## `dart:3.11.6-sdk`

**does not exist** (yet?)

## `dart:3.12.0-327.5.beta`

**does not exist** (yet?)

## `dart:3.12.0-327.5.beta-sdk`

**does not exist** (yet?)

## `dart:beta`

```console
$ docker pull dart@sha256:5306c1008b585f0fbcf23aa0d7145b8f65cd7bd8c63dce4b8038684c11c79833
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
$ docker pull dart@sha256:5a5e63038331ce1d0ba2b26156beac18341f18f8af335d62a324db216e6ceea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310944574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696277c100d28e5c203a6e0378d6b234c9d28e5e8f6287e9ededaa56c0801c58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:35 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fea2dadc9e88a7cb5110796aa9ee706ef9fa24d132e8189877a939a3a1113ac`  
		Last Modified: Wed, 22 Apr 2026 01:41:15 GMT  
		Size: 42.5 MB (42501514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee9b009bf16a2095f5d3ff0a2269578ac38b5f8a5ac44307d4714166ff95446`  
		Last Modified: Wed, 22 Apr 2026 01:41:13 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d718e7672003e0ecbcda896660f10705c198f569cf07915bd551236fac171`  
		Last Modified: Wed, 22 Apr 2026 01:41:19 GMT  
		Size: 236.8 MB (236793285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:44aa8794ab8724ea22e448586859a0a92f8499177e3062e9a50e153362e81fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c2cecdc200075a40947f2c4dec671cd5162af490df16dbd149e73bd30ecdf5`

```dockerfile
```

-	Layers:
	-	`sha256:5c7dadfe38c14b87c8732117752d8988c9a80e904b85d4068286945aece28d02`  
		Last Modified: Wed, 22 Apr 2026 01:41:13 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:0f83384caf05edf0fbf12ebe5d20ecef6871b3e0b0efb3357055651aae5503bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226069463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13fcf3c6962631dcd790b9e1f73e4fda45bfa468a442483c21f2ddfd9778586`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:22:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:22:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:22:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:44 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:22:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333237c91a49b39cc65409ad0d686f27fee3b94ea00c3b6098756977cbed4c73`  
		Last Modified: Wed, 22 Apr 2026 02:23:16 GMT  
		Size: 37.5 MB (37495198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4332623be9bbd9f28f0bbfe63861de75276b4e59bb3179634db01ead2085918f`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 1.3 MB (1273177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025ef8a42e6dfa285b483cade6428d2e97048c4f0c4fc8d03f4530d4e8866fb1`  
		Last Modified: Wed, 22 Apr 2026 02:23:19 GMT  
		Size: 161.1 MB (161086218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:91a8a7b4d40e261263a99b00abfa1ca159a7db691faa2af06370336b2781125e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10412fa3ea92b74319538f0db13a1e75eb2fc50faf55665c55a5bbe873147c3e`

```dockerfile
```

-	Layers:
	-	`sha256:27a58caa0f5fa624d220994788fb2439f256f46e24b36d7fbed154eeb58d85d5`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 19.0 KB (19027 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4524478ae3cc94f38485e9de1f6e2bf224b3b0ab6a5d20d54174ad984d458857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309383181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3596a293ebd89ca2f10efe0f3803a49bfef7d4b676af316fcf1a274edff6734`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:02 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:02 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bb19498fc5188bcb0a6d05429361508e0565823cc9ed18edfab4ff7e0f05ea`  
		Last Modified: Wed, 22 Apr 2026 01:44:48 GMT  
		Size: 42.3 MB (42281521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efad2cba797fc53fadcca3ac39d2deb216a26698b6ebdee5c9e7327e701ad60`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 1.6 MB (1564348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02afc3ca02d42ff44fa1f0ed4bce41fb4b90aac60ba1c59e51eb5ad7cd4232da`  
		Last Modified: Wed, 22 Apr 2026 01:44:52 GMT  
		Size: 235.4 MB (235393674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:53ed671f101995968d85ed151feb3097cc2a92e90214e3bea21f5406a33be8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19d2de0822429892c3a53aa70ce4f284a6586ac6a0400739bd0294ad8f6313e`

```dockerfile
```

-	Layers:
	-	`sha256:3ecd0b4a83a6293b699990b7418d362165d07b5f8397e912ddf6c621af212069`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:ce254eedba347917f65e808992a30ac4efec9718c3420e8f1396e15636810663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248324675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c17f11bc82545891728d30fc4cf2a1a7001d855bdd7bd6815073fe0bb5cde7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:22:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:22:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 23 Apr 2026 16:22:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 23 Apr 2026 16:22:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 16:22:50 GMT
WORKDIR /root
# Thu, 23 Apr 2026 16:23:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292a29185cf0bf4c445d39187669329882c9483017bde8938d8c55a972c82756`  
		Last Modified: Thu, 23 Apr 2026 16:28:09 GMT  
		Size: 41.6 MB (41571832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7799a370d87f67b50d4c560d23d70f778d2279e97845637fcced3620eec15311`  
		Last Modified: Thu, 23 Apr 2026 16:28:02 GMT  
		Size: 1.6 MB (1564396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09709d3eee05add19b965ec619b89d49ef06fd22e543948ead4c645d515dd0ee`  
		Last Modified: Thu, 23 Apr 2026 16:28:28 GMT  
		Size: 176.9 MB (176908220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:7e99c962e81b0b0a9752d8420b5463ef16c200a754e87b8ed9717666fa5f34b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004adff89a7f2681e3dbef2e7a176e93b3e6b0464ee50487ee4738f4e3c8992d`

```dockerfile
```

-	Layers:
	-	`sha256:44719592ec61a23feaca239275827afb044eecfc6c29e6d6bd449f21e79d4319`  
		Last Modified: Thu, 23 Apr 2026 16:27:56 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:5306c1008b585f0fbcf23aa0d7145b8f65cd7bd8c63dce4b8038684c11c79833
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
$ docker pull dart@sha256:5a5e63038331ce1d0ba2b26156beac18341f18f8af335d62a324db216e6ceea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310944574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696277c100d28e5c203a6e0378d6b234c9d28e5e8f6287e9ededaa56c0801c58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:35 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fea2dadc9e88a7cb5110796aa9ee706ef9fa24d132e8189877a939a3a1113ac`  
		Last Modified: Wed, 22 Apr 2026 01:41:15 GMT  
		Size: 42.5 MB (42501514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee9b009bf16a2095f5d3ff0a2269578ac38b5f8a5ac44307d4714166ff95446`  
		Last Modified: Wed, 22 Apr 2026 01:41:13 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644d718e7672003e0ecbcda896660f10705c198f569cf07915bd551236fac171`  
		Last Modified: Wed, 22 Apr 2026 01:41:19 GMT  
		Size: 236.8 MB (236793285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:44aa8794ab8724ea22e448586859a0a92f8499177e3062e9a50e153362e81fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c2cecdc200075a40947f2c4dec671cd5162af490df16dbd149e73bd30ecdf5`

```dockerfile
```

-	Layers:
	-	`sha256:5c7dadfe38c14b87c8732117752d8988c9a80e904b85d4068286945aece28d02`  
		Last Modified: Wed, 22 Apr 2026 01:41:13 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:0f83384caf05edf0fbf12ebe5d20ecef6871b3e0b0efb3357055651aae5503bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226069463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13fcf3c6962631dcd790b9e1f73e4fda45bfa468a442483c21f2ddfd9778586`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:22:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:22:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:22:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:44 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:22:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333237c91a49b39cc65409ad0d686f27fee3b94ea00c3b6098756977cbed4c73`  
		Last Modified: Wed, 22 Apr 2026 02:23:16 GMT  
		Size: 37.5 MB (37495198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4332623be9bbd9f28f0bbfe63861de75276b4e59bb3179634db01ead2085918f`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 1.3 MB (1273177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025ef8a42e6dfa285b483cade6428d2e97048c4f0c4fc8d03f4530d4e8866fb1`  
		Last Modified: Wed, 22 Apr 2026 02:23:19 GMT  
		Size: 161.1 MB (161086218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:91a8a7b4d40e261263a99b00abfa1ca159a7db691faa2af06370336b2781125e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10412fa3ea92b74319538f0db13a1e75eb2fc50faf55665c55a5bbe873147c3e`

```dockerfile
```

-	Layers:
	-	`sha256:27a58caa0f5fa624d220994788fb2439f256f46e24b36d7fbed154eeb58d85d5`  
		Last Modified: Wed, 22 Apr 2026 02:23:15 GMT  
		Size: 19.0 KB (19027 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4524478ae3cc94f38485e9de1f6e2bf224b3b0ab6a5d20d54174ad984d458857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309383181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3596a293ebd89ca2f10efe0f3803a49bfef7d4b676af316fcf1a274edff6734`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:02 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:02 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bb19498fc5188bcb0a6d05429361508e0565823cc9ed18edfab4ff7e0f05ea`  
		Last Modified: Wed, 22 Apr 2026 01:44:48 GMT  
		Size: 42.3 MB (42281521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efad2cba797fc53fadcca3ac39d2deb216a26698b6ebdee5c9e7327e701ad60`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 1.6 MB (1564348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02afc3ca02d42ff44fa1f0ed4bce41fb4b90aac60ba1c59e51eb5ad7cd4232da`  
		Last Modified: Wed, 22 Apr 2026 01:44:52 GMT  
		Size: 235.4 MB (235393674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:53ed671f101995968d85ed151feb3097cc2a92e90214e3bea21f5406a33be8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19d2de0822429892c3a53aa70ce4f284a6586ac6a0400739bd0294ad8f6313e`

```dockerfile
```

-	Layers:
	-	`sha256:3ecd0b4a83a6293b699990b7418d362165d07b5f8397e912ddf6c621af212069`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:ce254eedba347917f65e808992a30ac4efec9718c3420e8f1396e15636810663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248324675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c17f11bc82545891728d30fc4cf2a1a7001d855bdd7bd6815073fe0bb5cde7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 16:22:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 16:22:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 23 Apr 2026 16:22:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 23 Apr 2026 16:22:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 16:22:50 GMT
WORKDIR /root
# Thu, 23 Apr 2026 16:23:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=60484d3bb620de44f11b0078571f288fe1b5c6207369e4a5a92a0d942fe183d7;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bd92bd905c5208ce6b7063db7a820ae78d90b9d4c0b6a9d1091e794a93721d8d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1053dde7acf75a594b81f1612e7eab427a62b69f73339667b87f6224e705e695;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=90eafc92bc56cc141462cae7aef2ce02bcc1a0111e68be67bc188cf695fbf46b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292a29185cf0bf4c445d39187669329882c9483017bde8938d8c55a972c82756`  
		Last Modified: Thu, 23 Apr 2026 16:28:09 GMT  
		Size: 41.6 MB (41571832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7799a370d87f67b50d4c560d23d70f778d2279e97845637fcced3620eec15311`  
		Last Modified: Thu, 23 Apr 2026 16:28:02 GMT  
		Size: 1.6 MB (1564396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09709d3eee05add19b965ec619b89d49ef06fd22e543948ead4c645d515dd0ee`  
		Last Modified: Thu, 23 Apr 2026 16:28:28 GMT  
		Size: 176.9 MB (176908220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7e99c962e81b0b0a9752d8420b5463ef16c200a754e87b8ed9717666fa5f34b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004adff89a7f2681e3dbef2e7a176e93b3e6b0464ee50487ee4738f4e3c8992d`

```dockerfile
```

-	Layers:
	-	`sha256:44719592ec61a23feaca239275827afb044eecfc6c29e6d6bd449f21e79d4319`  
		Last Modified: Thu, 23 Apr 2026 16:27:56 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:03b628160f6906098352a6d9c97a147afaa28cf4af97cb588aa33655d6ec3125
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
$ docker pull dart@sha256:6fca8ec81f19ea02852181bb6d6b6f2c8af40b5af71bd44a6f1c17b32726b5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307116306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e27e26babd3fb01528bcf25882ca53099d08b7566bd3072dcba2577811b18c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:20 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93913ed0cb8033f0570b8477e52b7ca740ac11a84df86fc7d5115d437f815459`  
		Last Modified: Wed, 22 Apr 2026 01:41:03 GMT  
		Size: 42.5 MB (42501924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298179b974d51e9ab711dc5b1a58114f2de7132948b19bdb6b0f78f6e313770d`  
		Last Modified: Wed, 22 Apr 2026 01:41:02 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92796381bb8f3ff78540804b0774964079e5601ffeface570828e91b3ba5fa93`  
		Last Modified: Wed, 22 Apr 2026 01:41:07 GMT  
		Size: 233.0 MB (232964605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:83aacecd80616b3300f4ed485be9e1c5513b6a2fd2420dc14640efca1068b6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777686a7b563cad133740613839400d9e851d2f80d9527c112ffabe4a1894d1e`

```dockerfile
```

-	Layers:
	-	`sha256:e28c195613233f34185d9068b372c250d7b95a2bf198299d996a825e1d153c5b`  
		Last Modified: Wed, 22 Apr 2026 01:41:01 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:4767ba45583365fa95d6258dd5c909f1752a6db5c54d638235d85f37a08d5b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222906186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801f2c955e11a50b48164a06274b9126fb0bcb358dee91a5e11dfd03a94defee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:21:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:45 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:21:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d49b850ba491a47364b9d1f7274134b5aa79824e7409ad7bfbcdfca67d6a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:14 GMT  
		Size: 37.5 MB (37495194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d467bfbe77b21ad22523c4aa1c34f73801ab9853380e987d04c386c512eb987`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 1.3 MB (1273180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf038da165c351b846c0060f19a944cc8c9199b30d2022ff2c7bbf2a210d86`  
		Last Modified: Wed, 22 Apr 2026 02:22:18 GMT  
		Size: 157.9 MB (157922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:c0ebe10efd94f3a8be9079a32430f3a68a193d6a6bccd5784c5993285e394992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b09d831f5b96622cf47089865cfc978481009726e41f6782d1798c3dd0192c8`

```dockerfile
```

-	Layers:
	-	`sha256:7884d97136c9700429a63bb44c80547a5aeb1adc101019d0f2b3484317515d3a`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4fa41deadb0cacbe0afe5ef582cc23f656c31a200e35ec63ff227ea4ef0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305460142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747ef0f73bf5a7abf89263e14cfbb790381a26dedfae3c37d8fa71a586fe13e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:03 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2c50602dbae22665348dc0af6960c74d19aca2d3dbdef96e5f831827b5198`  
		Last Modified: Wed, 22 Apr 2026 01:44:43 GMT  
		Size: 42.3 MB (42281614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dffb5391455222f4a4e357fcf3cb2587738e0675054707558cacc130e804c`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ebf1b4fe1896ea7e885a9223dccd0352421f4b266d5b7a546ff0d7a6ee1b9`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 231.5 MB (231470539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:c3e6eeef0c6fcfa350f67726ccbfcb1a162eb5bfe1b547ed8e36ffab5610f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456fef4c864ae0024d5e2343ec0b97f126cf907a83940047c1befe569ca5eef`

```dockerfile
```

-	Layers:
	-	`sha256:c9bc5bc5932727ad6dcff9aae57456f06e748d575dcb7074e2248060abe20667`  
		Last Modified: Wed, 22 Apr 2026 01:44:39 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:7e1e984e969661d0f4165b8de3d66de9e557b8970a0026d3ed9e7232f51a6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251916485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15831e6542b6172fd4674a62c460d8b6a6a06b20e991adfdfed65a6212d70ac4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:24:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
ENV DART_SDK=/usr/lib/dart
# Sun, 26 Apr 2026 15:24:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 15:24:52 GMT
WORKDIR /root
# Sun, 26 Apr 2026 15:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186575cfef57b9d2a3865344d97ada65508c6cde820183fbd72e566cafc5a63`  
		Last Modified: Sun, 26 Apr 2026 15:29:47 GMT  
		Size: 41.6 MB (41571661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8913bbf72e845e075c1a1f1151b56d506d9ff2c90283b3acff0a53050750963`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 1.6 MB (1564398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96e20e050fd7e0bb6868f3f9528987929fbbb6741b55b0d13207363c142032`  
		Last Modified: Sun, 26 Apr 2026 15:30:06 GMT  
		Size: 180.5 MB (180500199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:5306ad4ab4c1eb7ba5aee65db233278fa8d7203d7aaf29470537d048df6f4199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ac85e8fde0cc7ff25159f6d0b92a2150e860aff1501f14b48631f6b790c26`

```dockerfile
```

-	Layers:
	-	`sha256:1135525fb00f68b7f118eb068b3ad6f7236f30278e047f35329303513753e321`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:03b628160f6906098352a6d9c97a147afaa28cf4af97cb588aa33655d6ec3125
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
$ docker pull dart@sha256:6fca8ec81f19ea02852181bb6d6b6f2c8af40b5af71bd44a6f1c17b32726b5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307116306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e27e26babd3fb01528bcf25882ca53099d08b7566bd3072dcba2577811b18c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:20 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93913ed0cb8033f0570b8477e52b7ca740ac11a84df86fc7d5115d437f815459`  
		Last Modified: Wed, 22 Apr 2026 01:41:03 GMT  
		Size: 42.5 MB (42501924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298179b974d51e9ab711dc5b1a58114f2de7132948b19bdb6b0f78f6e313770d`  
		Last Modified: Wed, 22 Apr 2026 01:41:02 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92796381bb8f3ff78540804b0774964079e5601ffeface570828e91b3ba5fa93`  
		Last Modified: Wed, 22 Apr 2026 01:41:07 GMT  
		Size: 233.0 MB (232964605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:83aacecd80616b3300f4ed485be9e1c5513b6a2fd2420dc14640efca1068b6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777686a7b563cad133740613839400d9e851d2f80d9527c112ffabe4a1894d1e`

```dockerfile
```

-	Layers:
	-	`sha256:e28c195613233f34185d9068b372c250d7b95a2bf198299d996a825e1d153c5b`  
		Last Modified: Wed, 22 Apr 2026 01:41:01 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4767ba45583365fa95d6258dd5c909f1752a6db5c54d638235d85f37a08d5b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222906186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801f2c955e11a50b48164a06274b9126fb0bcb358dee91a5e11dfd03a94defee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:21:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:45 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:21:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d49b850ba491a47364b9d1f7274134b5aa79824e7409ad7bfbcdfca67d6a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:14 GMT  
		Size: 37.5 MB (37495194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d467bfbe77b21ad22523c4aa1c34f73801ab9853380e987d04c386c512eb987`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 1.3 MB (1273180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf038da165c351b846c0060f19a944cc8c9199b30d2022ff2c7bbf2a210d86`  
		Last Modified: Wed, 22 Apr 2026 02:22:18 GMT  
		Size: 157.9 MB (157922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c0ebe10efd94f3a8be9079a32430f3a68a193d6a6bccd5784c5993285e394992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b09d831f5b96622cf47089865cfc978481009726e41f6782d1798c3dd0192c8`

```dockerfile
```

-	Layers:
	-	`sha256:7884d97136c9700429a63bb44c80547a5aeb1adc101019d0f2b3484317515d3a`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4fa41deadb0cacbe0afe5ef582cc23f656c31a200e35ec63ff227ea4ef0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305460142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747ef0f73bf5a7abf89263e14cfbb790381a26dedfae3c37d8fa71a586fe13e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:03 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2c50602dbae22665348dc0af6960c74d19aca2d3dbdef96e5f831827b5198`  
		Last Modified: Wed, 22 Apr 2026 01:44:43 GMT  
		Size: 42.3 MB (42281614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dffb5391455222f4a4e357fcf3cb2587738e0675054707558cacc130e804c`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ebf1b4fe1896ea7e885a9223dccd0352421f4b266d5b7a546ff0d7a6ee1b9`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 231.5 MB (231470539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c3e6eeef0c6fcfa350f67726ccbfcb1a162eb5bfe1b547ed8e36ffab5610f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456fef4c864ae0024d5e2343ec0b97f126cf907a83940047c1befe569ca5eef`

```dockerfile
```

-	Layers:
	-	`sha256:c9bc5bc5932727ad6dcff9aae57456f06e748d575dcb7074e2248060abe20667`  
		Last Modified: Wed, 22 Apr 2026 01:44:39 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:7e1e984e969661d0f4165b8de3d66de9e557b8970a0026d3ed9e7232f51a6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251916485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15831e6542b6172fd4674a62c460d8b6a6a06b20e991adfdfed65a6212d70ac4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:24:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
ENV DART_SDK=/usr/lib/dart
# Sun, 26 Apr 2026 15:24:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 15:24:52 GMT
WORKDIR /root
# Sun, 26 Apr 2026 15:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186575cfef57b9d2a3865344d97ada65508c6cde820183fbd72e566cafc5a63`  
		Last Modified: Sun, 26 Apr 2026 15:29:47 GMT  
		Size: 41.6 MB (41571661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8913bbf72e845e075c1a1f1151b56d506d9ff2c90283b3acff0a53050750963`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 1.6 MB (1564398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96e20e050fd7e0bb6868f3f9528987929fbbb6741b55b0d13207363c142032`  
		Last Modified: Sun, 26 Apr 2026 15:30:06 GMT  
		Size: 180.5 MB (180500199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5306ad4ab4c1eb7ba5aee65db233278fa8d7203d7aaf29470537d048df6f4199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ac85e8fde0cc7ff25159f6d0b92a2150e860aff1501f14b48631f6b790c26`

```dockerfile
```

-	Layers:
	-	`sha256:1135525fb00f68b7f118eb068b3ad6f7236f30278e047f35329303513753e321`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:03b628160f6906098352a6d9c97a147afaa28cf4af97cb588aa33655d6ec3125
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
$ docker pull dart@sha256:6fca8ec81f19ea02852181bb6d6b6f2c8af40b5af71bd44a6f1c17b32726b5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307116306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e27e26babd3fb01528bcf25882ca53099d08b7566bd3072dcba2577811b18c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:20 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93913ed0cb8033f0570b8477e52b7ca740ac11a84df86fc7d5115d437f815459`  
		Last Modified: Wed, 22 Apr 2026 01:41:03 GMT  
		Size: 42.5 MB (42501924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298179b974d51e9ab711dc5b1a58114f2de7132948b19bdb6b0f78f6e313770d`  
		Last Modified: Wed, 22 Apr 2026 01:41:02 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92796381bb8f3ff78540804b0774964079e5601ffeface570828e91b3ba5fa93`  
		Last Modified: Wed, 22 Apr 2026 01:41:07 GMT  
		Size: 233.0 MB (232964605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:83aacecd80616b3300f4ed485be9e1c5513b6a2fd2420dc14640efca1068b6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777686a7b563cad133740613839400d9e851d2f80d9527c112ffabe4a1894d1e`

```dockerfile
```

-	Layers:
	-	`sha256:e28c195613233f34185d9068b372c250d7b95a2bf198299d996a825e1d153c5b`  
		Last Modified: Wed, 22 Apr 2026 01:41:01 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:4767ba45583365fa95d6258dd5c909f1752a6db5c54d638235d85f37a08d5b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222906186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801f2c955e11a50b48164a06274b9126fb0bcb358dee91a5e11dfd03a94defee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:21:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:45 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:21:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d49b850ba491a47364b9d1f7274134b5aa79824e7409ad7bfbcdfca67d6a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:14 GMT  
		Size: 37.5 MB (37495194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d467bfbe77b21ad22523c4aa1c34f73801ab9853380e987d04c386c512eb987`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 1.3 MB (1273180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf038da165c351b846c0060f19a944cc8c9199b30d2022ff2c7bbf2a210d86`  
		Last Modified: Wed, 22 Apr 2026 02:22:18 GMT  
		Size: 157.9 MB (157922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:c0ebe10efd94f3a8be9079a32430f3a68a193d6a6bccd5784c5993285e394992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b09d831f5b96622cf47089865cfc978481009726e41f6782d1798c3dd0192c8`

```dockerfile
```

-	Layers:
	-	`sha256:7884d97136c9700429a63bb44c80547a5aeb1adc101019d0f2b3484317515d3a`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4fa41deadb0cacbe0afe5ef582cc23f656c31a200e35ec63ff227ea4ef0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305460142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747ef0f73bf5a7abf89263e14cfbb790381a26dedfae3c37d8fa71a586fe13e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:03 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2c50602dbae22665348dc0af6960c74d19aca2d3dbdef96e5f831827b5198`  
		Last Modified: Wed, 22 Apr 2026 01:44:43 GMT  
		Size: 42.3 MB (42281614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dffb5391455222f4a4e357fcf3cb2587738e0675054707558cacc130e804c`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ebf1b4fe1896ea7e885a9223dccd0352421f4b266d5b7a546ff0d7a6ee1b9`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 231.5 MB (231470539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:c3e6eeef0c6fcfa350f67726ccbfcb1a162eb5bfe1b547ed8e36ffab5610f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456fef4c864ae0024d5e2343ec0b97f126cf907a83940047c1befe569ca5eef`

```dockerfile
```

-	Layers:
	-	`sha256:c9bc5bc5932727ad6dcff9aae57456f06e748d575dcb7074e2248060abe20667`  
		Last Modified: Wed, 22 Apr 2026 01:44:39 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:7e1e984e969661d0f4165b8de3d66de9e557b8970a0026d3ed9e7232f51a6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251916485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15831e6542b6172fd4674a62c460d8b6a6a06b20e991adfdfed65a6212d70ac4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:24:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
ENV DART_SDK=/usr/lib/dart
# Sun, 26 Apr 2026 15:24:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 15:24:52 GMT
WORKDIR /root
# Sun, 26 Apr 2026 15:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186575cfef57b9d2a3865344d97ada65508c6cde820183fbd72e566cafc5a63`  
		Last Modified: Sun, 26 Apr 2026 15:29:47 GMT  
		Size: 41.6 MB (41571661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8913bbf72e845e075c1a1f1151b56d506d9ff2c90283b3acff0a53050750963`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 1.6 MB (1564398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96e20e050fd7e0bb6868f3f9528987929fbbb6741b55b0d13207363c142032`  
		Last Modified: Sun, 26 Apr 2026 15:30:06 GMT  
		Size: 180.5 MB (180500199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:5306ad4ab4c1eb7ba5aee65db233278fa8d7203d7aaf29470537d048df6f4199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ac85e8fde0cc7ff25159f6d0b92a2150e860aff1501f14b48631f6b790c26`

```dockerfile
```

-	Layers:
	-	`sha256:1135525fb00f68b7f118eb068b3ad6f7236f30278e047f35329303513753e321`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:03b628160f6906098352a6d9c97a147afaa28cf4af97cb588aa33655d6ec3125
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
$ docker pull dart@sha256:6fca8ec81f19ea02852181bb6d6b6f2c8af40b5af71bd44a6f1c17b32726b5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307116306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e27e26babd3fb01528bcf25882ca53099d08b7566bd3072dcba2577811b18c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:40:20 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:40:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:40:20 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:40:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93913ed0cb8033f0570b8477e52b7ca740ac11a84df86fc7d5115d437f815459`  
		Last Modified: Wed, 22 Apr 2026 01:41:03 GMT  
		Size: 42.5 MB (42501924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298179b974d51e9ab711dc5b1a58114f2de7132948b19bdb6b0f78f6e313770d`  
		Last Modified: Wed, 22 Apr 2026 01:41:02 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92796381bb8f3ff78540804b0774964079e5601ffeface570828e91b3ba5fa93`  
		Last Modified: Wed, 22 Apr 2026 01:41:07 GMT  
		Size: 233.0 MB (232964605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:83aacecd80616b3300f4ed485be9e1c5513b6a2fd2420dc14640efca1068b6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777686a7b563cad133740613839400d9e851d2f80d9527c112ffabe4a1894d1e`

```dockerfile
```

-	Layers:
	-	`sha256:e28c195613233f34185d9068b372c250d7b95a2bf198299d996a825e1d153c5b`  
		Last Modified: Wed, 22 Apr 2026 01:41:01 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4767ba45583365fa95d6258dd5c909f1752a6db5c54d638235d85f37a08d5b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222906186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801f2c955e11a50b48164a06274b9126fb0bcb358dee91a5e11dfd03a94defee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 02:21:45 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 02:21:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:45 GMT
WORKDIR /root
# Wed, 22 Apr 2026 02:21:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d49b850ba491a47364b9d1f7274134b5aa79824e7409ad7bfbcdfca67d6a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:14 GMT  
		Size: 37.5 MB (37495194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d467bfbe77b21ad22523c4aa1c34f73801ab9853380e987d04c386c512eb987`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 1.3 MB (1273180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badf038da165c351b846c0060f19a944cc8c9199b30d2022ff2c7bbf2a210d86`  
		Last Modified: Wed, 22 Apr 2026 02:22:18 GMT  
		Size: 157.9 MB (157922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c0ebe10efd94f3a8be9079a32430f3a68a193d6a6bccd5784c5993285e394992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b09d831f5b96622cf47089865cfc978481009726e41f6782d1798c3dd0192c8`

```dockerfile
```

-	Layers:
	-	`sha256:7884d97136c9700429a63bb44c80547a5aeb1adc101019d0f2b3484317515d3a`  
		Last Modified: Wed, 22 Apr 2026 02:22:12 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86a4fa41deadb0cacbe0afe5ef582cc23f656c31a200e35ec63ff227ea4ef0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305460142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2747ef0f73bf5a7abf89263e14cfbb790381a26dedfae3c37d8fa71a586fe13e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 22 Apr 2026 01:44:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:44:03 GMT
WORKDIR /root
# Wed, 22 Apr 2026 01:44:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2c50602dbae22665348dc0af6960c74d19aca2d3dbdef96e5f831827b5198`  
		Last Modified: Wed, 22 Apr 2026 01:44:43 GMT  
		Size: 42.3 MB (42281614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dffb5391455222f4a4e357fcf3cb2587738e0675054707558cacc130e804c`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65ebf1b4fe1896ea7e885a9223dccd0352421f4b266d5b7a546ff0d7a6ee1b9`  
		Last Modified: Wed, 22 Apr 2026 01:44:46 GMT  
		Size: 231.5 MB (231470539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c3e6eeef0c6fcfa350f67726ccbfcb1a162eb5bfe1b547ed8e36ffab5610f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b456fef4c864ae0024d5e2343ec0b97f126cf907a83940047c1befe569ca5eef`

```dockerfile
```

-	Layers:
	-	`sha256:c9bc5bc5932727ad6dcff9aae57456f06e748d575dcb7074e2248060abe20667`  
		Last Modified: Wed, 22 Apr 2026 01:44:39 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:7e1e984e969661d0f4165b8de3d66de9e557b8970a0026d3ed9e7232f51a6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251916485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15831e6542b6172fd4674a62c460d8b6a6a06b20e991adfdfed65a6212d70ac4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Sun, 26 Apr 2026 15:24:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Sun, 26 Apr 2026 15:24:52 GMT
ENV DART_SDK=/usr/lib/dart
# Sun, 26 Apr 2026 15:24:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 26 Apr 2026 15:24:52 GMT
WORKDIR /root
# Sun, 26 Apr 2026 15:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=57f3ab5ac24883060b1ff12bcdac472ed76563ec7364e88f8a6d41e4f0db075f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=27a3fd1eed416866171c833e98081d051ec7667d6c6f1d4a6d8f5637ac852433;             SDK_ARCH="arm";;         arm64)             DART_SHA256=50e9aba58f8717943854778a73074e63a80c42054355d35e2732a0cc0824a2fb;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=c4b5be61da02b440e82b02cf9084cafbbdd401b4bff1c436afcf0d634d696f40;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0186575cfef57b9d2a3865344d97ada65508c6cde820183fbd72e566cafc5a63`  
		Last Modified: Sun, 26 Apr 2026 15:29:47 GMT  
		Size: 41.6 MB (41571661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8913bbf72e845e075c1a1f1151b56d506d9ff2c90283b3acff0a53050750963`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 1.6 MB (1564398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96e20e050fd7e0bb6868f3f9528987929fbbb6741b55b0d13207363c142032`  
		Last Modified: Sun, 26 Apr 2026 15:30:06 GMT  
		Size: 180.5 MB (180500199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5306ad4ab4c1eb7ba5aee65db233278fa8d7203d7aaf29470537d048df6f4199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ac85e8fde0cc7ff25159f6d0b92a2150e860aff1501f14b48631f6b790c26`

```dockerfile
```

-	Layers:
	-	`sha256:1135525fb00f68b7f118eb068b3ad6f7236f30278e047f35329303513753e321`  
		Last Modified: Sun, 26 Apr 2026 15:29:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
