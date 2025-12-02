<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10`](#dart310)
-	[`dart:3.10-sdk`](#dart310-sdk)
-	[`dart:3.10.3`](#dart3103)
-	[`dart:3.10.3-sdk`](#dart3103-sdk)
-	[`dart:3.11.0-93.2.beta`](#dart3110-932beta)
-	[`dart:3.11.0-93.2.beta-sdk`](#dart3110-932beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:9bda6665fb4bbf91bd76ac22de9c794c6fa2729247a0e567ce7ed05e4fa227cf
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
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:8f71d7706ccb4056ae580ad6fd9d7a7443126f8752db4270fbfe4b3c8a84fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a55c968498bc692f7b54ed3f648b4b80efadc09d3a462c199872c0f4bc5ed8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 25 Nov 2025 23:42:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 23:42:03 GMT
WORKDIR /root
# Tue, 25 Nov 2025 23:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4d1582f8362f16308f09df2cc9fda05f7fdaf475e639b7881faa01628c12fd55;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c5aee772e3358f358e386189eb50fefb6c3b3f7c5139e9efe19e76a1f5fa2cad;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9c4a5d4de58dd0dac1f8db0c7c642916f7dcae9d2a7e3332cd3d5e869d10010d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2d52411bfefe30828193ba0a72b49fa53686856abd40a70aa89bf5425ba13b17;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e8f156955db89384e0c3c46f9f9990563aa96f1dec1d5fb80a49522390a8d`  
		Last Modified: Tue, 25 Nov 2025 23:47:17 GMT  
		Size: 41.6 MB (41560780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc918216557c937ff78b87a2de8e120afbb58c17c978291ae94ce0b2d862898`  
		Last Modified: Tue, 25 Nov 2025 23:47:11 GMT  
		Size: 1.6 MB (1567074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3de20ad580a49b4e8226bfaf7d62209795ba058c847c0e5b527df9d0bddc5e`  
		Last Modified: Tue, 25 Nov 2025 23:51:38 GMT  
		Size: 161.6 MB (161563090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:fc9c402e66f35f654d7079143d9fc20851b2db599b85c39ef6f430516a5ea051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae261d8639b433165568f3a39514dc827f2bd765aca5fa8e637d5a9ebb642fa`

```dockerfile
```

-	Layers:
	-	`sha256:97a344939c3fa005bdd8353af064bcec8ee4c24bf6a2cde4e1216de059ad518d`  
		Last Modified: Wed, 26 Nov 2025 00:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:9bda6665fb4bbf91bd76ac22de9c794c6fa2729247a0e567ce7ed05e4fa227cf
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
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8f71d7706ccb4056ae580ad6fd9d7a7443126f8752db4270fbfe4b3c8a84fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a55c968498bc692f7b54ed3f648b4b80efadc09d3a462c199872c0f4bc5ed8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 25 Nov 2025 23:42:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 23:42:03 GMT
WORKDIR /root
# Tue, 25 Nov 2025 23:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4d1582f8362f16308f09df2cc9fda05f7fdaf475e639b7881faa01628c12fd55;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c5aee772e3358f358e386189eb50fefb6c3b3f7c5139e9efe19e76a1f5fa2cad;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9c4a5d4de58dd0dac1f8db0c7c642916f7dcae9d2a7e3332cd3d5e869d10010d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2d52411bfefe30828193ba0a72b49fa53686856abd40a70aa89bf5425ba13b17;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e8f156955db89384e0c3c46f9f9990563aa96f1dec1d5fb80a49522390a8d`  
		Last Modified: Tue, 25 Nov 2025 23:47:17 GMT  
		Size: 41.6 MB (41560780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc918216557c937ff78b87a2de8e120afbb58c17c978291ae94ce0b2d862898`  
		Last Modified: Tue, 25 Nov 2025 23:47:11 GMT  
		Size: 1.6 MB (1567074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3de20ad580a49b4e8226bfaf7d62209795ba058c847c0e5b527df9d0bddc5e`  
		Last Modified: Tue, 25 Nov 2025 23:51:38 GMT  
		Size: 161.6 MB (161563090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fc9c402e66f35f654d7079143d9fc20851b2db599b85c39ef6f430516a5ea051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae261d8639b433165568f3a39514dc827f2bd765aca5fa8e637d5a9ebb642fa`

```dockerfile
```

-	Layers:
	-	`sha256:97a344939c3fa005bdd8353af064bcec8ee4c24bf6a2cde4e1216de059ad518d`  
		Last Modified: Wed, 26 Nov 2025 00:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10`

```console
$ docker pull dart@sha256:9bda6665fb4bbf91bd76ac22de9c794c6fa2729247a0e567ce7ed05e4fa227cf
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
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; riscv64

```console
$ docker pull dart@sha256:8f71d7706ccb4056ae580ad6fd9d7a7443126f8752db4270fbfe4b3c8a84fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a55c968498bc692f7b54ed3f648b4b80efadc09d3a462c199872c0f4bc5ed8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 25 Nov 2025 23:42:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 23:42:03 GMT
WORKDIR /root
# Tue, 25 Nov 2025 23:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4d1582f8362f16308f09df2cc9fda05f7fdaf475e639b7881faa01628c12fd55;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c5aee772e3358f358e386189eb50fefb6c3b3f7c5139e9efe19e76a1f5fa2cad;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9c4a5d4de58dd0dac1f8db0c7c642916f7dcae9d2a7e3332cd3d5e869d10010d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2d52411bfefe30828193ba0a72b49fa53686856abd40a70aa89bf5425ba13b17;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e8f156955db89384e0c3c46f9f9990563aa96f1dec1d5fb80a49522390a8d`  
		Last Modified: Tue, 25 Nov 2025 23:47:17 GMT  
		Size: 41.6 MB (41560780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc918216557c937ff78b87a2de8e120afbb58c17c978291ae94ce0b2d862898`  
		Last Modified: Tue, 25 Nov 2025 23:47:11 GMT  
		Size: 1.6 MB (1567074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3de20ad580a49b4e8226bfaf7d62209795ba058c847c0e5b527df9d0bddc5e`  
		Last Modified: Tue, 25 Nov 2025 23:51:38 GMT  
		Size: 161.6 MB (161563090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:fc9c402e66f35f654d7079143d9fc20851b2db599b85c39ef6f430516a5ea051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae261d8639b433165568f3a39514dc827f2bd765aca5fa8e637d5a9ebb642fa`

```dockerfile
```

-	Layers:
	-	`sha256:97a344939c3fa005bdd8353af064bcec8ee4c24bf6a2cde4e1216de059ad518d`  
		Last Modified: Wed, 26 Nov 2025 00:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10-sdk`

```console
$ docker pull dart@sha256:9bda6665fb4bbf91bd76ac22de9c794c6fa2729247a0e567ce7ed05e4fa227cf
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
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8f71d7706ccb4056ae580ad6fd9d7a7443126f8752db4270fbfe4b3c8a84fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a55c968498bc692f7b54ed3f648b4b80efadc09d3a462c199872c0f4bc5ed8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 25 Nov 2025 23:42:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 23:42:03 GMT
WORKDIR /root
# Tue, 25 Nov 2025 23:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4d1582f8362f16308f09df2cc9fda05f7fdaf475e639b7881faa01628c12fd55;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c5aee772e3358f358e386189eb50fefb6c3b3f7c5139e9efe19e76a1f5fa2cad;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9c4a5d4de58dd0dac1f8db0c7c642916f7dcae9d2a7e3332cd3d5e869d10010d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2d52411bfefe30828193ba0a72b49fa53686856abd40a70aa89bf5425ba13b17;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e8f156955db89384e0c3c46f9f9990563aa96f1dec1d5fb80a49522390a8d`  
		Last Modified: Tue, 25 Nov 2025 23:47:17 GMT  
		Size: 41.6 MB (41560780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc918216557c937ff78b87a2de8e120afbb58c17c978291ae94ce0b2d862898`  
		Last Modified: Tue, 25 Nov 2025 23:47:11 GMT  
		Size: 1.6 MB (1567074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3de20ad580a49b4e8226bfaf7d62209795ba058c847c0e5b527df9d0bddc5e`  
		Last Modified: Tue, 25 Nov 2025 23:51:38 GMT  
		Size: 161.6 MB (161563090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fc9c402e66f35f654d7079143d9fc20851b2db599b85c39ef6f430516a5ea051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae261d8639b433165568f3a39514dc827f2bd765aca5fa8e637d5a9ebb642fa`

```dockerfile
```

-	Layers:
	-	`sha256:97a344939c3fa005bdd8353af064bcec8ee4c24bf6a2cde4e1216de059ad518d`  
		Last Modified: Wed, 26 Nov 2025 00:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.3`

```console
$ docker pull dart@sha256:4126f20fb19310960b10e9eff60be7816b9d97a9c8a9f413a2406a6b77646e05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.10.3` - linux; amd64

```console
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.3` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.3` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.3` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.3` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.3-sdk`

```console
$ docker pull dart@sha256:4126f20fb19310960b10e9eff60be7816b9d97a9c8a9f413a2406a6b77646e05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.10.3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-93.2.beta`

```console
$ docker pull dart@sha256:f65f34c54c2fd57e115449046af8fe8b640a099682f01c7d459ad52e2aca8a10
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

### `dart:3.11.0-93.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:d65d30ccbc3e6b00cbbc83946b9ef517cb5531c0fc4da4a60644b9bc331a989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288383491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbb20cd91f9204144cebebc27862fe183455e029fa759e2474c717099e7d38f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 05:14:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 05:15:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2529f5cef81aeecc09c6572e1e0dbe33c3a22307a223b8ecfaa82bcf21743`  
		Last Modified: Tue, 18 Nov 2025 05:15:37 GMT  
		Size: 42.5 MB (42494038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4313a42c948bf5c26bf4c6050453a911eb2d1fa3107407e270ee2fc2fddfe5d4`  
		Last Modified: Tue, 18 Nov 2025 05:15:34 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0620f90d617bf0c728028c0832e588717bfb0641da01c0676a65d98fc0e15d28`  
		Last Modified: Tue, 18 Nov 2025 06:54:57 GMT  
		Size: 214.2 MB (214239319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:eec7307ccf0361b096c0a867fb42fb8f3f9123a6428875bbe63b49e42ee69397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f1187cf959d77b60c4506ad50860db4d263a3ec5c50464909798c4f5f649d0`

```dockerfile
```

-	Layers:
	-	`sha256:70542988e68a4f1c5f95cdbb38138b9b2408e2b300f5a99dd2d30926f4d268da`  
		Last Modified: Tue, 18 Nov 2025 06:54:25 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:cf7925494803272669575b769293f708d5084d4656bd9b0bd6a4086dbc5837ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220613957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08ed827579b12c3c097073fae9c6474dd75c4777bc26a85d1044472db8cd6a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 04:19:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 04:19:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c356f9e9c92c891333fb1ae718cd8215415ca2152ac62bfc037b5d3045f73`  
		Last Modified: Tue, 18 Nov 2025 04:20:30 GMT  
		Size: 37.5 MB (37498324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7540b58924232b2bb1574d0d8b1e8e792b566628223cfa20c25ed7987eb2a5`  
		Last Modified: Tue, 18 Nov 2025 04:20:28 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee1e2ebe1daf3426bddce8a256b002bc05a59760884fa8994ce596195c497e`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 155.6 MB (155630520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:184a6022b83f622547a2495a9e796bcce797395c321ac0cedb07ceddb26413a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dec425e6b4e3da0dbb5b06398ba32a1f19354510341b5670411f4e32c4f539`

```dockerfile
```

-	Layers:
	-	`sha256:fe6ca29c93fdd0ab41d450123bb49aaa9219b9def1ab330ad7870ff006b06a08`  
		Last Modified: Tue, 18 Nov 2025 06:54:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05f3c539161d72c4a364d2cd1ac4bd997582ef4a623b37dd90c444f53e7829a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287457827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e4810f2701354a5cf718dfbe5a0c2fa0e1fb7fab8bdd19574834e5f02ce71e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 03:37:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:37:33 GMT
WORKDIR /root
# Tue, 18 Nov 2025 03:37:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723c2ae08eef5cb2b007a95641953958457fb3609dbec7cbc9f221c7f47368fe`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 42.3 MB (42293339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818d083b0084d331d2dec2a8191772898e5557a265bb0a65f8aa0e63564bd0d1`  
		Last Modified: Tue, 18 Nov 2025 03:38:24 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1f46bc6c5aefeb405bb3a5c492c869e77e8556d5bbefe9b2005976f225b9`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 213.5 MB (213459193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:8be7b70e1b0b7cad4606e8af8d02cff66089a484b78b502df69af450319f7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd364dcaae13777b5e5251bc5b5e5b05f97ca3e0b3fd2e3d2898bc4c3ff6e72a`

```dockerfile
```

-	Layers:
	-	`sha256:d2284a78f7db258f1faaa3a1107c2b8f864af5d22ee7b6054345d72569e663c5`  
		Last Modified: Tue, 18 Nov 2025 06:54:31 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta` - linux; riscv64

```console
$ docker pull dart@sha256:c8bc712f21347aad6d0c3cd39199111ddf4f3f137f3e426e43d5b6d1493f430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233891852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7e6980b4837f225aa4f6cc3b93df3c987671b42740652105262f71ef524029`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:40:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 19 Nov 2025 19:40:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 19:40:39 GMT
WORKDIR /root
# Wed, 19 Nov 2025 19:41:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da213c1ee21f21efd577e634d99a65798e6b0e7656870692da1c2eac8842158`  
		Last Modified: Wed, 19 Nov 2025 19:45:54 GMT  
		Size: 41.6 MB (41560760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96193f29a66f7bd8c31765af875186499b40ca5be5f023e0d948d4ed85acebad`  
		Last Modified: Wed, 19 Nov 2025 19:45:49 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae03974c01b46162db481a23a9a00ce9f9556d82e65b3d1eca98a03262e076d`  
		Last Modified: Wed, 19 Nov 2025 19:51:06 GMT  
		Size: 162.5 MB (162490863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:925a00e6fd4c2ba95b31054816561b23857dfc1ef77f90e32875f2f24c7e79f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a99264debe5bf763c4c469cd7486c94416c4ab90cf4a2ef0e7fe13710378bf`

```dockerfile
```

-	Layers:
	-	`sha256:0b5b69fa5afb5567e074aaee573dfb695d0d597c3ca22938865f5519004a7e9d`  
		Last Modified: Wed, 19 Nov 2025 21:53:30 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-93.2.beta-sdk`

```console
$ docker pull dart@sha256:f65f34c54c2fd57e115449046af8fe8b640a099682f01c7d459ad52e2aca8a10
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

### `dart:3.11.0-93.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:d65d30ccbc3e6b00cbbc83946b9ef517cb5531c0fc4da4a60644b9bc331a989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288383491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbb20cd91f9204144cebebc27862fe183455e029fa759e2474c717099e7d38f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 05:14:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 05:15:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2529f5cef81aeecc09c6572e1e0dbe33c3a22307a223b8ecfaa82bcf21743`  
		Last Modified: Tue, 18 Nov 2025 05:15:37 GMT  
		Size: 42.5 MB (42494038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4313a42c948bf5c26bf4c6050453a911eb2d1fa3107407e270ee2fc2fddfe5d4`  
		Last Modified: Tue, 18 Nov 2025 05:15:34 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0620f90d617bf0c728028c0832e588717bfb0641da01c0676a65d98fc0e15d28`  
		Last Modified: Tue, 18 Nov 2025 06:54:57 GMT  
		Size: 214.2 MB (214239319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:eec7307ccf0361b096c0a867fb42fb8f3f9123a6428875bbe63b49e42ee69397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f1187cf959d77b60c4506ad50860db4d263a3ec5c50464909798c4f5f649d0`

```dockerfile
```

-	Layers:
	-	`sha256:70542988e68a4f1c5f95cdbb38138b9b2408e2b300f5a99dd2d30926f4d268da`  
		Last Modified: Tue, 18 Nov 2025 06:54:25 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:cf7925494803272669575b769293f708d5084d4656bd9b0bd6a4086dbc5837ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220613957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08ed827579b12c3c097073fae9c6474dd75c4777bc26a85d1044472db8cd6a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 04:19:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 04:19:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c356f9e9c92c891333fb1ae718cd8215415ca2152ac62bfc037b5d3045f73`  
		Last Modified: Tue, 18 Nov 2025 04:20:30 GMT  
		Size: 37.5 MB (37498324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7540b58924232b2bb1574d0d8b1e8e792b566628223cfa20c25ed7987eb2a5`  
		Last Modified: Tue, 18 Nov 2025 04:20:28 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee1e2ebe1daf3426bddce8a256b002bc05a59760884fa8994ce596195c497e`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 155.6 MB (155630520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:184a6022b83f622547a2495a9e796bcce797395c321ac0cedb07ceddb26413a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dec425e6b4e3da0dbb5b06398ba32a1f19354510341b5670411f4e32c4f539`

```dockerfile
```

-	Layers:
	-	`sha256:fe6ca29c93fdd0ab41d450123bb49aaa9219b9def1ab330ad7870ff006b06a08`  
		Last Modified: Tue, 18 Nov 2025 06:54:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05f3c539161d72c4a364d2cd1ac4bd997582ef4a623b37dd90c444f53e7829a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287457827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e4810f2701354a5cf718dfbe5a0c2fa0e1fb7fab8bdd19574834e5f02ce71e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 03:37:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:37:33 GMT
WORKDIR /root
# Tue, 18 Nov 2025 03:37:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723c2ae08eef5cb2b007a95641953958457fb3609dbec7cbc9f221c7f47368fe`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 42.3 MB (42293339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818d083b0084d331d2dec2a8191772898e5557a265bb0a65f8aa0e63564bd0d1`  
		Last Modified: Tue, 18 Nov 2025 03:38:24 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1f46bc6c5aefeb405bb3a5c492c869e77e8556d5bbefe9b2005976f225b9`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 213.5 MB (213459193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8be7b70e1b0b7cad4606e8af8d02cff66089a484b78b502df69af450319f7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd364dcaae13777b5e5251bc5b5e5b05f97ca3e0b3fd2e3d2898bc4c3ff6e72a`

```dockerfile
```

-	Layers:
	-	`sha256:d2284a78f7db258f1faaa3a1107c2b8f864af5d22ee7b6054345d72569e663c5`  
		Last Modified: Tue, 18 Nov 2025 06:54:31 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c8bc712f21347aad6d0c3cd39199111ddf4f3f137f3e426e43d5b6d1493f430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233891852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7e6980b4837f225aa4f6cc3b93df3c987671b42740652105262f71ef524029`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:40:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 19 Nov 2025 19:40:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 19:40:39 GMT
WORKDIR /root
# Wed, 19 Nov 2025 19:41:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da213c1ee21f21efd577e634d99a65798e6b0e7656870692da1c2eac8842158`  
		Last Modified: Wed, 19 Nov 2025 19:45:54 GMT  
		Size: 41.6 MB (41560760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96193f29a66f7bd8c31765af875186499b40ca5be5f023e0d948d4ed85acebad`  
		Last Modified: Wed, 19 Nov 2025 19:45:49 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae03974c01b46162db481a23a9a00ce9f9556d82e65b3d1eca98a03262e076d`  
		Last Modified: Wed, 19 Nov 2025 19:51:06 GMT  
		Size: 162.5 MB (162490863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:925a00e6fd4c2ba95b31054816561b23857dfc1ef77f90e32875f2f24c7e79f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a99264debe5bf763c4c469cd7486c94416c4ab90cf4a2ef0e7fe13710378bf`

```dockerfile
```

-	Layers:
	-	`sha256:0b5b69fa5afb5567e074aaee573dfb695d0d597c3ca22938865f5519004a7e9d`  
		Last Modified: Wed, 19 Nov 2025 21:53:30 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:f65f34c54c2fd57e115449046af8fe8b640a099682f01c7d459ad52e2aca8a10
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
$ docker pull dart@sha256:d65d30ccbc3e6b00cbbc83946b9ef517cb5531c0fc4da4a60644b9bc331a989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288383491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbb20cd91f9204144cebebc27862fe183455e029fa759e2474c717099e7d38f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 05:14:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 05:15:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2529f5cef81aeecc09c6572e1e0dbe33c3a22307a223b8ecfaa82bcf21743`  
		Last Modified: Tue, 18 Nov 2025 05:15:37 GMT  
		Size: 42.5 MB (42494038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4313a42c948bf5c26bf4c6050453a911eb2d1fa3107407e270ee2fc2fddfe5d4`  
		Last Modified: Tue, 18 Nov 2025 05:15:34 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0620f90d617bf0c728028c0832e588717bfb0641da01c0676a65d98fc0e15d28`  
		Last Modified: Tue, 18 Nov 2025 06:54:57 GMT  
		Size: 214.2 MB (214239319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:eec7307ccf0361b096c0a867fb42fb8f3f9123a6428875bbe63b49e42ee69397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f1187cf959d77b60c4506ad50860db4d263a3ec5c50464909798c4f5f649d0`

```dockerfile
```

-	Layers:
	-	`sha256:70542988e68a4f1c5f95cdbb38138b9b2408e2b300f5a99dd2d30926f4d268da`  
		Last Modified: Tue, 18 Nov 2025 06:54:25 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:cf7925494803272669575b769293f708d5084d4656bd9b0bd6a4086dbc5837ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220613957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08ed827579b12c3c097073fae9c6474dd75c4777bc26a85d1044472db8cd6a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 04:19:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 04:19:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c356f9e9c92c891333fb1ae718cd8215415ca2152ac62bfc037b5d3045f73`  
		Last Modified: Tue, 18 Nov 2025 04:20:30 GMT  
		Size: 37.5 MB (37498324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7540b58924232b2bb1574d0d8b1e8e792b566628223cfa20c25ed7987eb2a5`  
		Last Modified: Tue, 18 Nov 2025 04:20:28 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee1e2ebe1daf3426bddce8a256b002bc05a59760884fa8994ce596195c497e`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 155.6 MB (155630520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:184a6022b83f622547a2495a9e796bcce797395c321ac0cedb07ceddb26413a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dec425e6b4e3da0dbb5b06398ba32a1f19354510341b5670411f4e32c4f539`

```dockerfile
```

-	Layers:
	-	`sha256:fe6ca29c93fdd0ab41d450123bb49aaa9219b9def1ab330ad7870ff006b06a08`  
		Last Modified: Tue, 18 Nov 2025 06:54:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05f3c539161d72c4a364d2cd1ac4bd997582ef4a623b37dd90c444f53e7829a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287457827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e4810f2701354a5cf718dfbe5a0c2fa0e1fb7fab8bdd19574834e5f02ce71e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 03:37:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:37:33 GMT
WORKDIR /root
# Tue, 18 Nov 2025 03:37:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723c2ae08eef5cb2b007a95641953958457fb3609dbec7cbc9f221c7f47368fe`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 42.3 MB (42293339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818d083b0084d331d2dec2a8191772898e5557a265bb0a65f8aa0e63564bd0d1`  
		Last Modified: Tue, 18 Nov 2025 03:38:24 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1f46bc6c5aefeb405bb3a5c492c869e77e8556d5bbefe9b2005976f225b9`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 213.5 MB (213459193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:8be7b70e1b0b7cad4606e8af8d02cff66089a484b78b502df69af450319f7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd364dcaae13777b5e5251bc5b5e5b05f97ca3e0b3fd2e3d2898bc4c3ff6e72a`

```dockerfile
```

-	Layers:
	-	`sha256:d2284a78f7db258f1faaa3a1107c2b8f864af5d22ee7b6054345d72569e663c5`  
		Last Modified: Tue, 18 Nov 2025 06:54:31 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:c8bc712f21347aad6d0c3cd39199111ddf4f3f137f3e426e43d5b6d1493f430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233891852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7e6980b4837f225aa4f6cc3b93df3c987671b42740652105262f71ef524029`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:40:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 19 Nov 2025 19:40:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 19:40:39 GMT
WORKDIR /root
# Wed, 19 Nov 2025 19:41:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da213c1ee21f21efd577e634d99a65798e6b0e7656870692da1c2eac8842158`  
		Last Modified: Wed, 19 Nov 2025 19:45:54 GMT  
		Size: 41.6 MB (41560760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96193f29a66f7bd8c31765af875186499b40ca5be5f023e0d948d4ed85acebad`  
		Last Modified: Wed, 19 Nov 2025 19:45:49 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae03974c01b46162db481a23a9a00ce9f9556d82e65b3d1eca98a03262e076d`  
		Last Modified: Wed, 19 Nov 2025 19:51:06 GMT  
		Size: 162.5 MB (162490863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:925a00e6fd4c2ba95b31054816561b23857dfc1ef77f90e32875f2f24c7e79f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a99264debe5bf763c4c469cd7486c94416c4ab90cf4a2ef0e7fe13710378bf`

```dockerfile
```

-	Layers:
	-	`sha256:0b5b69fa5afb5567e074aaee573dfb695d0d597c3ca22938865f5519004a7e9d`  
		Last Modified: Wed, 19 Nov 2025 21:53:30 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:f65f34c54c2fd57e115449046af8fe8b640a099682f01c7d459ad52e2aca8a10
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
$ docker pull dart@sha256:d65d30ccbc3e6b00cbbc83946b9ef517cb5531c0fc4da4a60644b9bc331a989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288383491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbb20cd91f9204144cebebc27862fe183455e029fa759e2474c717099e7d38f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 05:14:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 05:15:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2529f5cef81aeecc09c6572e1e0dbe33c3a22307a223b8ecfaa82bcf21743`  
		Last Modified: Tue, 18 Nov 2025 05:15:37 GMT  
		Size: 42.5 MB (42494038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4313a42c948bf5c26bf4c6050453a911eb2d1fa3107407e270ee2fc2fddfe5d4`  
		Last Modified: Tue, 18 Nov 2025 05:15:34 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0620f90d617bf0c728028c0832e588717bfb0641da01c0676a65d98fc0e15d28`  
		Last Modified: Tue, 18 Nov 2025 06:54:57 GMT  
		Size: 214.2 MB (214239319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:eec7307ccf0361b096c0a867fb42fb8f3f9123a6428875bbe63b49e42ee69397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f1187cf959d77b60c4506ad50860db4d263a3ec5c50464909798c4f5f649d0`

```dockerfile
```

-	Layers:
	-	`sha256:70542988e68a4f1c5f95cdbb38138b9b2408e2b300f5a99dd2d30926f4d268da`  
		Last Modified: Tue, 18 Nov 2025 06:54:25 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:cf7925494803272669575b769293f708d5084d4656bd9b0bd6a4086dbc5837ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220613957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08ed827579b12c3c097073fae9c6474dd75c4777bc26a85d1044472db8cd6a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 04:19:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 04:19:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c356f9e9c92c891333fb1ae718cd8215415ca2152ac62bfc037b5d3045f73`  
		Last Modified: Tue, 18 Nov 2025 04:20:30 GMT  
		Size: 37.5 MB (37498324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7540b58924232b2bb1574d0d8b1e8e792b566628223cfa20c25ed7987eb2a5`  
		Last Modified: Tue, 18 Nov 2025 04:20:28 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee1e2ebe1daf3426bddce8a256b002bc05a59760884fa8994ce596195c497e`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 155.6 MB (155630520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:184a6022b83f622547a2495a9e796bcce797395c321ac0cedb07ceddb26413a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dec425e6b4e3da0dbb5b06398ba32a1f19354510341b5670411f4e32c4f539`

```dockerfile
```

-	Layers:
	-	`sha256:fe6ca29c93fdd0ab41d450123bb49aaa9219b9def1ab330ad7870ff006b06a08`  
		Last Modified: Tue, 18 Nov 2025 06:54:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05f3c539161d72c4a364d2cd1ac4bd997582ef4a623b37dd90c444f53e7829a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287457827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e4810f2701354a5cf718dfbe5a0c2fa0e1fb7fab8bdd19574834e5f02ce71e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 03:37:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:37:33 GMT
WORKDIR /root
# Tue, 18 Nov 2025 03:37:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723c2ae08eef5cb2b007a95641953958457fb3609dbec7cbc9f221c7f47368fe`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 42.3 MB (42293339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818d083b0084d331d2dec2a8191772898e5557a265bb0a65f8aa0e63564bd0d1`  
		Last Modified: Tue, 18 Nov 2025 03:38:24 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1f46bc6c5aefeb405bb3a5c492c869e77e8556d5bbefe9b2005976f225b9`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 213.5 MB (213459193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8be7b70e1b0b7cad4606e8af8d02cff66089a484b78b502df69af450319f7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd364dcaae13777b5e5251bc5b5e5b05f97ca3e0b3fd2e3d2898bc4c3ff6e72a`

```dockerfile
```

-	Layers:
	-	`sha256:d2284a78f7db258f1faaa3a1107c2b8f864af5d22ee7b6054345d72569e663c5`  
		Last Modified: Tue, 18 Nov 2025 06:54:31 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c8bc712f21347aad6d0c3cd39199111ddf4f3f137f3e426e43d5b6d1493f430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233891852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7e6980b4837f225aa4f6cc3b93df3c987671b42740652105262f71ef524029`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:40:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 19 Nov 2025 19:40:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 19:40:39 GMT
WORKDIR /root
# Wed, 19 Nov 2025 19:41:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da213c1ee21f21efd577e634d99a65798e6b0e7656870692da1c2eac8842158`  
		Last Modified: Wed, 19 Nov 2025 19:45:54 GMT  
		Size: 41.6 MB (41560760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96193f29a66f7bd8c31765af875186499b40ca5be5f023e0d948d4ed85acebad`  
		Last Modified: Wed, 19 Nov 2025 19:45:49 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae03974c01b46162db481a23a9a00ce9f9556d82e65b3d1eca98a03262e076d`  
		Last Modified: Wed, 19 Nov 2025 19:51:06 GMT  
		Size: 162.5 MB (162490863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:925a00e6fd4c2ba95b31054816561b23857dfc1ef77f90e32875f2f24c7e79f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a99264debe5bf763c4c469cd7486c94416c4ab90cf4a2ef0e7fe13710378bf`

```dockerfile
```

-	Layers:
	-	`sha256:0b5b69fa5afb5567e074aaee573dfb695d0d597c3ca22938865f5519004a7e9d`  
		Last Modified: Wed, 19 Nov 2025 21:53:30 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:9bda6665fb4bbf91bd76ac22de9c794c6fa2729247a0e567ce7ed05e4fa227cf
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
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:8f71d7706ccb4056ae580ad6fd9d7a7443126f8752db4270fbfe4b3c8a84fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a55c968498bc692f7b54ed3f648b4b80efadc09d3a462c199872c0f4bc5ed8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 25 Nov 2025 23:42:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 23:42:03 GMT
WORKDIR /root
# Tue, 25 Nov 2025 23:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4d1582f8362f16308f09df2cc9fda05f7fdaf475e639b7881faa01628c12fd55;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c5aee772e3358f358e386189eb50fefb6c3b3f7c5139e9efe19e76a1f5fa2cad;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9c4a5d4de58dd0dac1f8db0c7c642916f7dcae9d2a7e3332cd3d5e869d10010d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2d52411bfefe30828193ba0a72b49fa53686856abd40a70aa89bf5425ba13b17;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e8f156955db89384e0c3c46f9f9990563aa96f1dec1d5fb80a49522390a8d`  
		Last Modified: Tue, 25 Nov 2025 23:47:17 GMT  
		Size: 41.6 MB (41560780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc918216557c937ff78b87a2de8e120afbb58c17c978291ae94ce0b2d862898`  
		Last Modified: Tue, 25 Nov 2025 23:47:11 GMT  
		Size: 1.6 MB (1567074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3de20ad580a49b4e8226bfaf7d62209795ba058c847c0e5b527df9d0bddc5e`  
		Last Modified: Tue, 25 Nov 2025 23:51:38 GMT  
		Size: 161.6 MB (161563090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:fc9c402e66f35f654d7079143d9fc20851b2db599b85c39ef6f430516a5ea051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae261d8639b433165568f3a39514dc827f2bd765aca5fa8e637d5a9ebb642fa`

```dockerfile
```

-	Layers:
	-	`sha256:97a344939c3fa005bdd8353af064bcec8ee4c24bf6a2cde4e1216de059ad518d`  
		Last Modified: Wed, 26 Nov 2025 00:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:9bda6665fb4bbf91bd76ac22de9c794c6fa2729247a0e567ce7ed05e4fa227cf
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
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8f71d7706ccb4056ae580ad6fd9d7a7443126f8752db4270fbfe4b3c8a84fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a55c968498bc692f7b54ed3f648b4b80efadc09d3a462c199872c0f4bc5ed8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 25 Nov 2025 23:42:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 23:42:03 GMT
WORKDIR /root
# Tue, 25 Nov 2025 23:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4d1582f8362f16308f09df2cc9fda05f7fdaf475e639b7881faa01628c12fd55;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c5aee772e3358f358e386189eb50fefb6c3b3f7c5139e9efe19e76a1f5fa2cad;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9c4a5d4de58dd0dac1f8db0c7c642916f7dcae9d2a7e3332cd3d5e869d10010d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2d52411bfefe30828193ba0a72b49fa53686856abd40a70aa89bf5425ba13b17;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e8f156955db89384e0c3c46f9f9990563aa96f1dec1d5fb80a49522390a8d`  
		Last Modified: Tue, 25 Nov 2025 23:47:17 GMT  
		Size: 41.6 MB (41560780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc918216557c937ff78b87a2de8e120afbb58c17c978291ae94ce0b2d862898`  
		Last Modified: Tue, 25 Nov 2025 23:47:11 GMT  
		Size: 1.6 MB (1567074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3de20ad580a49b4e8226bfaf7d62209795ba058c847c0e5b527df9d0bddc5e`  
		Last Modified: Tue, 25 Nov 2025 23:51:38 GMT  
		Size: 161.6 MB (161563090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fc9c402e66f35f654d7079143d9fc20851b2db599b85c39ef6f430516a5ea051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae261d8639b433165568f3a39514dc827f2bd765aca5fa8e637d5a9ebb642fa`

```dockerfile
```

-	Layers:
	-	`sha256:97a344939c3fa005bdd8353af064bcec8ee4c24bf6a2cde4e1216de059ad518d`  
		Last Modified: Wed, 26 Nov 2025 00:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:9bda6665fb4bbf91bd76ac22de9c794c6fa2729247a0e567ce7ed05e4fa227cf
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
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:8f71d7706ccb4056ae580ad6fd9d7a7443126f8752db4270fbfe4b3c8a84fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a55c968498bc692f7b54ed3f648b4b80efadc09d3a462c199872c0f4bc5ed8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 25 Nov 2025 23:42:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 23:42:03 GMT
WORKDIR /root
# Tue, 25 Nov 2025 23:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4d1582f8362f16308f09df2cc9fda05f7fdaf475e639b7881faa01628c12fd55;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c5aee772e3358f358e386189eb50fefb6c3b3f7c5139e9efe19e76a1f5fa2cad;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9c4a5d4de58dd0dac1f8db0c7c642916f7dcae9d2a7e3332cd3d5e869d10010d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2d52411bfefe30828193ba0a72b49fa53686856abd40a70aa89bf5425ba13b17;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e8f156955db89384e0c3c46f9f9990563aa96f1dec1d5fb80a49522390a8d`  
		Last Modified: Tue, 25 Nov 2025 23:47:17 GMT  
		Size: 41.6 MB (41560780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc918216557c937ff78b87a2de8e120afbb58c17c978291ae94ce0b2d862898`  
		Last Modified: Tue, 25 Nov 2025 23:47:11 GMT  
		Size: 1.6 MB (1567074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3de20ad580a49b4e8226bfaf7d62209795ba058c847c0e5b527df9d0bddc5e`  
		Last Modified: Tue, 25 Nov 2025 23:51:38 GMT  
		Size: 161.6 MB (161563090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:fc9c402e66f35f654d7079143d9fc20851b2db599b85c39ef6f430516a5ea051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae261d8639b433165568f3a39514dc827f2bd765aca5fa8e637d5a9ebb642fa`

```dockerfile
```

-	Layers:
	-	`sha256:97a344939c3fa005bdd8353af064bcec8ee4c24bf6a2cde4e1216de059ad518d`  
		Last Modified: Wed, 26 Nov 2025 00:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:9bda6665fb4bbf91bd76ac22de9c794c6fa2729247a0e567ce7ed05e4fa227cf
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
$ docker pull dart@sha256:4ce169c6f41a33596a6d6c9fd6ed7825ee8d891948e2189f46db811cc8a12457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b86f401068f280b62199ca2fb11d3917908f8a02b803526d5c2fcf3b1e05c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:08:48 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:08:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:08:48 GMT
WORKDIR /root
# Tue, 02 Dec 2025 18:09:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004ad56be72499880ce677eee159fba4c910008210a08d4d3e6209d8d58ed69`  
		Last Modified: Tue, 02 Dec 2025 18:09:59 GMT  
		Size: 42.5 MB (42494059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea3e7c9b736b175f96c4215033737a5f5d702bca135f8377eefddb4f8875db`  
		Last Modified: Tue, 02 Dec 2025 18:09:54 GMT  
		Size: 1.9 MB (1873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a6d02af47f61c66f559abc4cfed3d96e75da28334f9333ec0cf3a269324b6`  
		Last Modified: Tue, 02 Dec 2025 18:54:24 GMT  
		Size: 213.1 MB (213123754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ea23e715e262b8a7dfdc7e5ac9641b8a9ef14a4076ef4cc1d67cc9052826ce50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a80b58c9a0e971165a622a306aad2e11399241622e62fe5a554a721d088aae`

```dockerfile
```

-	Layers:
	-	`sha256:da65be952fb26184c566c96b57b4ad65f99e000d1ff5d57aeb765943549d0c12`  
		Last Modified: Tue, 02 Dec 2025 18:53:20 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2261c04ab375a755bd85c8db99d694b0cb368be45909a1c93f707c2285053930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33a7e61f42f99086633bf5ff2c0b2f9ed8dbcb2456c40242a2962474d4d578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:55 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa8e9409eecd4a37f06721d3be4a6c48cdb952d5642243878c05de1ee00dd9`  
		Last Modified: Tue, 02 Dec 2025 18:53:57 GMT  
		Size: 37.5 MB (37498359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0872289df9c7beef9620e489b4dc7cc56cf1cc0d40126cbe8f5d599392daa30`  
		Last Modified: Tue, 02 Dec 2025 18:15:21 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbb273187859e4052e56ecff3cb00ffe2560d9440bf940de2bcf920cff0b450`  
		Last Modified: Tue, 02 Dec 2025 18:54:06 GMT  
		Size: 154.9 MB (154925372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a9dcf0f3a5de15f339be49f8ef0e003f99f503fc77db7c1339e8474b50c2129c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90819a6167a18a6c647a31a416dd2f6d3afc6cddd24dad85e3c3ed6da51a480b`

```dockerfile
```

-	Layers:
	-	`sha256:0f5eb18b8f0be4e8266afd0d329caf8eab2abf8eab1e369fbd6be6788c557ece`  
		Last Modified: Tue, 02 Dec 2025 18:53:32 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4e43a0df8ea7443267fe78e2970f531b481c9bf4c671241cf284910203f555cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9977dc828dbad4b689eb7289703922a3845f28d1b0604a611e65290649cba3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 17:53:58 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 17:53:58 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:53:58 GMT
WORKDIR /root
# Tue, 02 Dec 2025 17:54:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=db95cd3bbdb604ac1d2b8fc7a1524c909a67dfd44bff1fb4a075223b7d829e0f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c9c63650ef6255cf979ae3382b25fe3c158be7d28522f91bf4a43ff099425bb3;             SDK_ARCH="arm";;         arm64)             DART_SHA256=478986a2089cbfc6ac169bad356f90b13e291cfa4728e39fd45ac357ef7fa7df;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=251b76d37f27ffa6b8dbfe7c4832cc576644171a4af5526ddefcc08fcb5a95d0;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6709004cbe58965c4cd887501657a172b9474fe3412a127fd95592a332056e`  
		Last Modified: Tue, 02 Dec 2025 17:55:21 GMT  
		Size: 42.3 MB (42293353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9814a75c13eabb3da3100586b3e0ce6a4e69e05cdf3026e80c196b0b2dfc4709`  
		Last Modified: Tue, 02 Dec 2025 17:55:17 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40409564a940a75e44c6cc1a3c6775c321ec28d10c2853087ed3710d2ad37bd1`  
		Last Modified: Tue, 02 Dec 2025 18:43:52 GMT  
		Size: 212.4 MB (212350876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0e6dbc7c9e3975e7d58fd7cf6e5d58976b5fb9db5c5513d18a0167de3120c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863ef6765e301104a7f70bd3b8273d544a6ee1a19cdb1248be6f5782a38a94a`

```dockerfile
```

-	Layers:
	-	`sha256:1931cdd9d085c2bca6e4a5d44fb0277bd16be47c362a2d4151f4257bae19941b`  
		Last Modified: Tue, 02 Dec 2025 18:53:35 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8f71d7706ccb4056ae580ad6fd9d7a7443126f8752db4270fbfe4b3c8a84fa46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a55c968498bc692f7b54ed3f648b4b80efadc09d3a462c199872c0f4bc5ed8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 25 Nov 2025 23:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 25 Nov 2025 23:42:03 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 25 Nov 2025 23:42:03 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Nov 2025 23:42:03 GMT
WORKDIR /root
# Tue, 25 Nov 2025 23:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4d1582f8362f16308f09df2cc9fda05f7fdaf475e639b7881faa01628c12fd55;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c5aee772e3358f358e386189eb50fefb6c3b3f7c5139e9efe19e76a1f5fa2cad;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9c4a5d4de58dd0dac1f8db0c7c642916f7dcae9d2a7e3332cd3d5e869d10010d;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2d52411bfefe30828193ba0a72b49fa53686856abd40a70aa89bf5425ba13b17;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701e8f156955db89384e0c3c46f9f9990563aa96f1dec1d5fb80a49522390a8d`  
		Last Modified: Tue, 25 Nov 2025 23:47:17 GMT  
		Size: 41.6 MB (41560780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc918216557c937ff78b87a2de8e120afbb58c17c978291ae94ce0b2d862898`  
		Last Modified: Tue, 25 Nov 2025 23:47:11 GMT  
		Size: 1.6 MB (1567074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3de20ad580a49b4e8226bfaf7d62209795ba058c847c0e5b527df9d0bddc5e`  
		Last Modified: Tue, 25 Nov 2025 23:51:38 GMT  
		Size: 161.6 MB (161563090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fc9c402e66f35f654d7079143d9fc20851b2db599b85c39ef6f430516a5ea051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae261d8639b433165568f3a39514dc827f2bd765aca5fa8e637d5a9ebb642fa`

```dockerfile
```

-	Layers:
	-	`sha256:97a344939c3fa005bdd8353af064bcec8ee4c24bf6a2cde4e1216de059ad518d`  
		Last Modified: Wed, 26 Nov 2025 00:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
