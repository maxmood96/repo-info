<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.5`](#dart35)
-	[`dart:3.5-sdk`](#dart35-sdk)
-	[`dart:3.5.2`](#dart352)
-	[`dart:3.5.2-sdk`](#dart352-sdk)
-	[`dart:3.6.0-216.1.beta`](#dart360-2161beta)
-	[`dart:3.6.0-216.1.beta-sdk`](#dart360-2161beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3-sdk`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5-sdk`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.2`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.2` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.2-sdk`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.6.0-216.1.beta`

```console
$ docker pull dart@sha256:d6789f6c5f72690da0f7e9e058e6662f4f402148b298588fc66fe3d83d800a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `dart:3.6.0-216.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:f4211fec53f972987f5bc1dd0ffd3d3cb1fd820ac1ade4e45a7a0c7bffd71d58
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307570524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd0e136bbaadb16b4a43ce1a6c63e49831d45f03be7720f3af722ca57de3f06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Fri, 06 Sep 2024 20:20:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de403b0f3670c79662b1886ea90e95c4bf048e48f03030308541aaa569e4b6ea`  
		Last Modified: Fri, 06 Sep 2024 20:20:48 GMT  
		Size: 222.0 MB (221974384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-216.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f95b47cd41492d4a75cecf7662b2e6de37942ec1e6c8b40b8b7ff6e50fa98440
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306190939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe8c32128735d233274fc4567e4868f75a0ba6e92b59b7f05356ec81ce59ef1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Fri, 06 Sep 2024 20:39:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89e4887575d41cc9172252855b8165a4afc7cfba76838060f2606b8e6162bd0`  
		Last Modified: Fri, 06 Sep 2024 20:40:29 GMT  
		Size: 221.2 MB (221203744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.6.0-216.1.beta-sdk`

```console
$ docker pull dart@sha256:d6789f6c5f72690da0f7e9e058e6662f4f402148b298588fc66fe3d83d800a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `dart:3.6.0-216.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f4211fec53f972987f5bc1dd0ffd3d3cb1fd820ac1ade4e45a7a0c7bffd71d58
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307570524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd0e136bbaadb16b4a43ce1a6c63e49831d45f03be7720f3af722ca57de3f06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Fri, 06 Sep 2024 20:20:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de403b0f3670c79662b1886ea90e95c4bf048e48f03030308541aaa569e4b6ea`  
		Last Modified: Fri, 06 Sep 2024 20:20:48 GMT  
		Size: 222.0 MB (221974384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-216.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f95b47cd41492d4a75cecf7662b2e6de37942ec1e6c8b40b8b7ff6e50fa98440
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306190939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe8c32128735d233274fc4567e4868f75a0ba6e92b59b7f05356ec81ce59ef1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Fri, 06 Sep 2024 20:39:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89e4887575d41cc9172252855b8165a4afc7cfba76838060f2606b8e6162bd0`  
		Last Modified: Fri, 06 Sep 2024 20:40:29 GMT  
		Size: 221.2 MB (221203744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:de0d75aa5aa0723cf1415e9d85175f2b3d7795a4dc0a570ed268c6fb7ee8278f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:f4211fec53f972987f5bc1dd0ffd3d3cb1fd820ac1ade4e45a7a0c7bffd71d58
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307570524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd0e136bbaadb16b4a43ce1a6c63e49831d45f03be7720f3af722ca57de3f06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Fri, 06 Sep 2024 20:20:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de403b0f3670c79662b1886ea90e95c4bf048e48f03030308541aaa569e4b6ea`  
		Last Modified: Fri, 06 Sep 2024 20:20:48 GMT  
		Size: 222.0 MB (221974384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:7c189c07f46286f44c784df8cfa357460f950b9aeb225eeb301bf175dcac9594
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205160459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb690b56c929a93ccbc930feda6cd22469ca1c17cfc0984ab1100ffe0b6515a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:41:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633a7f0f67549809a3953ccd1cd181d3ce8a30263a9f2d35b8aec31bcfb96bf9`  
		Last Modified: Wed, 04 Sep 2024 22:42:40 GMT  
		Size: 130.1 MB (130052800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f95b47cd41492d4a75cecf7662b2e6de37942ec1e6c8b40b8b7ff6e50fa98440
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306190939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe8c32128735d233274fc4567e4868f75a0ba6e92b59b7f05356ec81ce59ef1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Fri, 06 Sep 2024 20:39:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89e4887575d41cc9172252855b8165a4afc7cfba76838060f2606b8e6162bd0`  
		Last Modified: Fri, 06 Sep 2024 20:40:29 GMT  
		Size: 221.2 MB (221203744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:de0d75aa5aa0723cf1415e9d85175f2b3d7795a4dc0a570ed268c6fb7ee8278f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f4211fec53f972987f5bc1dd0ffd3d3cb1fd820ac1ade4e45a7a0c7bffd71d58
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307570524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd0e136bbaadb16b4a43ce1a6c63e49831d45f03be7720f3af722ca57de3f06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Fri, 06 Sep 2024 20:20:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de403b0f3670c79662b1886ea90e95c4bf048e48f03030308541aaa569e4b6ea`  
		Last Modified: Fri, 06 Sep 2024 20:20:48 GMT  
		Size: 222.0 MB (221974384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:7c189c07f46286f44c784df8cfa357460f950b9aeb225eeb301bf175dcac9594
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205160459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb690b56c929a93ccbc930feda6cd22469ca1c17cfc0984ab1100ffe0b6515a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:41:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fd2480f5500a12d25578b15955e613641c23a4cbf6505054f8c969f3c7255b3d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ae12932960bcb44914df7d913eeb6b422c3c5b55a94310748a1164e036a32845;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f1f37f6df9922fe0d4897dbf70766591ac6d37447e9016e41405a8abe160e51c;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-149.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633a7f0f67549809a3953ccd1cd181d3ce8a30263a9f2d35b8aec31bcfb96bf9`  
		Last Modified: Wed, 04 Sep 2024 22:42:40 GMT  
		Size: 130.1 MB (130052800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f95b47cd41492d4a75cecf7662b2e6de37942ec1e6c8b40b8b7ff6e50fa98440
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306190939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe8c32128735d233274fc4567e4868f75a0ba6e92b59b7f05356ec81ce59ef1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Fri, 06 Sep 2024 20:39:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89e4887575d41cc9172252855b8165a4afc7cfba76838060f2606b8e6162bd0`  
		Last Modified: Fri, 06 Sep 2024 20:40:29 GMT  
		Size: 221.2 MB (221203744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:131b146729dfa9b7382e307f59db18109948b0c9d40f37f0b40457c12d294bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1fd62cb5036bdc42de89bdae747683277986639be9b0b0a0751d2c50bbd9441f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302953355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce37b7d9ada22f3a7d0db2d74bb0d3a2adbd44578a81c4ac2400df400da68a66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:05:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:05:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 23:05:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 23:05:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 23:05:38 GMT
WORKDIR /root
# Wed, 04 Sep 2024 23:05:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1223af30b32b8ee37934f219d2b38c0d11ff1b186ab6482124a74373af9a6409`  
		Last Modified: Wed, 04 Sep 2024 23:06:33 GMT  
		Size: 54.7 MB (54668734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c3d23caf29dd4c8420cff455659f40f6588a1bed71b484179b4035672c67c6`  
		Last Modified: Wed, 04 Sep 2024 23:06:26 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a69ce23e0bd33496ebb89a53f198f7279010e14dae93a61432f10f9c22c18`  
		Last Modified: Wed, 04 Sep 2024 23:06:57 GMT  
		Size: 217.4 MB (217357215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:00ef0e8d14bc8f3e09abcd19a8040a9c38450a9b101a5b0f2e91d96eb296ddad
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203181097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ff1ecba25115c5b062ada2bf896659d9e42d69bcf8b36526cd625feb64f2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:40:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:40:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:40:44 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:40:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:40:44 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:40:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20d1aa0333f0953c0fb89abffc3a7bb6b855c4bc92ed0a7e0462f9289cb42e0`  
		Last Modified: Wed, 04 Sep 2024 22:41:44 GMT  
		Size: 49.2 MB (49161862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead102acd61e6e9f89032d00360a82e562e3105d8153065b41c51beb1c80212b`  
		Last Modified: Wed, 04 Sep 2024 22:41:35 GMT  
		Size: 1.2 MB (1227532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0acbe2500f6bc488f1dd0243d096eab7b0ee9a65c4b4ab5544392e3feaaca34`  
		Last Modified: Wed, 04 Sep 2024 22:41:59 GMT  
		Size: 128.1 MB (128073438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05b49f405d01baca8fb4ccb663adb2af63e0e3fe25b1f0a570ff4597337a323b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301504310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e820bb1f223adabc7a0adbefa34f554f3a6b49d5a76cc40b5ae43ee30b0862`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:26:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 04 Sep 2024 22:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 04 Sep 2024 22:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Sep 2024 22:26:33 GMT
WORKDIR /root
# Wed, 04 Sep 2024 22:26:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564848c22a8ecc39be08482d7ef7c7d15f747e5f0d53657d1b1f715787f84e1`  
		Last Modified: Wed, 04 Sep 2024 22:27:31 GMT  
		Size: 54.3 MB (54336781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5dacfa3db55ec04eb95694652e2b59b0672cc6903b5c76693f49be1b708dc7`  
		Last Modified: Wed, 04 Sep 2024 22:27:26 GMT  
		Size: 1.5 MB (1493869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df3cd40c0d2b1da7278083229bdbe59f5368919b9c2653eedb8197afbddb190`  
		Last Modified: Wed, 04 Sep 2024 22:27:48 GMT  
		Size: 216.5 MB (216517115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
