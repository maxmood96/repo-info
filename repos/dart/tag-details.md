<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.11`](#dart311)
-	[`dart:3.11-sdk`](#dart311-sdk)
-	[`dart:3.11.0`](#dart3110)
-	[`dart:3.11.0-sdk`](#dart3110-sdk)
-	[`dart:3.12.0-113.1.beta`](#dart3120-1131beta)
-	[`dart:3.12.0-113.1.beta-sdk`](#dart3120-1131beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11-sdk`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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

### `dart:3.11.0` - linux; amd64

```console
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-sdk`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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

### `dart:3.11.0-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12.0-113.1.beta`

```console
$ docker pull dart@sha256:5a4ba925adb86aacc122912397cd7a387e680facd4e19b19d21acc9db422d8fa
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

### `dart:3.12.0-113.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:933feb1cd3fc9a571d34657439437e4b7adb698283f2f3373d366e9919d67019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309321074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ff85ab8053a1674249ee4c0a656d187831b849b11e223229ede29142f57287`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:02 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:02 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:25:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e0eecdb696cf91fb66d35b712e80fe5b8e7f14348d53643aa8f8a86353fcc`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 42.5 MB (42494484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acfca8aea94973917e72db7c6ab240deded3bf4677d34e247f1670144f33c6e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 1.9 MB (1870169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128548a4222d90a19929445a0bfedc2a38183b7f434f03b1d0d9bf43c6e8dda0`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 235.2 MB (235177793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:215bc4f77b68ab945362c2d4de7f4e3d5efd2ae6dde67c75fe34b3db22d57955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e721384d2358aa87d58749f361e6cf227c09052777a5d1d0498955a809bbd9c4`

```dockerfile
```

-	Layers:
	-	`sha256:b9a374cfd607dba2ede086bd5bd879b47440c08a31f2643cdc43472c1e27ef6d`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:ca346f06da5811f54b82befaae740ddcc6778d916d5b1159c358d201e20f0392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224083078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67aceed08cc994a405b6b093fab37865fde113ffa47fd8f3a3d96159e1446dc8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3988900bede93d4dd35593acaceb23bd229998424b048221869299e6422c04`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 159.1 MB (159098587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:a0338ac31acdb4256f020328124f8150c77cca66d377c01becfef31bb39fe565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045a0d0c8ded42990e00ce7760cde66618119b35c1b36c2401ec08ce2c8e7a9`

```dockerfile
```

-	Layers:
	-	`sha256:bd373a5498623a06601a763cc0344c2fb688859d80e8a7864371c437c986c840`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4c3c1f878995a188501a4a40f67a7a020ee47b221636a9aa9d05bcb6fb3682fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307708641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2875eb51a7972356def6f0669f36ea5f8b2579f6adc06c2e9e45a09d0d6e63e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:48 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:48 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:25:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef49be3087e8b63e1c987e57dcf6b0f55bb6dd0f98999667548f78680dc0c13`  
		Last Modified: Mon, 09 Feb 2026 19:25:33 GMT  
		Size: 42.3 MB (42293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b7b146673298f288dcaffa8a9fd990d407083ab1e20123281383f366a89dc`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 1.6 MB (1564511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6682cb1664a311aec6029923884f8ee3b18379ffd93364083493943e046375`  
		Last Modified: Mon, 09 Feb 2026 19:25:37 GMT  
		Size: 233.7 MB (233710233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:d8b38da5e3cb2905024958ecdca1ab8b54f2cd3269e22963a1141c9faf923edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e64b850429b5684a57b83c175b0e245809d8cfa96b1a8ba68806194a3f550d`

```dockerfile
```

-	Layers:
	-	`sha256:27efea74cbf1f7254c423436753eef2dd132c90b4ba020e55b134ca861111510`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.1.beta` - linux; riscv64

```console
$ docker pull dart@sha256:bd3c0206e676ff07f6549a95d93fadaea1be844e14ce2d829bda51ad8cf6f021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253070009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a800f76e464b3b694c13eb83117adb36249bd56cde27a708021c1d54dde4970`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:33:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:33:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:33:57 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:33:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:33:57 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:34:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b664aa1f102f914b66bbaf1d6fa623791b5ce2b8e17bf02fd490abc0e37296`  
		Last Modified: Mon, 09 Feb 2026 19:39:10 GMT  
		Size: 41.6 MB (41561500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9342222f0c3b0cc1297463bc9e085a4a9d09d144fd2932db7866d99dafcf61`  
		Last Modified: Mon, 09 Feb 2026 19:38:58 GMT  
		Size: 1.6 MB (1564661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04997eb84863b500c81b9d556fc1d2a757de400aac1a4d8049c79db783db6aea`  
		Last Modified: Mon, 09 Feb 2026 19:39:32 GMT  
		Size: 181.7 MB (181667427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:c7d01ce6077df1ff6da9179bb4b1a45aab6ea423d036a44216d0bbd4e71adf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9da5043a2dbb6d193ba01f26a11e1898b20b2181a21e6efbd973b51dc1576e0`

```dockerfile
```

-	Layers:
	-	`sha256:aa3c6f7f324f7f07a275547c1febbe4c839ffac743aa50b5778ccfdc09bfde87`  
		Last Modified: Mon, 09 Feb 2026 19:38:58 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12.0-113.1.beta-sdk`

```console
$ docker pull dart@sha256:5a4ba925adb86aacc122912397cd7a387e680facd4e19b19d21acc9db422d8fa
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

### `dart:3.12.0-113.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:933feb1cd3fc9a571d34657439437e4b7adb698283f2f3373d366e9919d67019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309321074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ff85ab8053a1674249ee4c0a656d187831b849b11e223229ede29142f57287`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:02 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:02 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:25:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e0eecdb696cf91fb66d35b712e80fe5b8e7f14348d53643aa8f8a86353fcc`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 42.5 MB (42494484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acfca8aea94973917e72db7c6ab240deded3bf4677d34e247f1670144f33c6e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 1.9 MB (1870169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128548a4222d90a19929445a0bfedc2a38183b7f434f03b1d0d9bf43c6e8dda0`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 235.2 MB (235177793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:215bc4f77b68ab945362c2d4de7f4e3d5efd2ae6dde67c75fe34b3db22d57955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e721384d2358aa87d58749f361e6cf227c09052777a5d1d0498955a809bbd9c4`

```dockerfile
```

-	Layers:
	-	`sha256:b9a374cfd607dba2ede086bd5bd879b47440c08a31f2643cdc43472c1e27ef6d`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:ca346f06da5811f54b82befaae740ddcc6778d916d5b1159c358d201e20f0392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224083078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67aceed08cc994a405b6b093fab37865fde113ffa47fd8f3a3d96159e1446dc8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3988900bede93d4dd35593acaceb23bd229998424b048221869299e6422c04`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 159.1 MB (159098587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a0338ac31acdb4256f020328124f8150c77cca66d377c01becfef31bb39fe565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045a0d0c8ded42990e00ce7760cde66618119b35c1b36c2401ec08ce2c8e7a9`

```dockerfile
```

-	Layers:
	-	`sha256:bd373a5498623a06601a763cc0344c2fb688859d80e8a7864371c437c986c840`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4c3c1f878995a188501a4a40f67a7a020ee47b221636a9aa9d05bcb6fb3682fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307708641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2875eb51a7972356def6f0669f36ea5f8b2579f6adc06c2e9e45a09d0d6e63e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:48 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:48 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:25:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef49be3087e8b63e1c987e57dcf6b0f55bb6dd0f98999667548f78680dc0c13`  
		Last Modified: Mon, 09 Feb 2026 19:25:33 GMT  
		Size: 42.3 MB (42293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b7b146673298f288dcaffa8a9fd990d407083ab1e20123281383f366a89dc`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 1.6 MB (1564511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6682cb1664a311aec6029923884f8ee3b18379ffd93364083493943e046375`  
		Last Modified: Mon, 09 Feb 2026 19:25:37 GMT  
		Size: 233.7 MB (233710233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d8b38da5e3cb2905024958ecdca1ab8b54f2cd3269e22963a1141c9faf923edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e64b850429b5684a57b83c175b0e245809d8cfa96b1a8ba68806194a3f550d`

```dockerfile
```

-	Layers:
	-	`sha256:27efea74cbf1f7254c423436753eef2dd132c90b4ba020e55b134ca861111510`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.1.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:bd3c0206e676ff07f6549a95d93fadaea1be844e14ce2d829bda51ad8cf6f021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253070009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a800f76e464b3b694c13eb83117adb36249bd56cde27a708021c1d54dde4970`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:33:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:33:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:33:57 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:33:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:33:57 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:34:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b664aa1f102f914b66bbaf1d6fa623791b5ce2b8e17bf02fd490abc0e37296`  
		Last Modified: Mon, 09 Feb 2026 19:39:10 GMT  
		Size: 41.6 MB (41561500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9342222f0c3b0cc1297463bc9e085a4a9d09d144fd2932db7866d99dafcf61`  
		Last Modified: Mon, 09 Feb 2026 19:38:58 GMT  
		Size: 1.6 MB (1564661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04997eb84863b500c81b9d556fc1d2a757de400aac1a4d8049c79db783db6aea`  
		Last Modified: Mon, 09 Feb 2026 19:39:32 GMT  
		Size: 181.7 MB (181667427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c7d01ce6077df1ff6da9179bb4b1a45aab6ea423d036a44216d0bbd4e71adf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9da5043a2dbb6d193ba01f26a11e1898b20b2181a21e6efbd973b51dc1576e0`

```dockerfile
```

-	Layers:
	-	`sha256:aa3c6f7f324f7f07a275547c1febbe4c839ffac743aa50b5778ccfdc09bfde87`  
		Last Modified: Mon, 09 Feb 2026 19:38:58 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:5a4ba925adb86aacc122912397cd7a387e680facd4e19b19d21acc9db422d8fa
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
$ docker pull dart@sha256:933feb1cd3fc9a571d34657439437e4b7adb698283f2f3373d366e9919d67019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309321074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ff85ab8053a1674249ee4c0a656d187831b849b11e223229ede29142f57287`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:02 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:02 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:25:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e0eecdb696cf91fb66d35b712e80fe5b8e7f14348d53643aa8f8a86353fcc`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 42.5 MB (42494484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acfca8aea94973917e72db7c6ab240deded3bf4677d34e247f1670144f33c6e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 1.9 MB (1870169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128548a4222d90a19929445a0bfedc2a38183b7f434f03b1d0d9bf43c6e8dda0`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 235.2 MB (235177793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:215bc4f77b68ab945362c2d4de7f4e3d5efd2ae6dde67c75fe34b3db22d57955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e721384d2358aa87d58749f361e6cf227c09052777a5d1d0498955a809bbd9c4`

```dockerfile
```

-	Layers:
	-	`sha256:b9a374cfd607dba2ede086bd5bd879b47440c08a31f2643cdc43472c1e27ef6d`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:ca346f06da5811f54b82befaae740ddcc6778d916d5b1159c358d201e20f0392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224083078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67aceed08cc994a405b6b093fab37865fde113ffa47fd8f3a3d96159e1446dc8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3988900bede93d4dd35593acaceb23bd229998424b048221869299e6422c04`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 159.1 MB (159098587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:a0338ac31acdb4256f020328124f8150c77cca66d377c01becfef31bb39fe565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045a0d0c8ded42990e00ce7760cde66618119b35c1b36c2401ec08ce2c8e7a9`

```dockerfile
```

-	Layers:
	-	`sha256:bd373a5498623a06601a763cc0344c2fb688859d80e8a7864371c437c986c840`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4c3c1f878995a188501a4a40f67a7a020ee47b221636a9aa9d05bcb6fb3682fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307708641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2875eb51a7972356def6f0669f36ea5f8b2579f6adc06c2e9e45a09d0d6e63e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:48 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:48 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:25:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef49be3087e8b63e1c987e57dcf6b0f55bb6dd0f98999667548f78680dc0c13`  
		Last Modified: Mon, 09 Feb 2026 19:25:33 GMT  
		Size: 42.3 MB (42293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b7b146673298f288dcaffa8a9fd990d407083ab1e20123281383f366a89dc`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 1.6 MB (1564511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6682cb1664a311aec6029923884f8ee3b18379ffd93364083493943e046375`  
		Last Modified: Mon, 09 Feb 2026 19:25:37 GMT  
		Size: 233.7 MB (233710233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:d8b38da5e3cb2905024958ecdca1ab8b54f2cd3269e22963a1141c9faf923edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e64b850429b5684a57b83c175b0e245809d8cfa96b1a8ba68806194a3f550d`

```dockerfile
```

-	Layers:
	-	`sha256:27efea74cbf1f7254c423436753eef2dd132c90b4ba020e55b134ca861111510`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:bd3c0206e676ff07f6549a95d93fadaea1be844e14ce2d829bda51ad8cf6f021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253070009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a800f76e464b3b694c13eb83117adb36249bd56cde27a708021c1d54dde4970`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:33:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:33:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:33:57 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:33:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:33:57 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:34:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b664aa1f102f914b66bbaf1d6fa623791b5ce2b8e17bf02fd490abc0e37296`  
		Last Modified: Mon, 09 Feb 2026 19:39:10 GMT  
		Size: 41.6 MB (41561500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9342222f0c3b0cc1297463bc9e085a4a9d09d144fd2932db7866d99dafcf61`  
		Last Modified: Mon, 09 Feb 2026 19:38:58 GMT  
		Size: 1.6 MB (1564661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04997eb84863b500c81b9d556fc1d2a757de400aac1a4d8049c79db783db6aea`  
		Last Modified: Mon, 09 Feb 2026 19:39:32 GMT  
		Size: 181.7 MB (181667427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:c7d01ce6077df1ff6da9179bb4b1a45aab6ea423d036a44216d0bbd4e71adf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9da5043a2dbb6d193ba01f26a11e1898b20b2181a21e6efbd973b51dc1576e0`

```dockerfile
```

-	Layers:
	-	`sha256:aa3c6f7f324f7f07a275547c1febbe4c839ffac743aa50b5778ccfdc09bfde87`  
		Last Modified: Mon, 09 Feb 2026 19:38:58 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:5a4ba925adb86aacc122912397cd7a387e680facd4e19b19d21acc9db422d8fa
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
$ docker pull dart@sha256:933feb1cd3fc9a571d34657439437e4b7adb698283f2f3373d366e9919d67019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309321074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ff85ab8053a1674249ee4c0a656d187831b849b11e223229ede29142f57287`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:02 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:02 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:25:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e0eecdb696cf91fb66d35b712e80fe5b8e7f14348d53643aa8f8a86353fcc`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 42.5 MB (42494484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acfca8aea94973917e72db7c6ab240deded3bf4677d34e247f1670144f33c6e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 1.9 MB (1870169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128548a4222d90a19929445a0bfedc2a38183b7f434f03b1d0d9bf43c6e8dda0`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 235.2 MB (235177793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:215bc4f77b68ab945362c2d4de7f4e3d5efd2ae6dde67c75fe34b3db22d57955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e721384d2358aa87d58749f361e6cf227c09052777a5d1d0498955a809bbd9c4`

```dockerfile
```

-	Layers:
	-	`sha256:b9a374cfd607dba2ede086bd5bd879b47440c08a31f2643cdc43472c1e27ef6d`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:ca346f06da5811f54b82befaae740ddcc6778d916d5b1159c358d201e20f0392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224083078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67aceed08cc994a405b6b093fab37865fde113ffa47fd8f3a3d96159e1446dc8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3988900bede93d4dd35593acaceb23bd229998424b048221869299e6422c04`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 159.1 MB (159098587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a0338ac31acdb4256f020328124f8150c77cca66d377c01becfef31bb39fe565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045a0d0c8ded42990e00ce7760cde66618119b35c1b36c2401ec08ce2c8e7a9`

```dockerfile
```

-	Layers:
	-	`sha256:bd373a5498623a06601a763cc0344c2fb688859d80e8a7864371c437c986c840`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4c3c1f878995a188501a4a40f67a7a020ee47b221636a9aa9d05bcb6fb3682fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307708641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2875eb51a7972356def6f0669f36ea5f8b2579f6adc06c2e9e45a09d0d6e63e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:48 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:48 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:48 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:25:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef49be3087e8b63e1c987e57dcf6b0f55bb6dd0f98999667548f78680dc0c13`  
		Last Modified: Mon, 09 Feb 2026 19:25:33 GMT  
		Size: 42.3 MB (42293801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b7b146673298f288dcaffa8a9fd990d407083ab1e20123281383f366a89dc`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 1.6 MB (1564511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6682cb1664a311aec6029923884f8ee3b18379ffd93364083493943e046375`  
		Last Modified: Mon, 09 Feb 2026 19:25:37 GMT  
		Size: 233.7 MB (233710233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d8b38da5e3cb2905024958ecdca1ab8b54f2cd3269e22963a1141c9faf923edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e64b850429b5684a57b83c175b0e245809d8cfa96b1a8ba68806194a3f550d`

```dockerfile
```

-	Layers:
	-	`sha256:27efea74cbf1f7254c423436753eef2dd132c90b4ba020e55b134ca861111510`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 19.1 KB (19056 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:bd3c0206e676ff07f6549a95d93fadaea1be844e14ce2d829bda51ad8cf6f021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253070009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a800f76e464b3b694c13eb83117adb36249bd56cde27a708021c1d54dde4970`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:33:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:33:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:33:57 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:33:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:33:57 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:34:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1af09b9c663079f5bdd76388d375e3051cfcadab625cd8705fde5970eb0b73e6;             SDK_ARCH="x64";;         armhf)             DART_SHA256=514a2c3363b8cef13206d98f191eefadafa3876d06c625221071b1a3f3b98157;             SDK_ARCH="arm";;         arm64)             DART_SHA256=13926be703ee660f53eacafecc3d46034aed73bc65a2d0265e2e7b67f41364b7;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=4e21c75c2e1e6e3cb6878f154d257e96e96490acb257bb5d77af5d3709fb97f7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b664aa1f102f914b66bbaf1d6fa623791b5ce2b8e17bf02fd490abc0e37296`  
		Last Modified: Mon, 09 Feb 2026 19:39:10 GMT  
		Size: 41.6 MB (41561500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9342222f0c3b0cc1297463bc9e085a4a9d09d144fd2932db7866d99dafcf61`  
		Last Modified: Mon, 09 Feb 2026 19:38:58 GMT  
		Size: 1.6 MB (1564661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04997eb84863b500c81b9d556fc1d2a757de400aac1a4d8049c79db783db6aea`  
		Last Modified: Mon, 09 Feb 2026 19:39:32 GMT  
		Size: 181.7 MB (181667427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c7d01ce6077df1ff6da9179bb4b1a45aab6ea423d036a44216d0bbd4e71adf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9da5043a2dbb6d193ba01f26a11e1898b20b2181a21e6efbd973b51dc1576e0`

```dockerfile
```

-	Layers:
	-	`sha256:aa3c6f7f324f7f07a275547c1febbe4c839ffac743aa50b5778ccfdc09bfde87`  
		Last Modified: Mon, 09 Feb 2026 19:38:58 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:193a4d037dcef48b56f2a3544f053f4ef3b5e9865953f8f5ff2a284554da567a
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
$ docker pull dart@sha256:1ca9cc486fbaf5eee88643c972028d9e5508b753910a97f4fb6ed2f18bdc9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307093659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d844a585395f9d6bec7ece33833377a4a6a3a5e7ce15d9b9c4bc4fc4b372d10`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:41 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:41 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85903e42e1352063f0c7ad6a2f718d6acfe002815f4b96b3c6bad91c78bd19`  
		Last Modified: Mon, 09 Feb 2026 19:25:22 GMT  
		Size: 42.5 MB (42494555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9293763496c2c0b21d401a8a71f17846c703e5496626da5870dd4b8c0bcf2b34`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 1.9 MB (1870172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a833740f3d0ec749f184182fa091049f1277027365648dae6da002da0e2750`  
		Last Modified: Mon, 09 Feb 2026 19:25:30 GMT  
		Size: 233.0 MB (232950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1563ac0eaeaba478b2bd8d55d6e5baa35aa55daf64e21290e49553f6e5a7c0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23baa865b9cc35fe517ac2784725619795032da2960d01659dd6c234b6f6a9`

```dockerfile
```

-	Layers:
	-	`sha256:4c0d4dcbfa7d746880e06a8f14e77a144a9cf517296a57d701552a2fe50327cf`  
		Last Modified: Mon, 09 Feb 2026 19:25:18 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6253ebcead9145ee29a79ba75a18eac46af91b870381f2038017a6cf9469c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222905944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b2e0920c14baab7743d741672cfbb4e1c1a22ef7615dc958b62a61ebebdbcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:07 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9f6b52daa6f897da9b73a23011b558953657a6841fe9ef5ad5ddf4e27eac`  
		Last Modified: Mon, 09 Feb 2026 19:24:40 GMT  
		Size: 37.5 MB (37497558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a36a97e768cf9d933800881d66e853b6440e386a12d4cde89b60880bd720068`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d3d3d5698a0d3607a63cdb5296a9eb6d074413da3e4f89bed57970509fdcdf`  
		Last Modified: Mon, 09 Feb 2026 19:24:42 GMT  
		Size: 157.9 MB (157921453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8bf196739404fc657e26721aa4a7a37a4f84a6330991757753d6a7e8f067faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6773b1b926b1c5675403ebb8ab1fe4efffdb1841f72b45c1a7dfec4cefbdd48`

```dockerfile
```

-	Layers:
	-	`sha256:c7a8b2ec3dca4cb0be3c62eee7375c24958fdd909b5e94ea9248f9bef4121a56`  
		Last Modified: Mon, 09 Feb 2026 19:24:38 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4b027aa3345aed156b651b5e1eddabe92a6500cd8e2e9ae160a2a28173394137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305450165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33e493cdcb37a1455f653e7d4fdcf00ffba059dd5f1c648ef40dd5bc55e3d85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:24:47 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:24:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:24:47 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:24:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369574876e98fc4896be67231afa547d1dc7e2be3942102d3617ab968d9cf4b`  
		Last Modified: Mon, 09 Feb 2026 19:25:31 GMT  
		Size: 42.3 MB (42293789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e833173bd6279b98267d2a5d58cb8c91c1670f041abe87ccdfbb89d3f50fd065`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 1.6 MB (1564519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ede1af4901b158ddc212c1ebee8593a7f2a09c8fbfb1f252b714b71c0035d`  
		Last Modified: Mon, 09 Feb 2026 19:25:34 GMT  
		Size: 231.5 MB (231451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4249e232d84b60e63e15fdda848fa488d0b2cc4ed89cdbc03af7b8a8f58f839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db715847133c25bbabaff7a8945c2afadf4f70892aae66a9f1c4ac4771a5b07`

```dockerfile
```

-	Layers:
	-	`sha256:31611401353449dfeb9e49e2e13a204c9151573c924cabd4e33b84660691e35f`  
		Last Modified: Mon, 09 Feb 2026 19:25:29 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c490a752c94e147e655cc4d64955f7bd3ed9c481713db9d3d23a1a288025e98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251887664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bef7d9cc57e853f747c3555e274c35fc1879f82df4396865f6f99dac0881f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 19:25:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 09 Feb 2026 19:25:39 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 09 Feb 2026 19:25:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 19:25:39 GMT
WORKDIR /root
# Mon, 09 Feb 2026 19:26:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f31729b567be318c7cc23bdafe6b9a997fa7ddbf829df5016f066227b6aa0c99;             SDK_ARCH="x64";;         armhf)             DART_SHA256=544e6137a072d73451148db128bfeb7fb73992615537b81d641b3396983c6884;             SDK_ARCH="arm";;         arm64)             DART_SHA256=76bfef5c809c082177df6c51bbf4800d8d4d755f2e96fb75162bf8d2b032ef83;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=07b8733bf47425e4b1111c63b402966cdfbb08d25b1b44f2970250acc5bc4628;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c186371176c0f3433b6f9a7a821a988b2c6c3256e51b184682e02c89f6264cef`  
		Last Modified: Mon, 09 Feb 2026 19:30:46 GMT  
		Size: 41.6 MB (41561542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08e71015c3cbce09d9f06b2e5ff630a0d26ab730398f310849ee32a32f0e486`  
		Last Modified: Mon, 09 Feb 2026 19:30:35 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ccc751654c2adbc783f062ced32348e13d5e1ed1664395df13b602cedc63a`  
		Last Modified: Mon, 09 Feb 2026 19:31:06 GMT  
		Size: 180.5 MB (180485038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7f65e3e16ef91ea813cd971eb320d79afa3896aa205b8947f75091f7d6d8b610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f7aa8fb10e002e7a7526e48161e308e3bb6e2c3e4a5f8ec699cdbfadda6274`

```dockerfile
```

-	Layers:
	-	`sha256:f2c021860e830724ab1063161aed0eaac968dfbb159635e1fde71ab59df3b0b5`  
		Last Modified: Mon, 09 Feb 2026 19:30:34 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
