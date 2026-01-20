<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10`](#dart310)
-	[`dart:3.10-sdk`](#dart310-sdk)
-	[`dart:3.10.7`](#dart3107)
-	[`dart:3.10.7-sdk`](#dart3107-sdk)
-	[`dart:3.11.0-296.3.beta`](#dart3110-2963beta)
-	[`dart:3.11.0-296.3.beta-sdk`](#dart3110-2963beta-sdk)
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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

## `dart:3.11.0-296.3.beta`

```console
$ docker pull dart@sha256:46155893a5946aca4baace5f5ae5f473c4284b2c669b3079c55693b33f48b126
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

### `dart:3.11.0-296.3.beta` - linux; amd64

```console
$ docker pull dart@sha256:da8b1a22344a2f13593e089c2f817e605143a97cba2df6747180ac1e2164b289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307090359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711f1ef91674dc25d2ed793614a27df6308e3346d316c5ef5e621f83e1651281`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:28 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:50:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31717fe3f63bc4b46ba25be85b210cb57797f444c36a4dfca836b72ac733b03`  
		Last Modified: Tue, 13 Jan 2026 17:51:15 GMT  
		Size: 42.5 MB (42496178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712442cdf2e67321fc56d12eea5e67631773644bb9f28b6842144404aa3f3e93`  
		Last Modified: Tue, 13 Jan 2026 17:51:23 GMT  
		Size: 1.9 MB (1870175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91853fa2cdb23195015c727705b9cce17ae6829dbba5a6bbb3660b1df49c934`  
		Last Modified: Tue, 13 Jan 2026 17:58:23 GMT  
		Size: 233.0 MB (232950289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.3.beta` - unknown; unknown

```console
$ docker pull dart@sha256:d48e28dd4c8aeebeb01e37093c655c63e1c6c200deff05f22703d090da0f616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b7073e3ee1c8b6e0ebdd4769999ebcfaf4fbdddb7ac9be324422810b463aa2`

```dockerfile
```

-	Layers:
	-	`sha256:bad1d6b497339b3fc55f95cc21a9d8ad6d9b07b7f00a52eb20dcba2947bc2602`  
		Last Modified: Tue, 13 Jan 2026 17:51:11 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.3.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:acc516f1026f5e3eadd227704c78e6bebd52b6d0346d82dc5263cae0670b7d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23901c4ad5601b3e2aada638af5790902c5c30ab93264e6be989b09ddb5b908`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:57:11 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:57:11 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:57:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61e99571e238da169385ef419321eb10f3cfa2347dabc10701a7d179c3d5c05`  
		Last Modified: Tue, 13 Jan 2026 17:58:00 GMT  
		Size: 37.5 MB (37497570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67315b84b37e5589e484d4ae8df9649947bec4b75a138f4cc185708eb8f8b9b5`  
		Last Modified: Tue, 13 Jan 2026 17:57:58 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137940b2a3a956f47e6e7ece44e42fa1447e20c516d533f23fa8eee1883276e2`  
		Last Modified: Tue, 13 Jan 2026 18:03:14 GMT  
		Size: 157.9 MB (157920234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.3.beta` - unknown; unknown

```console
$ docker pull dart@sha256:94fb5b34db15dd619559217fe18a56898177ffea36a29d9f81f77ab6fff1d038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac4295162cb419fb0455b29e9f9852e204a82482da33629844b4af4112de7cf`

```dockerfile
```

-	Layers:
	-	`sha256:804b0478f56366200665c1a79b9b6861f500a1aa16bcd958ebd200680d8a7a78`  
		Last Modified: Tue, 13 Jan 2026 21:53:30 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.3.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de918bbd30afe37e8870c7eadc5d976241f64676d7f98ebcac7934d3e288eafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a64ad138cc690fc78f75a9cef4b33af319ce4bffeb311a74371096d3add5664`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:53 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:51:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79982bc37f5efef6e806934713fe6a28e5ac139088dfaf71d2b351a0911c6393`  
		Last Modified: Tue, 13 Jan 2026 17:51:53 GMT  
		Size: 42.3 MB (42292862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e501186dc201888f65f869cd4e59980bfc8a046ff6933b917fab2703635be43d`  
		Last Modified: Tue, 13 Jan 2026 17:51:48 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59910d566c09cf83ab2de3c61a6165260bc3ec2eb2fbad0f3dcae98f85b7a0d`  
		Last Modified: Tue, 13 Jan 2026 17:51:42 GMT  
		Size: 231.4 MB (231448358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.3.beta` - unknown; unknown

```console
$ docker pull dart@sha256:69f73cfd0a536eba875eb069b5d87f59a04d28a65a78223e0d09eef06de0f096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8130eb1305a3635d1bbd42f45d6dc76e9f3cd8ddaea8efd667d1dbfbe46a54`

```dockerfile
```

-	Layers:
	-	`sha256:5a34a501e29491bfd0c311495aa36a82f474582701e69ec3462f9a7da2430799`  
		Last Modified: Tue, 13 Jan 2026 17:51:37 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.3.beta` - linux; riscv64

```console
$ docker pull dart@sha256:a57f40be582c674668d6f38ea2d341776e3393e9b5eec1a0a437d0c7b32a91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251881717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9caec59d2fb89ba9d61311f07ad7af40f441ef389712111facef7089ef97820d`
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
# Fri, 16 Jan 2026 06:57:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a74beac1fe3779da2a8b0ad5a08ce504626b511eeabbbf32147c1d33585aa1`  
		Last Modified: Fri, 16 Jan 2026 07:06:04 GMT  
		Size: 180.5 MB (180484395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.3.beta` - unknown; unknown

```console
$ docker pull dart@sha256:e060499a18c8318022841842d56e6c90343f7a1262cd40a55049fb77640fcbeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fd8cfb939349e19d01460ecc307e2c3ff0e25dbff62df8f001e817b5c5f2a0`

```dockerfile
```

-	Layers:
	-	`sha256:19b98a2a945bfcf32eafafa87831f859b0c6ca65f402bbe914e33e5a799d54b7`  
		Last Modified: Fri, 16 Jan 2026 07:01:23 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-296.3.beta-sdk`

```console
$ docker pull dart@sha256:46155893a5946aca4baace5f5ae5f473c4284b2c669b3079c55693b33f48b126
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

### `dart:3.11.0-296.3.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:da8b1a22344a2f13593e089c2f817e605143a97cba2df6747180ac1e2164b289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307090359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711f1ef91674dc25d2ed793614a27df6308e3346d316c5ef5e621f83e1651281`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:28 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:50:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31717fe3f63bc4b46ba25be85b210cb57797f444c36a4dfca836b72ac733b03`  
		Last Modified: Tue, 13 Jan 2026 17:51:15 GMT  
		Size: 42.5 MB (42496178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712442cdf2e67321fc56d12eea5e67631773644bb9f28b6842144404aa3f3e93`  
		Last Modified: Tue, 13 Jan 2026 17:51:23 GMT  
		Size: 1.9 MB (1870175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91853fa2cdb23195015c727705b9cce17ae6829dbba5a6bbb3660b1df49c934`  
		Last Modified: Tue, 13 Jan 2026 17:58:23 GMT  
		Size: 233.0 MB (232950289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.3.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d48e28dd4c8aeebeb01e37093c655c63e1c6c200deff05f22703d090da0f616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b7073e3ee1c8b6e0ebdd4769999ebcfaf4fbdddb7ac9be324422810b463aa2`

```dockerfile
```

-	Layers:
	-	`sha256:bad1d6b497339b3fc55f95cc21a9d8ad6d9b07b7f00a52eb20dcba2947bc2602`  
		Last Modified: Tue, 13 Jan 2026 17:51:11 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.3.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:acc516f1026f5e3eadd227704c78e6bebd52b6d0346d82dc5263cae0670b7d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23901c4ad5601b3e2aada638af5790902c5c30ab93264e6be989b09ddb5b908`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:57:11 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:57:11 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:57:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61e99571e238da169385ef419321eb10f3cfa2347dabc10701a7d179c3d5c05`  
		Last Modified: Tue, 13 Jan 2026 17:58:00 GMT  
		Size: 37.5 MB (37497570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67315b84b37e5589e484d4ae8df9649947bec4b75a138f4cc185708eb8f8b9b5`  
		Last Modified: Tue, 13 Jan 2026 17:57:58 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137940b2a3a956f47e6e7ece44e42fa1447e20c516d533f23fa8eee1883276e2`  
		Last Modified: Tue, 13 Jan 2026 18:03:14 GMT  
		Size: 157.9 MB (157920234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.3.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:94fb5b34db15dd619559217fe18a56898177ffea36a29d9f81f77ab6fff1d038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac4295162cb419fb0455b29e9f9852e204a82482da33629844b4af4112de7cf`

```dockerfile
```

-	Layers:
	-	`sha256:804b0478f56366200665c1a79b9b6861f500a1aa16bcd958ebd200680d8a7a78`  
		Last Modified: Tue, 13 Jan 2026 21:53:30 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.3.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de918bbd30afe37e8870c7eadc5d976241f64676d7f98ebcac7934d3e288eafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a64ad138cc690fc78f75a9cef4b33af319ce4bffeb311a74371096d3add5664`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:53 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:51:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79982bc37f5efef6e806934713fe6a28e5ac139088dfaf71d2b351a0911c6393`  
		Last Modified: Tue, 13 Jan 2026 17:51:53 GMT  
		Size: 42.3 MB (42292862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e501186dc201888f65f869cd4e59980bfc8a046ff6933b917fab2703635be43d`  
		Last Modified: Tue, 13 Jan 2026 17:51:48 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59910d566c09cf83ab2de3c61a6165260bc3ec2eb2fbad0f3dcae98f85b7a0d`  
		Last Modified: Tue, 13 Jan 2026 17:51:42 GMT  
		Size: 231.4 MB (231448358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.3.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:69f73cfd0a536eba875eb069b5d87f59a04d28a65a78223e0d09eef06de0f096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8130eb1305a3635d1bbd42f45d6dc76e9f3cd8ddaea8efd667d1dbfbe46a54`

```dockerfile
```

-	Layers:
	-	`sha256:5a34a501e29491bfd0c311495aa36a82f474582701e69ec3462f9a7da2430799`  
		Last Modified: Tue, 13 Jan 2026 17:51:37 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.3.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:a57f40be582c674668d6f38ea2d341776e3393e9b5eec1a0a437d0c7b32a91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251881717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9caec59d2fb89ba9d61311f07ad7af40f441ef389712111facef7089ef97820d`
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
# Fri, 16 Jan 2026 06:57:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a74beac1fe3779da2a8b0ad5a08ce504626b511eeabbbf32147c1d33585aa1`  
		Last Modified: Fri, 16 Jan 2026 07:06:04 GMT  
		Size: 180.5 MB (180484395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.3.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e060499a18c8318022841842d56e6c90343f7a1262cd40a55049fb77640fcbeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fd8cfb939349e19d01460ecc307e2c3ff0e25dbff62df8f001e817b5c5f2a0`

```dockerfile
```

-	Layers:
	-	`sha256:19b98a2a945bfcf32eafafa87831f859b0c6ca65f402bbe914e33e5a799d54b7`  
		Last Modified: Fri, 16 Jan 2026 07:01:23 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:46155893a5946aca4baace5f5ae5f473c4284b2c669b3079c55693b33f48b126
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
$ docker pull dart@sha256:da8b1a22344a2f13593e089c2f817e605143a97cba2df6747180ac1e2164b289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307090359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711f1ef91674dc25d2ed793614a27df6308e3346d316c5ef5e621f83e1651281`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:28 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:50:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31717fe3f63bc4b46ba25be85b210cb57797f444c36a4dfca836b72ac733b03`  
		Last Modified: Tue, 13 Jan 2026 17:51:15 GMT  
		Size: 42.5 MB (42496178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712442cdf2e67321fc56d12eea5e67631773644bb9f28b6842144404aa3f3e93`  
		Last Modified: Tue, 13 Jan 2026 17:51:23 GMT  
		Size: 1.9 MB (1870175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91853fa2cdb23195015c727705b9cce17ae6829dbba5a6bbb3660b1df49c934`  
		Last Modified: Tue, 13 Jan 2026 17:58:23 GMT  
		Size: 233.0 MB (232950289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:d48e28dd4c8aeebeb01e37093c655c63e1c6c200deff05f22703d090da0f616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b7073e3ee1c8b6e0ebdd4769999ebcfaf4fbdddb7ac9be324422810b463aa2`

```dockerfile
```

-	Layers:
	-	`sha256:bad1d6b497339b3fc55f95cc21a9d8ad6d9b07b7f00a52eb20dcba2947bc2602`  
		Last Modified: Tue, 13 Jan 2026 17:51:11 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:acc516f1026f5e3eadd227704c78e6bebd52b6d0346d82dc5263cae0670b7d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23901c4ad5601b3e2aada638af5790902c5c30ab93264e6be989b09ddb5b908`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:57:11 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:57:11 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:57:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61e99571e238da169385ef419321eb10f3cfa2347dabc10701a7d179c3d5c05`  
		Last Modified: Tue, 13 Jan 2026 17:58:00 GMT  
		Size: 37.5 MB (37497570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67315b84b37e5589e484d4ae8df9649947bec4b75a138f4cc185708eb8f8b9b5`  
		Last Modified: Tue, 13 Jan 2026 17:57:58 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137940b2a3a956f47e6e7ece44e42fa1447e20c516d533f23fa8eee1883276e2`  
		Last Modified: Tue, 13 Jan 2026 18:03:14 GMT  
		Size: 157.9 MB (157920234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:94fb5b34db15dd619559217fe18a56898177ffea36a29d9f81f77ab6fff1d038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac4295162cb419fb0455b29e9f9852e204a82482da33629844b4af4112de7cf`

```dockerfile
```

-	Layers:
	-	`sha256:804b0478f56366200665c1a79b9b6861f500a1aa16bcd958ebd200680d8a7a78`  
		Last Modified: Tue, 13 Jan 2026 21:53:30 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de918bbd30afe37e8870c7eadc5d976241f64676d7f98ebcac7934d3e288eafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a64ad138cc690fc78f75a9cef4b33af319ce4bffeb311a74371096d3add5664`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:53 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:51:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79982bc37f5efef6e806934713fe6a28e5ac139088dfaf71d2b351a0911c6393`  
		Last Modified: Tue, 13 Jan 2026 17:51:53 GMT  
		Size: 42.3 MB (42292862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e501186dc201888f65f869cd4e59980bfc8a046ff6933b917fab2703635be43d`  
		Last Modified: Tue, 13 Jan 2026 17:51:48 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59910d566c09cf83ab2de3c61a6165260bc3ec2eb2fbad0f3dcae98f85b7a0d`  
		Last Modified: Tue, 13 Jan 2026 17:51:42 GMT  
		Size: 231.4 MB (231448358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:69f73cfd0a536eba875eb069b5d87f59a04d28a65a78223e0d09eef06de0f096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8130eb1305a3635d1bbd42f45d6dc76e9f3cd8ddaea8efd667d1dbfbe46a54`

```dockerfile
```

-	Layers:
	-	`sha256:5a34a501e29491bfd0c311495aa36a82f474582701e69ec3462f9a7da2430799`  
		Last Modified: Tue, 13 Jan 2026 17:51:37 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:a57f40be582c674668d6f38ea2d341776e3393e9b5eec1a0a437d0c7b32a91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251881717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9caec59d2fb89ba9d61311f07ad7af40f441ef389712111facef7089ef97820d`
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
# Fri, 16 Jan 2026 06:57:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a74beac1fe3779da2a8b0ad5a08ce504626b511eeabbbf32147c1d33585aa1`  
		Last Modified: Fri, 16 Jan 2026 07:06:04 GMT  
		Size: 180.5 MB (180484395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:e060499a18c8318022841842d56e6c90343f7a1262cd40a55049fb77640fcbeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fd8cfb939349e19d01460ecc307e2c3ff0e25dbff62df8f001e817b5c5f2a0`

```dockerfile
```

-	Layers:
	-	`sha256:19b98a2a945bfcf32eafafa87831f859b0c6ca65f402bbe914e33e5a799d54b7`  
		Last Modified: Fri, 16 Jan 2026 07:01:23 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:46155893a5946aca4baace5f5ae5f473c4284b2c669b3079c55693b33f48b126
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
$ docker pull dart@sha256:da8b1a22344a2f13593e089c2f817e605143a97cba2df6747180ac1e2164b289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307090359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711f1ef91674dc25d2ed793614a27df6308e3346d316c5ef5e621f83e1651281`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:28 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:50:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31717fe3f63bc4b46ba25be85b210cb57797f444c36a4dfca836b72ac733b03`  
		Last Modified: Tue, 13 Jan 2026 17:51:15 GMT  
		Size: 42.5 MB (42496178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712442cdf2e67321fc56d12eea5e67631773644bb9f28b6842144404aa3f3e93`  
		Last Modified: Tue, 13 Jan 2026 17:51:23 GMT  
		Size: 1.9 MB (1870175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91853fa2cdb23195015c727705b9cce17ae6829dbba5a6bbb3660b1df49c934`  
		Last Modified: Tue, 13 Jan 2026 17:58:23 GMT  
		Size: 233.0 MB (232950289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d48e28dd4c8aeebeb01e37093c655c63e1c6c200deff05f22703d090da0f616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b7073e3ee1c8b6e0ebdd4769999ebcfaf4fbdddb7ac9be324422810b463aa2`

```dockerfile
```

-	Layers:
	-	`sha256:bad1d6b497339b3fc55f95cc21a9d8ad6d9b07b7f00a52eb20dcba2947bc2602`  
		Last Modified: Tue, 13 Jan 2026 17:51:11 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:acc516f1026f5e3eadd227704c78e6bebd52b6d0346d82dc5263cae0670b7d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23901c4ad5601b3e2aada638af5790902c5c30ab93264e6be989b09ddb5b908`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:57:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:57:11 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:57:11 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:57:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61e99571e238da169385ef419321eb10f3cfa2347dabc10701a7d179c3d5c05`  
		Last Modified: Tue, 13 Jan 2026 17:58:00 GMT  
		Size: 37.5 MB (37497570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67315b84b37e5589e484d4ae8df9649947bec4b75a138f4cc185708eb8f8b9b5`  
		Last Modified: Tue, 13 Jan 2026 17:57:58 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137940b2a3a956f47e6e7ece44e42fa1447e20c516d533f23fa8eee1883276e2`  
		Last Modified: Tue, 13 Jan 2026 18:03:14 GMT  
		Size: 157.9 MB (157920234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:94fb5b34db15dd619559217fe18a56898177ffea36a29d9f81f77ab6fff1d038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac4295162cb419fb0455b29e9f9852e204a82482da33629844b4af4112de7cf`

```dockerfile
```

-	Layers:
	-	`sha256:804b0478f56366200665c1a79b9b6861f500a1aa16bcd958ebd200680d8a7a78`  
		Last Modified: Tue, 13 Jan 2026 21:53:30 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:de918bbd30afe37e8870c7eadc5d976241f64676d7f98ebcac7934d3e288eafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305439814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a64ad138cc690fc78f75a9cef4b33af319ce4bffeb311a74371096d3add5664`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:50:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 17:50:53 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 17:50:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:50:53 GMT
WORKDIR /root
# Tue, 13 Jan 2026 17:51:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79982bc37f5efef6e806934713fe6a28e5ac139088dfaf71d2b351a0911c6393`  
		Last Modified: Tue, 13 Jan 2026 17:51:53 GMT  
		Size: 42.3 MB (42292862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e501186dc201888f65f869cd4e59980bfc8a046ff6933b917fab2703635be43d`  
		Last Modified: Tue, 13 Jan 2026 17:51:48 GMT  
		Size: 1.6 MB (1564520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59910d566c09cf83ab2de3c61a6165260bc3ec2eb2fbad0f3dcae98f85b7a0d`  
		Last Modified: Tue, 13 Jan 2026 17:51:42 GMT  
		Size: 231.4 MB (231448358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:69f73cfd0a536eba875eb069b5d87f59a04d28a65a78223e0d09eef06de0f096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8130eb1305a3635d1bbd42f45d6dc76e9f3cd8ddaea8efd667d1dbfbe46a54`

```dockerfile
```

-	Layers:
	-	`sha256:5a34a501e29491bfd0c311495aa36a82f474582701e69ec3462f9a7da2430799`  
		Last Modified: Tue, 13 Jan 2026 17:51:37 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:a57f40be582c674668d6f38ea2d341776e3393e9b5eec1a0a437d0c7b32a91c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251881717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9caec59d2fb89ba9d61311f07ad7af40f441ef389712111facef7089ef97820d`
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
# Fri, 16 Jan 2026 06:57:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1d7139fda640af2f0039bbb842901f61a88ef59a20525ca35c6a6047163e76;             SDK_ARCH="x64";;         armhf)             DART_SHA256=be890d3df1f4397a25a3e3104e252e2421166a1b1e88143dc4dac72ae1682c50;             SDK_ARCH="arm";;         arm64)             DART_SHA256=c06fe3aee69a0bb0ded664a28eba38176558ccbe69a8eb6f0d26c700956a5fe8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=09e74f6b142c79b524242a03abb1fe409ccd0fb8fc5661343fa8b680e511ec62;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e0087c2a006d0b12f7e259209c0dcc911138aeb7078877b58369d28bc62942`  
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a74beac1fe3779da2a8b0ad5a08ce504626b511eeabbbf32147c1d33585aa1`  
		Last Modified: Fri, 16 Jan 2026 07:06:04 GMT  
		Size: 180.5 MB (180484395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e060499a18c8318022841842d56e6c90343f7a1262cd40a55049fb77640fcbeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fd8cfb939349e19d01460ecc307e2c3ff0e25dbff62df8f001e817b5c5f2a0`

```dockerfile
```

-	Layers:
	-	`sha256:19b98a2a945bfcf32eafafa87831f859b0c6ca65f402bbe914e33e5a799d54b7`  
		Last Modified: Fri, 16 Jan 2026 07:01:23 GMT  
		Size: 19.0 KB (18971 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc0e02a8624300d1cd18f598a1fddc6ca3588d0a2448844ef8bda007202fe0`  
		Last Modified: Tue, 13 Jan 2026 02:18:02 GMT  
		Size: 42.5 MB (42495963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e3a0e8c6d141f4dcaf2343fec174a06a1123b6deae6fe2f01da4ed1fe1d54`  
		Last Modified: Tue, 13 Jan 2026 02:18:00 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536b39c7eb6c3c92475bb4c5928d2fa02598aa74a137819c0bf68fca42bc0b9`  
		Last Modified: Tue, 13 Jan 2026 02:18:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 37.5 MB (37497725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705299ea0a828c37c489da6e6bd9700bab9fa8c23c63ee55aae2ee440b598e9`  
		Last Modified: Tue, 13 Jan 2026 03:04:41 GMT  
		Size: 1.3 MB (1273167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41a1426c65a828e5e191d8c50d288e0d1da7e653e2065cd232ca8c497f519af`  
		Last Modified: Tue, 13 Jan 2026 03:05:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b484ab8308638e6d45692f5b7a323876de3dfab26f562b5cb16fa5d66036648`  
		Last Modified: Tue, 13 Jan 2026 02:24:04 GMT  
		Size: 42.3 MB (42292620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2d8b432ef4df219d1802a1201086654fae4da86d83c958b7fb22c5244ad6a`  
		Last Modified: Tue, 13 Jan 2026 02:24:00 GMT  
		Size: 1.6 MB (1564523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8f1f356928393f6802d5671cdc40e9864dd0effd81ee331f83ebcb83b96e6`  
		Last Modified: Tue, 13 Jan 2026 02:24:29 GMT  
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
		Last Modified: Tue, 13 Jan 2026 03:54:30 GMT  
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
		Last Modified: Fri, 16 Jan 2026 06:56:14 GMT  
		Size: 41.6 MB (41560935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2a5fe4c4d5c936a0ba263b540d0a1974535f68fb4e9f3400384e8d6e5ac2a`  
		Last Modified: Fri, 16 Jan 2026 06:55:32 GMT  
		Size: 1.6 MB (1564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a982445dae78b52b283e870d33a044419fe82da96adb4458c53dae5e0d6316f`  
		Last Modified: Fri, 16 Jan 2026 07:11:04 GMT  
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
