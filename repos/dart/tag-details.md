<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10.0-162.1.beta`](#dart3100-1621beta)
-	[`dart:3.10.0-162.1.beta-sdk`](#dart3100-1621beta-sdk)
-	[`dart:3.9`](#dart39)
-	[`dart:3.9-sdk`](#dart39-sdk)
-	[`dart:3.9.3`](#dart393)
-	[`dart:3.9.3-sdk`](#dart393-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:9ce249a31fea84c84e1ed4f146efd151e396a5ecb7e63132761b31ef49b806f8
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
$ docker pull dart@sha256:dbafa8fb6b7c32c1b7b5c99490a2fc8fa01b13802fa4c94eb80a3aa3080693f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3354ad9bfad9b68af66ae0e60ab850a48425f98dfe5f3fe61d9399602b2fd6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa017a2e4e070dc98cedc8136363140f1334ed1f59a8e561edf5d8a120c23c`  
		Last Modified: Wed, 10 Sep 2025 22:33:41 GMT  
		Size: 42.5 MB (42482435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772f519b79547b31df7388c527ed606ae7a98ddb485f95f74236e2ae535fec6`  
		Last Modified: Wed, 10 Sep 2025 22:33:53 GMT  
		Size: 1.9 MB (1873599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a56ce38740fdf24d591a6aec4b3e16d4c8aaa8ad6214bf1926f130b137d3d`  
		Last Modified: Wed, 10 Sep 2025 23:54:34 GMT  
		Size: 221.2 MB (221236204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:e696f277562a36065824bb02956d7ffa857829ae162c1754658aeb6c8fa9f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47775006165bb8bce196426d9b0949cf8032131dca0d95712d34ddac44093a04`

```dockerfile
```

-	Layers:
	-	`sha256:45d14cb197a3c4a8d76e5ae2d59fa4c1b4d7164fdf1ed403680349bd366cb008`  
		Last Modified: Wed, 10 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:560c1175ec393e649a466b7cba87dcc5ad4efbb67448199564104d98f8b38bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294668027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f150a6dde5176f97876201bf912130bd852c4275c27e8f05d6c127ebc5403a7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151afe059b51b63d546871fc76cbbee94277727ccc3c2ff21341fcfa77c5fffa`  
		Last Modified: Wed, 10 Sep 2025 22:34:09 GMT  
		Size: 42.3 MB (42270175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c5056acb14aaa96e99a889410f2097e61c8486626b8537227ad1f25854d6c`  
		Last Modified: Wed, 10 Sep 2025 22:34:05 GMT  
		Size: 1.6 MB (1566644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1df9496327e6a1b9aec08023aba133fdaf8d118d3863f4268ea2afdbbe2ca4`  
		Last Modified: Wed, 10 Sep 2025 23:55:36 GMT  
		Size: 220.7 MB (220694545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:24a75bbe04cb8f717fb2bc08507550381b38c3915ae926da6e4428cab447dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b24020ae92d43aca15de543d94ceb9befc90495d3b15a17566fdb319d0655`

```dockerfile
```

-	Layers:
	-	`sha256:c84885172024c41151d9a0ba3aa1f1199a2524384f8ae30909e86edf36918def`  
		Last Modified: Wed, 10 Sep 2025 23:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:9ce249a31fea84c84e1ed4f146efd151e396a5ecb7e63132761b31ef49b806f8
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
$ docker pull dart@sha256:dbafa8fb6b7c32c1b7b5c99490a2fc8fa01b13802fa4c94eb80a3aa3080693f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3354ad9bfad9b68af66ae0e60ab850a48425f98dfe5f3fe61d9399602b2fd6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa017a2e4e070dc98cedc8136363140f1334ed1f59a8e561edf5d8a120c23c`  
		Last Modified: Wed, 10 Sep 2025 22:33:41 GMT  
		Size: 42.5 MB (42482435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772f519b79547b31df7388c527ed606ae7a98ddb485f95f74236e2ae535fec6`  
		Last Modified: Wed, 10 Sep 2025 22:33:53 GMT  
		Size: 1.9 MB (1873599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a56ce38740fdf24d591a6aec4b3e16d4c8aaa8ad6214bf1926f130b137d3d`  
		Last Modified: Wed, 10 Sep 2025 23:54:34 GMT  
		Size: 221.2 MB (221236204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e696f277562a36065824bb02956d7ffa857829ae162c1754658aeb6c8fa9f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47775006165bb8bce196426d9b0949cf8032131dca0d95712d34ddac44093a04`

```dockerfile
```

-	Layers:
	-	`sha256:45d14cb197a3c4a8d76e5ae2d59fa4c1b4d7164fdf1ed403680349bd366cb008`  
		Last Modified: Wed, 10 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:560c1175ec393e649a466b7cba87dcc5ad4efbb67448199564104d98f8b38bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294668027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f150a6dde5176f97876201bf912130bd852c4275c27e8f05d6c127ebc5403a7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151afe059b51b63d546871fc76cbbee94277727ccc3c2ff21341fcfa77c5fffa`  
		Last Modified: Wed, 10 Sep 2025 22:34:09 GMT  
		Size: 42.3 MB (42270175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c5056acb14aaa96e99a889410f2097e61c8486626b8537227ad1f25854d6c`  
		Last Modified: Wed, 10 Sep 2025 22:34:05 GMT  
		Size: 1.6 MB (1566644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1df9496327e6a1b9aec08023aba133fdaf8d118d3863f4268ea2afdbbe2ca4`  
		Last Modified: Wed, 10 Sep 2025 23:55:36 GMT  
		Size: 220.7 MB (220694545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:24a75bbe04cb8f717fb2bc08507550381b38c3915ae926da6e4428cab447dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b24020ae92d43aca15de543d94ceb9befc90495d3b15a17566fdb319d0655`

```dockerfile
```

-	Layers:
	-	`sha256:c84885172024c41151d9a0ba3aa1f1199a2524384f8ae30909e86edf36918def`  
		Last Modified: Wed, 10 Sep 2025 23:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-162.1.beta`

```console
$ docker pull dart@sha256:77cda94da2b0c5ac5396e7fd8bcd401ab5f1315308340f41c7d8873a9a6302bf
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

### `dart:3.10.0-162.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:ee5dcb135870b1a039b0132d5d1cbda179a89997e9a13b0e49e53ab7710431e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285674344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc9e4c9ab79478de68a3f80d5d72ccdc122fc746b377384f1fd3279cacf3851`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6048941f04ffda44cec4bccd989475c7c9cc95d7f4f2c1ddbd7d3047bd690c`  
		Last Modified: Tue, 30 Sep 2025 00:13:23 GMT  
		Size: 42.5 MB (42482645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4405596079890b306cff94599c654c78fe673b9caefbb013194dbafbc745fc5`  
		Last Modified: Tue, 30 Sep 2025 00:13:20 GMT  
		Size: 1.9 MB (1873614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689ad9fb8fc0849199be3d8997eacf3c486e55d332b38557f3577beded0f33c0`  
		Last Modified: Tue, 30 Sep 2025 20:55:15 GMT  
		Size: 211.5 MB (211540287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:cbcf95105d26a32c8258fcd36a5ecfc710a5c015b15c1614c3cbfae9862654f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f1da3c2640cb6cf9f3a2334ef9938f91247d05d7151b9531c8f47ffe689568`

```dockerfile
```

-	Layers:
	-	`sha256:80be05639a1d1fdb163237c48b4d415a1b17626c8328a09817de72259212e640`  
		Last Modified: Tue, 30 Sep 2025 20:53:20 GMT  
		Size: 19.0 KB (18965 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-162.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:c606212d22f4b2078cf2a2e440b8d924cef6ae10e3a0c7afe0ed17ca25522e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218745426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95188e190071230b9cb0b13dbfc08319b425985af33a3feaf59414b4a949e07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Sep 2025 11:42:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:42:45 GMT
WORKDIR /root
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbab51fd941bfbf6894d5ee7b1ae01abfb3076cfdb1e3f4371f13b39a54dddbe`  
		Last Modified: Mon, 08 Sep 2025 23:54:03 GMT  
		Size: 37.5 MB (37479176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206df88050e16bafd852282e462194d8df0920b42252c3bd860ca91615777cf5`  
		Last Modified: Mon, 08 Sep 2025 22:47:14 GMT  
		Size: 1.3 MB (1275115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800bb6b7413bbcd1380ad6590e1cf724afce7386c7bcd4c3d5db32a864c06ae7`  
		Last Modified: Tue, 09 Sep 2025 09:53:27 GMT  
		Size: 153.8 MB (153783256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:964c33d7f39661cd706ac0561d400307f98caf0747c9d5394a8ededaa0cd6b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a785ccf4475420b72e572cda89bbdc900326c006a6c0f57bf51276152f63ff8`

```dockerfile
```

-	Layers:
	-	`sha256:fb2e25bc7affa0449ceae956cb65e3851ed6e2a746a1fab0a8350dd619e2d5c1`  
		Last Modified: Mon, 08 Sep 2025 23:53:39 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-162.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cc6e1efe0ccaf82e263bef608e143aedf4c3c6b73e573d0250c04f67be1d895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284888716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8275d4bc438c73cdbf73aac3fb00b5a9a1825aaf89e358db879fb193fed2d9fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Sep 2025 11:42:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:42:45 GMT
WORKDIR /root
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f89d69a51684f84a0769ff272a135e820627c2f0d17635b87386b8556e7d03`  
		Last Modified: Mon, 08 Sep 2025 22:31:10 GMT  
		Size: 42.3 MB (42270008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123341c443b49228dd642399a401a37640a47e145ee3cf26c2402c466c8c6d5`  
		Last Modified: Mon, 08 Sep 2025 22:04:04 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8403eae81c4d4bd441ef47eb5297d3bc2f977e25307b11ab670d34e0c66d28c7`  
		Last Modified: Mon, 08 Sep 2025 22:31:08 GMT  
		Size: 210.9 MB (210915399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:28ca783d7f1d813039c444aed686b2eb0dbacb7806380bf87096fd81174450ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561fbee50dd68f2c0ece118c7559db733590306ffe98169e8df0f8d519087bf9`

```dockerfile
```

-	Layers:
	-	`sha256:b17277cd2be2f2c0dd838ac93c5c9486658a66d53c105f82bcfe37c72efaf468`  
		Last Modified: Mon, 08 Sep 2025 23:53:43 GMT  
		Size: 19.1 KB (19100 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-162.1.beta` - linux; riscv64

```console
$ docker pull dart@sha256:0824896c3635178640a866888571670fde47cb5f94701c9c664235b5e1ceca6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231819901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40450849884f7fcbe60b8c33d9b55b1c6c21cc100ef257f99869d9afbb3e0e3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7109b7e9bd6ab41707df02c7d0e4f792f522902a928d58b1c0061eb1fe108a43`  
		Last Modified: Thu, 11 Sep 2025 01:52:01 GMT  
		Size: 41.6 MB (41553255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c5150a8a2900e580473fbfa46ae631ad996da8e9dead53e064607a8d06e010`  
		Last Modified: Thu, 11 Sep 2025 01:51:57 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa771d564a3f34dc85c1a96c0bea55a3c71e4d4be67d3b2fd4fed468955e503`  
		Last Modified: Thu, 11 Sep 2025 02:53:44 GMT  
		Size: 160.4 MB (160428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:831cdc4dbee079bd9df32f9c777e715bf45cc481d282e8f1c6d0fdcde3607dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526b3ca3f37cdf3a9adb065bc62ab274d599c38d58186b73eaedd9f1273e0c4`

```dockerfile
```

-	Layers:
	-	`sha256:9695883e9f56e8332fcf7d82cc85c9d21765669145120d62e97b786a2389b4fb`  
		Last Modified: Thu, 11 Sep 2025 02:53:25 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-162.1.beta-sdk`

```console
$ docker pull dart@sha256:d7ec28a8aaaa63dca3b4e7927b163e2c83e97c7f129bc6b3087f4792cf26de70
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

### `dart:3.10.0-162.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:ee5dcb135870b1a039b0132d5d1cbda179a89997e9a13b0e49e53ab7710431e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285674344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc9e4c9ab79478de68a3f80d5d72ccdc122fc746b377384f1fd3279cacf3851`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6048941f04ffda44cec4bccd989475c7c9cc95d7f4f2c1ddbd7d3047bd690c`  
		Last Modified: Tue, 30 Sep 2025 00:13:23 GMT  
		Size: 42.5 MB (42482645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4405596079890b306cff94599c654c78fe673b9caefbb013194dbafbc745fc5`  
		Last Modified: Tue, 30 Sep 2025 00:13:20 GMT  
		Size: 1.9 MB (1873614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689ad9fb8fc0849199be3d8997eacf3c486e55d332b38557f3577beded0f33c0`  
		Last Modified: Tue, 30 Sep 2025 20:55:15 GMT  
		Size: 211.5 MB (211540287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cbcf95105d26a32c8258fcd36a5ecfc710a5c015b15c1614c3cbfae9862654f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f1da3c2640cb6cf9f3a2334ef9938f91247d05d7151b9531c8f47ffe689568`

```dockerfile
```

-	Layers:
	-	`sha256:80be05639a1d1fdb163237c48b4d415a1b17626c8328a09817de72259212e640`  
		Last Modified: Tue, 30 Sep 2025 20:53:20 GMT  
		Size: 19.0 KB (18965 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-162.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c606212d22f4b2078cf2a2e440b8d924cef6ae10e3a0c7afe0ed17ca25522e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218745426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95188e190071230b9cb0b13dbfc08319b425985af33a3feaf59414b4a949e07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Sep 2025 11:42:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:42:45 GMT
WORKDIR /root
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbab51fd941bfbf6894d5ee7b1ae01abfb3076cfdb1e3f4371f13b39a54dddbe`  
		Last Modified: Mon, 08 Sep 2025 23:54:03 GMT  
		Size: 37.5 MB (37479176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206df88050e16bafd852282e462194d8df0920b42252c3bd860ca91615777cf5`  
		Last Modified: Mon, 08 Sep 2025 22:47:14 GMT  
		Size: 1.3 MB (1275115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800bb6b7413bbcd1380ad6590e1cf724afce7386c7bcd4c3d5db32a864c06ae7`  
		Last Modified: Tue, 09 Sep 2025 09:53:27 GMT  
		Size: 153.8 MB (153783256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:964c33d7f39661cd706ac0561d400307f98caf0747c9d5394a8ededaa0cd6b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a785ccf4475420b72e572cda89bbdc900326c006a6c0f57bf51276152f63ff8`

```dockerfile
```

-	Layers:
	-	`sha256:fb2e25bc7affa0449ceae956cb65e3851ed6e2a746a1fab0a8350dd619e2d5c1`  
		Last Modified: Mon, 08 Sep 2025 23:53:39 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-162.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ca6ff3f563dd97d20a5cb187aa0e13ed434c633b187a519bd4f726d21c2d0fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284893012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e03f36a240aa049732473e5a5e67004bd277535834eb4a49413919b3a7e18b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a0025da7a49d97100d3f5038b6bb022624ad7c985d0c64a092ba12a27846af`  
		Last Modified: Tue, 30 Sep 2025 00:17:16 GMT  
		Size: 42.3 MB (42270040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94a2f736f4fa64461dcba879ceedadd508d4a16a740d2c64f37507c903f787`  
		Last Modified: Tue, 30 Sep 2025 00:17:04 GMT  
		Size: 1.6 MB (1566647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc11c7d6b6d336fa2200e0b2ce7d63c00ddbab38e8207ba8e6420cf3e874158`  
		Last Modified: Tue, 30 Sep 2025 11:53:46 GMT  
		Size: 210.9 MB (210915451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:988242dd7712cbdb760f47a0c5c68b8833d1ca815f58673ecce3397b7478a213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc19f751acef5f9681150218b0042e39f345f05a7ad8520d9ad14040f66a397`

```dockerfile
```

-	Layers:
	-	`sha256:e0bd59ac11bb3579ed3f6d8d5f66a720df54d30fc178a4030a674a6671258abd`  
		Last Modified: Tue, 30 Sep 2025 11:53:24 GMT  
		Size: 19.1 KB (19100 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-162.1.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:0824896c3635178640a866888571670fde47cb5f94701c9c664235b5e1ceca6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231819901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40450849884f7fcbe60b8c33d9b55b1c6c21cc100ef257f99869d9afbb3e0e3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7109b7e9bd6ab41707df02c7d0e4f792f522902a928d58b1c0061eb1fe108a43`  
		Last Modified: Thu, 11 Sep 2025 01:52:01 GMT  
		Size: 41.6 MB (41553255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c5150a8a2900e580473fbfa46ae631ad996da8e9dead53e064607a8d06e010`  
		Last Modified: Thu, 11 Sep 2025 01:51:57 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa771d564a3f34dc85c1a96c0bea55a3c71e4d4be67d3b2fd4fed468955e503`  
		Last Modified: Thu, 11 Sep 2025 02:53:44 GMT  
		Size: 160.4 MB (160428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-162.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:831cdc4dbee079bd9df32f9c777e715bf45cc481d282e8f1c6d0fdcde3607dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526b3ca3f37cdf3a9adb065bc62ab274d599c38d58186b73eaedd9f1273e0c4`

```dockerfile
```

-	Layers:
	-	`sha256:9695883e9f56e8332fcf7d82cc85c9d21765669145120d62e97b786a2389b4fb`  
		Last Modified: Thu, 11 Sep 2025 02:53:25 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9`

```console
$ docker pull dart@sha256:9ce249a31fea84c84e1ed4f146efd151e396a5ecb7e63132761b31ef49b806f8
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
$ docker pull dart@sha256:dbafa8fb6b7c32c1b7b5c99490a2fc8fa01b13802fa4c94eb80a3aa3080693f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3354ad9bfad9b68af66ae0e60ab850a48425f98dfe5f3fe61d9399602b2fd6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa017a2e4e070dc98cedc8136363140f1334ed1f59a8e561edf5d8a120c23c`  
		Last Modified: Wed, 10 Sep 2025 22:33:41 GMT  
		Size: 42.5 MB (42482435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772f519b79547b31df7388c527ed606ae7a98ddb485f95f74236e2ae535fec6`  
		Last Modified: Wed, 10 Sep 2025 22:33:53 GMT  
		Size: 1.9 MB (1873599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a56ce38740fdf24d591a6aec4b3e16d4c8aaa8ad6214bf1926f130b137d3d`  
		Last Modified: Wed, 10 Sep 2025 23:54:34 GMT  
		Size: 221.2 MB (221236204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:e696f277562a36065824bb02956d7ffa857829ae162c1754658aeb6c8fa9f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47775006165bb8bce196426d9b0949cf8032131dca0d95712d34ddac44093a04`

```dockerfile
```

-	Layers:
	-	`sha256:45d14cb197a3c4a8d76e5ae2d59fa4c1b4d7164fdf1ed403680349bd366cb008`  
		Last Modified: Wed, 10 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:560c1175ec393e649a466b7cba87dcc5ad4efbb67448199564104d98f8b38bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294668027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f150a6dde5176f97876201bf912130bd852c4275c27e8f05d6c127ebc5403a7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151afe059b51b63d546871fc76cbbee94277727ccc3c2ff21341fcfa77c5fffa`  
		Last Modified: Wed, 10 Sep 2025 22:34:09 GMT  
		Size: 42.3 MB (42270175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c5056acb14aaa96e99a889410f2097e61c8486626b8537227ad1f25854d6c`  
		Last Modified: Wed, 10 Sep 2025 22:34:05 GMT  
		Size: 1.6 MB (1566644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1df9496327e6a1b9aec08023aba133fdaf8d118d3863f4268ea2afdbbe2ca4`  
		Last Modified: Wed, 10 Sep 2025 23:55:36 GMT  
		Size: 220.7 MB (220694545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:24a75bbe04cb8f717fb2bc08507550381b38c3915ae926da6e4428cab447dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b24020ae92d43aca15de543d94ceb9befc90495d3b15a17566fdb319d0655`

```dockerfile
```

-	Layers:
	-	`sha256:c84885172024c41151d9a0ba3aa1f1199a2524384f8ae30909e86edf36918def`  
		Last Modified: Wed, 10 Sep 2025 23:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9-sdk`

```console
$ docker pull dart@sha256:eb614f08b3a9b7e980103c4ed2f12817ca37dfca0109bf7078ca319d51dff55a
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
$ docker pull dart@sha256:5e9fe5d86c2460406b73cabc62b3b22815d009028a637178847c3e4af228f731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295370540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbec76453be73d5cff08b3dcbd1951f996f9cc41d805b5f2fc8d347cd996dc31`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef14805de385cf1670328d7af0c82f7a81cf5a16f5e39e1630f455c5edd6836`  
		Last Modified: Tue, 30 Sep 2025 00:13:11 GMT  
		Size: 42.5 MB (42482552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63920ce1f2e5a569f909ca847b169b48f2a83af71ceca5d933ffb822b0e6c9f7`  
		Last Modified: Tue, 30 Sep 2025 00:13:09 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554b1fd920300365d20b816904e2ac3aa92fb3cd1d123f21c263d9bea1aade82`  
		Last Modified: Tue, 30 Sep 2025 20:56:07 GMT  
		Size: 221.2 MB (221236575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:51ab610b7fd0da9e00e19091634d81ec0a0a21dc5399cebf48b10e00c1378a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b513d608ae957eab6a77be4ad7e2c4f7ed0c343b0780c80867472ea10083fb76`

```dockerfile
```

-	Layers:
	-	`sha256:dd4f180a5a059010d0870e305069dcfe28df812fad7278641cdbb45c332e6bb6`  
		Last Modified: Tue, 30 Sep 2025 20:53:29 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:560c1175ec393e649a466b7cba87dcc5ad4efbb67448199564104d98f8b38bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294668027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f150a6dde5176f97876201bf912130bd852c4275c27e8f05d6c127ebc5403a7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151afe059b51b63d546871fc76cbbee94277727ccc3c2ff21341fcfa77c5fffa`  
		Last Modified: Wed, 10 Sep 2025 22:34:09 GMT  
		Size: 42.3 MB (42270175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c5056acb14aaa96e99a889410f2097e61c8486626b8537227ad1f25854d6c`  
		Last Modified: Wed, 10 Sep 2025 22:34:05 GMT  
		Size: 1.6 MB (1566644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1df9496327e6a1b9aec08023aba133fdaf8d118d3863f4268ea2afdbbe2ca4`  
		Last Modified: Wed, 10 Sep 2025 23:55:36 GMT  
		Size: 220.7 MB (220694545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:24a75bbe04cb8f717fb2bc08507550381b38c3915ae926da6e4428cab447dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b24020ae92d43aca15de543d94ceb9befc90495d3b15a17566fdb319d0655`

```dockerfile
```

-	Layers:
	-	`sha256:c84885172024c41151d9a0ba3aa1f1199a2524384f8ae30909e86edf36918def`  
		Last Modified: Wed, 10 Sep 2025 23:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.3`

```console
$ docker pull dart@sha256:9ce249a31fea84c84e1ed4f146efd151e396a5ecb7e63132761b31ef49b806f8
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

### `dart:3.9.3` - linux; amd64

```console
$ docker pull dart@sha256:dbafa8fb6b7c32c1b7b5c99490a2fc8fa01b13802fa4c94eb80a3aa3080693f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3354ad9bfad9b68af66ae0e60ab850a48425f98dfe5f3fe61d9399602b2fd6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa017a2e4e070dc98cedc8136363140f1334ed1f59a8e561edf5d8a120c23c`  
		Last Modified: Wed, 10 Sep 2025 22:33:41 GMT  
		Size: 42.5 MB (42482435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772f519b79547b31df7388c527ed606ae7a98ddb485f95f74236e2ae535fec6`  
		Last Modified: Wed, 10 Sep 2025 22:33:53 GMT  
		Size: 1.9 MB (1873599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a56ce38740fdf24d591a6aec4b3e16d4c8aaa8ad6214bf1926f130b137d3d`  
		Last Modified: Wed, 10 Sep 2025 23:54:34 GMT  
		Size: 221.2 MB (221236204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.3` - unknown; unknown

```console
$ docker pull dart@sha256:e696f277562a36065824bb02956d7ffa857829ae162c1754658aeb6c8fa9f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47775006165bb8bce196426d9b0949cf8032131dca0d95712d34ddac44093a04`

```dockerfile
```

-	Layers:
	-	`sha256:45d14cb197a3c4a8d76e5ae2d59fa4c1b4d7164fdf1ed403680349bd366cb008`  
		Last Modified: Wed, 10 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.3` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.3` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:560c1175ec393e649a466b7cba87dcc5ad4efbb67448199564104d98f8b38bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294668027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f150a6dde5176f97876201bf912130bd852c4275c27e8f05d6c127ebc5403a7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151afe059b51b63d546871fc76cbbee94277727ccc3c2ff21341fcfa77c5fffa`  
		Last Modified: Wed, 10 Sep 2025 22:34:09 GMT  
		Size: 42.3 MB (42270175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c5056acb14aaa96e99a889410f2097e61c8486626b8537227ad1f25854d6c`  
		Last Modified: Wed, 10 Sep 2025 22:34:05 GMT  
		Size: 1.6 MB (1566644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1df9496327e6a1b9aec08023aba133fdaf8d118d3863f4268ea2afdbbe2ca4`  
		Last Modified: Wed, 10 Sep 2025 23:55:36 GMT  
		Size: 220.7 MB (220694545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.3` - unknown; unknown

```console
$ docker pull dart@sha256:24a75bbe04cb8f717fb2bc08507550381b38c3915ae926da6e4428cab447dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b24020ae92d43aca15de543d94ceb9befc90495d3b15a17566fdb319d0655`

```dockerfile
```

-	Layers:
	-	`sha256:c84885172024c41151d9a0ba3aa1f1199a2524384f8ae30909e86edf36918def`  
		Last Modified: Wed, 10 Sep 2025 23:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.3` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.3` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.3-sdk`

```console
$ docker pull dart@sha256:62c81aa18e73479e58ef3ba2c2ec3cd1c563d00475903f83f6f0e49588b150a7
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

### `dart:3.9.3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5e9fe5d86c2460406b73cabc62b3b22815d009028a637178847c3e4af228f731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295370540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbec76453be73d5cff08b3dcbd1951f996f9cc41d805b5f2fc8d347cd996dc31`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef14805de385cf1670328d7af0c82f7a81cf5a16f5e39e1630f455c5edd6836`  
		Last Modified: Tue, 30 Sep 2025 00:13:11 GMT  
		Size: 42.5 MB (42482552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63920ce1f2e5a569f909ca847b169b48f2a83af71ceca5d933ffb822b0e6c9f7`  
		Last Modified: Tue, 30 Sep 2025 00:13:09 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554b1fd920300365d20b816904e2ac3aa92fb3cd1d123f21c263d9bea1aade82`  
		Last Modified: Tue, 30 Sep 2025 20:56:07 GMT  
		Size: 221.2 MB (221236575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:51ab610b7fd0da9e00e19091634d81ec0a0a21dc5399cebf48b10e00c1378a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b513d608ae957eab6a77be4ad7e2c4f7ed0c343b0780c80867472ea10083fb76`

```dockerfile
```

-	Layers:
	-	`sha256:dd4f180a5a059010d0870e305069dcfe28df812fad7278641cdbb45c332e6bb6`  
		Last Modified: Tue, 30 Sep 2025 20:53:29 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:2837abf374f9c435d37e5801e4cab553116a05ca547da60b331f018713f2530a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294672278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ede4d008fccddfd3e67cf96ca2dcb78c9246e83e92243c9a85ac757688a248`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9bd4b5d062da9a77e9a4bdb4b34d48112b1a4d4e8e4ca19df86104b8f9276`  
		Last Modified: Tue, 30 Sep 2025 11:53:42 GMT  
		Size: 42.3 MB (42269987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a5f91f33becc4d2e4609a5ec725fe8488059ec0e0bf372827338154289e0a3`  
		Last Modified: Tue, 30 Sep 2025 01:07:03 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0dae158065c918d2a27f5097a3931eb88fc3c389ab213df08a722bba6cff3a`  
		Last Modified: Tue, 30 Sep 2025 11:53:48 GMT  
		Size: 220.7 MB (220694772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2be935ad0733fa32fe631f7e6e52751f4f58ada7ec388cebfbb8a1d1f65b1e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441127b6f3a19845f2e9ed71bd51d68ccfb1f2fecef5026bf7d0071ace0000aa`

```dockerfile
```

-	Layers:
	-	`sha256:c637057541681d6e136521ac0b6b99eab7137c5d875653cc17ab2bd58ec42b03`  
		Last Modified: Tue, 30 Sep 2025 11:53:30 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:77cda94da2b0c5ac5396e7fd8bcd401ab5f1315308340f41c7d8873a9a6302bf
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
$ docker pull dart@sha256:ee5dcb135870b1a039b0132d5d1cbda179a89997e9a13b0e49e53ab7710431e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285674344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc9e4c9ab79478de68a3f80d5d72ccdc122fc746b377384f1fd3279cacf3851`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6048941f04ffda44cec4bccd989475c7c9cc95d7f4f2c1ddbd7d3047bd690c`  
		Last Modified: Tue, 30 Sep 2025 00:13:23 GMT  
		Size: 42.5 MB (42482645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4405596079890b306cff94599c654c78fe673b9caefbb013194dbafbc745fc5`  
		Last Modified: Tue, 30 Sep 2025 00:13:20 GMT  
		Size: 1.9 MB (1873614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689ad9fb8fc0849199be3d8997eacf3c486e55d332b38557f3577beded0f33c0`  
		Last Modified: Tue, 30 Sep 2025 20:55:15 GMT  
		Size: 211.5 MB (211540287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:cbcf95105d26a32c8258fcd36a5ecfc710a5c015b15c1614c3cbfae9862654f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f1da3c2640cb6cf9f3a2334ef9938f91247d05d7151b9531c8f47ffe689568`

```dockerfile
```

-	Layers:
	-	`sha256:80be05639a1d1fdb163237c48b4d415a1b17626c8328a09817de72259212e640`  
		Last Modified: Tue, 30 Sep 2025 20:53:20 GMT  
		Size: 19.0 KB (18965 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:c606212d22f4b2078cf2a2e440b8d924cef6ae10e3a0c7afe0ed17ca25522e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218745426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95188e190071230b9cb0b13dbfc08319b425985af33a3feaf59414b4a949e07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Sep 2025 11:42:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:42:45 GMT
WORKDIR /root
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbab51fd941bfbf6894d5ee7b1ae01abfb3076cfdb1e3f4371f13b39a54dddbe`  
		Last Modified: Mon, 08 Sep 2025 23:54:03 GMT  
		Size: 37.5 MB (37479176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206df88050e16bafd852282e462194d8df0920b42252c3bd860ca91615777cf5`  
		Last Modified: Mon, 08 Sep 2025 22:47:14 GMT  
		Size: 1.3 MB (1275115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800bb6b7413bbcd1380ad6590e1cf724afce7386c7bcd4c3d5db32a864c06ae7`  
		Last Modified: Tue, 09 Sep 2025 09:53:27 GMT  
		Size: 153.8 MB (153783256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:964c33d7f39661cd706ac0561d400307f98caf0747c9d5394a8ededaa0cd6b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a785ccf4475420b72e572cda89bbdc900326c006a6c0f57bf51276152f63ff8`

```dockerfile
```

-	Layers:
	-	`sha256:fb2e25bc7affa0449ceae956cb65e3851ed6e2a746a1fab0a8350dd619e2d5c1`  
		Last Modified: Mon, 08 Sep 2025 23:53:39 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cc6e1efe0ccaf82e263bef608e143aedf4c3c6b73e573d0250c04f67be1d895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284888716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8275d4bc438c73cdbf73aac3fb00b5a9a1825aaf89e358db879fb193fed2d9fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Sep 2025 11:42:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:42:45 GMT
WORKDIR /root
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f89d69a51684f84a0769ff272a135e820627c2f0d17635b87386b8556e7d03`  
		Last Modified: Mon, 08 Sep 2025 22:31:10 GMT  
		Size: 42.3 MB (42270008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123341c443b49228dd642399a401a37640a47e145ee3cf26c2402c466c8c6d5`  
		Last Modified: Mon, 08 Sep 2025 22:04:04 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8403eae81c4d4bd441ef47eb5297d3bc2f977e25307b11ab670d34e0c66d28c7`  
		Last Modified: Mon, 08 Sep 2025 22:31:08 GMT  
		Size: 210.9 MB (210915399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:28ca783d7f1d813039c444aed686b2eb0dbacb7806380bf87096fd81174450ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561fbee50dd68f2c0ece118c7559db733590306ffe98169e8df0f8d519087bf9`

```dockerfile
```

-	Layers:
	-	`sha256:b17277cd2be2f2c0dd838ac93c5c9486658a66d53c105f82bcfe37c72efaf468`  
		Last Modified: Mon, 08 Sep 2025 23:53:43 GMT  
		Size: 19.1 KB (19100 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:0824896c3635178640a866888571670fde47cb5f94701c9c664235b5e1ceca6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231819901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40450849884f7fcbe60b8c33d9b55b1c6c21cc100ef257f99869d9afbb3e0e3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7109b7e9bd6ab41707df02c7d0e4f792f522902a928d58b1c0061eb1fe108a43`  
		Last Modified: Thu, 11 Sep 2025 01:52:01 GMT  
		Size: 41.6 MB (41553255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c5150a8a2900e580473fbfa46ae631ad996da8e9dead53e064607a8d06e010`  
		Last Modified: Thu, 11 Sep 2025 01:51:57 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa771d564a3f34dc85c1a96c0bea55a3c71e4d4be67d3b2fd4fed468955e503`  
		Last Modified: Thu, 11 Sep 2025 02:53:44 GMT  
		Size: 160.4 MB (160428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:831cdc4dbee079bd9df32f9c777e715bf45cc481d282e8f1c6d0fdcde3607dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526b3ca3f37cdf3a9adb065bc62ab274d599c38d58186b73eaedd9f1273e0c4`

```dockerfile
```

-	Layers:
	-	`sha256:9695883e9f56e8332fcf7d82cc85c9d21765669145120d62e97b786a2389b4fb`  
		Last Modified: Thu, 11 Sep 2025 02:53:25 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:77cda94da2b0c5ac5396e7fd8bcd401ab5f1315308340f41c7d8873a9a6302bf
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
$ docker pull dart@sha256:ee5dcb135870b1a039b0132d5d1cbda179a89997e9a13b0e49e53ab7710431e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285674344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc9e4c9ab79478de68a3f80d5d72ccdc122fc746b377384f1fd3279cacf3851`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6048941f04ffda44cec4bccd989475c7c9cc95d7f4f2c1ddbd7d3047bd690c`  
		Last Modified: Tue, 30 Sep 2025 00:13:23 GMT  
		Size: 42.5 MB (42482645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4405596079890b306cff94599c654c78fe673b9caefbb013194dbafbc745fc5`  
		Last Modified: Tue, 30 Sep 2025 00:13:20 GMT  
		Size: 1.9 MB (1873614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689ad9fb8fc0849199be3d8997eacf3c486e55d332b38557f3577beded0f33c0`  
		Last Modified: Tue, 30 Sep 2025 20:55:15 GMT  
		Size: 211.5 MB (211540287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cbcf95105d26a32c8258fcd36a5ecfc710a5c015b15c1614c3cbfae9862654f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f1da3c2640cb6cf9f3a2334ef9938f91247d05d7151b9531c8f47ffe689568`

```dockerfile
```

-	Layers:
	-	`sha256:80be05639a1d1fdb163237c48b4d415a1b17626c8328a09817de72259212e640`  
		Last Modified: Tue, 30 Sep 2025 20:53:20 GMT  
		Size: 19.0 KB (18965 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c606212d22f4b2078cf2a2e440b8d924cef6ae10e3a0c7afe0ed17ca25522e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218745426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95188e190071230b9cb0b13dbfc08319b425985af33a3feaf59414b4a949e07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Sep 2025 11:42:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:42:45 GMT
WORKDIR /root
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbab51fd941bfbf6894d5ee7b1ae01abfb3076cfdb1e3f4371f13b39a54dddbe`  
		Last Modified: Mon, 08 Sep 2025 23:54:03 GMT  
		Size: 37.5 MB (37479176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206df88050e16bafd852282e462194d8df0920b42252c3bd860ca91615777cf5`  
		Last Modified: Mon, 08 Sep 2025 22:47:14 GMT  
		Size: 1.3 MB (1275115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800bb6b7413bbcd1380ad6590e1cf724afce7386c7bcd4c3d5db32a864c06ae7`  
		Last Modified: Tue, 09 Sep 2025 09:53:27 GMT  
		Size: 153.8 MB (153783256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:964c33d7f39661cd706ac0561d400307f98caf0747c9d5394a8ededaa0cd6b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a785ccf4475420b72e572cda89bbdc900326c006a6c0f57bf51276152f63ff8`

```dockerfile
```

-	Layers:
	-	`sha256:fb2e25bc7affa0449ceae956cb65e3851ed6e2a746a1fab0a8350dd619e2d5c1`  
		Last Modified: Mon, 08 Sep 2025 23:53:39 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cc6e1efe0ccaf82e263bef608e143aedf4c3c6b73e573d0250c04f67be1d895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284888716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8275d4bc438c73cdbf73aac3fb00b5a9a1825aaf89e358db879fb193fed2d9fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Sep 2025 11:42:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:42:45 GMT
WORKDIR /root
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f89d69a51684f84a0769ff272a135e820627c2f0d17635b87386b8556e7d03`  
		Last Modified: Mon, 08 Sep 2025 22:31:10 GMT  
		Size: 42.3 MB (42270008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123341c443b49228dd642399a401a37640a47e145ee3cf26c2402c466c8c6d5`  
		Last Modified: Mon, 08 Sep 2025 22:04:04 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8403eae81c4d4bd441ef47eb5297d3bc2f977e25307b11ab670d34e0c66d28c7`  
		Last Modified: Mon, 08 Sep 2025 22:31:08 GMT  
		Size: 210.9 MB (210915399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:28ca783d7f1d813039c444aed686b2eb0dbacb7806380bf87096fd81174450ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561fbee50dd68f2c0ece118c7559db733590306ffe98169e8df0f8d519087bf9`

```dockerfile
```

-	Layers:
	-	`sha256:b17277cd2be2f2c0dd838ac93c5c9486658a66d53c105f82bcfe37c72efaf468`  
		Last Modified: Mon, 08 Sep 2025 23:53:43 GMT  
		Size: 19.1 KB (19100 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:0824896c3635178640a866888571670fde47cb5f94701c9c664235b5e1ceca6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231819901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40450849884f7fcbe60b8c33d9b55b1c6c21cc100ef257f99869d9afbb3e0e3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7109b7e9bd6ab41707df02c7d0e4f792f522902a928d58b1c0061eb1fe108a43`  
		Last Modified: Thu, 11 Sep 2025 01:52:01 GMT  
		Size: 41.6 MB (41553255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c5150a8a2900e580473fbfa46ae631ad996da8e9dead53e064607a8d06e010`  
		Last Modified: Thu, 11 Sep 2025 01:51:57 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa771d564a3f34dc85c1a96c0bea55a3c71e4d4be67d3b2fd4fed468955e503`  
		Last Modified: Thu, 11 Sep 2025 02:53:44 GMT  
		Size: 160.4 MB (160428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:831cdc4dbee079bd9df32f9c777e715bf45cc481d282e8f1c6d0fdcde3607dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526b3ca3f37cdf3a9adb065bc62ab274d599c38d58186b73eaedd9f1273e0c4`

```dockerfile
```

-	Layers:
	-	`sha256:9695883e9f56e8332fcf7d82cc85c9d21765669145120d62e97b786a2389b4fb`  
		Last Modified: Thu, 11 Sep 2025 02:53:25 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:9ce249a31fea84c84e1ed4f146efd151e396a5ecb7e63132761b31ef49b806f8
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
$ docker pull dart@sha256:dbafa8fb6b7c32c1b7b5c99490a2fc8fa01b13802fa4c94eb80a3aa3080693f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3354ad9bfad9b68af66ae0e60ab850a48425f98dfe5f3fe61d9399602b2fd6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa017a2e4e070dc98cedc8136363140f1334ed1f59a8e561edf5d8a120c23c`  
		Last Modified: Wed, 10 Sep 2025 22:33:41 GMT  
		Size: 42.5 MB (42482435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772f519b79547b31df7388c527ed606ae7a98ddb485f95f74236e2ae535fec6`  
		Last Modified: Wed, 10 Sep 2025 22:33:53 GMT  
		Size: 1.9 MB (1873599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a56ce38740fdf24d591a6aec4b3e16d4c8aaa8ad6214bf1926f130b137d3d`  
		Last Modified: Wed, 10 Sep 2025 23:54:34 GMT  
		Size: 221.2 MB (221236204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:e696f277562a36065824bb02956d7ffa857829ae162c1754658aeb6c8fa9f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47775006165bb8bce196426d9b0949cf8032131dca0d95712d34ddac44093a04`

```dockerfile
```

-	Layers:
	-	`sha256:45d14cb197a3c4a8d76e5ae2d59fa4c1b4d7164fdf1ed403680349bd366cb008`  
		Last Modified: Wed, 10 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:560c1175ec393e649a466b7cba87dcc5ad4efbb67448199564104d98f8b38bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294668027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f150a6dde5176f97876201bf912130bd852c4275c27e8f05d6c127ebc5403a7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151afe059b51b63d546871fc76cbbee94277727ccc3c2ff21341fcfa77c5fffa`  
		Last Modified: Wed, 10 Sep 2025 22:34:09 GMT  
		Size: 42.3 MB (42270175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c5056acb14aaa96e99a889410f2097e61c8486626b8537227ad1f25854d6c`  
		Last Modified: Wed, 10 Sep 2025 22:34:05 GMT  
		Size: 1.6 MB (1566644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1df9496327e6a1b9aec08023aba133fdaf8d118d3863f4268ea2afdbbe2ca4`  
		Last Modified: Wed, 10 Sep 2025 23:55:36 GMT  
		Size: 220.7 MB (220694545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:24a75bbe04cb8f717fb2bc08507550381b38c3915ae926da6e4428cab447dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b24020ae92d43aca15de543d94ceb9befc90495d3b15a17566fdb319d0655`

```dockerfile
```

-	Layers:
	-	`sha256:c84885172024c41151d9a0ba3aa1f1199a2524384f8ae30909e86edf36918def`  
		Last Modified: Wed, 10 Sep 2025 23:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:9ce249a31fea84c84e1ed4f146efd151e396a5ecb7e63132761b31ef49b806f8
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
$ docker pull dart@sha256:dbafa8fb6b7c32c1b7b5c99490a2fc8fa01b13802fa4c94eb80a3aa3080693f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3354ad9bfad9b68af66ae0e60ab850a48425f98dfe5f3fe61d9399602b2fd6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa017a2e4e070dc98cedc8136363140f1334ed1f59a8e561edf5d8a120c23c`  
		Last Modified: Wed, 10 Sep 2025 22:33:41 GMT  
		Size: 42.5 MB (42482435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772f519b79547b31df7388c527ed606ae7a98ddb485f95f74236e2ae535fec6`  
		Last Modified: Wed, 10 Sep 2025 22:33:53 GMT  
		Size: 1.9 MB (1873599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a56ce38740fdf24d591a6aec4b3e16d4c8aaa8ad6214bf1926f130b137d3d`  
		Last Modified: Wed, 10 Sep 2025 23:54:34 GMT  
		Size: 221.2 MB (221236204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e696f277562a36065824bb02956d7ffa857829ae162c1754658aeb6c8fa9f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47775006165bb8bce196426d9b0949cf8032131dca0d95712d34ddac44093a04`

```dockerfile
```

-	Layers:
	-	`sha256:45d14cb197a3c4a8d76e5ae2d59fa4c1b4d7164fdf1ed403680349bd366cb008`  
		Last Modified: Wed, 10 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:560c1175ec393e649a466b7cba87dcc5ad4efbb67448199564104d98f8b38bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294668027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f150a6dde5176f97876201bf912130bd852c4275c27e8f05d6c127ebc5403a7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151afe059b51b63d546871fc76cbbee94277727ccc3c2ff21341fcfa77c5fffa`  
		Last Modified: Wed, 10 Sep 2025 22:34:09 GMT  
		Size: 42.3 MB (42270175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c5056acb14aaa96e99a889410f2097e61c8486626b8537227ad1f25854d6c`  
		Last Modified: Wed, 10 Sep 2025 22:34:05 GMT  
		Size: 1.6 MB (1566644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1df9496327e6a1b9aec08023aba133fdaf8d118d3863f4268ea2afdbbe2ca4`  
		Last Modified: Wed, 10 Sep 2025 23:55:36 GMT  
		Size: 220.7 MB (220694545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:24a75bbe04cb8f717fb2bc08507550381b38c3915ae926da6e4428cab447dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b24020ae92d43aca15de543d94ceb9befc90495d3b15a17566fdb319d0655`

```dockerfile
```

-	Layers:
	-	`sha256:c84885172024c41151d9a0ba3aa1f1199a2524384f8ae30909e86edf36918def`  
		Last Modified: Wed, 10 Sep 2025 23:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:faa9ed5be7d51ec227cf11d32b4272fbf374506dffc71fbce53032d6e85d96d0
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
$ docker pull dart@sha256:dbafa8fb6b7c32c1b7b5c99490a2fc8fa01b13802fa4c94eb80a3aa3080693f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3354ad9bfad9b68af66ae0e60ab850a48425f98dfe5f3fe61d9399602b2fd6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa017a2e4e070dc98cedc8136363140f1334ed1f59a8e561edf5d8a120c23c`  
		Last Modified: Wed, 10 Sep 2025 22:33:41 GMT  
		Size: 42.5 MB (42482435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772f519b79547b31df7388c527ed606ae7a98ddb485f95f74236e2ae535fec6`  
		Last Modified: Wed, 10 Sep 2025 22:33:53 GMT  
		Size: 1.9 MB (1873599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a56ce38740fdf24d591a6aec4b3e16d4c8aaa8ad6214bf1926f130b137d3d`  
		Last Modified: Wed, 10 Sep 2025 23:54:34 GMT  
		Size: 221.2 MB (221236204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e696f277562a36065824bb02956d7ffa857829ae162c1754658aeb6c8fa9f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47775006165bb8bce196426d9b0949cf8032131dca0d95712d34ddac44093a04`

```dockerfile
```

-	Layers:
	-	`sha256:45d14cb197a3c4a8d76e5ae2d59fa4c1b4d7164fdf1ed403680349bd366cb008`  
		Last Modified: Wed, 10 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:2837abf374f9c435d37e5801e4cab553116a05ca547da60b331f018713f2530a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294672278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ede4d008fccddfd3e67cf96ca2dcb78c9246e83e92243c9a85ac757688a248`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9bd4b5d062da9a77e9a4bdb4b34d48112b1a4d4e8e4ca19df86104b8f9276`  
		Last Modified: Tue, 30 Sep 2025 11:53:42 GMT  
		Size: 42.3 MB (42269987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a5f91f33becc4d2e4609a5ec725fe8488059ec0e0bf372827338154289e0a3`  
		Last Modified: Tue, 30 Sep 2025 01:07:03 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0dae158065c918d2a27f5097a3931eb88fc3c389ab213df08a722bba6cff3a`  
		Last Modified: Tue, 30 Sep 2025 11:53:48 GMT  
		Size: 220.7 MB (220694772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:2be935ad0733fa32fe631f7e6e52751f4f58ada7ec388cebfbb8a1d1f65b1e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441127b6f3a19845f2e9ed71bd51d68ccfb1f2fecef5026bf7d0071ace0000aa`

```dockerfile
```

-	Layers:
	-	`sha256:c637057541681d6e136521ac0b6b99eab7137c5d875653cc17ab2bd58ec42b03`  
		Last Modified: Tue, 30 Sep 2025 11:53:30 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:9ce249a31fea84c84e1ed4f146efd151e396a5ecb7e63132761b31ef49b806f8
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
$ docker pull dart@sha256:dbafa8fb6b7c32c1b7b5c99490a2fc8fa01b13802fa4c94eb80a3aa3080693f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295365765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3354ad9bfad9b68af66ae0e60ab850a48425f98dfe5f3fe61d9399602b2fd6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fa017a2e4e070dc98cedc8136363140f1334ed1f59a8e561edf5d8a120c23c`  
		Last Modified: Wed, 10 Sep 2025 22:33:41 GMT  
		Size: 42.5 MB (42482435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b772f519b79547b31df7388c527ed606ae7a98ddb485f95f74236e2ae535fec6`  
		Last Modified: Wed, 10 Sep 2025 22:33:53 GMT  
		Size: 1.9 MB (1873599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a56ce38740fdf24d591a6aec4b3e16d4c8aaa8ad6214bf1926f130b137d3d`  
		Last Modified: Wed, 10 Sep 2025 23:54:34 GMT  
		Size: 221.2 MB (221236204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e696f277562a36065824bb02956d7ffa857829ae162c1754658aeb6c8fa9f79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47775006165bb8bce196426d9b0949cf8032131dca0d95712d34ddac44093a04`

```dockerfile
```

-	Layers:
	-	`sha256:45d14cb197a3c4a8d76e5ae2d59fa4c1b4d7164fdf1ed403680349bd366cb008`  
		Last Modified: Wed, 10 Sep 2025 23:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f79815fd151d12ccf2ae8d142557f026e887492eb2cc5fa05fcf0740212c8eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107757aaae122304c7c31995552023fef874c361b2a0ab41c8555f743d71128e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ac2ec22d65244066414f5a55c06da7e1f8c9b04290e422a02bb6fa9f3ed4d9`  
		Last Modified: Thu, 11 Sep 2025 04:43:43 GMT  
		Size: 37.5 MB (37479037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc0b23ff6bbc834aac4922de4ce6a46b54debed2220f6eb1cccc38382dc9f0a`  
		Last Modified: Thu, 11 Sep 2025 04:43:40 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e8c9af79bdfa704ea02aea13a8993475b600b042f416c326497feab08896a2`  
		Last Modified: Thu, 11 Sep 2025 05:53:53 GMT  
		Size: 155.8 MB (155804470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a36a26ba5ece94a63a23a372ea60d18f8eccbeffdcdb4fb5b237eb9ec7b8bba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b75c8875ba3e536d7fd2af9d11d54f18076857a2c5e15d843ef44bdda348f`

```dockerfile
```

-	Layers:
	-	`sha256:bef7f64f211942a87c0cbbf5168947b640c9a7e1f2ff7eb192a59c23f45c50bb`  
		Last Modified: Thu, 11 Sep 2025 05:53:19 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:560c1175ec393e649a466b7cba87dcc5ad4efbb67448199564104d98f8b38bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294668027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f150a6dde5176f97876201bf912130bd852c4275c27e8f05d6c127ebc5403a7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151afe059b51b63d546871fc76cbbee94277727ccc3c2ff21341fcfa77c5fffa`  
		Last Modified: Wed, 10 Sep 2025 22:34:09 GMT  
		Size: 42.3 MB (42270175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c5056acb14aaa96e99a889410f2097e61c8486626b8537227ad1f25854d6c`  
		Last Modified: Wed, 10 Sep 2025 22:34:05 GMT  
		Size: 1.6 MB (1566644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1df9496327e6a1b9aec08023aba133fdaf8d118d3863f4268ea2afdbbe2ca4`  
		Last Modified: Wed, 10 Sep 2025 23:55:36 GMT  
		Size: 220.7 MB (220694545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:24a75bbe04cb8f717fb2bc08507550381b38c3915ae926da6e4428cab447dfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b24020ae92d43aca15de543d94ceb9befc90495d3b15a17566fdb319d0655`

```dockerfile
```

-	Layers:
	-	`sha256:c84885172024c41151d9a0ba3aa1f1199a2524384f8ae30909e86edf36918def`  
		Last Modified: Wed, 10 Sep 2025 23:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:487a4f03ec06d3e92ae6147293a518ac8258356845650b12d91f2cd56005d8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232354694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94270a625817439c222b7d328a888f8495bd875ac3995e2f2e7e7e223d09743`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d19311deb35104a41a40db7ae36c496b1503745a5caed5a415d322b4c273f1db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=19eb5aefdeb2322fb4cd6f6353f5acfa8a6e737307bcf83e066c648762996911;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8847c4847bf77aed958c062bccf8d595795ed484876712680baf4c6c8317c356;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=cd0fbcdcfbaf5455b05355a7ecac8811651b65bb8901e3520d85693070af2e59;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487bade7c1f2c6d318deefc56dcd2f3b57c9e9b8edcb9c7acff0685b6dd45f47`  
		Last Modified: Fri, 12 Sep 2025 02:30:59 GMT  
		Size: 41.6 MB (41553204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab7da32ffd5eb9e4d0f4b80406da83fc8883e5c7e25ed26da2c19101b8f4e4d`  
		Last Modified: Fri, 12 Sep 2025 02:30:51 GMT  
		Size: 1.6 MB (1567061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefacbbd56550208f8ee9a29268582b03e59be47f3e902e45f72d6784c9e5af6`  
		Last Modified: Fri, 12 Sep 2025 03:10:47 GMT  
		Size: 161.0 MB (160963025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:144ed8803a2ed4e7691a1eac4a9cd4a369b567ed89b2d0482b19ffe82f3b71a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1741de95e4efdd949c439e3333bacccc5293256558fadcb9b32e9981df429831`

```dockerfile
```

-	Layers:
	-	`sha256:7191e36c55b23642fdbf49bcb46792cb0aafb84fb02b76e3b05e0b096603f046`  
		Last Modified: Fri, 12 Sep 2025 05:53:23 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json
