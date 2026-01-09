<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10`](#dart310)
-	[`dart:3.10-sdk`](#dart310-sdk)
-	[`dart:3.10.7`](#dart3107)
-	[`dart:3.10.7-sdk`](#dart3107-sdk)
-	[`dart:3.11.0-296.2.beta`](#dart3110-2962beta)
-	[`dart:3.11.0-296.2.beta-sdk`](#dart3110-2962beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10-sdk`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.7`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.7-sdk`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-296.2.beta`

```console
$ docker pull dart@sha256:5d62742063e2a2609098bc6c78b5fa53c0fe9a29f1d7f6ce60407c88f03cba0d
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

### `dart:3.11.0-296.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:624726518dae59b422b65da8cd8fb5f2bc55c0937c940b95b1191e8b0ce4bc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307098689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568f06972aac0a279aa17139ffd74b33ee05e8bf842d82b43cec87b00bc44bbe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:05:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:05:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:05:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:05:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:05:51 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:06:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c3b779f1386e9859cf25c53908ff2ab8e4c0ada608bc5e74534b45ad804a4`  
		Last Modified: Thu, 08 Jan 2026 19:06:49 GMT  
		Size: 42.5 MB (42493667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff61e08c77335df4f9c4c38d0725749478c358bb8ac7bc24dec1689a115aae55`  
		Last Modified: Thu, 08 Jan 2026 19:06:44 GMT  
		Size: 1.9 MB (1873601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3da07d77c22b51141d1de8df829b6cd2d8b9f6b1e9481571317f285b23787d`  
		Last Modified: Thu, 08 Jan 2026 19:07:49 GMT  
		Size: 233.0 MB (232954856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:cec395b44938940645a28d16c14decf735ad9ba514ec9689b69f6f0cefe4513a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7691a4a2398d49b9b47ebaa5ca1d1d63a541ed874d87871ff6bc8344ce63fd85`

```dockerfile
```

-	Layers:
	-	`sha256:8a5fd747ac41d9962aca4482b2db1b1d7aab3a1b4b713bc654648dacbcc9f3d3`  
		Last Modified: Thu, 08 Jan 2026 21:53:29 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:7ee12064ef9a023b2fa86e978a5b16bc4971813a2a90a67dfd3af53244eaa2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222900247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed18a9393d5c206fd053b2ea42d4c0761a7abee9789734dcb64538a437990b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:04:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:04:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:04:05 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:04:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:04:05 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:04:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1516d24d3fa028611165774ce28e7006301684b55a6c8a1ee5bf436ae05425`  
		Last Modified: Thu, 08 Jan 2026 19:04:57 GMT  
		Size: 37.5 MB (37498489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794b8af47085a9593f12e84ffe85663411cce053cef9e12dcead13f457c48cef`  
		Last Modified: Thu, 08 Jan 2026 19:13:36 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e7525308e66f07e9f0898658e00dd80d512d1d9c70f290fcd54c2d4bf10f3f`  
		Last Modified: Thu, 08 Jan 2026 20:20:19 GMT  
		Size: 157.9 MB (157916603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:9be3da9e001c8e2c0929e16d0cf03927c81126fe0179291532dca25c6224128a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd28b89806645621bb7ed253983b1d6db5e470d822b67c024228b48705697fa7`

```dockerfile
```

-	Layers:
	-	`sha256:1911751b38b517418614dad57cddad44eee9324466d7712b4e948728e0d0237f`  
		Last Modified: Thu, 08 Jan 2026 21:53:33 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:766ea8321902bd65948a2ce2cdd8a06ed81633566380024855433cd272d821c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305475748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94367b38962e13f3af3814219150025424aeea58e6d8ab1818afd2db6d3c8afa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:07:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:07:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:07:39 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:07:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:07:39 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:07:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab15191003ab3b1a6ec45e2b972a5e33b1119a1c7ecbc03016548a39e3aa7b4`  
		Last Modified: Thu, 08 Jan 2026 19:08:39 GMT  
		Size: 42.3 MB (42292536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbbe1186eb6d57c193efab7b96a8721d633dc8d3640d96e35b6f3e8f70c1619`  
		Last Modified: Thu, 08 Jan 2026 19:08:34 GMT  
		Size: 1.6 MB (1566650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620aa91db4975161ad1b9bdb903e41a19fbd607acb0586c4704f9c7fc0ed238`  
		Last Modified: Thu, 08 Jan 2026 19:08:51 GMT  
		Size: 231.5 MB (231477894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:57a82f4c5df11cdcdffbddae9f26d34216572651bb57f2fe549b67c0d6acb6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30587d0675c4139326ce31941049f19be46dbacbf9c2e7e7f4751d22e3e505f4`

```dockerfile
```

-	Layers:
	-	`sha256:c4ffd721cda072cf62daf8933565137e5013b7896a88a9dd17bd3332136c0936`  
		Last Modified: Thu, 08 Jan 2026 21:53:36 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.2.beta` - linux; riscv64

```console
$ docker pull dart@sha256:2cfdd54bdc709dd57f5e9967e59dcf202795d53070353a674b7466068ed75939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b877615a26388ddead16a06e335acd030c2aaa08ad3ed4964cf6845f15b057d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:53:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:53:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:53:21 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7371402766e4abc95eaf0d0fca5d28b341ec201064383d231f20c9f6c9cbfd42`  
		Last Modified: Wed, 07 Jan 2026 17:59:02 GMT  
		Size: 41.6 MB (41560755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33684bab959ef2a5be84df6d39f37456a938f2f54f81fa698516adc65104c8b`  
		Last Modified: Wed, 07 Jan 2026 17:58:56 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20287815c4db5622d2036c3b61c21b86ac227bcbfc7a019cc23c3d372c0027`  
		Last Modified: Thu, 08 Jan 2026 19:09:04 GMT  
		Size: 180.5 MB (180493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:9ffb45d7609846f4cdfeec23d2d0f8a0f20aa8ff3b1abc4e57712587b0a74a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac32ba00dccfda38803d938d9c652855a1927a5b4ed811dc448294c7c79d096`

```dockerfile
```

-	Layers:
	-	`sha256:05c7bb5d7458d535a1e4271e1e71355be0072e8f31152f6a4ecca5a2c3a14823`  
		Last Modified: Thu, 08 Jan 2026 21:53:39 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-296.2.beta-sdk`

```console
$ docker pull dart@sha256:5d62742063e2a2609098bc6c78b5fa53c0fe9a29f1d7f6ce60407c88f03cba0d
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

### `dart:3.11.0-296.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:624726518dae59b422b65da8cd8fb5f2bc55c0937c940b95b1191e8b0ce4bc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307098689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568f06972aac0a279aa17139ffd74b33ee05e8bf842d82b43cec87b00bc44bbe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:05:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:05:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:05:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:05:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:05:51 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:06:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c3b779f1386e9859cf25c53908ff2ab8e4c0ada608bc5e74534b45ad804a4`  
		Last Modified: Thu, 08 Jan 2026 19:06:49 GMT  
		Size: 42.5 MB (42493667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff61e08c77335df4f9c4c38d0725749478c358bb8ac7bc24dec1689a115aae55`  
		Last Modified: Thu, 08 Jan 2026 19:06:44 GMT  
		Size: 1.9 MB (1873601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3da07d77c22b51141d1de8df829b6cd2d8b9f6b1e9481571317f285b23787d`  
		Last Modified: Thu, 08 Jan 2026 19:07:49 GMT  
		Size: 233.0 MB (232954856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cec395b44938940645a28d16c14decf735ad9ba514ec9689b69f6f0cefe4513a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7691a4a2398d49b9b47ebaa5ca1d1d63a541ed874d87871ff6bc8344ce63fd85`

```dockerfile
```

-	Layers:
	-	`sha256:8a5fd747ac41d9962aca4482b2db1b1d7aab3a1b4b713bc654648dacbcc9f3d3`  
		Last Modified: Thu, 08 Jan 2026 21:53:29 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:7ee12064ef9a023b2fa86e978a5b16bc4971813a2a90a67dfd3af53244eaa2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222900247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed18a9393d5c206fd053b2ea42d4c0761a7abee9789734dcb64538a437990b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:04:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:04:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:04:05 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:04:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:04:05 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:04:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1516d24d3fa028611165774ce28e7006301684b55a6c8a1ee5bf436ae05425`  
		Last Modified: Thu, 08 Jan 2026 19:04:57 GMT  
		Size: 37.5 MB (37498489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794b8af47085a9593f12e84ffe85663411cce053cef9e12dcead13f457c48cef`  
		Last Modified: Thu, 08 Jan 2026 19:13:36 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e7525308e66f07e9f0898658e00dd80d512d1d9c70f290fcd54c2d4bf10f3f`  
		Last Modified: Thu, 08 Jan 2026 20:20:19 GMT  
		Size: 157.9 MB (157916603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9be3da9e001c8e2c0929e16d0cf03927c81126fe0179291532dca25c6224128a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd28b89806645621bb7ed253983b1d6db5e470d822b67c024228b48705697fa7`

```dockerfile
```

-	Layers:
	-	`sha256:1911751b38b517418614dad57cddad44eee9324466d7712b4e948728e0d0237f`  
		Last Modified: Thu, 08 Jan 2026 21:53:33 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:766ea8321902bd65948a2ce2cdd8a06ed81633566380024855433cd272d821c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305475748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94367b38962e13f3af3814219150025424aeea58e6d8ab1818afd2db6d3c8afa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:07:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:07:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:07:39 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:07:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:07:39 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:07:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab15191003ab3b1a6ec45e2b972a5e33b1119a1c7ecbc03016548a39e3aa7b4`  
		Last Modified: Thu, 08 Jan 2026 19:08:39 GMT  
		Size: 42.3 MB (42292536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbbe1186eb6d57c193efab7b96a8721d633dc8d3640d96e35b6f3e8f70c1619`  
		Last Modified: Thu, 08 Jan 2026 19:08:34 GMT  
		Size: 1.6 MB (1566650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620aa91db4975161ad1b9bdb903e41a19fbd607acb0586c4704f9c7fc0ed238`  
		Last Modified: Thu, 08 Jan 2026 19:08:51 GMT  
		Size: 231.5 MB (231477894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57a82f4c5df11cdcdffbddae9f26d34216572651bb57f2fe549b67c0d6acb6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30587d0675c4139326ce31941049f19be46dbacbf9c2e7e7f4751d22e3e505f4`

```dockerfile
```

-	Layers:
	-	`sha256:c4ffd721cda072cf62daf8933565137e5013b7896a88a9dd17bd3332136c0936`  
		Last Modified: Thu, 08 Jan 2026 21:53:36 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.2.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:2cfdd54bdc709dd57f5e9967e59dcf202795d53070353a674b7466068ed75939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b877615a26388ddead16a06e335acd030c2aaa08ad3ed4964cf6845f15b057d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:53:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:53:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:53:21 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7371402766e4abc95eaf0d0fca5d28b341ec201064383d231f20c9f6c9cbfd42`  
		Last Modified: Wed, 07 Jan 2026 17:59:02 GMT  
		Size: 41.6 MB (41560755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33684bab959ef2a5be84df6d39f37456a938f2f54f81fa698516adc65104c8b`  
		Last Modified: Wed, 07 Jan 2026 17:58:56 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20287815c4db5622d2036c3b61c21b86ac227bcbfc7a019cc23c3d372c0027`  
		Last Modified: Thu, 08 Jan 2026 19:09:04 GMT  
		Size: 180.5 MB (180493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9ffb45d7609846f4cdfeec23d2d0f8a0f20aa8ff3b1abc4e57712587b0a74a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac32ba00dccfda38803d938d9c652855a1927a5b4ed811dc448294c7c79d096`

```dockerfile
```

-	Layers:
	-	`sha256:05c7bb5d7458d535a1e4271e1e71355be0072e8f31152f6a4ecca5a2c3a14823`  
		Last Modified: Thu, 08 Jan 2026 21:53:39 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:5d62742063e2a2609098bc6c78b5fa53c0fe9a29f1d7f6ce60407c88f03cba0d
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
$ docker pull dart@sha256:624726518dae59b422b65da8cd8fb5f2bc55c0937c940b95b1191e8b0ce4bc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307098689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568f06972aac0a279aa17139ffd74b33ee05e8bf842d82b43cec87b00bc44bbe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:05:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:05:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:05:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:05:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:05:51 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:06:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c3b779f1386e9859cf25c53908ff2ab8e4c0ada608bc5e74534b45ad804a4`  
		Last Modified: Thu, 08 Jan 2026 19:06:49 GMT  
		Size: 42.5 MB (42493667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff61e08c77335df4f9c4c38d0725749478c358bb8ac7bc24dec1689a115aae55`  
		Last Modified: Thu, 08 Jan 2026 19:06:44 GMT  
		Size: 1.9 MB (1873601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3da07d77c22b51141d1de8df829b6cd2d8b9f6b1e9481571317f285b23787d`  
		Last Modified: Thu, 08 Jan 2026 19:07:49 GMT  
		Size: 233.0 MB (232954856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:cec395b44938940645a28d16c14decf735ad9ba514ec9689b69f6f0cefe4513a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7691a4a2398d49b9b47ebaa5ca1d1d63a541ed874d87871ff6bc8344ce63fd85`

```dockerfile
```

-	Layers:
	-	`sha256:8a5fd747ac41d9962aca4482b2db1b1d7aab3a1b4b713bc654648dacbcc9f3d3`  
		Last Modified: Thu, 08 Jan 2026 21:53:29 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:7ee12064ef9a023b2fa86e978a5b16bc4971813a2a90a67dfd3af53244eaa2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222900247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed18a9393d5c206fd053b2ea42d4c0761a7abee9789734dcb64538a437990b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:04:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:04:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:04:05 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:04:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:04:05 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:04:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1516d24d3fa028611165774ce28e7006301684b55a6c8a1ee5bf436ae05425`  
		Last Modified: Thu, 08 Jan 2026 19:04:57 GMT  
		Size: 37.5 MB (37498489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794b8af47085a9593f12e84ffe85663411cce053cef9e12dcead13f457c48cef`  
		Last Modified: Thu, 08 Jan 2026 19:13:36 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e7525308e66f07e9f0898658e00dd80d512d1d9c70f290fcd54c2d4bf10f3f`  
		Last Modified: Thu, 08 Jan 2026 20:20:19 GMT  
		Size: 157.9 MB (157916603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:9be3da9e001c8e2c0929e16d0cf03927c81126fe0179291532dca25c6224128a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd28b89806645621bb7ed253983b1d6db5e470d822b67c024228b48705697fa7`

```dockerfile
```

-	Layers:
	-	`sha256:1911751b38b517418614dad57cddad44eee9324466d7712b4e948728e0d0237f`  
		Last Modified: Thu, 08 Jan 2026 21:53:33 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:766ea8321902bd65948a2ce2cdd8a06ed81633566380024855433cd272d821c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305475748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94367b38962e13f3af3814219150025424aeea58e6d8ab1818afd2db6d3c8afa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:07:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:07:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:07:39 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:07:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:07:39 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:07:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab15191003ab3b1a6ec45e2b972a5e33b1119a1c7ecbc03016548a39e3aa7b4`  
		Last Modified: Thu, 08 Jan 2026 19:08:39 GMT  
		Size: 42.3 MB (42292536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbbe1186eb6d57c193efab7b96a8721d633dc8d3640d96e35b6f3e8f70c1619`  
		Last Modified: Thu, 08 Jan 2026 19:08:34 GMT  
		Size: 1.6 MB (1566650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620aa91db4975161ad1b9bdb903e41a19fbd607acb0586c4704f9c7fc0ed238`  
		Last Modified: Thu, 08 Jan 2026 19:08:51 GMT  
		Size: 231.5 MB (231477894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:57a82f4c5df11cdcdffbddae9f26d34216572651bb57f2fe549b67c0d6acb6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30587d0675c4139326ce31941049f19be46dbacbf9c2e7e7f4751d22e3e505f4`

```dockerfile
```

-	Layers:
	-	`sha256:c4ffd721cda072cf62daf8933565137e5013b7896a88a9dd17bd3332136c0936`  
		Last Modified: Thu, 08 Jan 2026 21:53:36 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:2cfdd54bdc709dd57f5e9967e59dcf202795d53070353a674b7466068ed75939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b877615a26388ddead16a06e335acd030c2aaa08ad3ed4964cf6845f15b057d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:53:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:53:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:53:21 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7371402766e4abc95eaf0d0fca5d28b341ec201064383d231f20c9f6c9cbfd42`  
		Last Modified: Wed, 07 Jan 2026 17:59:02 GMT  
		Size: 41.6 MB (41560755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33684bab959ef2a5be84df6d39f37456a938f2f54f81fa698516adc65104c8b`  
		Last Modified: Wed, 07 Jan 2026 17:58:56 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20287815c4db5622d2036c3b61c21b86ac227bcbfc7a019cc23c3d372c0027`  
		Last Modified: Thu, 08 Jan 2026 19:09:04 GMT  
		Size: 180.5 MB (180493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:9ffb45d7609846f4cdfeec23d2d0f8a0f20aa8ff3b1abc4e57712587b0a74a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac32ba00dccfda38803d938d9c652855a1927a5b4ed811dc448294c7c79d096`

```dockerfile
```

-	Layers:
	-	`sha256:05c7bb5d7458d535a1e4271e1e71355be0072e8f31152f6a4ecca5a2c3a14823`  
		Last Modified: Thu, 08 Jan 2026 21:53:39 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:5d62742063e2a2609098bc6c78b5fa53c0fe9a29f1d7f6ce60407c88f03cba0d
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
$ docker pull dart@sha256:624726518dae59b422b65da8cd8fb5f2bc55c0937c940b95b1191e8b0ce4bc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307098689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568f06972aac0a279aa17139ffd74b33ee05e8bf842d82b43cec87b00bc44bbe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:05:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:05:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:05:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:05:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:05:51 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:06:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4c3b779f1386e9859cf25c53908ff2ab8e4c0ada608bc5e74534b45ad804a4`  
		Last Modified: Thu, 08 Jan 2026 19:06:49 GMT  
		Size: 42.5 MB (42493667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff61e08c77335df4f9c4c38d0725749478c358bb8ac7bc24dec1689a115aae55`  
		Last Modified: Thu, 08 Jan 2026 19:06:44 GMT  
		Size: 1.9 MB (1873601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3da07d77c22b51141d1de8df829b6cd2d8b9f6b1e9481571317f285b23787d`  
		Last Modified: Thu, 08 Jan 2026 19:07:49 GMT  
		Size: 233.0 MB (232954856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cec395b44938940645a28d16c14decf735ad9ba514ec9689b69f6f0cefe4513a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7691a4a2398d49b9b47ebaa5ca1d1d63a541ed874d87871ff6bc8344ce63fd85`

```dockerfile
```

-	Layers:
	-	`sha256:8a5fd747ac41d9962aca4482b2db1b1d7aab3a1b4b713bc654648dacbcc9f3d3`  
		Last Modified: Thu, 08 Jan 2026 21:53:29 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:7ee12064ef9a023b2fa86e978a5b16bc4971813a2a90a67dfd3af53244eaa2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222900247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed18a9393d5c206fd053b2ea42d4c0761a7abee9789734dcb64538a437990b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:04:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:04:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:04:05 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:04:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:04:05 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:04:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1516d24d3fa028611165774ce28e7006301684b55a6c8a1ee5bf436ae05425`  
		Last Modified: Thu, 08 Jan 2026 19:04:57 GMT  
		Size: 37.5 MB (37498489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794b8af47085a9593f12e84ffe85663411cce053cef9e12dcead13f457c48cef`  
		Last Modified: Thu, 08 Jan 2026 19:13:36 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e7525308e66f07e9f0898658e00dd80d512d1d9c70f290fcd54c2d4bf10f3f`  
		Last Modified: Thu, 08 Jan 2026 20:20:19 GMT  
		Size: 157.9 MB (157916603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9be3da9e001c8e2c0929e16d0cf03927c81126fe0179291532dca25c6224128a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd28b89806645621bb7ed253983b1d6db5e470d822b67c024228b48705697fa7`

```dockerfile
```

-	Layers:
	-	`sha256:1911751b38b517418614dad57cddad44eee9324466d7712b4e948728e0d0237f`  
		Last Modified: Thu, 08 Jan 2026 21:53:33 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:766ea8321902bd65948a2ce2cdd8a06ed81633566380024855433cd272d821c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305475748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94367b38962e13f3af3814219150025424aeea58e6d8ab1818afd2db6d3c8afa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Thu, 08 Jan 2026 19:07:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:07:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 08 Jan 2026 19:07:39 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 08 Jan 2026 19:07:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:07:39 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:07:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab15191003ab3b1a6ec45e2b972a5e33b1119a1c7ecbc03016548a39e3aa7b4`  
		Last Modified: Thu, 08 Jan 2026 19:08:39 GMT  
		Size: 42.3 MB (42292536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbbe1186eb6d57c193efab7b96a8721d633dc8d3640d96e35b6f3e8f70c1619`  
		Last Modified: Thu, 08 Jan 2026 19:08:34 GMT  
		Size: 1.6 MB (1566650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620aa91db4975161ad1b9bdb903e41a19fbd607acb0586c4704f9c7fc0ed238`  
		Last Modified: Thu, 08 Jan 2026 19:08:51 GMT  
		Size: 231.5 MB (231477894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57a82f4c5df11cdcdffbddae9f26d34216572651bb57f2fe549b67c0d6acb6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30587d0675c4139326ce31941049f19be46dbacbf9c2e7e7f4751d22e3e505f4`

```dockerfile
```

-	Layers:
	-	`sha256:c4ffd721cda072cf62daf8933565137e5013b7896a88a9dd17bd3332136c0936`  
		Last Modified: Thu, 08 Jan 2026 21:53:36 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:2cfdd54bdc709dd57f5e9967e59dcf202795d53070353a674b7466068ed75939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b877615a26388ddead16a06e335acd030c2aaa08ad3ed4964cf6845f15b057d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:53:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:53:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:53:21 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7371402766e4abc95eaf0d0fca5d28b341ec201064383d231f20c9f6c9cbfd42`  
		Last Modified: Wed, 07 Jan 2026 17:59:02 GMT  
		Size: 41.6 MB (41560755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33684bab959ef2a5be84df6d39f37456a938f2f54f81fa698516adc65104c8b`  
		Last Modified: Wed, 07 Jan 2026 17:58:56 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20287815c4db5622d2036c3b61c21b86ac227bcbfc7a019cc23c3d372c0027`  
		Last Modified: Thu, 08 Jan 2026 19:09:04 GMT  
		Size: 180.5 MB (180493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:9ffb45d7609846f4cdfeec23d2d0f8a0f20aa8ff3b1abc4e57712587b0a74a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac32ba00dccfda38803d938d9c652855a1927a5b4ed811dc448294c7c79d096`

```dockerfile
```

-	Layers:
	-	`sha256:05c7bb5d7458d535a1e4271e1e71355be0072e8f31152f6a4ecca5a2c3a14823`  
		Last Modified: Thu, 08 Jan 2026 21:53:39 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:da57a8fe35ff09c18d7c12fccc223b2f26908db837a3d8752e50c9eb7049839c
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
$ docker pull dart@sha256:206a7416f2b9b67cb7f8b0f36b63014436667a4e751ce127b557fe3f05ed7b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232963690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154336063b24e78138a297527297885f919b02ca033eb85c19db92332d399c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:19:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 31 Dec 2025 10:19:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Dec 2025 10:19:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Dec 2025 10:19:31 GMT
WORKDIR /root
# Wed, 31 Dec 2025 10:20:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8a4eeacf4d7690e03389d6328241bc69a1b61cb980f23d50f62ebacb5920ec74;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9638b38559de736ca6ee1fd4d78b23b3f6c8d341e20b657a2a44ca6b90afda86;             SDK_ARCH="arm";;         arm64)             DART_SHA256=81bdcd8828606981713c513e3d4377eeedec431c46bf35f3277c6abaf2d7bd51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dc3103fc6041556b816f07060c5a29d42b348886dbc8c5f34cb91a7f3bc7be9b;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00638884bf67e17413e83e373290e17ac45605178a8f610de8d093c97be477d`  
		Last Modified: Wed, 31 Dec 2025 10:24:44 GMT  
		Size: 41.6 MB (41560727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dacd48722b98fce8b7f8e416eae47df82b1b2df087aff653832b95484000bc5`  
		Last Modified: Wed, 31 Dec 2025 10:24:41 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f05087c6282274ef144a9afaa6b38e7754393905e5bcbace29048ad6bf399`  
		Last Modified: Wed, 31 Dec 2025 10:24:50 GMT  
		Size: 161.6 MB (161562730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:189c22c1d9d9d23ca92db17bf20e025de21aa8fffcc8d63944822644050f2bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfecc80afad7f43084fca96fa9aff21d55886ba99d5f4e71e67972d9fefbf883`

```dockerfile
```

-	Layers:
	-	`sha256:259dd0b0bc03d44b4cfcc761e551aad027586e0428741987ef029a8ea8346e84`  
		Last Modified: Wed, 31 Dec 2025 12:53:23 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
