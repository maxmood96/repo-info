<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.5`](#dart35)
-	[`dart:3.5-sdk`](#dart35-sdk)
-	[`dart:3.5.1`](#dart351)
-	[`dart:3.5.1-sdk`](#dart351-sdk)
-	[`dart:3.6.0-149.3.beta`](#dart360-1493beta)
-	[`dart:3.6.0-149.3.beta-sdk`](#dart360-1493beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3-sdk`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5-sdk`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5-sdk` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.1`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.1` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.1-sdk`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.6.0-149.3.beta`

```console
$ docker pull dart@sha256:7814610e38a230b9561ccd519e9a5deeb9d90750086a20a58db117079ee7dda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.6.0-149.3.beta` - linux; amd64

```console
$ docker pull dart@sha256:08ea49f5c651af5e6c902c24260980691dea31dd8cf16e84605dd1a1a10c5a01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306374705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6eeec496f2f0aa81398015c35ceb88d51aab48d2a4ac960b2de1378bb28b08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a4342a071afaf6a67f6c42a8966ef26536c867f875936c4e92905bc691e9aa`  
		Last Modified: Thu, 22 Aug 2024 19:21:55 GMT  
		Size: 220.8 MB (220785831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-149.3.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:f47c0e4b2356857ee98d3d515ac7b241bcce09bfd2554296f5a1b10a4b940b59
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205166789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c83f72e8f448953ff764f9fdcb4a30ad41c04db535a603f11d1bb2e1c63c5b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:27:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e46c3c2a42e29e3912f2937ae65e1d25f957fdb80b67a83d7eb04fe85e74bd`  
		Last Modified: Thu, 22 Aug 2024 21:28:30 GMT  
		Size: 130.1 MB (130052767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-149.3.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cea52eeaac362fa346bd1cc93a7c1ad3dac3f24e56c1b8ab589cd9bf069c67a9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304989751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7b6918e3073f2a4421d69352685f822a538cfb0eb1f70e3d3fe97e12ce7787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fac628fcd077b3ca909a957cddc005b8cd5016e6b161d7ed58242126fa1adcd`  
		Last Modified: Thu, 22 Aug 2024 19:41:23 GMT  
		Size: 220.0 MB (220012132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.6.0-149.3.beta-sdk`

```console
$ docker pull dart@sha256:7814610e38a230b9561ccd519e9a5deeb9d90750086a20a58db117079ee7dda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.6.0-149.3.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:08ea49f5c651af5e6c902c24260980691dea31dd8cf16e84605dd1a1a10c5a01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306374705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6eeec496f2f0aa81398015c35ceb88d51aab48d2a4ac960b2de1378bb28b08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a4342a071afaf6a67f6c42a8966ef26536c867f875936c4e92905bc691e9aa`  
		Last Modified: Thu, 22 Aug 2024 19:21:55 GMT  
		Size: 220.8 MB (220785831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-149.3.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f47c0e4b2356857ee98d3d515ac7b241bcce09bfd2554296f5a1b10a4b940b59
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205166789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c83f72e8f448953ff764f9fdcb4a30ad41c04db535a603f11d1bb2e1c63c5b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:27:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e46c3c2a42e29e3912f2937ae65e1d25f957fdb80b67a83d7eb04fe85e74bd`  
		Last Modified: Thu, 22 Aug 2024 21:28:30 GMT  
		Size: 130.1 MB (130052767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-149.3.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cea52eeaac362fa346bd1cc93a7c1ad3dac3f24e56c1b8ab589cd9bf069c67a9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304989751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7b6918e3073f2a4421d69352685f822a538cfb0eb1f70e3d3fe97e12ce7787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fac628fcd077b3ca909a957cddc005b8cd5016e6b161d7ed58242126fa1adcd`  
		Last Modified: Thu, 22 Aug 2024 19:41:23 GMT  
		Size: 220.0 MB (220012132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:7814610e38a230b9561ccd519e9a5deeb9d90750086a20a58db117079ee7dda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:08ea49f5c651af5e6c902c24260980691dea31dd8cf16e84605dd1a1a10c5a01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306374705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6eeec496f2f0aa81398015c35ceb88d51aab48d2a4ac960b2de1378bb28b08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a4342a071afaf6a67f6c42a8966ef26536c867f875936c4e92905bc691e9aa`  
		Last Modified: Thu, 22 Aug 2024 19:21:55 GMT  
		Size: 220.8 MB (220785831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:f47c0e4b2356857ee98d3d515ac7b241bcce09bfd2554296f5a1b10a4b940b59
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205166789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c83f72e8f448953ff764f9fdcb4a30ad41c04db535a603f11d1bb2e1c63c5b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:27:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e46c3c2a42e29e3912f2937ae65e1d25f957fdb80b67a83d7eb04fe85e74bd`  
		Last Modified: Thu, 22 Aug 2024 21:28:30 GMT  
		Size: 130.1 MB (130052767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cea52eeaac362fa346bd1cc93a7c1ad3dac3f24e56c1b8ab589cd9bf069c67a9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304989751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7b6918e3073f2a4421d69352685f822a538cfb0eb1f70e3d3fe97e12ce7787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fac628fcd077b3ca909a957cddc005b8cd5016e6b161d7ed58242126fa1adcd`  
		Last Modified: Thu, 22 Aug 2024 19:41:23 GMT  
		Size: 220.0 MB (220012132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:7814610e38a230b9561ccd519e9a5deeb9d90750086a20a58db117079ee7dda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:08ea49f5c651af5e6c902c24260980691dea31dd8cf16e84605dd1a1a10c5a01
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306374705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6eeec496f2f0aa81398015c35ceb88d51aab48d2a4ac960b2de1378bb28b08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a4342a071afaf6a67f6c42a8966ef26536c867f875936c4e92905bc691e9aa`  
		Last Modified: Thu, 22 Aug 2024 19:21:55 GMT  
		Size: 220.8 MB (220785831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f47c0e4b2356857ee98d3d515ac7b241bcce09bfd2554296f5a1b10a4b940b59
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205166789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c83f72e8f448953ff764f9fdcb4a30ad41c04db535a603f11d1bb2e1c63c5b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:27:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e46c3c2a42e29e3912f2937ae65e1d25f957fdb80b67a83d7eb04fe85e74bd`  
		Last Modified: Thu, 22 Aug 2024 21:28:30 GMT  
		Size: 130.1 MB (130052767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cea52eeaac362fa346bd1cc93a7c1ad3dac3f24e56c1b8ab589cd9bf069c67a9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304989751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7b6918e3073f2a4421d69352685f822a538cfb0eb1f70e3d3fe97e12ce7787`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fac628fcd077b3ca909a957cddc005b8cd5016e6b161d7ed58242126fa1adcd`  
		Last Modified: Thu, 22 Aug 2024 19:41:23 GMT  
		Size: 220.0 MB (220012132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:ee87c0298f660f632e068488b5912b1ced250cd0afb79dcfb505b2a55c206ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:9691ef011d44e46b5cdda7db7ef13fc4c5442075c36c43611d06116996556fcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302928633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e64edecb3543e4e4586168476cb1975d7693a03c92b2b88a92fd0534eb676d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:54:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 00:54:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 00:54:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 00:54:12 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:20:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27827d55be4ad7b75d2f3fadb43b8f03f3edd4a0e1aaec564e8d1ae6cef4dd6`  
		Last Modified: Tue, 13 Aug 2024 00:54:48 GMT  
		Size: 54.7 MB (54661749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9f01d3ad071b2b6c358a69b5dc4e5667250e4be1fbd440e0b21f3d252b49bb`  
		Last Modified: Tue, 13 Aug 2024 00:54:40 GMT  
		Size: 1.8 MB (1800893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82581fe502165ae0407a41bf4b4256314b716c2fb5f2a659566ed2648124092c`  
		Last Modified: Thu, 22 Aug 2024 19:21:05 GMT  
		Size: 217.3 MB (217339759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:989af244dbc635cca15d3450df0a27bf2155eef5589224dfb46ffc452ae8ddde
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203188760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f03639824197114f98e5e61204e99704d4e2ae9b3116c38e5c0379d9fad5b40`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:36:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:36:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:36:59 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:36:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:37:00 GMT
WORKDIR /root
# Thu, 22 Aug 2024 21:26:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317bbb7202953610ab3fa2cf49800934054abb6c1d9d2a347ac2337b7fce0f99`  
		Last Modified: Tue, 13 Aug 2024 01:37:32 GMT  
		Size: 49.2 MB (49168334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0435028ff85935dadac55a648a58a87326525afaf7622d5992f17c5328eff`  
		Last Modified: Tue, 13 Aug 2024 01:37:25 GMT  
		Size: 1.2 MB (1227546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbf20243658becbccb1b7d67f8800f06397c81fd5bc00c32aab319c9452d334`  
		Last Modified: Thu, 22 Aug 2024 21:27:43 GMT  
		Size: 128.1 MB (128074738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:20ab68efa0257a358567428cc45cd14adc10e945d6f50aec65cf0f25257ae02a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301483802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8257aef525605cd7a9b476073ae24419d6b2c2a0b7c87b3b3e3e30160f0101e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:13:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 13 Aug 2024 01:13:16 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Aug 2024 01:13:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 01:13:17 GMT
WORKDIR /root
# Thu, 22 Aug 2024 19:39:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ec7cf3dab7b7b19f42bc5bbdde9f04911260ca828604e877862046ae10afc27e;             SDK_ARCH="x64";;         armhf)             DART_SHA256=bb3633bc6a32cf676b9824421bbb1639c05c821dc3fde9727f62ba9eaf349ffe;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1bb01530d5caa7d623f3ea30307aa129d84e8fca9d63b36240ed8c3bfcdc9653;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9988c56bc1b6f5f1592cda79327aad029d0550933fefea3440946cb10db39e`  
		Last Modified: Tue, 13 Aug 2024 01:13:51 GMT  
		Size: 54.3 MB (54326838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5075b18caf4a1998296d6573ca30a782ffa8120cbb46fcf236adaa7637f65e17`  
		Last Modified: Tue, 13 Aug 2024 01:13:46 GMT  
		Size: 1.5 MB (1494253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bf5c9f56e94da81741549682b15f5cab1d7df374e2b6c87a55e6eade059f6`  
		Last Modified: Thu, 22 Aug 2024 19:40:38 GMT  
		Size: 216.5 MB (216506183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
