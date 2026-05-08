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

```console
$ docker pull dart@sha256:f807c88dc71fb29a7115d90c0792c0a6807e04d552049f2db49b1dba5e0ee899
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.13.0-103.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:94ca56aa61360e5a055f94df151e3677633fd8bbccec4f98a259ac4e52dcbab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311865197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a327aa06cea95ddbfe541e5519df23df264d4a07f12bf730cb8d1e3c190c6c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:50:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:50:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:50:26 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:50:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:50:26 GMT
WORKDIR /root
# Fri, 08 May 2026 17:50:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c093f35686f5d269d1b0d109e34c8777fe8a82e50f3f180b34dee0544132a7e2`  
		Last Modified: Fri, 08 May 2026 17:51:11 GMT  
		Size: 42.5 MB (42501614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29e3ddc0d2473169cfee062beff831a25e9923c1f75b508105d161765c5cc5e`  
		Last Modified: Fri, 08 May 2026 17:51:09 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96122daaef5b83bb1b8bf01177cee206a2c672cb7fe106b7badffcb74ad49c87`  
		Last Modified: Fri, 08 May 2026 17:51:15 GMT  
		Size: 237.7 MB (237713810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:80da9fa33470594981e6be02245e0e50bd114d3d752d88205cbb1812786c2def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed414b8972685dfde9b3d95b5be7b4563c45862c5ef395b091ac6d907a8554c`

```dockerfile
```

-	Layers:
	-	`sha256:13d368fd59c4320d6c05e83bf2fd9b727b09f9730f2cf42a1fb91de6ceea30b6`  
		Last Modified: Fri, 08 May 2026 17:51:08 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:4edb57b87b04ae662cca14a48db7df76d22281e8ed2f73204463830de78980ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226609054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9528849af21a9e62ffe996c518d119bcfae29f6572448b3c9970e51633110b42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:53:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:53:28 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:53:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:53:28 GMT
WORKDIR /root
# Fri, 08 May 2026 17:53:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aed0a9d6064969a943b74c857544a11339b01dc5bff1156f3d7249f7d37d33`  
		Last Modified: Fri, 08 May 2026 17:53:58 GMT  
		Size: 37.5 MB (37495341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3cbd5d8f5f8a77d1ba760267d84ed56f532f0fa8db90597ceb89240784bed`  
		Last Modified: Fri, 08 May 2026 17:53:56 GMT  
		Size: 1.3 MB (1273162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ac4e1dbe1442b7a79d01a9192ffe51329682e547a46f9c5f8a196fd4eeae9`  
		Last Modified: Fri, 08 May 2026 17:54:00 GMT  
		Size: 161.6 MB (161625681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:7a2fc9c3cfc35cbb6a0d6e746e2bf5af099e138b151703ba49b66fdab53622aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a440ffa6bc8f3f40618986be43ea82e819503b2018b40891ca3e5008e351b2`

```dockerfile
```

-	Layers:
	-	`sha256:c4bbc2308d479e873883d91377a75914a8824dc95dd6f068a70a3489fd5ae0da`  
		Last Modified: Fri, 08 May 2026 17:53:55 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:069eb1cc945411d4f9476c62868f02cc5f1723b85f26e180c2d73778fc4e6947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310467695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7b842f6a7afda79175ed4342c414f6d189de4c5c68cf241166a17234a233a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:50:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:50:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:50:43 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:50:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:50:43 GMT
WORKDIR /root
# Fri, 08 May 2026 17:50:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f319ce74def9fc4e538287e8afa2f73d1222d15a7bf9358a70ebeee2e2a616`  
		Last Modified: Fri, 08 May 2026 17:51:28 GMT  
		Size: 42.3 MB (42281588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b3161b79aa1c9c794a3d80fc998ce457aeb96c97fa4c1d45b6c7cea06360b`  
		Last Modified: Fri, 08 May 2026 17:51:26 GMT  
		Size: 1.6 MB (1564357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829c1dd119c35d838d920a5e54a287366d6a0ac58e2b6dd473115a156067dba8`  
		Last Modified: Fri, 08 May 2026 17:51:31 GMT  
		Size: 236.5 MB (236478112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:97e43fdd3bd0ccff40b60f4f87b4ee1a64035fb091505bda6934aa98b3b3e64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a51593e19c16aee40e384349abe503abe901a79520620bf59cc43cf231a3af`

```dockerfile
```

-	Layers:
	-	`sha256:c35d61efca62d8dfc73f005fbdef3f2aeeb65acf2b92631f8e09ecf31284799a`  
		Last Modified: Fri, 08 May 2026 17:51:26 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.13.0-103.1.beta-sdk`

```console
$ docker pull dart@sha256:f807c88dc71fb29a7115d90c0792c0a6807e04d552049f2db49b1dba5e0ee899
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.13.0-103.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:94ca56aa61360e5a055f94df151e3677633fd8bbccec4f98a259ac4e52dcbab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311865197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a327aa06cea95ddbfe541e5519df23df264d4a07f12bf730cb8d1e3c190c6c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:50:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:50:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:50:26 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:50:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:50:26 GMT
WORKDIR /root
# Fri, 08 May 2026 17:50:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c093f35686f5d269d1b0d109e34c8777fe8a82e50f3f180b34dee0544132a7e2`  
		Last Modified: Fri, 08 May 2026 17:51:11 GMT  
		Size: 42.5 MB (42501614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29e3ddc0d2473169cfee062beff831a25e9923c1f75b508105d161765c5cc5e`  
		Last Modified: Fri, 08 May 2026 17:51:09 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96122daaef5b83bb1b8bf01177cee206a2c672cb7fe106b7badffcb74ad49c87`  
		Last Modified: Fri, 08 May 2026 17:51:15 GMT  
		Size: 237.7 MB (237713810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:80da9fa33470594981e6be02245e0e50bd114d3d752d88205cbb1812786c2def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed414b8972685dfde9b3d95b5be7b4563c45862c5ef395b091ac6d907a8554c`

```dockerfile
```

-	Layers:
	-	`sha256:13d368fd59c4320d6c05e83bf2fd9b727b09f9730f2cf42a1fb91de6ceea30b6`  
		Last Modified: Fri, 08 May 2026 17:51:08 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4edb57b87b04ae662cca14a48db7df76d22281e8ed2f73204463830de78980ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226609054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9528849af21a9e62ffe996c518d119bcfae29f6572448b3c9970e51633110b42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:53:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:53:28 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:53:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:53:28 GMT
WORKDIR /root
# Fri, 08 May 2026 17:53:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aed0a9d6064969a943b74c857544a11339b01dc5bff1156f3d7249f7d37d33`  
		Last Modified: Fri, 08 May 2026 17:53:58 GMT  
		Size: 37.5 MB (37495341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3cbd5d8f5f8a77d1ba760267d84ed56f532f0fa8db90597ceb89240784bed`  
		Last Modified: Fri, 08 May 2026 17:53:56 GMT  
		Size: 1.3 MB (1273162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ac4e1dbe1442b7a79d01a9192ffe51329682e547a46f9c5f8a196fd4eeae9`  
		Last Modified: Fri, 08 May 2026 17:54:00 GMT  
		Size: 161.6 MB (161625681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7a2fc9c3cfc35cbb6a0d6e746e2bf5af099e138b151703ba49b66fdab53622aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a440ffa6bc8f3f40618986be43ea82e819503b2018b40891ca3e5008e351b2`

```dockerfile
```

-	Layers:
	-	`sha256:c4bbc2308d479e873883d91377a75914a8824dc95dd6f068a70a3489fd5ae0da`  
		Last Modified: Fri, 08 May 2026 17:53:55 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:069eb1cc945411d4f9476c62868f02cc5f1723b85f26e180c2d73778fc4e6947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310467695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7b842f6a7afda79175ed4342c414f6d189de4c5c68cf241166a17234a233a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:50:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:50:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:50:43 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:50:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:50:43 GMT
WORKDIR /root
# Fri, 08 May 2026 17:50:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f319ce74def9fc4e538287e8afa2f73d1222d15a7bf9358a70ebeee2e2a616`  
		Last Modified: Fri, 08 May 2026 17:51:28 GMT  
		Size: 42.3 MB (42281588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b3161b79aa1c9c794a3d80fc998ce457aeb96c97fa4c1d45b6c7cea06360b`  
		Last Modified: Fri, 08 May 2026 17:51:26 GMT  
		Size: 1.6 MB (1564357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829c1dd119c35d838d920a5e54a287366d6a0ac58e2b6dd473115a156067dba8`  
		Last Modified: Fri, 08 May 2026 17:51:31 GMT  
		Size: 236.5 MB (236478112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:97e43fdd3bd0ccff40b60f4f87b4ee1a64035fb091505bda6934aa98b3b3e64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a51593e19c16aee40e384349abe503abe901a79520620bf59cc43cf231a3af`

```dockerfile
```

-	Layers:
	-	`sha256:c35d61efca62d8dfc73f005fbdef3f2aeeb65acf2b92631f8e09ecf31284799a`  
		Last Modified: Fri, 08 May 2026 17:51:26 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:c62370a4ec7443038cdb9cb1cc7b1806eda8c6b02aaca95607e7bdad738ec480
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
$ docker pull dart@sha256:94ca56aa61360e5a055f94df151e3677633fd8bbccec4f98a259ac4e52dcbab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311865197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a327aa06cea95ddbfe541e5519df23df264d4a07f12bf730cb8d1e3c190c6c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:50:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:50:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:50:26 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:50:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:50:26 GMT
WORKDIR /root
# Fri, 08 May 2026 17:50:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c093f35686f5d269d1b0d109e34c8777fe8a82e50f3f180b34dee0544132a7e2`  
		Last Modified: Fri, 08 May 2026 17:51:11 GMT  
		Size: 42.5 MB (42501614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29e3ddc0d2473169cfee062beff831a25e9923c1f75b508105d161765c5cc5e`  
		Last Modified: Fri, 08 May 2026 17:51:09 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96122daaef5b83bb1b8bf01177cee206a2c672cb7fe106b7badffcb74ad49c87`  
		Last Modified: Fri, 08 May 2026 17:51:15 GMT  
		Size: 237.7 MB (237713810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:80da9fa33470594981e6be02245e0e50bd114d3d752d88205cbb1812786c2def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed414b8972685dfde9b3d95b5be7b4563c45862c5ef395b091ac6d907a8554c`

```dockerfile
```

-	Layers:
	-	`sha256:13d368fd59c4320d6c05e83bf2fd9b727b09f9730f2cf42a1fb91de6ceea30b6`  
		Last Modified: Fri, 08 May 2026 17:51:08 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:4edb57b87b04ae662cca14a48db7df76d22281e8ed2f73204463830de78980ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226609054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9528849af21a9e62ffe996c518d119bcfae29f6572448b3c9970e51633110b42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:53:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:53:28 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:53:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:53:28 GMT
WORKDIR /root
# Fri, 08 May 2026 17:53:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aed0a9d6064969a943b74c857544a11339b01dc5bff1156f3d7249f7d37d33`  
		Last Modified: Fri, 08 May 2026 17:53:58 GMT  
		Size: 37.5 MB (37495341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3cbd5d8f5f8a77d1ba760267d84ed56f532f0fa8db90597ceb89240784bed`  
		Last Modified: Fri, 08 May 2026 17:53:56 GMT  
		Size: 1.3 MB (1273162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ac4e1dbe1442b7a79d01a9192ffe51329682e547a46f9c5f8a196fd4eeae9`  
		Last Modified: Fri, 08 May 2026 17:54:00 GMT  
		Size: 161.6 MB (161625681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:7a2fc9c3cfc35cbb6a0d6e746e2bf5af099e138b151703ba49b66fdab53622aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a440ffa6bc8f3f40618986be43ea82e819503b2018b40891ca3e5008e351b2`

```dockerfile
```

-	Layers:
	-	`sha256:c4bbc2308d479e873883d91377a75914a8824dc95dd6f068a70a3489fd5ae0da`  
		Last Modified: Fri, 08 May 2026 17:53:55 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:069eb1cc945411d4f9476c62868f02cc5f1723b85f26e180c2d73778fc4e6947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310467695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7b842f6a7afda79175ed4342c414f6d189de4c5c68cf241166a17234a233a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:50:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:50:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:50:43 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:50:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:50:43 GMT
WORKDIR /root
# Fri, 08 May 2026 17:50:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f319ce74def9fc4e538287e8afa2f73d1222d15a7bf9358a70ebeee2e2a616`  
		Last Modified: Fri, 08 May 2026 17:51:28 GMT  
		Size: 42.3 MB (42281588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b3161b79aa1c9c794a3d80fc998ce457aeb96c97fa4c1d45b6c7cea06360b`  
		Last Modified: Fri, 08 May 2026 17:51:26 GMT  
		Size: 1.6 MB (1564357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829c1dd119c35d838d920a5e54a287366d6a0ac58e2b6dd473115a156067dba8`  
		Last Modified: Fri, 08 May 2026 17:51:31 GMT  
		Size: 236.5 MB (236478112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:97e43fdd3bd0ccff40b60f4f87b4ee1a64035fb091505bda6934aa98b3b3e64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a51593e19c16aee40e384349abe503abe901a79520620bf59cc43cf231a3af`

```dockerfile
```

-	Layers:
	-	`sha256:c35d61efca62d8dfc73f005fbdef3f2aeeb65acf2b92631f8e09ecf31284799a`  
		Last Modified: Fri, 08 May 2026 17:51:26 GMT  
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
$ docker pull dart@sha256:c62370a4ec7443038cdb9cb1cc7b1806eda8c6b02aaca95607e7bdad738ec480
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
$ docker pull dart@sha256:94ca56aa61360e5a055f94df151e3677633fd8bbccec4f98a259ac4e52dcbab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311865197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a327aa06cea95ddbfe541e5519df23df264d4a07f12bf730cb8d1e3c190c6c2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:50:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:50:26 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:50:26 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:50:26 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:50:26 GMT
WORKDIR /root
# Fri, 08 May 2026 17:50:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c093f35686f5d269d1b0d109e34c8777fe8a82e50f3f180b34dee0544132a7e2`  
		Last Modified: Fri, 08 May 2026 17:51:11 GMT  
		Size: 42.5 MB (42501614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29e3ddc0d2473169cfee062beff831a25e9923c1f75b508105d161765c5cc5e`  
		Last Modified: Fri, 08 May 2026 17:51:09 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96122daaef5b83bb1b8bf01177cee206a2c672cb7fe106b7badffcb74ad49c87`  
		Last Modified: Fri, 08 May 2026 17:51:15 GMT  
		Size: 237.7 MB (237713810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:80da9fa33470594981e6be02245e0e50bd114d3d752d88205cbb1812786c2def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed414b8972685dfde9b3d95b5be7b4563c45862c5ef395b091ac6d907a8554c`

```dockerfile
```

-	Layers:
	-	`sha256:13d368fd59c4320d6c05e83bf2fd9b727b09f9730f2cf42a1fb91de6ceea30b6`  
		Last Modified: Fri, 08 May 2026 17:51:08 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:4edb57b87b04ae662cca14a48db7df76d22281e8ed2f73204463830de78980ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226609054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9528849af21a9e62ffe996c518d119bcfae29f6572448b3c9970e51633110b42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:53:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:53:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:53:28 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:53:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:53:28 GMT
WORKDIR /root
# Fri, 08 May 2026 17:53:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40aed0a9d6064969a943b74c857544a11339b01dc5bff1156f3d7249f7d37d33`  
		Last Modified: Fri, 08 May 2026 17:53:58 GMT  
		Size: 37.5 MB (37495341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a3cbd5d8f5f8a77d1ba760267d84ed56f532f0fa8db90597ceb89240784bed`  
		Last Modified: Fri, 08 May 2026 17:53:56 GMT  
		Size: 1.3 MB (1273162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ac4e1dbe1442b7a79d01a9192ffe51329682e547a46f9c5f8a196fd4eeae9`  
		Last Modified: Fri, 08 May 2026 17:54:00 GMT  
		Size: 161.6 MB (161625681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7a2fc9c3cfc35cbb6a0d6e746e2bf5af099e138b151703ba49b66fdab53622aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a440ffa6bc8f3f40618986be43ea82e819503b2018b40891ca3e5008e351b2`

```dockerfile
```

-	Layers:
	-	`sha256:c4bbc2308d479e873883d91377a75914a8824dc95dd6f068a70a3489fd5ae0da`  
		Last Modified: Fri, 08 May 2026 17:53:55 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:069eb1cc945411d4f9476c62868f02cc5f1723b85f26e180c2d73778fc4e6947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310467695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7b842f6a7afda79175ed4342c414f6d189de4c5c68cf241166a17234a233a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 17:50:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 17:50:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 17:50:43 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 17:50:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 17:50:43 GMT
WORKDIR /root
# Fri, 08 May 2026 17:50:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f319ce74def9fc4e538287e8afa2f73d1222d15a7bf9358a70ebeee2e2a616`  
		Last Modified: Fri, 08 May 2026 17:51:28 GMT  
		Size: 42.3 MB (42281588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b3161b79aa1c9c794a3d80fc998ce457aeb96c97fa4c1d45b6c7cea06360b`  
		Last Modified: Fri, 08 May 2026 17:51:26 GMT  
		Size: 1.6 MB (1564357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829c1dd119c35d838d920a5e54a287366d6a0ac58e2b6dd473115a156067dba8`  
		Last Modified: Fri, 08 May 2026 17:51:31 GMT  
		Size: 236.5 MB (236478112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:97e43fdd3bd0ccff40b60f4f87b4ee1a64035fb091505bda6934aa98b3b3e64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a51593e19c16aee40e384349abe503abe901a79520620bf59cc43cf231a3af`

```dockerfile
```

-	Layers:
	-	`sha256:c35d61efca62d8dfc73f005fbdef3f2aeeb65acf2b92631f8e09ecf31284799a`  
		Last Modified: Fri, 08 May 2026 17:51:26 GMT  
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
