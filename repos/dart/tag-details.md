<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10`](#dart310)
-	[`dart:3.10-sdk`](#dart310-sdk)
-	[`dart:3.10.7`](#dart3107)
-	[`dart:3.10.7-sdk`](#dart3107-sdk)
-	[`dart:3.11.0-200.1.beta`](#dart3110-2001beta)
-	[`dart:3.11.0-200.1.beta-sdk`](#dart3110-2001beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10-sdk`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.7`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.7-sdk`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.7-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-200.1.beta`

```console
$ docker pull dart@sha256:971f1fa17ddfbf9e89d277c1f2329c3fb77984189ea65c6c31b0695295018c1e
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

### `dart:3.11.0-200.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:7888a6187a3d58646727a0d96f149a1a5f2ba1acb85352bc95895617a9273aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305114342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe2dceb57ec3673f397ae51a95d7fb9325ae941e971e0482f1144fa30448f12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:42 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:42 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb34a82fa0a057031d007d9df365ecf8471b0061f66a830800d50f002591c3b`  
		Last Modified: Mon, 29 Dec 2025 23:52:35 GMT  
		Size: 42.5 MB (42494066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05b2e16b304f23eed4b44045de1f005ba61ac8d5ff8e55468666f0f1e6a9072`  
		Last Modified: Mon, 29 Dec 2025 23:52:32 GMT  
		Size: 1.9 MB (1873624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24617996f1a1166b9fef181bad9065f328c3fc1efd3592650d4ff88e15e6d1c0`  
		Last Modified: Mon, 29 Dec 2025 23:52:37 GMT  
		Size: 231.0 MB (230970087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-200.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:0ea7fe5a27865940eee395980d94a64447898526e9d5b3db45b4f4438fdc4f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53cc6f9fd78202340c63bb4bd831b910017e05806a28636dbaacdc55c98ba7f`

```dockerfile
```

-	Layers:
	-	`sha256:470ec0382ba25f60e2896f12c48eba46b010575cc9d0cdf4242482b5c19e20b0`  
		Last Modified: Tue, 30 Dec 2025 03:54:12 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-200.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:95aebdb2dbde210629916e5eb4ce2fb4b4bf7a212f64ddd6a2b8cb024b81a1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221092294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978fcd718ddacc928a54a521251a339a4e3d24cba7fff9a3c1da128ff661d931`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:57 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b419915413989b3b0c82047e7e83099dea0b1180774e10873b11d73ccc04b48`  
		Last Modified: Tue, 30 Dec 2025 00:40:49 GMT  
		Size: 37.5 MB (37498257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bbf5df565ab82c3e83638ffb17b451898ff2bd40f396a5ea238d3b1c68f52a`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567954c5720340465d1be67f45b0e489e025cda98ce96c83cfb78b1dbb1b7401`  
		Last Modified: Tue, 30 Dec 2025 00:40:56 GMT  
		Size: 156.1 MB (156108887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-200.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:b5d7e0420633dafb1609851c70631232aa422ee269c01f95c135f3d3cabb353b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98d5a500b7108a8f1e993c2963009bdb784060abe89ecbbc90c46334fe56ad1`

```dockerfile
```

-	Layers:
	-	`sha256:dcd551d7ca4edbe83f60d1aeb869b99d420d088100e0a0ab9b2d85dca39ecf29`  
		Last Modified: Tue, 30 Dec 2025 03:54:15 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-200.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b330209e06405e3b7001c4f2e4753c4e6447922c45547e66d7b882b7a96fbae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303583382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f6c3e6ff8d85375becc20ca6ea04786083e231360b1f64d2976789344955a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:31 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:31 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623dc20318c56f2d04936eb6f8a9897af2fb7ed80d1482687ffcb7a3305a003f`  
		Last Modified: Mon, 29 Dec 2025 23:53:25 GMT  
		Size: 42.3 MB (42293323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884f7b12fe8c3fdd29f7873c457a22c15797b87c9eb4fc3d1665c4bb4546876e`  
		Last Modified: Mon, 29 Dec 2025 23:53:21 GMT  
		Size: 1.6 MB (1566647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4b66b1700bab7c5f818c14dbc6b81c92b65af4a5c53a63a835c7c4b67419f4`  
		Last Modified: Mon, 29 Dec 2025 23:53:31 GMT  
		Size: 229.6 MB (229584744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-200.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:4c562c03f2b4462b03e1e95a3148660c5e2edd0e1cd353d861b477d09c19fb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cc494622a5f6a14255f782d6d31c3f1898d9ec442199911941bb2c285d0700`

```dockerfile
```

-	Layers:
	-	`sha256:27095514af2f0bed0585ad1bc18c9ca1484cc655e4d8fde5688fbdfa3beca2ac`  
		Last Modified: Tue, 30 Dec 2025 03:54:18 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-200.1.beta` - linux; riscv64

```console
$ docker pull dart@sha256:562faca8a2198d098a17dea84f1f5bf82252107457b2ae5361d2a6ae123a41ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249840467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda0875958945d11786a6d10186bb46a644a9f10291d81234afb3d54c7dee7c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 08:42:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 11 Dec 2025 08:42:47 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Dec 2025 08:42:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 08:42:47 GMT
WORKDIR /root
# Thu, 11 Dec 2025 08:48:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad167056c1684d9fd70daef5b5d6c675f1f459163debcc0ca67b5999ef6fb297`  
		Last Modified: Thu, 11 Dec 2025 08:47:52 GMT  
		Size: 41.6 MB (41560777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8999e9abae129f285c549c47544c31e0f18872591db1bd7128872e607d214358`  
		Last Modified: Thu, 11 Dec 2025 08:47:46 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d36788d5cd40cb10770666deffca011203789dd0fb9d77bf4955ee12ffd5602`  
		Last Modified: Thu, 11 Dec 2025 10:01:14 GMT  
		Size: 178.4 MB (178439433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-200.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:62f7418567560db27b0fb84d16108980e254225be4d38c894f6e1ea8f73f9344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54fe31334dc86fc0aaa22d64e36fd2c9059b281146751489e968e9b9e49087e`

```dockerfile
```

-	Layers:
	-	`sha256:7638ff6890594999f475b9b7387b8ec38cc33066193594ec9a58d7c78eb981f5`  
		Last Modified: Thu, 11 Dec 2025 09:53:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-200.1.beta-sdk`

```console
$ docker pull dart@sha256:971f1fa17ddfbf9e89d277c1f2329c3fb77984189ea65c6c31b0695295018c1e
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

### `dart:3.11.0-200.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7888a6187a3d58646727a0d96f149a1a5f2ba1acb85352bc95895617a9273aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305114342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe2dceb57ec3673f397ae51a95d7fb9325ae941e971e0482f1144fa30448f12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:42 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:42 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb34a82fa0a057031d007d9df365ecf8471b0061f66a830800d50f002591c3b`  
		Last Modified: Mon, 29 Dec 2025 23:52:35 GMT  
		Size: 42.5 MB (42494066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05b2e16b304f23eed4b44045de1f005ba61ac8d5ff8e55468666f0f1e6a9072`  
		Last Modified: Mon, 29 Dec 2025 23:52:32 GMT  
		Size: 1.9 MB (1873624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24617996f1a1166b9fef181bad9065f328c3fc1efd3592650d4ff88e15e6d1c0`  
		Last Modified: Mon, 29 Dec 2025 23:52:37 GMT  
		Size: 231.0 MB (230970087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-200.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0ea7fe5a27865940eee395980d94a64447898526e9d5b3db45b4f4438fdc4f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53cc6f9fd78202340c63bb4bd831b910017e05806a28636dbaacdc55c98ba7f`

```dockerfile
```

-	Layers:
	-	`sha256:470ec0382ba25f60e2896f12c48eba46b010575cc9d0cdf4242482b5c19e20b0`  
		Last Modified: Tue, 30 Dec 2025 03:54:12 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-200.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:95aebdb2dbde210629916e5eb4ce2fb4b4bf7a212f64ddd6a2b8cb024b81a1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221092294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978fcd718ddacc928a54a521251a339a4e3d24cba7fff9a3c1da128ff661d931`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:57 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b419915413989b3b0c82047e7e83099dea0b1180774e10873b11d73ccc04b48`  
		Last Modified: Tue, 30 Dec 2025 00:40:49 GMT  
		Size: 37.5 MB (37498257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bbf5df565ab82c3e83638ffb17b451898ff2bd40f396a5ea238d3b1c68f52a`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567954c5720340465d1be67f45b0e489e025cda98ce96c83cfb78b1dbb1b7401`  
		Last Modified: Tue, 30 Dec 2025 00:40:56 GMT  
		Size: 156.1 MB (156108887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-200.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b5d7e0420633dafb1609851c70631232aa422ee269c01f95c135f3d3cabb353b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98d5a500b7108a8f1e993c2963009bdb784060abe89ecbbc90c46334fe56ad1`

```dockerfile
```

-	Layers:
	-	`sha256:dcd551d7ca4edbe83f60d1aeb869b99d420d088100e0a0ab9b2d85dca39ecf29`  
		Last Modified: Tue, 30 Dec 2025 03:54:15 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-200.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b330209e06405e3b7001c4f2e4753c4e6447922c45547e66d7b882b7a96fbae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303583382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f6c3e6ff8d85375becc20ca6ea04786083e231360b1f64d2976789344955a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:31 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:31 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623dc20318c56f2d04936eb6f8a9897af2fb7ed80d1482687ffcb7a3305a003f`  
		Last Modified: Mon, 29 Dec 2025 23:53:25 GMT  
		Size: 42.3 MB (42293323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884f7b12fe8c3fdd29f7873c457a22c15797b87c9eb4fc3d1665c4bb4546876e`  
		Last Modified: Mon, 29 Dec 2025 23:53:21 GMT  
		Size: 1.6 MB (1566647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4b66b1700bab7c5f818c14dbc6b81c92b65af4a5c53a63a835c7c4b67419f4`  
		Last Modified: Mon, 29 Dec 2025 23:53:31 GMT  
		Size: 229.6 MB (229584744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-200.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4c562c03f2b4462b03e1e95a3148660c5e2edd0e1cd353d861b477d09c19fb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cc494622a5f6a14255f782d6d31c3f1898d9ec442199911941bb2c285d0700`

```dockerfile
```

-	Layers:
	-	`sha256:27095514af2f0bed0585ad1bc18c9ca1484cc655e4d8fde5688fbdfa3beca2ac`  
		Last Modified: Tue, 30 Dec 2025 03:54:18 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-200.1.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:562faca8a2198d098a17dea84f1f5bf82252107457b2ae5361d2a6ae123a41ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249840467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda0875958945d11786a6d10186bb46a644a9f10291d81234afb3d54c7dee7c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 08:42:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 11 Dec 2025 08:42:47 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Dec 2025 08:42:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 08:42:47 GMT
WORKDIR /root
# Thu, 11 Dec 2025 08:48:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad167056c1684d9fd70daef5b5d6c675f1f459163debcc0ca67b5999ef6fb297`  
		Last Modified: Thu, 11 Dec 2025 08:47:52 GMT  
		Size: 41.6 MB (41560777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8999e9abae129f285c549c47544c31e0f18872591db1bd7128872e607d214358`  
		Last Modified: Thu, 11 Dec 2025 08:47:46 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d36788d5cd40cb10770666deffca011203789dd0fb9d77bf4955ee12ffd5602`  
		Last Modified: Thu, 11 Dec 2025 10:01:14 GMT  
		Size: 178.4 MB (178439433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-200.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:62f7418567560db27b0fb84d16108980e254225be4d38c894f6e1ea8f73f9344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54fe31334dc86fc0aaa22d64e36fd2c9059b281146751489e968e9b9e49087e`

```dockerfile
```

-	Layers:
	-	`sha256:7638ff6890594999f475b9b7387b8ec38cc33066193594ec9a58d7c78eb981f5`  
		Last Modified: Thu, 11 Dec 2025 09:53:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:971f1fa17ddfbf9e89d277c1f2329c3fb77984189ea65c6c31b0695295018c1e
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
$ docker pull dart@sha256:7888a6187a3d58646727a0d96f149a1a5f2ba1acb85352bc95895617a9273aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305114342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe2dceb57ec3673f397ae51a95d7fb9325ae941e971e0482f1144fa30448f12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:42 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:42 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb34a82fa0a057031d007d9df365ecf8471b0061f66a830800d50f002591c3b`  
		Last Modified: Mon, 29 Dec 2025 23:52:35 GMT  
		Size: 42.5 MB (42494066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05b2e16b304f23eed4b44045de1f005ba61ac8d5ff8e55468666f0f1e6a9072`  
		Last Modified: Mon, 29 Dec 2025 23:52:32 GMT  
		Size: 1.9 MB (1873624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24617996f1a1166b9fef181bad9065f328c3fc1efd3592650d4ff88e15e6d1c0`  
		Last Modified: Mon, 29 Dec 2025 23:52:37 GMT  
		Size: 231.0 MB (230970087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:0ea7fe5a27865940eee395980d94a64447898526e9d5b3db45b4f4438fdc4f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53cc6f9fd78202340c63bb4bd831b910017e05806a28636dbaacdc55c98ba7f`

```dockerfile
```

-	Layers:
	-	`sha256:470ec0382ba25f60e2896f12c48eba46b010575cc9d0cdf4242482b5c19e20b0`  
		Last Modified: Tue, 30 Dec 2025 03:54:12 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:95aebdb2dbde210629916e5eb4ce2fb4b4bf7a212f64ddd6a2b8cb024b81a1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221092294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978fcd718ddacc928a54a521251a339a4e3d24cba7fff9a3c1da128ff661d931`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:57 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b419915413989b3b0c82047e7e83099dea0b1180774e10873b11d73ccc04b48`  
		Last Modified: Tue, 30 Dec 2025 00:40:49 GMT  
		Size: 37.5 MB (37498257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bbf5df565ab82c3e83638ffb17b451898ff2bd40f396a5ea238d3b1c68f52a`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567954c5720340465d1be67f45b0e489e025cda98ce96c83cfb78b1dbb1b7401`  
		Last Modified: Tue, 30 Dec 2025 00:40:56 GMT  
		Size: 156.1 MB (156108887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:b5d7e0420633dafb1609851c70631232aa422ee269c01f95c135f3d3cabb353b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98d5a500b7108a8f1e993c2963009bdb784060abe89ecbbc90c46334fe56ad1`

```dockerfile
```

-	Layers:
	-	`sha256:dcd551d7ca4edbe83f60d1aeb869b99d420d088100e0a0ab9b2d85dca39ecf29`  
		Last Modified: Tue, 30 Dec 2025 03:54:15 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b330209e06405e3b7001c4f2e4753c4e6447922c45547e66d7b882b7a96fbae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303583382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f6c3e6ff8d85375becc20ca6ea04786083e231360b1f64d2976789344955a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:31 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:31 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623dc20318c56f2d04936eb6f8a9897af2fb7ed80d1482687ffcb7a3305a003f`  
		Last Modified: Mon, 29 Dec 2025 23:53:25 GMT  
		Size: 42.3 MB (42293323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884f7b12fe8c3fdd29f7873c457a22c15797b87c9eb4fc3d1665c4bb4546876e`  
		Last Modified: Mon, 29 Dec 2025 23:53:21 GMT  
		Size: 1.6 MB (1566647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4b66b1700bab7c5f818c14dbc6b81c92b65af4a5c53a63a835c7c4b67419f4`  
		Last Modified: Mon, 29 Dec 2025 23:53:31 GMT  
		Size: 229.6 MB (229584744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:4c562c03f2b4462b03e1e95a3148660c5e2edd0e1cd353d861b477d09c19fb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cc494622a5f6a14255f782d6d31c3f1898d9ec442199911941bb2c285d0700`

```dockerfile
```

-	Layers:
	-	`sha256:27095514af2f0bed0585ad1bc18c9ca1484cc655e4d8fde5688fbdfa3beca2ac`  
		Last Modified: Tue, 30 Dec 2025 03:54:18 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:562faca8a2198d098a17dea84f1f5bf82252107457b2ae5361d2a6ae123a41ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249840467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda0875958945d11786a6d10186bb46a644a9f10291d81234afb3d54c7dee7c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 08:42:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 11 Dec 2025 08:42:47 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Dec 2025 08:42:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 08:42:47 GMT
WORKDIR /root
# Thu, 11 Dec 2025 08:48:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad167056c1684d9fd70daef5b5d6c675f1f459163debcc0ca67b5999ef6fb297`  
		Last Modified: Thu, 11 Dec 2025 08:47:52 GMT  
		Size: 41.6 MB (41560777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8999e9abae129f285c549c47544c31e0f18872591db1bd7128872e607d214358`  
		Last Modified: Thu, 11 Dec 2025 08:47:46 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d36788d5cd40cb10770666deffca011203789dd0fb9d77bf4955ee12ffd5602`  
		Last Modified: Thu, 11 Dec 2025 10:01:14 GMT  
		Size: 178.4 MB (178439433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:62f7418567560db27b0fb84d16108980e254225be4d38c894f6e1ea8f73f9344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54fe31334dc86fc0aaa22d64e36fd2c9059b281146751489e968e9b9e49087e`

```dockerfile
```

-	Layers:
	-	`sha256:7638ff6890594999f475b9b7387b8ec38cc33066193594ec9a58d7c78eb981f5`  
		Last Modified: Thu, 11 Dec 2025 09:53:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:971f1fa17ddfbf9e89d277c1f2329c3fb77984189ea65c6c31b0695295018c1e
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
$ docker pull dart@sha256:7888a6187a3d58646727a0d96f149a1a5f2ba1acb85352bc95895617a9273aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305114342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe2dceb57ec3673f397ae51a95d7fb9325ae941e971e0482f1144fa30448f12`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:42 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:42 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb34a82fa0a057031d007d9df365ecf8471b0061f66a830800d50f002591c3b`  
		Last Modified: Mon, 29 Dec 2025 23:52:35 GMT  
		Size: 42.5 MB (42494066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05b2e16b304f23eed4b44045de1f005ba61ac8d5ff8e55468666f0f1e6a9072`  
		Last Modified: Mon, 29 Dec 2025 23:52:32 GMT  
		Size: 1.9 MB (1873624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24617996f1a1166b9fef181bad9065f328c3fc1efd3592650d4ff88e15e6d1c0`  
		Last Modified: Mon, 29 Dec 2025 23:52:37 GMT  
		Size: 231.0 MB (230970087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0ea7fe5a27865940eee395980d94a64447898526e9d5b3db45b4f4438fdc4f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53cc6f9fd78202340c63bb4bd831b910017e05806a28636dbaacdc55c98ba7f`

```dockerfile
```

-	Layers:
	-	`sha256:470ec0382ba25f60e2896f12c48eba46b010575cc9d0cdf4242482b5c19e20b0`  
		Last Modified: Tue, 30 Dec 2025 03:54:12 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:95aebdb2dbde210629916e5eb4ce2fb4b4bf7a212f64ddd6a2b8cb024b81a1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221092294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978fcd718ddacc928a54a521251a339a4e3d24cba7fff9a3c1da128ff661d931`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:57 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b419915413989b3b0c82047e7e83099dea0b1180774e10873b11d73ccc04b48`  
		Last Modified: Tue, 30 Dec 2025 00:40:49 GMT  
		Size: 37.5 MB (37498257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bbf5df565ab82c3e83638ffb17b451898ff2bd40f396a5ea238d3b1c68f52a`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567954c5720340465d1be67f45b0e489e025cda98ce96c83cfb78b1dbb1b7401`  
		Last Modified: Tue, 30 Dec 2025 00:40:56 GMT  
		Size: 156.1 MB (156108887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b5d7e0420633dafb1609851c70631232aa422ee269c01f95c135f3d3cabb353b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98d5a500b7108a8f1e993c2963009bdb784060abe89ecbbc90c46334fe56ad1`

```dockerfile
```

-	Layers:
	-	`sha256:dcd551d7ca4edbe83f60d1aeb869b99d420d088100e0a0ab9b2d85dca39ecf29`  
		Last Modified: Tue, 30 Dec 2025 03:54:15 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b330209e06405e3b7001c4f2e4753c4e6447922c45547e66d7b882b7a96fbae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303583382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f6c3e6ff8d85375becc20ca6ea04786083e231360b1f64d2976789344955a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:31 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:31 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623dc20318c56f2d04936eb6f8a9897af2fb7ed80d1482687ffcb7a3305a003f`  
		Last Modified: Mon, 29 Dec 2025 23:53:25 GMT  
		Size: 42.3 MB (42293323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884f7b12fe8c3fdd29f7873c457a22c15797b87c9eb4fc3d1665c4bb4546876e`  
		Last Modified: Mon, 29 Dec 2025 23:53:21 GMT  
		Size: 1.6 MB (1566647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4b66b1700bab7c5f818c14dbc6b81c92b65af4a5c53a63a835c7c4b67419f4`  
		Last Modified: Mon, 29 Dec 2025 23:53:31 GMT  
		Size: 229.6 MB (229584744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4c562c03f2b4462b03e1e95a3148660c5e2edd0e1cd353d861b477d09c19fb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cc494622a5f6a14255f782d6d31c3f1898d9ec442199911941bb2c285d0700`

```dockerfile
```

-	Layers:
	-	`sha256:27095514af2f0bed0585ad1bc18c9ca1484cc655e4d8fde5688fbdfa3beca2ac`  
		Last Modified: Tue, 30 Dec 2025 03:54:18 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:562faca8a2198d098a17dea84f1f5bf82252107457b2ae5361d2a6ae123a41ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249840467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda0875958945d11786a6d10186bb46a644a9f10291d81234afb3d54c7dee7c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 08:42:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 11 Dec 2025 08:42:47 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Dec 2025 08:42:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 08:42:47 GMT
WORKDIR /root
# Thu, 11 Dec 2025 08:48:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad167056c1684d9fd70daef5b5d6c675f1f459163debcc0ca67b5999ef6fb297`  
		Last Modified: Thu, 11 Dec 2025 08:47:52 GMT  
		Size: 41.6 MB (41560777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8999e9abae129f285c549c47544c31e0f18872591db1bd7128872e607d214358`  
		Last Modified: Thu, 11 Dec 2025 08:47:46 GMT  
		Size: 1.6 MB (1567069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d36788d5cd40cb10770666deffca011203789dd0fb9d77bf4955ee12ffd5602`  
		Last Modified: Thu, 11 Dec 2025 10:01:14 GMT  
		Size: 178.4 MB (178439433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:62f7418567560db27b0fb84d16108980e254225be4d38c894f6e1ea8f73f9344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54fe31334dc86fc0aaa22d64e36fd2c9059b281146751489e968e9b9e49087e`

```dockerfile
```

-	Layers:
	-	`sha256:7638ff6890594999f475b9b7387b8ec38cc33066193594ec9a58d7c78eb981f5`  
		Last Modified: Thu, 11 Dec 2025 09:53:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:93bece41fe4ef52960ce54c332169d969f8f0b087831a183f30080a718c40df6
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
$ docker pull dart@sha256:16aae9cffef6e435ecda6eade25eeb77f8c052614503762f77b735df4ca3f876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287264685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1ceba46f05941e90c9006501c76b041e5704237157809d8b658c4a36196f55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:51:24 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:51:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:51:24 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:51:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399ba215801f5b0955b9fe11fff5ca84c54784453cd93ab354ad1d675d3a265`  
		Last Modified: Mon, 29 Dec 2025 23:52:15 GMT  
		Size: 42.5 MB (42494119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e00085b9951537636b893ee47fb679feb3e3d98c2f67075b5b816b801510ea1`  
		Last Modified: Mon, 29 Dec 2025 23:52:12 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591584856eb6f9206f73421780309da3e5611be6d4b8736d42e916527d179e5`  
		Last Modified: Mon, 29 Dec 2025 23:52:22 GMT  
		Size: 213.1 MB (213120383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4ebe645183ca354badb4669b16eb3ae71b1130df4ca0d030f7e6d5fd18a8ec3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ca8c77dd29f328e66eca3a2cb4a30c1acebbccb6036e53928615ecef5473a`

```dockerfile
```

-	Layers:
	-	`sha256:8a5b36d32e5f3ad9e797f47e39cc725f5779f86671a5cc78cf715d2ea31cb5c5`  
		Last Modified: Tue, 30 Dec 2025 03:53:49 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d90059d04dfbdd3b86c088d1b97c1f16f6c378637c4add7f28da601858b76dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219908007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b846d7e9c27c80c81b509085f089ea2316230687c8881f9b23aac8ce8baa78f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 30 Dec 2025 00:39:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 30 Dec 2025 00:39:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:39:59 GMT
WORKDIR /root
# Tue, 30 Dec 2025 00:40:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35905f4f4b79dd740f80ad1ad94571f5a363fa4aa54bd8d332493e4445a575a`  
		Last Modified: Tue, 30 Dec 2025 00:40:43 GMT  
		Size: 37.5 MB (37498459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fb33e3ebc2b6da90772f3b1fdf31bf2937e6182c743908971edbacdcf058a9`  
		Last Modified: Tue, 30 Dec 2025 00:40:40 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a21c0d56ebc32eb017b19866fbe9d2f5e6d23ee4f2d1f823ceb9c3dd441e4f7`  
		Last Modified: Tue, 30 Dec 2025 00:41:03 GMT  
		Size: 154.9 MB (154924393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ada1b02b23534206c1ac1b92ab9010a8cca380576d2af8bd6e27dfacc6804dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e1ae6177fa958c2c24ae65b7df8822ed56ae0e70f86ce58947b2fffb13e7ae`

```dockerfile
```

-	Layers:
	-	`sha256:177cbc68fa4ff25cdfd09c39184e9989211506f686d13a1c6a0647b1c9037599`  
		Last Modified: Tue, 30 Dec 2025 03:53:51 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3fc84852d8d2406fe7b59a8f3332e8df268edc4f623b858b00c3dbe414825ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286349358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1522b8b8cd4b1ea8fa38ca359dcd23a66ff17c7ef6c9e966bab4e1ca792693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 29 Dec 2025 23:52:13 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 29 Dec 2025 23:52:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:52:13 GMT
WORKDIR /root
# Mon, 29 Dec 2025 23:52:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1d7648050052a7c366ca9af13dd4472bb9bf3ab71157e8a873ea7220f9552`  
		Last Modified: Mon, 29 Dec 2025 23:53:04 GMT  
		Size: 42.3 MB (42293224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2a10287556154945da4f781b18665add3f90e2ba922591d2c7d3b7a1464da3`  
		Last Modified: Mon, 29 Dec 2025 23:53:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c060dfb6cbaa346a7f8e466774f95d753c74f19e70ef2873a50ddc6238735f1a`  
		Last Modified: Mon, 29 Dec 2025 23:53:10 GMT  
		Size: 212.4 MB (212350825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b78d256dbc58dae9871203d2ba4c1de692b55c74240e96ffac24a2d32f9a1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6761a896610ae0bc3d564c7f73a15556f72c16f6c6a8afbee23aac49131765e`

```dockerfile
```

-	Layers:
	-	`sha256:aadc2c804a306b781f7f408b05ec0919ffeb1bae0b82d41675f0d8bcb81b632e`  
		Last Modified: Tue, 30 Dec 2025 03:53:57 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:e802671271446437095fc506345b4f5d5a83ad599c03edaba604110a60fb22a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18e19b9e9bd189caf57943b581adae5362d41692083a30c1297549cbe3e3219`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 24 Dec 2025 06:13:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 24 Dec 2025 06:13:50 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 24 Dec 2025 06:13:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:13:50 GMT
WORKDIR /root
# Wed, 24 Dec 2025 06:14:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb5ade3b4e9a8f24869b39ad23438a603fde2d8a12ea624539070e8bc2c45e`  
		Last Modified: Wed, 24 Dec 2025 06:18:53 GMT  
		Size: 41.6 MB (41560696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682922fc41687ae3c133003349218fcde27010b9cc636c601fd7775d629e7c13`  
		Last Modified: Wed, 24 Dec 2025 06:18:50 GMT  
		Size: 1.6 MB (1567076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6e345b242f355d1fb540857d320a14664826b7f5e63b51c447e9336392d31`  
		Last Modified: Wed, 24 Dec 2025 07:01:13 GMT  
		Size: 161.6 MB (161562788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6b7ab8bfe0bcf679ca868fc935a9c0939230c305a0f3e190f829a15d319e7f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd9719d0b0baf4c1b80c9fd8e9d73b9280ac4d0e33667d7df96389a1705eb5b`

```dockerfile
```

-	Layers:
	-	`sha256:013a2d8351a1c42f55fdc85fae65a0ddaa900856de77863a0243b6f085551d90`  
		Last Modified: Wed, 24 Dec 2025 09:53:22 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
