<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.11`](#dart311)
-	[`dart:3.11-sdk`](#dart311-sdk)
-	[`dart:3.11.6`](#dart3116)
-	[`dart:3.11.6-sdk`](#dart3116-sdk)
-	[`dart:3.13.0-103.1.beta`](#dart3130-1031beta)
-	[`dart:3.13.0-103.1.beta-sdk`](#dart3130-1031beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11-sdk`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.6`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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

### `dart:3.11.6` - linux; amd64

```console
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.6-sdk`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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

### `dart:3.11.6-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.13.0-103.1.beta`

**does not exist** (yet?)

## `dart:3.13.0-103.1.beta-sdk`

**does not exist** (yet?)

## `dart:beta`

```console
$ docker pull dart@sha256:c2200bf085f75497eba59709cb6d2e071295c4406b6e8c39aa07c32a0821ae9c
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
$ docker pull dart@sha256:a3748cee5dae42b03b89c95b13edfc439aa54c315a0f3223e7616bd39d34fd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f23b90bd8990a940b5d3bc7d4f457c5ae2b236ead6a94d27b9a07e82e393a9a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:40 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:40 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ccf7731b12d893775e11baed34447193ea314383314155a26167f319cece58b5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c25833e91bcdcd7d0726257e97272ad15f2c4162f0b6a9a1c4fb350a2b5df6c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e09bb89a033fa2351964debcfeb6638b40aa3c9d8d1b05ee72fe1ab850c99397;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3e5d12e69de4924f2eceae9da726972e991c33a687ba10277a0fbbe2b9886faa;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f743bc32dde2d568650066b10fe1eb6ed349fafa2a1c91dfe125dbcdb14f76`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 42.5 MB (42501685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609b5d32b9535b36fefc5dd429895b84e077d1c37e5b7de6a30d59a9c9e15cf8`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 1.9 MB (1869566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ed338fdf934503b7fdf8b31575847fbcc6058a12abc4e9009c1746b9d461ae`  
		Last Modified: Wed, 06 May 2026 17:10:27 GMT  
		Size: 236.8 MB (236791077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:807cb40acb981f66762906d36dfe8d9934865f40f88eddea0488c9bdf7749afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4316206fe06952ae181eb07682b423a94f15a5b77ddaeb6c253306179a5c62`

```dockerfile
```

-	Layers:
	-	`sha256:5a960e506c1044446764864abf1d9e6122776d4334a8682eb081b4564926d292`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:92b5d38e6ae7d529969e6ed6ab4a8b4c7b91b87b74e6d8b6794dbc0907b32b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226072977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdaa33b51ce826f8db7f787b521878d20e9dec4a24e57142933f2d6593f0e60e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ccf7731b12d893775e11baed34447193ea314383314155a26167f319cece58b5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c25833e91bcdcd7d0726257e97272ad15f2c4162f0b6a9a1c4fb350a2b5df6c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e09bb89a033fa2351964debcfeb6638b40aa3c9d8d1b05ee72fe1ab850c99397;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3e5d12e69de4924f2eceae9da726972e991c33a687ba10277a0fbbe2b9886faa;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac54218df35aa1ac02734f3828f06f85edebe059db29ef20b7bc34c8e37ed685`  
		Last Modified: Wed, 06 May 2026 17:09:37 GMT  
		Size: 161.1 MB (161089522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:0f95c60717bbfbd0e9784b9d33a4126779fb717a3af3ca788dd0ebfba11b8b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c208457f58e6239447cde93543cf0926fa7907f5c53288ac13d9340a3935990c`

```dockerfile
```

-	Layers:
	-	`sha256:2699f91951cdab757733bb76373c06229e60c5e4e2d4cf7d66283b19dad3c9f7`  
		Last Modified: Wed, 06 May 2026 17:09:33 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c9af4d1f6699514e135c312446c89c292cc8fd1298232392012f51296061a00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309387182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40df81b5ff06e3c5cfb004a1159a166641dfdc29f9902715166f5f5ff99df405`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:40 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:40 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ccf7731b12d893775e11baed34447193ea314383314155a26167f319cece58b5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c25833e91bcdcd7d0726257e97272ad15f2c4162f0b6a9a1c4fb350a2b5df6c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e09bb89a033fa2351964debcfeb6638b40aa3c9d8d1b05ee72fe1ab850c99397;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3e5d12e69de4924f2eceae9da726972e991c33a687ba10277a0fbbe2b9886faa;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d96bef88474e7c388f5013d68b46bd4ddc6407396ac39085465dbd45abc9aca`  
		Last Modified: Wed, 06 May 2026 17:10:27 GMT  
		Size: 42.3 MB (42281560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e58d75364633f1444ae343a24f6d42516422c573bceb583a5f8072f00d2bfc5`  
		Last Modified: Wed, 06 May 2026 17:10:24 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00db32807b2a838fe34c0ecbef19ff94804857a99ab12c3329991627fcb0e27`  
		Last Modified: Wed, 06 May 2026 17:10:37 GMT  
		Size: 235.4 MB (235397628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:215ec030abb4848d4d0100893a2ae9158b007688eeb4d6926dab7592b3dd3b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406bdd74fe63ea4f2d877efef1482039129c68601c15adc37b1d25c26826c91e`

```dockerfile
```

-	Layers:
	-	`sha256:f75d25c1c13194e9cb41f1d18da4eb88db28fe6701990593cb77bef030845472`  
		Last Modified: Wed, 06 May 2026 17:10:24 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:11b68920fc487084e0b7d3fb58b6a1a690baa8da7f277593cff28bd164c5c3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248323761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7171b5d8a144630fca15d4db90b283129e87c21115c45c67d12ad981e2c07815`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:15:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ccf7731b12d893775e11baed34447193ea314383314155a26167f319cece58b5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c25833e91bcdcd7d0726257e97272ad15f2c4162f0b6a9a1c4fb350a2b5df6c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e09bb89a033fa2351964debcfeb6638b40aa3c9d8d1b05ee72fe1ab850c99397;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3e5d12e69de4924f2eceae9da726972e991c33a687ba10277a0fbbe2b9886faa;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc3d73ce260b9b93e4ad16d83afd28b41d8347eeee9cf67619ebce3aec98171`  
		Last Modified: Wed, 06 May 2026 17:19:54 GMT  
		Size: 176.9 MB (176907220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:dfe3b567d49f7d371427be7dbdfb40de34241e7813f4886a221a0cbf31f9550d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef686903e80a238933deedf27fba72a2f7402e00dfc064e941620ef8d2fb6988`

```dockerfile
```

-	Layers:
	-	`sha256:931dd79408e5afa8d917983cb66a9efec5beefcd9d6b2afd06d27bc63d780a9f`  
		Last Modified: Wed, 06 May 2026 17:19:28 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:c2200bf085f75497eba59709cb6d2e071295c4406b6e8c39aa07c32a0821ae9c
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
$ docker pull dart@sha256:a3748cee5dae42b03b89c95b13edfc439aa54c315a0f3223e7616bd39d34fd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f23b90bd8990a940b5d3bc7d4f457c5ae2b236ead6a94d27b9a07e82e393a9a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:40 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:40 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ccf7731b12d893775e11baed34447193ea314383314155a26167f319cece58b5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c25833e91bcdcd7d0726257e97272ad15f2c4162f0b6a9a1c4fb350a2b5df6c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e09bb89a033fa2351964debcfeb6638b40aa3c9d8d1b05ee72fe1ab850c99397;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3e5d12e69de4924f2eceae9da726972e991c33a687ba10277a0fbbe2b9886faa;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f743bc32dde2d568650066b10fe1eb6ed349fafa2a1c91dfe125dbcdb14f76`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 42.5 MB (42501685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609b5d32b9535b36fefc5dd429895b84e077d1c37e5b7de6a30d59a9c9e15cf8`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 1.9 MB (1869566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ed338fdf934503b7fdf8b31575847fbcc6058a12abc4e9009c1746b9d461ae`  
		Last Modified: Wed, 06 May 2026 17:10:27 GMT  
		Size: 236.8 MB (236791077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:807cb40acb981f66762906d36dfe8d9934865f40f88eddea0488c9bdf7749afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4316206fe06952ae181eb07682b423a94f15a5b77ddaeb6c253306179a5c62`

```dockerfile
```

-	Layers:
	-	`sha256:5a960e506c1044446764864abf1d9e6122776d4334a8682eb081b4564926d292`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:92b5d38e6ae7d529969e6ed6ab4a8b4c7b91b87b74e6d8b6794dbc0907b32b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226072977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdaa33b51ce826f8db7f787b521878d20e9dec4a24e57142933f2d6593f0e60e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ccf7731b12d893775e11baed34447193ea314383314155a26167f319cece58b5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c25833e91bcdcd7d0726257e97272ad15f2c4162f0b6a9a1c4fb350a2b5df6c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e09bb89a033fa2351964debcfeb6638b40aa3c9d8d1b05ee72fe1ab850c99397;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3e5d12e69de4924f2eceae9da726972e991c33a687ba10277a0fbbe2b9886faa;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac54218df35aa1ac02734f3828f06f85edebe059db29ef20b7bc34c8e37ed685`  
		Last Modified: Wed, 06 May 2026 17:09:37 GMT  
		Size: 161.1 MB (161089522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0f95c60717bbfbd0e9784b9d33a4126779fb717a3af3ca788dd0ebfba11b8b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c208457f58e6239447cde93543cf0926fa7907f5c53288ac13d9340a3935990c`

```dockerfile
```

-	Layers:
	-	`sha256:2699f91951cdab757733bb76373c06229e60c5e4e2d4cf7d66283b19dad3c9f7`  
		Last Modified: Wed, 06 May 2026 17:09:33 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c9af4d1f6699514e135c312446c89c292cc8fd1298232392012f51296061a00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309387182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40df81b5ff06e3c5cfb004a1159a166641dfdc29f9902715166f5f5ff99df405`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:40 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:40 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:40 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ccf7731b12d893775e11baed34447193ea314383314155a26167f319cece58b5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c25833e91bcdcd7d0726257e97272ad15f2c4162f0b6a9a1c4fb350a2b5df6c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e09bb89a033fa2351964debcfeb6638b40aa3c9d8d1b05ee72fe1ab850c99397;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3e5d12e69de4924f2eceae9da726972e991c33a687ba10277a0fbbe2b9886faa;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d96bef88474e7c388f5013d68b46bd4ddc6407396ac39085465dbd45abc9aca`  
		Last Modified: Wed, 06 May 2026 17:10:27 GMT  
		Size: 42.3 MB (42281560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e58d75364633f1444ae343a24f6d42516422c573bceb583a5f8072f00d2bfc5`  
		Last Modified: Wed, 06 May 2026 17:10:24 GMT  
		Size: 1.6 MB (1564356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00db32807b2a838fe34c0ecbef19ff94804857a99ab12c3329991627fcb0e27`  
		Last Modified: Wed, 06 May 2026 17:10:37 GMT  
		Size: 235.4 MB (235397628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:215ec030abb4848d4d0100893a2ae9158b007688eeb4d6926dab7592b3dd3b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406bdd74fe63ea4f2d877efef1482039129c68601c15adc37b1d25c26826c91e`

```dockerfile
```

-	Layers:
	-	`sha256:f75d25c1c13194e9cb41f1d18da4eb88db28fe6701990593cb77bef030845472`  
		Last Modified: Wed, 06 May 2026 17:10:24 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:11b68920fc487084e0b7d3fb58b6a1a690baa8da7f277593cff28bd164c5c3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248323761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7171b5d8a144630fca15d4db90b283129e87c21115c45c67d12ad981e2c07815`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:15:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ccf7731b12d893775e11baed34447193ea314383314155a26167f319cece58b5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c25833e91bcdcd7d0726257e97272ad15f2c4162f0b6a9a1c4fb350a2b5df6c3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e09bb89a033fa2351964debcfeb6638b40aa3c9d8d1b05ee72fe1ab850c99397;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3e5d12e69de4924f2eceae9da726972e991c33a687ba10277a0fbbe2b9886faa;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc3d73ce260b9b93e4ad16d83afd28b41d8347eeee9cf67619ebce3aec98171`  
		Last Modified: Wed, 06 May 2026 17:19:54 GMT  
		Size: 176.9 MB (176907220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dfe3b567d49f7d371427be7dbdfb40de34241e7813f4886a221a0cbf31f9550d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef686903e80a238933deedf27fba72a2f7402e00dfc064e941620ef8d2fb6988`

```dockerfile
```

-	Layers:
	-	`sha256:931dd79408e5afa8d917983cb66a9efec5beefcd9d6b2afd06d27bc63d780a9f`  
		Last Modified: Wed, 06 May 2026 17:19:28 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:08546959a91b0651185e0c7f7a009affc56f928bde47249511406fcb780a6b57
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
$ docker pull dart@sha256:a24dfbefd678b88cbfb233bd8c1cc42e3cf7f044b5a2e059ae5bae85d45661f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da24a1099a91be446789775f54fbd6dd20e383a98f23792d29bb006d0ce0c5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3ecc91e92fdff858eaa680f7471c671fc26173177bae0700f003ad524c1ec0`  
		Last Modified: Wed, 06 May 2026 17:10:19 GMT  
		Size: 42.5 MB (42501811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6722807d0491a0e730b36c6f95994f8252cd768f1287a97d2e152f52fec0fb`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 1.9 MB (1869569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d9ab7b5fa93a41e00385fb8f86d1524d5bb56324a3edbb64d60f4f16eacd9`  
		Last Modified: Wed, 06 May 2026 17:10:23 GMT  
		Size: 233.0 MB (232962940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:82dae9da1d3b26788ce9b69f278c14e069530a8a5fd7e1bd0e2739c205ad5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b7479b82cd6e66fab1651831411edf5180a28d7788b968a2f13a4665c8c1f0`

```dockerfile
```

-	Layers:
	-	`sha256:b8e48920e8a39abb65bb12e63642b2eb4f71d0ce8b046484940c28515165dd5f`  
		Last Modified: Wed, 06 May 2026 17:10:17 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:69cc763c9507d4d1a24edbb8f2b76d8a7bb03254f2695dd4e54ebb6ddedb44fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6476c0dd5c89904074c616549a9df21c8f459524d8c6754e96f3a5546b5ca3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:08:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:08:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:08:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:08:28 GMT
WORKDIR /root
# Wed, 06 May 2026 17:08:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a8679e1e99301c259706290f49cb6f0be1eda86255520de838e9b5720e6c3a`  
		Last Modified: Wed, 06 May 2026 17:08:57 GMT  
		Size: 37.5 MB (37495424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cf25cdc7e417e6fc1e168848b1800fe715d44d5ffb3d2633dbe5a81cb101e`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 1.3 MB (1273161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb9f0217a01d308b9c5ce9ffdea4aeaddc2e4c8ad6d736d221ec641bbb4a17`  
		Last Modified: Wed, 06 May 2026 17:08:59 GMT  
		Size: 157.9 MB (157918546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9e5dd4a36b04e61e74ad5c229fbb6dbd1e492590040bdcb1967f84caef97ebef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14fbe633cb076dc82186915bc3e6135f4b281b2c8439023d5adcabcd604827a`

```dockerfile
```

-	Layers:
	-	`sha256:2c260d57d01692b401dec81f228d78620d984aa8d2a54b3c04cca57b58689f54`  
		Last Modified: Wed, 06 May 2026 17:08:55 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:70ee7cc1e810cf6f469f04f5e6d9cbf67132ce9292ecd3e45816209545874953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305471043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e02c44a01e1dea9105e11272b5c273591ab894ec7c9ceaf185a849761d226`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:35 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:35 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61e665f429c0e0dc9b10832ce4fe69945d2fd63fc45b34931d6ff4c0db2d0e`  
		Last Modified: Wed, 06 May 2026 17:10:21 GMT  
		Size: 42.3 MB (42281610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d506fa53587dbeb67ac3d3f85eae24bcf2695a3c05b8a8621dfe704d1b58bc3`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab05146d7de7ece5f9220da5953454b9dbd5e92f2bd4666faece0dab6b5e51c`  
		Last Modified: Wed, 06 May 2026 17:10:25 GMT  
		Size: 231.5 MB (231481444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a25e6d7dc6798b81755676b9294c7819a28e4bb9de49e1489c4f6258106a605e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbeede498b1654d75050245946a0f64bf699001a838e5052e12d040585419a2`

```dockerfile
```

-	Layers:
	-	`sha256:1d8a8ffd02f42257a62432dcde0e6e8d60dbd24185b109bbeada03662f78994e`  
		Last Modified: Wed, 06 May 2026 17:10:20 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:5f97293f707d741fbfc48069f9f1cbae35da80ce06779e1f41dd9b2dc1b28e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251918227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abd9ff82cd2b69077bc735307fe6f7b3889a7b180df8b8efa13cf92856aeed0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 06 May 2026 17:09:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 17:09:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 06 May 2026 17:09:01 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 06 May 2026 17:09:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 17:09:01 GMT
WORKDIR /root
# Wed, 06 May 2026 17:09:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d4e0a91f98dae70acfe21d9810283afd8d9e5281a344a5f19a998f5077fda6`  
		Last Modified: Wed, 06 May 2026 17:13:58 GMT  
		Size: 41.6 MB (41571919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bbad47a9585c88a7ad173b284fcc6b965a05da831050096a52e61726252b73`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 1.6 MB (1564395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9d988ea80803e857fee306416102f829fd230c8ccf2758cee0b1ab8e7ff35`  
		Last Modified: Wed, 06 May 2026 17:14:17 GMT  
		Size: 180.5 MB (180501686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:09d0fea9032ef7f604678f8d8a2161d8e2e2a793ab653af67d5430a3a2035e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b6d7f096cdcb96843dc738dd932c9e8081d67b9d15a85181fa40b525a22ae`

```dockerfile
```

-	Layers:
	-	`sha256:19ab201cfab580ca8fe16942e509416ca2544264fc0cdf3196142b78d067bb00`  
		Last Modified: Wed, 06 May 2026 17:13:46 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
