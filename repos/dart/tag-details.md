<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10`](#dart310)
-	[`dart:3.10-sdk`](#dart310-sdk)
-	[`dart:3.10.7`](#dart3107)
-	[`dart:3.10.7-sdk`](#dart3107-sdk)
-	[`dart:3.11.0-296.1.beta`](#dart3110-2961beta)
-	[`dart:3.11.0-296.1.beta-sdk`](#dart3110-2961beta-sdk)
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

## `dart:3.11.0-296.1.beta`

```console
$ docker pull dart@sha256:d256655791f0d24c4028c182675123e922fbcf8978c7ad2693293c100ad2abe1
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

### `dart:3.11.0-296.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:62c68f17891b4e2ceb4786cc0387c205af9a60ea600c33888a21c10a9fb08a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307098575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e10cae157c0299b962ec1125a73ebbefe50950af7cd59a048cf52a634af614e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:50:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:50:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:50:52 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:50:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:50:52 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:51:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e934391056c6d631f12449cb42253756ab099672c3d866e4f381d6be5bc7a`  
		Last Modified: Wed, 07 Jan 2026 17:52:05 GMT  
		Size: 42.5 MB (42494275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbca804ee2f8187e29bf0153d54ad20a13723783147ec50b5f02462cd41bdae5`  
		Last Modified: Wed, 07 Jan 2026 17:51:59 GMT  
		Size: 1.9 MB (1873625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbcb35814a5c2f8fd64278c3a3080e717c3a3891ed4e580a28db66e8ed97927`  
		Last Modified: Wed, 07 Jan 2026 17:53:34 GMT  
		Size: 233.0 MB (232954110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:1110c277753aaeb99596fef34340a4a363b579ceab60295066e4a34bbc625bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c65b5451d3d33d1670e3df8b26ca60849cf6ad234cd2a876db5b42259789367`

```dockerfile
```

-	Layers:
	-	`sha256:d98f6f00979923adf9cb0d788b396f414a0e1960270bf29f95328f7ae2265378`  
		Last Modified: Wed, 07 Jan 2026 18:53:29 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:55b474e48f53971f82f78f37c53e15a7a14a1bbd5a600afcf74387b87b277648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3498d938934e61d4404509ae9d81b7f713731d708930814d73d4a285392a96`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:52:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:52:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:52:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:52:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:52:43 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:52:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1887bce0e19ca576ff7c4aeb7fa22c03210d7fb65adf1b3dfeba305ed5c9bf`  
		Last Modified: Wed, 07 Jan 2026 17:53:35 GMT  
		Size: 37.5 MB (37498369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada461ffe0b58475ad4e8fc5e89fae60875e206ef16fdad27f16536694122830`  
		Last Modified: Wed, 07 Jan 2026 17:53:31 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0623eb3d480202a2b76f85bc5df5bd6c968f1f745b5385d58f9cde7af422d787`  
		Last Modified: Wed, 07 Jan 2026 17:53:45 GMT  
		Size: 157.9 MB (157915855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:315d3d9600f07cae6383adaa3de0e687d8fd5dd49ce96ee5a122afb3f9a6025a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd47c0c3e210d11213eed5f7044893b8dacf2ecf5bbd6ed5eeaed8cb52226ec`

```dockerfile
```

-	Layers:
	-	`sha256:e086b49bf675648b23bee12f7761fdd935ed0e697fe51d1738903e2a03367d5f`  
		Last Modified: Wed, 07 Jan 2026 18:53:33 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3000bf85fe94f5603882cec63dc648059bccf6505d3d6d8034beb6145bc10dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305476612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d01bbde6690b997732f9e94804ae46cd19aea8e317c54f2c38d803fab46d0ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:52:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:52:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:52:10 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:52:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:52:10 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:52:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61a76a6d9e25ec9e53962905d6faf4d3f15bfd4e765924dacbcd79d8861d41`  
		Last Modified: Wed, 07 Jan 2026 17:53:24 GMT  
		Size: 42.3 MB (42293344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf9746c470f8298d71a63784523435d1fd7413a4f8a9e72bce00f2499d14f75`  
		Last Modified: Wed, 07 Jan 2026 17:53:20 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95efa40606926f85361ea0532fc90ab1bf1c77b635c42ce511915f0b763b1b1`  
		Last Modified: Wed, 07 Jan 2026 17:54:43 GMT  
		Size: 231.5 MB (231477954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:6dce2f3998002dd9234a6ada8385582a3b52ea2436e7ab9a48a72860c5971851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc20c3c908612d754236a0baa52bedc35bccabb36902e5ced7937fd5676a540`

```dockerfile
```

-	Layers:
	-	`sha256:88f7279a2e4479e86d266131b1d4e6b8b53460ae91b3d4ca1a9444f045fabea3`  
		Last Modified: Wed, 07 Jan 2026 18:53:36 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.1.beta` - linux; riscv64

```console
$ docker pull dart@sha256:e650d5abc68e5b7aff3faed8f66a79e1044c06ab7cd466d96dbfeee13f1ce6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110033cbb0e7862e7adab578bbe8ae1c53b795a820f92c9542ceafbb4497c20`
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
# Wed, 07 Jan 2026 17:54:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:eda7757ffd2ae490f0ae5d1b41f7a16a5467f66db5ceb43abc25164572fb344f`  
		Last Modified: Wed, 07 Jan 2026 17:59:16 GMT  
		Size: 180.5 MB (180493045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:5e16ca410bc2f12c8e7a9874874ca3682f26445816b92e0a4ae9a90510dadfa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c276762d830affc6299aecd9f3e0bac8af3a2c078667c5bc1cea2bfa64e8d04a`

```dockerfile
```

-	Layers:
	-	`sha256:c6c7b1c46e93e3dc234f893e4da79cd96e0ffdfc189e93c477f9744a94a7ebe0`  
		Last Modified: Wed, 07 Jan 2026 18:53:39 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-296.1.beta-sdk`

```console
$ docker pull dart@sha256:d256655791f0d24c4028c182675123e922fbcf8978c7ad2693293c100ad2abe1
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

### `dart:3.11.0-296.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:62c68f17891b4e2ceb4786cc0387c205af9a60ea600c33888a21c10a9fb08a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307098575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e10cae157c0299b962ec1125a73ebbefe50950af7cd59a048cf52a634af614e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:50:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:50:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:50:52 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:50:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:50:52 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:51:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e934391056c6d631f12449cb42253756ab099672c3d866e4f381d6be5bc7a`  
		Last Modified: Wed, 07 Jan 2026 17:52:05 GMT  
		Size: 42.5 MB (42494275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbca804ee2f8187e29bf0153d54ad20a13723783147ec50b5f02462cd41bdae5`  
		Last Modified: Wed, 07 Jan 2026 17:51:59 GMT  
		Size: 1.9 MB (1873625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbcb35814a5c2f8fd64278c3a3080e717c3a3891ed4e580a28db66e8ed97927`  
		Last Modified: Wed, 07 Jan 2026 17:53:34 GMT  
		Size: 233.0 MB (232954110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1110c277753aaeb99596fef34340a4a363b579ceab60295066e4a34bbc625bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c65b5451d3d33d1670e3df8b26ca60849cf6ad234cd2a876db5b42259789367`

```dockerfile
```

-	Layers:
	-	`sha256:d98f6f00979923adf9cb0d788b396f414a0e1960270bf29f95328f7ae2265378`  
		Last Modified: Wed, 07 Jan 2026 18:53:29 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:55b474e48f53971f82f78f37c53e15a7a14a1bbd5a600afcf74387b87b277648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3498d938934e61d4404509ae9d81b7f713731d708930814d73d4a285392a96`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:52:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:52:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:52:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:52:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:52:43 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:52:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1887bce0e19ca576ff7c4aeb7fa22c03210d7fb65adf1b3dfeba305ed5c9bf`  
		Last Modified: Wed, 07 Jan 2026 17:53:35 GMT  
		Size: 37.5 MB (37498369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada461ffe0b58475ad4e8fc5e89fae60875e206ef16fdad27f16536694122830`  
		Last Modified: Wed, 07 Jan 2026 17:53:31 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0623eb3d480202a2b76f85bc5df5bd6c968f1f745b5385d58f9cde7af422d787`  
		Last Modified: Wed, 07 Jan 2026 17:53:45 GMT  
		Size: 157.9 MB (157915855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:315d3d9600f07cae6383adaa3de0e687d8fd5dd49ce96ee5a122afb3f9a6025a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd47c0c3e210d11213eed5f7044893b8dacf2ecf5bbd6ed5eeaed8cb52226ec`

```dockerfile
```

-	Layers:
	-	`sha256:e086b49bf675648b23bee12f7761fdd935ed0e697fe51d1738903e2a03367d5f`  
		Last Modified: Wed, 07 Jan 2026 18:53:33 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3000bf85fe94f5603882cec63dc648059bccf6505d3d6d8034beb6145bc10dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305476612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d01bbde6690b997732f9e94804ae46cd19aea8e317c54f2c38d803fab46d0ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:52:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:52:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:52:10 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:52:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:52:10 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:52:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61a76a6d9e25ec9e53962905d6faf4d3f15bfd4e765924dacbcd79d8861d41`  
		Last Modified: Wed, 07 Jan 2026 17:53:24 GMT  
		Size: 42.3 MB (42293344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf9746c470f8298d71a63784523435d1fd7413a4f8a9e72bce00f2499d14f75`  
		Last Modified: Wed, 07 Jan 2026 17:53:20 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95efa40606926f85361ea0532fc90ab1bf1c77b635c42ce511915f0b763b1b1`  
		Last Modified: Wed, 07 Jan 2026 17:54:43 GMT  
		Size: 231.5 MB (231477954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6dce2f3998002dd9234a6ada8385582a3b52ea2436e7ab9a48a72860c5971851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc20c3c908612d754236a0baa52bedc35bccabb36902e5ced7937fd5676a540`

```dockerfile
```

-	Layers:
	-	`sha256:88f7279a2e4479e86d266131b1d4e6b8b53460ae91b3d4ca1a9444f045fabea3`  
		Last Modified: Wed, 07 Jan 2026 18:53:36 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-296.1.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:e650d5abc68e5b7aff3faed8f66a79e1044c06ab7cd466d96dbfeee13f1ce6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110033cbb0e7862e7adab578bbe8ae1c53b795a820f92c9542ceafbb4497c20`
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
# Wed, 07 Jan 2026 17:54:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:eda7757ffd2ae490f0ae5d1b41f7a16a5467f66db5ceb43abc25164572fb344f`  
		Last Modified: Wed, 07 Jan 2026 17:59:16 GMT  
		Size: 180.5 MB (180493045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-296.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5e16ca410bc2f12c8e7a9874874ca3682f26445816b92e0a4ae9a90510dadfa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c276762d830affc6299aecd9f3e0bac8af3a2c078667c5bc1cea2bfa64e8d04a`

```dockerfile
```

-	Layers:
	-	`sha256:c6c7b1c46e93e3dc234f893e4da79cd96e0ffdfc189e93c477f9744a94a7ebe0`  
		Last Modified: Wed, 07 Jan 2026 18:53:39 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:d256655791f0d24c4028c182675123e922fbcf8978c7ad2693293c100ad2abe1
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
$ docker pull dart@sha256:62c68f17891b4e2ceb4786cc0387c205af9a60ea600c33888a21c10a9fb08a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307098575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e10cae157c0299b962ec1125a73ebbefe50950af7cd59a048cf52a634af614e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:50:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:50:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:50:52 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:50:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:50:52 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:51:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e934391056c6d631f12449cb42253756ab099672c3d866e4f381d6be5bc7a`  
		Last Modified: Wed, 07 Jan 2026 17:52:05 GMT  
		Size: 42.5 MB (42494275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbca804ee2f8187e29bf0153d54ad20a13723783147ec50b5f02462cd41bdae5`  
		Last Modified: Wed, 07 Jan 2026 17:51:59 GMT  
		Size: 1.9 MB (1873625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbcb35814a5c2f8fd64278c3a3080e717c3a3891ed4e580a28db66e8ed97927`  
		Last Modified: Wed, 07 Jan 2026 17:53:34 GMT  
		Size: 233.0 MB (232954110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:1110c277753aaeb99596fef34340a4a363b579ceab60295066e4a34bbc625bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c65b5451d3d33d1670e3df8b26ca60849cf6ad234cd2a876db5b42259789367`

```dockerfile
```

-	Layers:
	-	`sha256:d98f6f00979923adf9cb0d788b396f414a0e1960270bf29f95328f7ae2265378`  
		Last Modified: Wed, 07 Jan 2026 18:53:29 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:55b474e48f53971f82f78f37c53e15a7a14a1bbd5a600afcf74387b87b277648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3498d938934e61d4404509ae9d81b7f713731d708930814d73d4a285392a96`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:52:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:52:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:52:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:52:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:52:43 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:52:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1887bce0e19ca576ff7c4aeb7fa22c03210d7fb65adf1b3dfeba305ed5c9bf`  
		Last Modified: Wed, 07 Jan 2026 17:53:35 GMT  
		Size: 37.5 MB (37498369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada461ffe0b58475ad4e8fc5e89fae60875e206ef16fdad27f16536694122830`  
		Last Modified: Wed, 07 Jan 2026 17:53:31 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0623eb3d480202a2b76f85bc5df5bd6c968f1f745b5385d58f9cde7af422d787`  
		Last Modified: Wed, 07 Jan 2026 17:53:45 GMT  
		Size: 157.9 MB (157915855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:315d3d9600f07cae6383adaa3de0e687d8fd5dd49ce96ee5a122afb3f9a6025a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd47c0c3e210d11213eed5f7044893b8dacf2ecf5bbd6ed5eeaed8cb52226ec`

```dockerfile
```

-	Layers:
	-	`sha256:e086b49bf675648b23bee12f7761fdd935ed0e697fe51d1738903e2a03367d5f`  
		Last Modified: Wed, 07 Jan 2026 18:53:33 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3000bf85fe94f5603882cec63dc648059bccf6505d3d6d8034beb6145bc10dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305476612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d01bbde6690b997732f9e94804ae46cd19aea8e317c54f2c38d803fab46d0ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:52:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:52:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:52:10 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:52:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:52:10 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:52:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61a76a6d9e25ec9e53962905d6faf4d3f15bfd4e765924dacbcd79d8861d41`  
		Last Modified: Wed, 07 Jan 2026 17:53:24 GMT  
		Size: 42.3 MB (42293344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf9746c470f8298d71a63784523435d1fd7413a4f8a9e72bce00f2499d14f75`  
		Last Modified: Wed, 07 Jan 2026 17:53:20 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95efa40606926f85361ea0532fc90ab1bf1c77b635c42ce511915f0b763b1b1`  
		Last Modified: Wed, 07 Jan 2026 17:54:43 GMT  
		Size: 231.5 MB (231477954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:6dce2f3998002dd9234a6ada8385582a3b52ea2436e7ab9a48a72860c5971851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc20c3c908612d754236a0baa52bedc35bccabb36902e5ced7937fd5676a540`

```dockerfile
```

-	Layers:
	-	`sha256:88f7279a2e4479e86d266131b1d4e6b8b53460ae91b3d4ca1a9444f045fabea3`  
		Last Modified: Wed, 07 Jan 2026 18:53:36 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:e650d5abc68e5b7aff3faed8f66a79e1044c06ab7cd466d96dbfeee13f1ce6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110033cbb0e7862e7adab578bbe8ae1c53b795a820f92c9542ceafbb4497c20`
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
# Wed, 07 Jan 2026 17:54:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:eda7757ffd2ae490f0ae5d1b41f7a16a5467f66db5ceb43abc25164572fb344f`  
		Last Modified: Wed, 07 Jan 2026 17:59:16 GMT  
		Size: 180.5 MB (180493045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:5e16ca410bc2f12c8e7a9874874ca3682f26445816b92e0a4ae9a90510dadfa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c276762d830affc6299aecd9f3e0bac8af3a2c078667c5bc1cea2bfa64e8d04a`

```dockerfile
```

-	Layers:
	-	`sha256:c6c7b1c46e93e3dc234f893e4da79cd96e0ffdfc189e93c477f9744a94a7ebe0`  
		Last Modified: Wed, 07 Jan 2026 18:53:39 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:d256655791f0d24c4028c182675123e922fbcf8978c7ad2693293c100ad2abe1
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
$ docker pull dart@sha256:62c68f17891b4e2ceb4786cc0387c205af9a60ea600c33888a21c10a9fb08a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307098575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e10cae157c0299b962ec1125a73ebbefe50950af7cd59a048cf52a634af614e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:50:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:50:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:50:52 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:50:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:50:52 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:51:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e934391056c6d631f12449cb42253756ab099672c3d866e4f381d6be5bc7a`  
		Last Modified: Wed, 07 Jan 2026 17:52:05 GMT  
		Size: 42.5 MB (42494275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbca804ee2f8187e29bf0153d54ad20a13723783147ec50b5f02462cd41bdae5`  
		Last Modified: Wed, 07 Jan 2026 17:51:59 GMT  
		Size: 1.9 MB (1873625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbcb35814a5c2f8fd64278c3a3080e717c3a3891ed4e580a28db66e8ed97927`  
		Last Modified: Wed, 07 Jan 2026 17:53:34 GMT  
		Size: 233.0 MB (232954110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1110c277753aaeb99596fef34340a4a363b579ceab60295066e4a34bbc625bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c65b5451d3d33d1670e3df8b26ca60849cf6ad234cd2a876db5b42259789367`

```dockerfile
```

-	Layers:
	-	`sha256:d98f6f00979923adf9cb0d788b396f414a0e1960270bf29f95328f7ae2265378`  
		Last Modified: Wed, 07 Jan 2026 18:53:29 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:55b474e48f53971f82f78f37c53e15a7a14a1bbd5a600afcf74387b87b277648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222899377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3498d938934e61d4404509ae9d81b7f713731d708930814d73d4a285392a96`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:52:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:52:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:52:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:52:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:52:43 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:52:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1887bce0e19ca576ff7c4aeb7fa22c03210d7fb65adf1b3dfeba305ed5c9bf`  
		Last Modified: Wed, 07 Jan 2026 17:53:35 GMT  
		Size: 37.5 MB (37498369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada461ffe0b58475ad4e8fc5e89fae60875e206ef16fdad27f16536694122830`  
		Last Modified: Wed, 07 Jan 2026 17:53:31 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0623eb3d480202a2b76f85bc5df5bd6c968f1f745b5385d58f9cde7af422d787`  
		Last Modified: Wed, 07 Jan 2026 17:53:45 GMT  
		Size: 157.9 MB (157915855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:315d3d9600f07cae6383adaa3de0e687d8fd5dd49ce96ee5a122afb3f9a6025a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd47c0c3e210d11213eed5f7044893b8dacf2ecf5bbd6ed5eeaed8cb52226ec`

```dockerfile
```

-	Layers:
	-	`sha256:e086b49bf675648b23bee12f7761fdd935ed0e697fe51d1738903e2a03367d5f`  
		Last Modified: Wed, 07 Jan 2026 18:53:33 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3000bf85fe94f5603882cec63dc648059bccf6505d3d6d8034beb6145bc10dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305476612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d01bbde6690b997732f9e94804ae46cd19aea8e317c54f2c38d803fab46d0ce`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:52:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:52:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:52:10 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:52:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:52:10 GMT
WORKDIR /root
# Wed, 07 Jan 2026 17:52:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61a76a6d9e25ec9e53962905d6faf4d3f15bfd4e765924dacbcd79d8861d41`  
		Last Modified: Wed, 07 Jan 2026 17:53:24 GMT  
		Size: 42.3 MB (42293344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf9746c470f8298d71a63784523435d1fd7413a4f8a9e72bce00f2499d14f75`  
		Last Modified: Wed, 07 Jan 2026 17:53:20 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95efa40606926f85361ea0532fc90ab1bf1c77b635c42ce511915f0b763b1b1`  
		Last Modified: Wed, 07 Jan 2026 17:54:43 GMT  
		Size: 231.5 MB (231477954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6dce2f3998002dd9234a6ada8385582a3b52ea2436e7ab9a48a72860c5971851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc20c3c908612d754236a0baa52bedc35bccabb36902e5ced7937fd5676a540`

```dockerfile
```

-	Layers:
	-	`sha256:88f7279a2e4479e86d266131b1d4e6b8b53460ae91b3d4ca1a9444f045fabea3`  
		Last Modified: Wed, 07 Jan 2026 18:53:36 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:e650d5abc68e5b7aff3faed8f66a79e1044c06ab7cd466d96dbfeee13f1ce6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c110033cbb0e7862e7adab578bbe8ae1c53b795a820f92c9542ceafbb4497c20`
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
# Wed, 07 Jan 2026 17:54:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=163831e359ee9aae24d17d3570935d5be37becc2d6f45e4943931ae6d9f0ac21;             SDK_ARCH="x64";;         armhf)             DART_SHA256=5fdb41493e4ed1d0157a227b5438d691b4ff29e2b5c214b397f895ccaa7c1d1e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=cdf24a4342bd9b139dca341f83d43cdc5bcb536cc8858e1bc25cdc481c5435cc;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=2a2bcf8fbff979a8e15d9156d6ce1e23e21d60151806a7ea80e720f1e94a3225;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:eda7757ffd2ae490f0ae5d1b41f7a16a5467f66db5ceb43abc25164572fb344f`  
		Last Modified: Wed, 07 Jan 2026 17:59:16 GMT  
		Size: 180.5 MB (180493045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5e16ca410bc2f12c8e7a9874874ca3682f26445816b92e0a4ae9a90510dadfa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c276762d830affc6299aecd9f3e0bac8af3a2c078667c5bc1cea2bfa64e8d04a`

```dockerfile
```

-	Layers:
	-	`sha256:c6c7b1c46e93e3dc234f893e4da79cd96e0ffdfc189e93c477f9744a94a7ebe0`  
		Last Modified: Wed, 07 Jan 2026 18:53:39 GMT  
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
