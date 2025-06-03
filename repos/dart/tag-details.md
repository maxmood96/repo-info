<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.8`](#dart38)
-	[`dart:3.8-sdk`](#dart38-sdk)
-	[`dart:3.8.1`](#dart381)
-	[`dart:3.8.1-sdk`](#dart381-sdk)
-	[`dart:3.9.0-100.2.beta`](#dart390-1002beta)
-	[`dart:3.9.0-100.2.beta-sdk`](#dart390-1002beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8-sdk`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8-sdk` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.1`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.1` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.1-sdk`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-100.2.beta`

```console
$ docker pull dart@sha256:66489fe773c404431290502d2cd60e0211160f6a0b0de786c565cd417d672a2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0-100.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:8b2e8dfe4518fbe9e67d26526701b4f8d34c95ed329caa5b910f013f7ac38826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb3ae80660606c11d78657f0daad75a8565ec606fe9d6264c472e92b267e34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb0a4507c9ee778e2e7fe8b0fd36061bda9b5b37be4892e1f7e26ae64ca63cd`  
		Last Modified: Tue, 03 Jun 2025 14:20:36 GMT  
		Size: 54.9 MB (54910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377ea873cd754a6a20978f50996cd442a5a656557176945efe2a8b512c8ec67`  
		Last Modified: Tue, 03 Jun 2025 14:20:32 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5658be57652ba42697ef25b7a9fcbfdc40cbe1eeeb11544166e1fa153bd9`  
		Last Modified: Tue, 03 Jun 2025 14:20:46 GMT  
		Size: 214.8 MB (214763045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:57bb63a6f945d0fdf4b08888b1d0edbf0f243e17dfea9d07ccd8722a9802fe69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb00aa04bf21daef47629493fe69ebaba48417832b96f54c57be7e9b1e1981d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acf42fdf38ffa5f72d16502b4159a55abdc7a254940dad6aef18b6ba08ebbe`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:03a3b7b47326962209f87beeacd3eb2beb77ae1a58147c294437796b564a0c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223850960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0415e30900574f17287de1bf08ed29754670482974ceb0ef47156da3903e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674a4e954f37a2bea7b39bb7bb33f0526ff54a763b6f563b9717ee1a01bcf36`  
		Last Modified: Thu, 22 May 2025 02:38:00 GMT  
		Size: 149.1 MB (149141400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:ab6333dc024d7ceab9fc6de6dedcccb1a761752efd73d4821f25be1930a5068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847a17d042ccd5aff4eb4fab301da9b1c6bf85409ce308354c661871063aba0b`

```dockerfile
```

-	Layers:
	-	`sha256:5a1ae61141b68903af3af9a9e6523ba36f73d56da8b962383e0900856e083d1f`  
		Last Modified: Thu, 22 May 2025 02:37:55 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0cd5e15325a895087d8d0a9680d5020a75865954b678fd23b6e50890e6da57d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298384382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9793712575419414a0b91a392b076824d7c037fca5673686a82a1e0c2ced825d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4e386db6cc4700dfab329e9817bf54f58b0793d4429d1d34a2ea344a1d2d43`  
		Last Modified: Thu, 22 May 2025 08:19:57 GMT  
		Size: 54.7 MB (54682805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fdc18782299615847c130f05a333ae7ff5df5aa327b4c5e585b3592d2212f`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce4953d9d9148ba328eb4570971c9a32bb08d3794bcf6dd6e255605e1d1ad30`  
		Last Modified: Thu, 22 May 2025 08:20:00 GMT  
		Size: 214.1 MB (214148053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:1e423facc53e25464ea0ab09e9070c64cbf3ba353e6668db9a690ef724ceb24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108dd0f99ab6cde3c9a98a846f04cd6b57ab573b70aef98278eafff83619ccd2`

```dockerfile
```

-	Layers:
	-	`sha256:e9638a2b32d865f861bd8de2bd4518a8a598e12e80d71f0b149bc2be3a62c275`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-100.2.beta-sdk`

```console
$ docker pull dart@sha256:66489fe773c404431290502d2cd60e0211160f6a0b0de786c565cd417d672a2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0-100.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:8b2e8dfe4518fbe9e67d26526701b4f8d34c95ed329caa5b910f013f7ac38826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb3ae80660606c11d78657f0daad75a8565ec606fe9d6264c472e92b267e34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb0a4507c9ee778e2e7fe8b0fd36061bda9b5b37be4892e1f7e26ae64ca63cd`  
		Last Modified: Tue, 03 Jun 2025 14:20:36 GMT  
		Size: 54.9 MB (54910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377ea873cd754a6a20978f50996cd442a5a656557176945efe2a8b512c8ec67`  
		Last Modified: Tue, 03 Jun 2025 14:20:32 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5658be57652ba42697ef25b7a9fcbfdc40cbe1eeeb11544166e1fa153bd9`  
		Last Modified: Tue, 03 Jun 2025 14:20:46 GMT  
		Size: 214.8 MB (214763045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57bb63a6f945d0fdf4b08888b1d0edbf0f243e17dfea9d07ccd8722a9802fe69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb00aa04bf21daef47629493fe69ebaba48417832b96f54c57be7e9b1e1981d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acf42fdf38ffa5f72d16502b4159a55abdc7a254940dad6aef18b6ba08ebbe`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:03a3b7b47326962209f87beeacd3eb2beb77ae1a58147c294437796b564a0c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223850960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0415e30900574f17287de1bf08ed29754670482974ceb0ef47156da3903e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674a4e954f37a2bea7b39bb7bb33f0526ff54a763b6f563b9717ee1a01bcf36`  
		Last Modified: Thu, 22 May 2025 02:38:00 GMT  
		Size: 149.1 MB (149141400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ab6333dc024d7ceab9fc6de6dedcccb1a761752efd73d4821f25be1930a5068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847a17d042ccd5aff4eb4fab301da9b1c6bf85409ce308354c661871063aba0b`

```dockerfile
```

-	Layers:
	-	`sha256:5a1ae61141b68903af3af9a9e6523ba36f73d56da8b962383e0900856e083d1f`  
		Last Modified: Thu, 22 May 2025 02:37:55 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-100.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0cd5e15325a895087d8d0a9680d5020a75865954b678fd23b6e50890e6da57d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298384382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9793712575419414a0b91a392b076824d7c037fca5673686a82a1e0c2ced825d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4e386db6cc4700dfab329e9817bf54f58b0793d4429d1d34a2ea344a1d2d43`  
		Last Modified: Thu, 22 May 2025 08:19:57 GMT  
		Size: 54.7 MB (54682805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fdc18782299615847c130f05a333ae7ff5df5aa327b4c5e585b3592d2212f`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce4953d9d9148ba328eb4570971c9a32bb08d3794bcf6dd6e255605e1d1ad30`  
		Last Modified: Thu, 22 May 2025 08:20:00 GMT  
		Size: 214.1 MB (214148053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-100.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1e423facc53e25464ea0ab09e9070c64cbf3ba353e6668db9a690ef724ceb24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108dd0f99ab6cde3c9a98a846f04cd6b57ab573b70aef98278eafff83619ccd2`

```dockerfile
```

-	Layers:
	-	`sha256:e9638a2b32d865f861bd8de2bd4518a8a598e12e80d71f0b149bc2be3a62c275`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:66489fe773c404431290502d2cd60e0211160f6a0b0de786c565cd417d672a2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:8b2e8dfe4518fbe9e67d26526701b4f8d34c95ed329caa5b910f013f7ac38826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb3ae80660606c11d78657f0daad75a8565ec606fe9d6264c472e92b267e34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb0a4507c9ee778e2e7fe8b0fd36061bda9b5b37be4892e1f7e26ae64ca63cd`  
		Last Modified: Tue, 03 Jun 2025 14:20:36 GMT  
		Size: 54.9 MB (54910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377ea873cd754a6a20978f50996cd442a5a656557176945efe2a8b512c8ec67`  
		Last Modified: Tue, 03 Jun 2025 14:20:32 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5658be57652ba42697ef25b7a9fcbfdc40cbe1eeeb11544166e1fa153bd9`  
		Last Modified: Tue, 03 Jun 2025 14:20:46 GMT  
		Size: 214.8 MB (214763045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:57bb63a6f945d0fdf4b08888b1d0edbf0f243e17dfea9d07ccd8722a9802fe69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb00aa04bf21daef47629493fe69ebaba48417832b96f54c57be7e9b1e1981d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acf42fdf38ffa5f72d16502b4159a55abdc7a254940dad6aef18b6ba08ebbe`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:03a3b7b47326962209f87beeacd3eb2beb77ae1a58147c294437796b564a0c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223850960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0415e30900574f17287de1bf08ed29754670482974ceb0ef47156da3903e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674a4e954f37a2bea7b39bb7bb33f0526ff54a763b6f563b9717ee1a01bcf36`  
		Last Modified: Thu, 22 May 2025 02:38:00 GMT  
		Size: 149.1 MB (149141400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:ab6333dc024d7ceab9fc6de6dedcccb1a761752efd73d4821f25be1930a5068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847a17d042ccd5aff4eb4fab301da9b1c6bf85409ce308354c661871063aba0b`

```dockerfile
```

-	Layers:
	-	`sha256:5a1ae61141b68903af3af9a9e6523ba36f73d56da8b962383e0900856e083d1f`  
		Last Modified: Thu, 22 May 2025 02:37:55 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0cd5e15325a895087d8d0a9680d5020a75865954b678fd23b6e50890e6da57d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298384382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9793712575419414a0b91a392b076824d7c037fca5673686a82a1e0c2ced825d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4e386db6cc4700dfab329e9817bf54f58b0793d4429d1d34a2ea344a1d2d43`  
		Last Modified: Thu, 22 May 2025 08:19:57 GMT  
		Size: 54.7 MB (54682805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fdc18782299615847c130f05a333ae7ff5df5aa327b4c5e585b3592d2212f`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce4953d9d9148ba328eb4570971c9a32bb08d3794bcf6dd6e255605e1d1ad30`  
		Last Modified: Thu, 22 May 2025 08:20:00 GMT  
		Size: 214.1 MB (214148053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:1e423facc53e25464ea0ab09e9070c64cbf3ba353e6668db9a690ef724ceb24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108dd0f99ab6cde3c9a98a846f04cd6b57ab573b70aef98278eafff83619ccd2`

```dockerfile
```

-	Layers:
	-	`sha256:e9638a2b32d865f861bd8de2bd4518a8a598e12e80d71f0b149bc2be3a62c275`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:66489fe773c404431290502d2cd60e0211160f6a0b0de786c565cd417d672a2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:8b2e8dfe4518fbe9e67d26526701b4f8d34c95ed329caa5b910f013f7ac38826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299684128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81eb3ae80660606c11d78657f0daad75a8565ec606fe9d6264c472e92b267e34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb0a4507c9ee778e2e7fe8b0fd36061bda9b5b37be4892e1f7e26ae64ca63cd`  
		Last Modified: Tue, 03 Jun 2025 14:20:36 GMT  
		Size: 54.9 MB (54910275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377ea873cd754a6a20978f50996cd442a5a656557176945efe2a8b512c8ec67`  
		Last Modified: Tue, 03 Jun 2025 14:20:32 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5658be57652ba42697ef25b7a9fcbfdc40cbe1eeeb11544166e1fa153bd9`  
		Last Modified: Tue, 03 Jun 2025 14:20:46 GMT  
		Size: 214.8 MB (214763045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:57bb63a6f945d0fdf4b08888b1d0edbf0f243e17dfea9d07ccd8722a9802fe69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb00aa04bf21daef47629493fe69ebaba48417832b96f54c57be7e9b1e1981d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acf42fdf38ffa5f72d16502b4159a55abdc7a254940dad6aef18b6ba08ebbe`  
		Last Modified: Wed, 21 May 2025 23:21:39 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:03a3b7b47326962209f87beeacd3eb2beb77ae1a58147c294437796b564a0c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223850960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea0415e30900574f17287de1bf08ed29754670482974ceb0ef47156da3903e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c85147be7637b7c2750d42cfef2af5f2b7a9b21edf1baf341d3b9ff16d0d0b`  
		Last Modified: Thu, 22 May 2025 02:37:05 GMT  
		Size: 49.6 MB (49554662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40929bf8357109c1a8d00381005b544ba68df0322b49f6d2e58998e671ea0c84`  
		Last Modified: Thu, 22 May 2025 02:37:03 GMT  
		Size: 1.2 MB (1221944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e674a4e954f37a2bea7b39bb7bb33f0526ff54a763b6f563b9717ee1a01bcf36`  
		Last Modified: Thu, 22 May 2025 02:38:00 GMT  
		Size: 149.1 MB (149141400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ab6333dc024d7ceab9fc6de6dedcccb1a761752efd73d4821f25be1930a5068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847a17d042ccd5aff4eb4fab301da9b1c6bf85409ce308354c661871063aba0b`

```dockerfile
```

-	Layers:
	-	`sha256:5a1ae61141b68903af3af9a9e6523ba36f73d56da8b962383e0900856e083d1f`  
		Last Modified: Thu, 22 May 2025 02:37:55 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:0cd5e15325a895087d8d0a9680d5020a75865954b678fd23b6e50890e6da57d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298384382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9793712575419414a0b91a392b076824d7c037fca5673686a82a1e0c2ced825d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 20 May 2025 17:43:00 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 20 May 2025 17:43:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 May 2025 17:43:00 GMT
WORKDIR /root
# Tue, 20 May 2025 17:43:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9b503e642c862f404b46490cb6ba652c71d276fb7eb415283abe172a8574806f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de3439e67cf932c8d1f5fc82e8b68635cebcb8b0fb95a52a3a34122027c1cc51;             SDK_ARCH="arm";;         arm64)             DART_SHA256=fd0871a012ccc9c49ee8e9b2e6ba0ea36336c7cc38af05646ca513c4ccb0b616;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.9.0-100.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4e386db6cc4700dfab329e9817bf54f58b0793d4429d1d34a2ea344a1d2d43`  
		Last Modified: Thu, 22 May 2025 08:19:57 GMT  
		Size: 54.7 MB (54682805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0fdc18782299615847c130f05a333ae7ff5df5aa327b4c5e585b3592d2212f`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce4953d9d9148ba328eb4570971c9a32bb08d3794bcf6dd6e255605e1d1ad30`  
		Last Modified: Thu, 22 May 2025 08:20:00 GMT  
		Size: 214.1 MB (214148053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1e423facc53e25464ea0ab09e9070c64cbf3ba353e6668db9a690ef724ceb24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108dd0f99ab6cde3c9a98a846f04cd6b57ab573b70aef98278eafff83619ccd2`

```dockerfile
```

-	Layers:
	-	`sha256:e9638a2b32d865f861bd8de2bd4518a8a598e12e80d71f0b149bc2be3a62c275`  
		Last Modified: Thu, 22 May 2025 08:19:55 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:fe642bf69ca5f7948398845c4d0d52f58dcd3a0f49267052540864f9dfac279d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:10371204eeb4295fa0c72c8bfada0695a6e9fa11771aa5c071124b11306b33ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285785431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15ec1ab5cfb67609eaeaa917b2fd7100eac2c8263aefa061faa36591a33af3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e78b61684b8296f9d7618456ae85171f797dcdf620e989c6aafe47fd53b5e30`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 54.9 MB (54910587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa6e1c585b883e8daba14205bdc2d2204234f2d07fe5e1afa1ec106da37aeb3`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 1.8 MB (1785450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7b697e25f2bee4da0ee14654f91ae3475fcb7b8fff29316131203b359de62`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 200.9 MB (200864032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f868a0e5912d69882b609c7b66f4d18ac0d1c204cd6794d65bca5c9758a3a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcce69bc98ae927d47451d555fc1de731ec46b85d544c9c37ec5f50356461e8`

```dockerfile
```

-	Layers:
	-	`sha256:4092980da37acebcf0cb814fcacf86b254f596d1c8e14208c4aa0cc42c460cee`  
		Last Modified: Mon, 02 Jun 2025 17:15:29 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:930bd44ba22a139d993ac59d72a2818e556555f6fc6f1a555bbb5674759430ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214484909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2ada96ac98018bb65a23d63274ef771179859e019aea63810056bb724ce13`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62428aa22c39b2dd2bf24735afb12d5b3440c734552991508ea60c3d659b5e36`  
		Last Modified: Tue, 03 Jun 2025 13:42:00 GMT  
		Size: 49.6 MB (49554608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d582c126c6d2f44adda0ecfacce831f59ffb34a05594716e8bca567ebcf1b`  
		Last Modified: Tue, 03 Jun 2025 13:41:55 GMT  
		Size: 1.2 MB (1221948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18bd7fbac210b7350c504d921a5f074aec9c42dd8d59d71023a07acc1040a6`  
		Last Modified: Tue, 03 Jun 2025 13:42:04 GMT  
		Size: 139.8 MB (139775399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b02798cec717a2c5a3b39e3985560315cd7246f6c0e2c01ed9044499c2c7247e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246143c88f649a6a140237a6ebc9728e05171b26e0b5ec00a4982281708545af`

```dockerfile
```

-	Layers:
	-	`sha256:f586435635f21c94c52c00297d05a38c8606572832f112d8ced6c60edcca958b`  
		Last Modified: Mon, 02 Jun 2025 18:05:50 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5628e0da718392653859079830983fde80b91a1d7e8a450d06570c74db8f3882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284458153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0882304c771fff3f4ddc03cb416cadb307ddfd3069e419f880588b4cf8621717`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 28 May 2025 10:45:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 28 May 2025 10:45:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 May 2025 10:45:30 GMT
WORKDIR /root
# Wed, 28 May 2025 10:45:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0d58c010a361f3f1588b1c2f57942f7ccaf7b7abbe03404fef7a102eb638f09d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=02adb724b0b684573f7630b3d79ef729f8cf9fff561f5170bcc195ee2477e1e6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=78a3240097bee3b79b009c69ead22e1aaedededcbe093eaa980084c5661096c8;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.8.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ae5e8520d41cc02224fd810c40c9ad2053f8ad9b1b985de2082ef3d78ca8af`  
		Last Modified: Tue, 03 Jun 2025 13:38:18 GMT  
		Size: 54.7 MB (54682986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95208646e9dc96bca3dc45198cbc6a6f39279c8878d16c432e307c4cce52d5`  
		Last Modified: Tue, 03 Jun 2025 13:38:15 GMT  
		Size: 1.5 MB (1488225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ae03d01727840f3d984c029252468303f72a2b3b7191436095727d90bc9661`  
		Last Modified: Tue, 03 Jun 2025 13:38:26 GMT  
		Size: 200.2 MB (200221630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:da9b9bf20357028a22593e52ae40e28562e9f6419e93a232939d506c818d6a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b8e7b24aa16d4efe176cff28f012f3f3d5d36c15b673a86fc1a04b8541f15b`

```dockerfile
```

-	Layers:
	-	`sha256:0a1ccf21747c27aeb53881e8e807ac1e443f348d3e99c8a03ca927f08462e143`  
		Last Modified: Mon, 02 Jun 2025 18:18:49 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
