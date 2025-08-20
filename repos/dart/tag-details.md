<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10.0-75.2.beta`](#dart3100-752beta)
-	[`dart:3.10.0-75.2.beta-sdk`](#dart3100-752beta-sdk)
-	[`dart:3.9`](#dart39)
-	[`dart:3.9-sdk`](#dart39-sdk)
-	[`dart:3.9.1`](#dart391)
-	[`dart:3.9.1-sdk`](#dart391-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:570376d123ff9ddc55c2f01dff3e5161b19f818f38a401c9dc19a9a9f2d12ef5
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
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:167e64a40bca0723a2855103c66851c56fd815593d65ec4885d88160d1bf595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28107717a0f106f1afa443c80f73599a673731c51ef2b30c511bf9a4edc8a5e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=75bf2badc56cd6aff829042a0112ca5f3cf50bcf7fd95c29bc76650579dc00e1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c2bc9f74f3d77ff5e2d66b10eb9acb81e1978ef7ec88772a8a0231d0dbc526ac;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9a028b0be5325e2cbf5118ab6c6c407d302fb220ae5dc7d9d6f5648676fb724;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=81df475711bf672ef4d04bcbef3cc563b6e9224ba0742f73cd538ff649361d74;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92992550b3126ba3ff441f4e84d0dd756d8b7414d2d6cf8fc71947270abdc82`  
		Last Modified: Sun, 17 Aug 2025 08:07:24 GMT  
		Size: 161.0 MB (160964166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:e098104ba0efa6950ccb94ceb88ed40c63088c24b8325a8a412783f4d57602d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8f479460e0e1346a48da29857aba544f754de2052708dadd0dc214d611e93`

```dockerfile
```

-	Layers:
	-	`sha256:bae4bba6c3775f017525bb113980671e82aaf3c3798e7004f3679b2afaf5dd80`  
		Last Modified: Sun, 17 Aug 2025 08:53:24 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:570376d123ff9ddc55c2f01dff3e5161b19f818f38a401c9dc19a9a9f2d12ef5
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
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:167e64a40bca0723a2855103c66851c56fd815593d65ec4885d88160d1bf595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28107717a0f106f1afa443c80f73599a673731c51ef2b30c511bf9a4edc8a5e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=75bf2badc56cd6aff829042a0112ca5f3cf50bcf7fd95c29bc76650579dc00e1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c2bc9f74f3d77ff5e2d66b10eb9acb81e1978ef7ec88772a8a0231d0dbc526ac;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9a028b0be5325e2cbf5118ab6c6c407d302fb220ae5dc7d9d6f5648676fb724;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=81df475711bf672ef4d04bcbef3cc563b6e9224ba0742f73cd538ff649361d74;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92992550b3126ba3ff441f4e84d0dd756d8b7414d2d6cf8fc71947270abdc82`  
		Last Modified: Sun, 17 Aug 2025 08:07:24 GMT  
		Size: 161.0 MB (160964166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e098104ba0efa6950ccb94ceb88ed40c63088c24b8325a8a412783f4d57602d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8f479460e0e1346a48da29857aba544f754de2052708dadd0dc214d611e93`

```dockerfile
```

-	Layers:
	-	`sha256:bae4bba6c3775f017525bb113980671e82aaf3c3798e7004f3679b2afaf5dd80`  
		Last Modified: Sun, 17 Aug 2025 08:53:24 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-75.2.beta`

```console
$ docker pull dart@sha256:992b71d420a72acd27c8135c59647fdda93cc2a895e06f9061667d1c2ca62725
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.10.0-75.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:b6378c512ec83f5eca5f5fce2273fcdb8994d0b5b5c20785204269aa64857145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282051742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73772d903bce62e961e7f57a0e24cd37f59cfcb2abc3ae3ff6f366d90e850b38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38957d8c988c1b2918c2851da073d829ed717aed6c20a0db7c765970e4454eb7`  
		Last Modified: Wed, 20 Aug 2025 18:40:49 GMT  
		Size: 42.5 MB (42480170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a809654f230d0f007cc01cb902ea5a09d387bafd46a6602a0b914f96b9784e1`  
		Last Modified: Wed, 20 Aug 2025 20:54:06 GMT  
		Size: 207.9 MB (207924648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:4dc57f26035f8dc52c2e45dabd6078585da8166099282623161725993e8edd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3f0e94468d41f8eba6af03807e16bc677a900e68f8429c353832396b7601f3`

```dockerfile
```

-	Layers:
	-	`sha256:f0e9246662234c3fc1435b0f1ba767acc50b73604b03eb13c3cbb642f3b39b99`  
		Last Modified: Wed, 20 Aug 2025 20:53:35 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb46ce3f842d3e3ad8a72df540071b5f14447a5e23c655d989215d773be460ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215046111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d30927b42ac20f74ccd8f91ab91d4c3727b6730639befebce1c7f0d144b76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab492f2b844ab0e6b83f1dc61379567ed6a187423e24cec259e149feb4e4ab7`  
		Last Modified: Wed, 20 Aug 2025 20:54:03 GMT  
		Size: 150.1 MB (150085066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:0b86c429573db488866051100a0ee632d741e53055907ab493fc41060f16aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfe09089a4f3219c68e4b394b1be7050c1f0d390e7a77b39e69bf84a046622`

```dockerfile
```

-	Layers:
	-	`sha256:4e19f7e18f207d87738b361b1ca6f8302f261685c106c5a6661d8e51c60bfeb9`  
		Last Modified: Wed, 20 Aug 2025 20:53:39 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d9e367080af7d7a6a57f2781f4333dbd9005d26f548ebc29fe1450190e10834f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fadbfae3509bbf907a973d7280590d1150a03a20cb3cab8c369cc9239c3988`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24702d5295002e9267969550b7c98f0c74f8875fcae5a97f82eae1fb8e5b650`  
		Last Modified: Wed, 20 Aug 2025 20:54:14 GMT  
		Size: 207.3 MB (207296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:7eeaa1f52aec4062754c686bd18467badb4ec5c00aedc1064875a2e139c209bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05292d6b123362939cc2dd9bfed071412be258ccfdb530ae71e2f4fd0460ce61`

```dockerfile
```

-	Layers:
	-	`sha256:aaeefecd88aeccafb0315f2b0305431275103d192379b42d10e06b20294a3a87`  
		Last Modified: Wed, 20 Aug 2025 20:53:42 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-75.2.beta-sdk`

```console
$ docker pull dart@sha256:992b71d420a72acd27c8135c59647fdda93cc2a895e06f9061667d1c2ca62725
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.10.0-75.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b6378c512ec83f5eca5f5fce2273fcdb8994d0b5b5c20785204269aa64857145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282051742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73772d903bce62e961e7f57a0e24cd37f59cfcb2abc3ae3ff6f366d90e850b38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38957d8c988c1b2918c2851da073d829ed717aed6c20a0db7c765970e4454eb7`  
		Last Modified: Wed, 20 Aug 2025 18:40:49 GMT  
		Size: 42.5 MB (42480170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a809654f230d0f007cc01cb902ea5a09d387bafd46a6602a0b914f96b9784e1`  
		Last Modified: Wed, 20 Aug 2025 20:54:06 GMT  
		Size: 207.9 MB (207924648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4dc57f26035f8dc52c2e45dabd6078585da8166099282623161725993e8edd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3f0e94468d41f8eba6af03807e16bc677a900e68f8429c353832396b7601f3`

```dockerfile
```

-	Layers:
	-	`sha256:f0e9246662234c3fc1435b0f1ba767acc50b73604b03eb13c3cbb642f3b39b99`  
		Last Modified: Wed, 20 Aug 2025 20:53:35 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb46ce3f842d3e3ad8a72df540071b5f14447a5e23c655d989215d773be460ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215046111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d30927b42ac20f74ccd8f91ab91d4c3727b6730639befebce1c7f0d144b76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab492f2b844ab0e6b83f1dc61379567ed6a187423e24cec259e149feb4e4ab7`  
		Last Modified: Wed, 20 Aug 2025 20:54:03 GMT  
		Size: 150.1 MB (150085066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0b86c429573db488866051100a0ee632d741e53055907ab493fc41060f16aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfe09089a4f3219c68e4b394b1be7050c1f0d390e7a77b39e69bf84a046622`

```dockerfile
```

-	Layers:
	-	`sha256:4e19f7e18f207d87738b361b1ca6f8302f261685c106c5a6661d8e51c60bfeb9`  
		Last Modified: Wed, 20 Aug 2025 20:53:39 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d9e367080af7d7a6a57f2781f4333dbd9005d26f548ebc29fe1450190e10834f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fadbfae3509bbf907a973d7280590d1150a03a20cb3cab8c369cc9239c3988`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24702d5295002e9267969550b7c98f0c74f8875fcae5a97f82eae1fb8e5b650`  
		Last Modified: Wed, 20 Aug 2025 20:54:14 GMT  
		Size: 207.3 MB (207296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7eeaa1f52aec4062754c686bd18467badb4ec5c00aedc1064875a2e139c209bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05292d6b123362939cc2dd9bfed071412be258ccfdb530ae71e2f4fd0460ce61`

```dockerfile
```

-	Layers:
	-	`sha256:aaeefecd88aeccafb0315f2b0305431275103d192379b42d10e06b20294a3a87`  
		Last Modified: Wed, 20 Aug 2025 20:53:42 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9`

```console
$ docker pull dart@sha256:570376d123ff9ddc55c2f01dff3e5161b19f818f38a401c9dc19a9a9f2d12ef5
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

### `dart:3.9` - linux; amd64

```console
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; riscv64

```console
$ docker pull dart@sha256:167e64a40bca0723a2855103c66851c56fd815593d65ec4885d88160d1bf595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28107717a0f106f1afa443c80f73599a673731c51ef2b30c511bf9a4edc8a5e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=75bf2badc56cd6aff829042a0112ca5f3cf50bcf7fd95c29bc76650579dc00e1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c2bc9f74f3d77ff5e2d66b10eb9acb81e1978ef7ec88772a8a0231d0dbc526ac;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9a028b0be5325e2cbf5118ab6c6c407d302fb220ae5dc7d9d6f5648676fb724;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=81df475711bf672ef4d04bcbef3cc563b6e9224ba0742f73cd538ff649361d74;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92992550b3126ba3ff441f4e84d0dd756d8b7414d2d6cf8fc71947270abdc82`  
		Last Modified: Sun, 17 Aug 2025 08:07:24 GMT  
		Size: 161.0 MB (160964166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:e098104ba0efa6950ccb94ceb88ed40c63088c24b8325a8a412783f4d57602d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8f479460e0e1346a48da29857aba544f754de2052708dadd0dc214d611e93`

```dockerfile
```

-	Layers:
	-	`sha256:bae4bba6c3775f017525bb113980671e82aaf3c3798e7004f3679b2afaf5dd80`  
		Last Modified: Sun, 17 Aug 2025 08:53:24 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9-sdk`

```console
$ docker pull dart@sha256:570376d123ff9ddc55c2f01dff3e5161b19f818f38a401c9dc19a9a9f2d12ef5
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

### `dart:3.9-sdk` - linux; amd64

```console
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:167e64a40bca0723a2855103c66851c56fd815593d65ec4885d88160d1bf595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28107717a0f106f1afa443c80f73599a673731c51ef2b30c511bf9a4edc8a5e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=75bf2badc56cd6aff829042a0112ca5f3cf50bcf7fd95c29bc76650579dc00e1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c2bc9f74f3d77ff5e2d66b10eb9acb81e1978ef7ec88772a8a0231d0dbc526ac;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9a028b0be5325e2cbf5118ab6c6c407d302fb220ae5dc7d9d6f5648676fb724;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=81df475711bf672ef4d04bcbef3cc563b6e9224ba0742f73cd538ff649361d74;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92992550b3126ba3ff441f4e84d0dd756d8b7414d2d6cf8fc71947270abdc82`  
		Last Modified: Sun, 17 Aug 2025 08:07:24 GMT  
		Size: 161.0 MB (160964166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e098104ba0efa6950ccb94ceb88ed40c63088c24b8325a8a412783f4d57602d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8f479460e0e1346a48da29857aba544f754de2052708dadd0dc214d611e93`

```dockerfile
```

-	Layers:
	-	`sha256:bae4bba6c3775f017525bb113980671e82aaf3c3798e7004f3679b2afaf5dd80`  
		Last Modified: Sun, 17 Aug 2025 08:53:24 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.1`

```console
$ docker pull dart@sha256:c6db51771f5b376e0df79be594ec0e37e72862c1f03f46c7365d778073bdd4fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.1` - linux; amd64

```console
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.1` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.1` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.1` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.1-sdk`

```console
$ docker pull dart@sha256:c6db51771f5b376e0df79be594ec0e37e72862c1f03f46c7365d778073bdd4fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:04318e081a53a32654483f58803043bfae1159332b50ecdc3f407f1fece04cf3
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
$ docker pull dart@sha256:b6378c512ec83f5eca5f5fce2273fcdb8994d0b5b5c20785204269aa64857145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282051742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73772d903bce62e961e7f57a0e24cd37f59cfcb2abc3ae3ff6f366d90e850b38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38957d8c988c1b2918c2851da073d829ed717aed6c20a0db7c765970e4454eb7`  
		Last Modified: Wed, 20 Aug 2025 18:40:49 GMT  
		Size: 42.5 MB (42480170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a809654f230d0f007cc01cb902ea5a09d387bafd46a6602a0b914f96b9784e1`  
		Last Modified: Wed, 20 Aug 2025 20:54:06 GMT  
		Size: 207.9 MB (207924648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:4dc57f26035f8dc52c2e45dabd6078585da8166099282623161725993e8edd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3f0e94468d41f8eba6af03807e16bc677a900e68f8429c353832396b7601f3`

```dockerfile
```

-	Layers:
	-	`sha256:f0e9246662234c3fc1435b0f1ba767acc50b73604b03eb13c3cbb642f3b39b99`  
		Last Modified: Wed, 20 Aug 2025 20:53:35 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb46ce3f842d3e3ad8a72df540071b5f14447a5e23c655d989215d773be460ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215046111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d30927b42ac20f74ccd8f91ab91d4c3727b6730639befebce1c7f0d144b76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab492f2b844ab0e6b83f1dc61379567ed6a187423e24cec259e149feb4e4ab7`  
		Last Modified: Wed, 20 Aug 2025 20:54:03 GMT  
		Size: 150.1 MB (150085066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:0b86c429573db488866051100a0ee632d741e53055907ab493fc41060f16aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfe09089a4f3219c68e4b394b1be7050c1f0d390e7a77b39e69bf84a046622`

```dockerfile
```

-	Layers:
	-	`sha256:4e19f7e18f207d87738b361b1ca6f8302f261685c106c5a6661d8e51c60bfeb9`  
		Last Modified: Wed, 20 Aug 2025 20:53:39 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d9e367080af7d7a6a57f2781f4333dbd9005d26f548ebc29fe1450190e10834f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fadbfae3509bbf907a973d7280590d1150a03a20cb3cab8c369cc9239c3988`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24702d5295002e9267969550b7c98f0c74f8875fcae5a97f82eae1fb8e5b650`  
		Last Modified: Wed, 20 Aug 2025 20:54:14 GMT  
		Size: 207.3 MB (207296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:7eeaa1f52aec4062754c686bd18467badb4ec5c00aedc1064875a2e139c209bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05292d6b123362939cc2dd9bfed071412be258ccfdb530ae71e2f4fd0460ce61`

```dockerfile
```

-	Layers:
	-	`sha256:aaeefecd88aeccafb0315f2b0305431275103d192379b42d10e06b20294a3a87`  
		Last Modified: Wed, 20 Aug 2025 20:53:42 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:a1db8bea4b6ff98727c8660a8ac81ed37f9e18ba888c1ab4079656a3e824109c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228193472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8c8f39e9e01ad257482ed6ca88f45a9475181fc0ac20e25a6c93b111991c09`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98cf6429f72af7a992e4bcfff5510dd3164edd23f3bb202809589b7bce1b3b`  
		Last Modified: Sun, 17 Aug 2025 08:53:48 GMT  
		Size: 156.8 MB (156804770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:c668999dc1e250b5c9806a843e2fa482ba63486cbbc3ddb077fbbbeaabbe8d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f9999299f4457e6e27b6ecbae07393bae56fead4d0d67b4f1fa20a31e998e4`

```dockerfile
```

-	Layers:
	-	`sha256:e71a8a2e018558fec3134833d220363401c441ebf4a6bc6d60ac8fa6404438c4`  
		Last Modified: Sun, 17 Aug 2025 08:53:29 GMT  
		Size: 19.0 KB (19009 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:04318e081a53a32654483f58803043bfae1159332b50ecdc3f407f1fece04cf3
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
$ docker pull dart@sha256:b6378c512ec83f5eca5f5fce2273fcdb8994d0b5b5c20785204269aa64857145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282051742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73772d903bce62e961e7f57a0e24cd37f59cfcb2abc3ae3ff6f366d90e850b38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38957d8c988c1b2918c2851da073d829ed717aed6c20a0db7c765970e4454eb7`  
		Last Modified: Wed, 20 Aug 2025 18:40:49 GMT  
		Size: 42.5 MB (42480170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a809654f230d0f007cc01cb902ea5a09d387bafd46a6602a0b914f96b9784e1`  
		Last Modified: Wed, 20 Aug 2025 20:54:06 GMT  
		Size: 207.9 MB (207924648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4dc57f26035f8dc52c2e45dabd6078585da8166099282623161725993e8edd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3f0e94468d41f8eba6af03807e16bc677a900e68f8429c353832396b7601f3`

```dockerfile
```

-	Layers:
	-	`sha256:f0e9246662234c3fc1435b0f1ba767acc50b73604b03eb13c3cbb642f3b39b99`  
		Last Modified: Wed, 20 Aug 2025 20:53:35 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb46ce3f842d3e3ad8a72df540071b5f14447a5e23c655d989215d773be460ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215046111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d30927b42ac20f74ccd8f91ab91d4c3727b6730639befebce1c7f0d144b76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab492f2b844ab0e6b83f1dc61379567ed6a187423e24cec259e149feb4e4ab7`  
		Last Modified: Wed, 20 Aug 2025 20:54:03 GMT  
		Size: 150.1 MB (150085066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0b86c429573db488866051100a0ee632d741e53055907ab493fc41060f16aad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfe09089a4f3219c68e4b394b1be7050c1f0d390e7a77b39e69bf84a046622`

```dockerfile
```

-	Layers:
	-	`sha256:4e19f7e18f207d87738b361b1ca6f8302f261685c106c5a6661d8e51c60bfeb9`  
		Last Modified: Wed, 20 Aug 2025 20:53:39 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d9e367080af7d7a6a57f2781f4333dbd9005d26f548ebc29fe1450190e10834f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fadbfae3509bbf907a973d7280590d1150a03a20cb3cab8c369cc9239c3988`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4676a8e1596743d8280d8d3262564c318ae3b13f3a186b094eb05eba95378c12;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a1775a100b5a626805c2c1186ed96786a7f426be173ca30782df8964896b32f;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9bab193cf5d2f0f13e26ef61bbbbf49de262f69677e4e343cb5bfe7f3395066b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=45774de998358caed569d29bd786f309ebb9b3e804cd5ef530f77f2bed0cc94c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24702d5295002e9267969550b7c98f0c74f8875fcae5a97f82eae1fb8e5b650`  
		Last Modified: Wed, 20 Aug 2025 20:54:14 GMT  
		Size: 207.3 MB (207296661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7eeaa1f52aec4062754c686bd18467badb4ec5c00aedc1064875a2e139c209bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05292d6b123362939cc2dd9bfed071412be258ccfdb530ae71e2f4fd0460ce61`

```dockerfile
```

-	Layers:
	-	`sha256:aaeefecd88aeccafb0315f2b0305431275103d192379b42d10e06b20294a3a87`  
		Last Modified: Wed, 20 Aug 2025 20:53:42 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:a1db8bea4b6ff98727c8660a8ac81ed37f9e18ba888c1ab4079656a3e824109c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228193472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8c8f39e9e01ad257482ed6ca88f45a9475181fc0ac20e25a6c93b111991c09`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb98cf6429f72af7a992e4bcfff5510dd3164edd23f3bb202809589b7bce1b3b`  
		Last Modified: Sun, 17 Aug 2025 08:53:48 GMT  
		Size: 156.8 MB (156804770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c668999dc1e250b5c9806a843e2fa482ba63486cbbc3ddb077fbbbeaabbe8d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f9999299f4457e6e27b6ecbae07393bae56fead4d0d67b4f1fa20a31e998e4`

```dockerfile
```

-	Layers:
	-	`sha256:e71a8a2e018558fec3134833d220363401c441ebf4a6bc6d60ac8fa6404438c4`  
		Last Modified: Sun, 17 Aug 2025 08:53:29 GMT  
		Size: 19.0 KB (19009 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:570376d123ff9ddc55c2f01dff3e5161b19f818f38a401c9dc19a9a9f2d12ef5
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
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:167e64a40bca0723a2855103c66851c56fd815593d65ec4885d88160d1bf595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28107717a0f106f1afa443c80f73599a673731c51ef2b30c511bf9a4edc8a5e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=75bf2badc56cd6aff829042a0112ca5f3cf50bcf7fd95c29bc76650579dc00e1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c2bc9f74f3d77ff5e2d66b10eb9acb81e1978ef7ec88772a8a0231d0dbc526ac;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9a028b0be5325e2cbf5118ab6c6c407d302fb220ae5dc7d9d6f5648676fb724;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=81df475711bf672ef4d04bcbef3cc563b6e9224ba0742f73cd538ff649361d74;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92992550b3126ba3ff441f4e84d0dd756d8b7414d2d6cf8fc71947270abdc82`  
		Last Modified: Sun, 17 Aug 2025 08:07:24 GMT  
		Size: 161.0 MB (160964166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:e098104ba0efa6950ccb94ceb88ed40c63088c24b8325a8a412783f4d57602d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8f479460e0e1346a48da29857aba544f754de2052708dadd0dc214d611e93`

```dockerfile
```

-	Layers:
	-	`sha256:bae4bba6c3775f017525bb113980671e82aaf3c3798e7004f3679b2afaf5dd80`  
		Last Modified: Sun, 17 Aug 2025 08:53:24 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:570376d123ff9ddc55c2f01dff3e5161b19f818f38a401c9dc19a9a9f2d12ef5
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
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:167e64a40bca0723a2855103c66851c56fd815593d65ec4885d88160d1bf595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28107717a0f106f1afa443c80f73599a673731c51ef2b30c511bf9a4edc8a5e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=75bf2badc56cd6aff829042a0112ca5f3cf50bcf7fd95c29bc76650579dc00e1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c2bc9f74f3d77ff5e2d66b10eb9acb81e1978ef7ec88772a8a0231d0dbc526ac;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9a028b0be5325e2cbf5118ab6c6c407d302fb220ae5dc7d9d6f5648676fb724;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=81df475711bf672ef4d04bcbef3cc563b6e9224ba0742f73cd538ff649361d74;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92992550b3126ba3ff441f4e84d0dd756d8b7414d2d6cf8fc71947270abdc82`  
		Last Modified: Sun, 17 Aug 2025 08:07:24 GMT  
		Size: 161.0 MB (160964166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e098104ba0efa6950ccb94ceb88ed40c63088c24b8325a8a412783f4d57602d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8f479460e0e1346a48da29857aba544f754de2052708dadd0dc214d611e93`

```dockerfile
```

-	Layers:
	-	`sha256:bae4bba6c3775f017525bb113980671e82aaf3c3798e7004f3679b2afaf5dd80`  
		Last Modified: Sun, 17 Aug 2025 08:53:24 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:570376d123ff9ddc55c2f01dff3e5161b19f818f38a401c9dc19a9a9f2d12ef5
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
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:167e64a40bca0723a2855103c66851c56fd815593d65ec4885d88160d1bf595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28107717a0f106f1afa443c80f73599a673731c51ef2b30c511bf9a4edc8a5e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=75bf2badc56cd6aff829042a0112ca5f3cf50bcf7fd95c29bc76650579dc00e1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c2bc9f74f3d77ff5e2d66b10eb9acb81e1978ef7ec88772a8a0231d0dbc526ac;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9a028b0be5325e2cbf5118ab6c6c407d302fb220ae5dc7d9d6f5648676fb724;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=81df475711bf672ef4d04bcbef3cc563b6e9224ba0742f73cd538ff649361d74;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92992550b3126ba3ff441f4e84d0dd756d8b7414d2d6cf8fc71947270abdc82`  
		Last Modified: Sun, 17 Aug 2025 08:07:24 GMT  
		Size: 161.0 MB (160964166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e098104ba0efa6950ccb94ceb88ed40c63088c24b8325a8a412783f4d57602d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8f479460e0e1346a48da29857aba544f754de2052708dadd0dc214d611e93`

```dockerfile
```

-	Layers:
	-	`sha256:bae4bba6c3775f017525bb113980671e82aaf3c3798e7004f3679b2afaf5dd80`  
		Last Modified: Sun, 17 Aug 2025 08:53:24 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:570376d123ff9ddc55c2f01dff3e5161b19f818f38a401c9dc19a9a9f2d12ef5
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
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:167e64a40bca0723a2855103c66851c56fd815593d65ec4885d88160d1bf595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28107717a0f106f1afa443c80f73599a673731c51ef2b30c511bf9a4edc8a5e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=75bf2badc56cd6aff829042a0112ca5f3cf50bcf7fd95c29bc76650579dc00e1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c2bc9f74f3d77ff5e2d66b10eb9acb81e1978ef7ec88772a8a0231d0dbc526ac;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9a028b0be5325e2cbf5118ab6c6c407d302fb220ae5dc7d9d6f5648676fb724;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=81df475711bf672ef4d04bcbef3cc563b6e9224ba0742f73cd538ff649361d74;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92992550b3126ba3ff441f4e84d0dd756d8b7414d2d6cf8fc71947270abdc82`  
		Last Modified: Sun, 17 Aug 2025 08:07:24 GMT  
		Size: 161.0 MB (160964166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e098104ba0efa6950ccb94ceb88ed40c63088c24b8325a8a412783f4d57602d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8f479460e0e1346a48da29857aba544f754de2052708dadd0dc214d611e93`

```dockerfile
```

-	Layers:
	-	`sha256:bae4bba6c3775f017525bb113980671e82aaf3c3798e7004f3679b2afaf5dd80`  
		Last Modified: Sun, 17 Aug 2025 08:53:24 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json
