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
