## `dart:sdk`

```console
$ docker pull dart@sha256:7240a3b57c8c755912674fcc95408ad00f4b1541397a7d54fa24a55e9deade7b
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
$ docker pull dart@sha256:c5d34d6d6c84228136366ac7df4d4aa3ba5fa0963eea69c871dcdf48ef3df6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae58756ec846b14c4417adc880d0c2620e2942e9ae7ffcfe42b381f3ee93f9d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:08:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 08 Dec 2025 23:08:56 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 08 Dec 2025 23:08:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:08:56 GMT
WORKDIR /root
# Mon, 08 Dec 2025 23:09:19 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1289ab7c7b6fa2d36a63b51e87b4666bc887341692f61437a0b556336f0c151a`  
		Last Modified: Mon, 08 Dec 2025 23:10:02 GMT  
		Size: 42.5 MB (42494027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e683b41f3e327630cea5ba33eeb45c96827ea45676e1722a892c23c0728a8106`  
		Last Modified: Mon, 08 Dec 2025 23:09:57 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac59f3cf5c2a6e69099eab2494e0de75495d85bb871549b275164ae395bc0379`  
		Last Modified: Mon, 08 Dec 2025 23:10:15 GMT  
		Size: 213.1 MB (213123730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0f477089806d36ef5df1b6f01649b0b27f470e12afd5b5eb43efd578df4d3b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1004550d227fb09e7abceb993ceb9c45fc4c645bd7cad8110944d6986cc5b2e0`

```dockerfile
```

-	Layers:
	-	`sha256:4b40b060369dc82e02904a55bd1da2de1b0675dd3328b51932c64dfa70cee4cf`  
		Last Modified: Tue, 09 Dec 2025 00:54:07 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:5026365945d5641a1e0a543f0b7787b3f1ed32a743c83025618016d2bb7f41bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219909622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef98bfdcb583201111630125e02bb4ef5354d98ecc9f891d3b554b6117832d44`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:11:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Dec 2025 00:11:17 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Dec 2025 00:11:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:11:17 GMT
WORKDIR /root
# Tue, 09 Dec 2025 00:11:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330db800000ceb71a5b4931c7af3bb78787caf15aebffe56b9fea88aea0d0038`  
		Last Modified: Tue, 09 Dec 2025 00:12:08 GMT  
		Size: 37.5 MB (37498187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2eb7e5542c2940a48aa0d3e709578dc644b7aa8ba3a4b849edc3e1e945af130`  
		Last Modified: Tue, 09 Dec 2025 00:12:05 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343578e7013e5eaf786fab6d5ad6b9e9fcbde89e03d585d7711d8e2493c109ae`  
		Last Modified: Tue, 09 Dec 2025 03:54:11 GMT  
		Size: 154.9 MB (154926269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2dbecca792f138832d0d0358cdb67d1d9da36127c6d0367d82d33f3300695f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57fb0ff953049de32a6a52193db53750c3d48634bf3a60297844b3e513ebc00`

```dockerfile
```

-	Layers:
	-	`sha256:e2151cabe75ab2f25660247151962498d32d1debcdcc069f29a6a58c92599098`  
		Last Modified: Tue, 09 Dec 2025 03:53:38 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b025cbf3ef15ee29d39c2b25166cbf4ceff650c563d3325b51052fde49ead5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c5e30b386e979b1133ab296cb28312fed93647063b9c9c192c2653748b50ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:12:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:12:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 08 Dec 2025 23:12:26 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 08 Dec 2025 23:12:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:12:26 GMT
WORKDIR /root
# Mon, 08 Dec 2025 23:12:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4277d4a195d6c5a03dfcc80e29845b846c81e09fd789ad3181a6fb60360cbd`  
		Last Modified: Mon, 08 Dec 2025 23:13:30 GMT  
		Size: 42.3 MB (42293374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58718d0e9028ed662a2db8110cfa8ff4d0f3fa32febd6de730b2102adaf6deda`  
		Last Modified: Mon, 08 Dec 2025 23:13:29 GMT  
		Size: 1.6 MB (1566654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d895e396ee508dccf7f951b130d92a4747abfb9e73ab0e09eda7ff3c659c4daa`  
		Last Modified: Mon, 08 Dec 2025 23:13:37 GMT  
		Size: 212.4 MB (212350809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7a7b4081a9b4ce312ad0b6effe48fd9f63b469581ad162aba69674e531afe4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bd14fb3fbab3e640a60a92621fc5cf02f5cd0b000af9237fc5f977f69380aa`

```dockerfile
```

-	Layers:
	-	`sha256:e3ba7b8fd93d9ae523e720fed98cdb80300696e290f72679709527d2cdb8c733`  
		Last Modified: Tue, 09 Dec 2025 03:53:41 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:ca2e682d07ac57d02e0dda00444fe59b57672fcb42fbd6782df5fda63eacff63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232965995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55e9f87a7ee15b1ac6a02c3f8e09054342da93f74fc64ff9fe90e8f43ea3877`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:21:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:21:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:21:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:21:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:21:05 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:21:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d187aa75d6411bfc9c015781547398506ff8a5d8e0c4ee5c89cba4597dca7658`  
		Last Modified: Tue, 02 Dec 2025 18:26:43 GMT  
		Size: 41.6 MB (41560771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1041beabf784b9a8a14f47ab8166f4c0734faf36f7141b1c5273529ee215bb06`  
		Last Modified: Tue, 02 Dec 2025 18:26:40 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d30c1df1fdda02922e7a0ffdd4a3481728a7b1db6fc160dc082a2d48f343b13`  
		Last Modified: Tue, 02 Dec 2025 21:54:07 GMT  
		Size: 161.6 MB (161564995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:409895074372ea1efcccec2f8f04996c052225c55cf490471d1572fd2aa334e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16ea2ecf25712c5b092186fcfa862d382097777b9f55cb66dab6c1ea6c792b6`

```dockerfile
```

-	Layers:
	-	`sha256:1fc85e7d225072d54ab114ef92e8df8e00b681a43cfdcb19f58e8a0d3c44b9e0`  
		Last Modified: Tue, 02 Dec 2025 21:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
