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
