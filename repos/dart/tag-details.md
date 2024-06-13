<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.4`](#dart34)
-	[`dart:3.4-sdk`](#dart34-sdk)
-	[`dart:3.4.4`](#dart344)
-	[`dart:3.4.4-sdk`](#dart344-sdk)
-	[`dart:3.5.0-180.3.beta`](#dart350-1803beta)
-	[`dart:3.5.0-180.3.beta-sdk`](#dart350-1803beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3-sdk`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.4`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.4` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.4-sdk`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.4-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.4.4`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.4.4` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4.4` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4.4` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.4.4-sdk`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.4.4-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4.4-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.4.4-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.0-180.3.beta`

```console
$ docker pull dart@sha256:b1bc4796953cec93dc6e0333ccb41c38c981564558e63ce6fbeee609cbb92bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.0-180.3.beta` - linux; amd64

```console
$ docker pull dart@sha256:70fc62b40ad9283289325220299cfcc3f6063df9bdaf74b58f9bd12aa73707a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302242497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93ecab26cc9cc57c5009be96222f7bbb70fde8468f61ce6a3221284a4abdec`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 04:00:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a10c1fae9859f8c09e9cb497fdad626d0cd79600b85f4876855570c2d7a0b6`  
		Last Modified: Thu, 13 Jun 2024 04:02:02 GMT  
		Size: 216.6 MB (216633525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.0-180.3.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:6176186e3cd72d531928a7b37f1957969834fdc5b0429949e4131febd2662313
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202692529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd512277db3ef6c1ae9c119d7536f4141c4a44c650747fd7b0e354385f596436`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 01:41:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1e82f99c391f6badc5bb4cb9871d95aff0da19f29154d46c16a7849eff21ca`  
		Last Modified: Thu, 13 Jun 2024 01:42:56 GMT  
		Size: 127.6 MB (127587394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.0-180.3.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3d23ff943da4ef66bc6fe9f38c4bc561afff1b26da87a6d73772ca827a8fa9ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300873938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbae76c0d0c180157d8cae89a355eaaa65263725088ac3558d19944d0b36130b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 01:35:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eca07a058237a32737bd22f667b82d9533b3d849ac384010549b4041a52822f`  
		Last Modified: Thu, 13 Jun 2024 01:37:09 GMT  
		Size: 215.9 MB (215873918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.0-180.3.beta-sdk`

```console
$ docker pull dart@sha256:b1bc4796953cec93dc6e0333ccb41c38c981564558e63ce6fbeee609cbb92bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.0-180.3.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:70fc62b40ad9283289325220299cfcc3f6063df9bdaf74b58f9bd12aa73707a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302242497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93ecab26cc9cc57c5009be96222f7bbb70fde8468f61ce6a3221284a4abdec`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 04:00:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a10c1fae9859f8c09e9cb497fdad626d0cd79600b85f4876855570c2d7a0b6`  
		Last Modified: Thu, 13 Jun 2024 04:02:02 GMT  
		Size: 216.6 MB (216633525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.0-180.3.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6176186e3cd72d531928a7b37f1957969834fdc5b0429949e4131febd2662313
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202692529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd512277db3ef6c1ae9c119d7536f4141c4a44c650747fd7b0e354385f596436`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 01:41:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1e82f99c391f6badc5bb4cb9871d95aff0da19f29154d46c16a7849eff21ca`  
		Last Modified: Thu, 13 Jun 2024 01:42:56 GMT  
		Size: 127.6 MB (127587394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.0-180.3.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3d23ff943da4ef66bc6fe9f38c4bc561afff1b26da87a6d73772ca827a8fa9ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300873938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbae76c0d0c180157d8cae89a355eaaa65263725088ac3558d19944d0b36130b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 01:35:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eca07a058237a32737bd22f667b82d9533b3d849ac384010549b4041a52822f`  
		Last Modified: Thu, 13 Jun 2024 01:37:09 GMT  
		Size: 215.9 MB (215873918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:b1bc4796953cec93dc6e0333ccb41c38c981564558e63ce6fbeee609cbb92bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:70fc62b40ad9283289325220299cfcc3f6063df9bdaf74b58f9bd12aa73707a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302242497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93ecab26cc9cc57c5009be96222f7bbb70fde8468f61ce6a3221284a4abdec`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 04:00:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a10c1fae9859f8c09e9cb497fdad626d0cd79600b85f4876855570c2d7a0b6`  
		Last Modified: Thu, 13 Jun 2024 04:02:02 GMT  
		Size: 216.6 MB (216633525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:6176186e3cd72d531928a7b37f1957969834fdc5b0429949e4131febd2662313
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202692529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd512277db3ef6c1ae9c119d7536f4141c4a44c650747fd7b0e354385f596436`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 01:41:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1e82f99c391f6badc5bb4cb9871d95aff0da19f29154d46c16a7849eff21ca`  
		Last Modified: Thu, 13 Jun 2024 01:42:56 GMT  
		Size: 127.6 MB (127587394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3d23ff943da4ef66bc6fe9f38c4bc561afff1b26da87a6d73772ca827a8fa9ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300873938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbae76c0d0c180157d8cae89a355eaaa65263725088ac3558d19944d0b36130b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 01:35:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eca07a058237a32737bd22f667b82d9533b3d849ac384010549b4041a52822f`  
		Last Modified: Thu, 13 Jun 2024 01:37:09 GMT  
		Size: 215.9 MB (215873918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:b1bc4796953cec93dc6e0333ccb41c38c981564558e63ce6fbeee609cbb92bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:70fc62b40ad9283289325220299cfcc3f6063df9bdaf74b58f9bd12aa73707a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302242497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93ecab26cc9cc57c5009be96222f7bbb70fde8468f61ce6a3221284a4abdec`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 04:00:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a10c1fae9859f8c09e9cb497fdad626d0cd79600b85f4876855570c2d7a0b6`  
		Last Modified: Thu, 13 Jun 2024 04:02:02 GMT  
		Size: 216.6 MB (216633525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6176186e3cd72d531928a7b37f1957969834fdc5b0429949e4131febd2662313
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202692529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd512277db3ef6c1ae9c119d7536f4141c4a44c650747fd7b0e354385f596436`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 01:41:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1e82f99c391f6badc5bb4cb9871d95aff0da19f29154d46c16a7849eff21ca`  
		Last Modified: Thu, 13 Jun 2024 01:42:56 GMT  
		Size: 127.6 MB (127587394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:3d23ff943da4ef66bc6fe9f38c4bc561afff1b26da87a6d73772ca827a8fa9ba
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300873938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbae76c0d0c180157d8cae89a355eaaa65263725088ac3558d19944d0b36130b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 01:35:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=bc1269cc539193036c9b8b8394cc66bb2b1c493cf0932f8f3901eb17af7f9dbd;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0ec722221ce891c0f37acc53e22031984fcec32655eadf16be1d68882f88cd1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=05fafa6b872a5512d5caf5aec88dc0e13bda595210d124f6886a4df11ecf834a;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.5.0-180.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eca07a058237a32737bd22f667b82d9533b3d849ac384010549b4041a52822f`  
		Last Modified: Thu, 13 Jun 2024 01:37:09 GMT  
		Size: 215.9 MB (215873918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:cbe4ddbd97ffe990873306bc69edc29f252b190dbbe26fd75c5f6bd9f2fe958f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:0f1a4c052f66f8746b236df30bdd85ac2f775ccdf55dd7a94aef8061ca9b46dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322141543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13369d36becbfa23721f1dd6fae0913e8699ebdeb2838d56b7101903c06e839`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:59:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 03:59:51 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 03:59:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 03:59:51 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:20:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce7edfd843cff5728a1106fc6d4dc65af903330d1e9cf446ef96f460522cf19`  
		Last Modified: Thu, 13 Jun 2024 04:00:47 GMT  
		Size: 54.7 MB (54657651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35be5b0b873e8398d310383b52d5dc61d1f7d59c81dafdec5e8bb53719580b0`  
		Last Modified: Thu, 13 Jun 2024 04:00:40 GMT  
		Size: 1.8 MB (1800891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432a37df6fead55bbfaf20a7e126d11b5d4fe9a3fd305f38a3d5d601964b2255`  
		Last Modified: Thu, 13 Jun 2024 18:21:00 GMT  
		Size: 236.5 MB (236532571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f2f11b3ecd06e419f15e928eb8faf59b4858068fccf6e9e85487b875b88e8247
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208885738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2472cf3c9b6e31b6578e31d1854b2878adfba2ddd8a4b2114dfa8582a820c0dc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:40:58 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:41:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:41:00 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:41:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:41:00 GMT
WORKDIR /root
# Thu, 13 Jun 2024 19:27:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8addf98d69be30e611eb98843238dbf864e01e8b3e1136f26129d0b58b2c215f`  
		Last Modified: Thu, 13 Jun 2024 01:42:02 GMT  
		Size: 49.1 MB (49137378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2795fba491482b21210b783f53905c804fb4d50fc58d062ef97aeb33a6afa82`  
		Last Modified: Thu, 13 Jun 2024 01:41:55 GMT  
		Size: 1.2 MB (1227542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3abc71daaae63dd1611dad0e1487356f56c9204691b052ef805cfd540c21f6`  
		Last Modified: Thu, 13 Jun 2024 19:28:02 GMT  
		Size: 133.8 MB (133780603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:d1afe79136a00deed8e5f2509f5d48fe80638db3b5e6dbe9f7e47b4a50e0f061
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320839029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c8be784100b49ba0d73ad0e0f798551c66baa188ed9ab76d3bd796f291a807`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:35:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:35:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 13 Jun 2024 01:35:06 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 13 Jun 2024 01:35:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 01:35:06 GMT
WORKDIR /root
# Thu, 13 Jun 2024 18:18:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1968cc9ee12802317f9a2320165f6966cf949dc3574cac1cb91a1bc7f0de67db;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ef98f20dd52440bc664d7f215ac888a40755878a0e96cd4356a8cbbf0c20b6e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b4cee491863d2ca6c324fad2d8fe2dfa123f78164630d7ca5eee45b940f70346;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.4.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829908208ac3060b4d56ebfaba8a72649639512fa6e4bdd90959f60e4d40f4dc`  
		Last Modified: Thu, 13 Jun 2024 01:36:07 GMT  
		Size: 54.3 MB (54326084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9329fe487607d92702315fa26f71bb784d6d4d96155f8627a60e12179d4143ad`  
		Last Modified: Thu, 13 Jun 2024 01:36:01 GMT  
		Size: 1.5 MB (1494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521afe7d3d04252902e5fd5b36b745d36cbd0d7efacf7d1e41131c80b3a21e82`  
		Last Modified: Thu, 13 Jun 2024 18:18:59 GMT  
		Size: 235.8 MB (235839009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
