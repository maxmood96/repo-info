<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10`](#dart310)
-	[`dart:3.10-sdk`](#dart310-sdk)
-	[`dart:3.10.7`](#dart3107)
-	[`dart:3.10.7-sdk`](#dart3107-sdk)
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
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10`

```console
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10-sdk`

```console
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.7`

```console
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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

### `dart:3.10.7` - linux; amd64

```console
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.7-sdk`

```console
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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

### `dart:3.10.7-sdk` - linux; amd64

```console
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
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
		Last Modified: Tue, 20 Jan 2026 18:53:42 GMT  
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
		Last Modified: Thu, 22 Jan 2026 10:12:30 GMT  
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
		Last Modified: Thu, 22 Jan 2026 09:53:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
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
		Last Modified: Tue, 20 Jan 2026 18:53:42 GMT  
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
		Last Modified: Thu, 22 Jan 2026 10:12:30 GMT  
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
		Last Modified: Thu, 22 Jan 2026 09:53:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
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
		Last Modified: Tue, 20 Jan 2026 18:53:42 GMT  
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
		Last Modified: Thu, 22 Jan 2026 10:12:30 GMT  
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
		Last Modified: Thu, 22 Jan 2026 09:53:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
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
		Last Modified: Tue, 20 Jan 2026 18:53:42 GMT  
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
		Last Modified: Thu, 22 Jan 2026 10:12:30 GMT  
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
		Last Modified: Thu, 22 Jan 2026 09:53:29 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:1145610ae62ba69acf88af40b3bae53768709338b5b219a580206f823e62d755
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
$ docker pull dart@sha256:56958c602dd9eb419a36278db313584b226b01b22c039b63d65c54ee349a8fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e88fdab1131a3483fa69bb89f8db7328d225e30665bc62bf3fe035f39cae3f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:17:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:17:23 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:17:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:17:23 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:17:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:14 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:05 GMT  
		Size: 213.1 MB (213120659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cdbcd07432537dda38159c3517dea1bb7ff48e7270adff2d94120ef43b4604d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127fe1f13c54a9ceece6ca72fca1dbad798988864ddc8aa46b97e3ea8d78f35f`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ce8122967afd0c3b5ac6306d9a0b24d6b584617fbeb3094e6b3b8557e9a27`  
		Last Modified: Tue, 13 Jan 2026 03:54:08 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:89dd00e44342e22954ad06d041ce47a372217d00ef6948bdbe94bff7b3dd1d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219904097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0250197224faaaf3429deb65b1d2633025bfd0ba9c879b5c524b31961e7ce909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:04:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:04:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:04:04 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:04:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7661415e9a927d825ae7a2e6fd6799e1fcc68743be79871ca0b030321832c6`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:04:36 GMT  
		Size: 154.9 MB (154924595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8d19a22cbb7393e69152f0a08c6d4b0970a537f3394e5714e28d4027804ea86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e51e96c8e9946363a4484c5a164e8dd86bc4d7ad226d78dd547faeda8674c4`

```dockerfile
```

-	Layers:
	-	`sha256:f213052323724335c2c08dabd9b374be53ce5f48587ee05e51fe6226f3bc9ac9`  
		Last Modified: Tue, 13 Jan 2026 03:04:31 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c613572f78c7451cf8c7204a44cb27733903e2ea9dbcad61ecdb40cf83870943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286341681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f523e61c7a039c963ecf3e4b5dc81ebb8ba74449efaa25fb5844575189994c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:13 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:23:51 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:23:55 GMT  
		Size: 212.4 MB (212350464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8c3715d4939730ce207fd703d1285638248b90c32404b4340a39fe63b45d8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3816945a12014ecd951aaef2d87393aefcea1ce8a59ee2926d2a4fb5bbed9d`

```dockerfile
```

-	Layers:
	-	`sha256:24ec61c7be0943e6802334d0eea11c10ee723bf7058c049fafc12e82dd3b8fcd`  
		Last Modified: Tue, 13 Jan 2026 02:23:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3edd9f6a294befd0047ae15417eeb3731544e1ce33194719249137fddf126871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232960243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90133f3f71ec1898776ee22923255a2ebe16c1b2736d6012f7fd3f5af30f1cd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 06:50:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 16 Jan 2026 06:50:59 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 16 Jan 2026 06:50:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 06:50:59 GMT
WORKDIR /root
# Fri, 16 Jan 2026 06:51:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:55:44 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 06:56:01 GMT  
		Size: 161.6 MB (161562921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:dc22f30008bf2b9c0ad4c95b05c954271af04a04e1cf4ce87b0824fee0e60b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b95529c6fb6f3a056d09575593ddd8d3b1aecb73c6fd5aced57540636adc627`

```dockerfile
```

-	Layers:
	-	`sha256:b74cb7892f2da8a67b7f229837cf4152f28f8aa9531721442709cc0360574e28`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
