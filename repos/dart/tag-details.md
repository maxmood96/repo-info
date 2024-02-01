<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.2`](#dart32)
-	[`dart:3.2-sdk`](#dart32-sdk)
-	[`dart:3.2.6`](#dart326)
-	[`dart:3.2.6-sdk`](#dart326-sdk)
-	[`dart:3.3.0-279.3.beta`](#dart330-2793beta)
-	[`dart:3.3.0-279.3.beta-sdk`](#dart330-2793beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:5a27bc3ef833434a5d46ec3debca6fcb301513733719bb6f230b37557de20bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:5c699373db8da9377a1d0ca4920f7500fac5a70a2fa6c287a575f2c8054c6b89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d4acbe8d70dd32ea2920d45a8f05c5b03f51aeac81be8013da9cd62bf0af37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704f8df99f396b60049ca52963e733dea846a9777f6e87e1f3f35fa613a4a689`  
		Last Modified: Thu, 01 Feb 2024 06:46:38 GMT  
		Size: 223.0 MB (222961095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:1d7cbc4a9c4fcd653e05e8d0c5cd464af5b008097fad3c5c7977945dff390d54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203454992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5caa75731033bb7e4c9a41196a35e8b1b11b6a9ee855bd2d09887e5d80058b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:04:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0236aea81b71b2bf2a81eae3a163b6ef212639a686f61165b17e3a678d572e`  
		Last Modified: Thu, 01 Feb 2024 03:05:52 GMT  
		Size: 128.3 MB (128348880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:08456097f865fda9c193e5053627ac92c21f9e2344a17211c6ef55ac4761df8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307211401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0b61b51b05e49deb40706b9cef8f04c293f63c873e54b971da6dd3125f064`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Wed, 31 Jan 2024 23:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8a1ca907b9ef7458c126c7f50945fff6d8045755e3f4a4f1e95b5768e260fc`  
		Last Modified: Thu, 01 Feb 2024 00:00:56 GMT  
		Size: 222.2 MB (222212411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3-sdk`

```console
$ docker pull dart@sha256:5a27bc3ef833434a5d46ec3debca6fcb301513733719bb6f230b37557de20bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5c699373db8da9377a1d0ca4920f7500fac5a70a2fa6c287a575f2c8054c6b89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d4acbe8d70dd32ea2920d45a8f05c5b03f51aeac81be8013da9cd62bf0af37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704f8df99f396b60049ca52963e733dea846a9777f6e87e1f3f35fa613a4a689`  
		Last Modified: Thu, 01 Feb 2024 06:46:38 GMT  
		Size: 223.0 MB (222961095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:1d7cbc4a9c4fcd653e05e8d0c5cd464af5b008097fad3c5c7977945dff390d54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203454992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5caa75731033bb7e4c9a41196a35e8b1b11b6a9ee855bd2d09887e5d80058b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:04:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0236aea81b71b2bf2a81eae3a163b6ef212639a686f61165b17e3a678d572e`  
		Last Modified: Thu, 01 Feb 2024 03:05:52 GMT  
		Size: 128.3 MB (128348880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:08456097f865fda9c193e5053627ac92c21f9e2344a17211c6ef55ac4761df8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307211401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0b61b51b05e49deb40706b9cef8f04c293f63c873e54b971da6dd3125f064`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Wed, 31 Jan 2024 23:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8a1ca907b9ef7458c126c7f50945fff6d8045755e3f4a4f1e95b5768e260fc`  
		Last Modified: Thu, 01 Feb 2024 00:00:56 GMT  
		Size: 222.2 MB (222212411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.2`

```console
$ docker pull dart@sha256:5a27bc3ef833434a5d46ec3debca6fcb301513733719bb6f230b37557de20bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2` - linux; amd64

```console
$ docker pull dart@sha256:5c699373db8da9377a1d0ca4920f7500fac5a70a2fa6c287a575f2c8054c6b89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d4acbe8d70dd32ea2920d45a8f05c5b03f51aeac81be8013da9cd62bf0af37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704f8df99f396b60049ca52963e733dea846a9777f6e87e1f3f35fa613a4a689`  
		Last Modified: Thu, 01 Feb 2024 06:46:38 GMT  
		Size: 223.0 MB (222961095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:1d7cbc4a9c4fcd653e05e8d0c5cd464af5b008097fad3c5c7977945dff390d54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203454992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5caa75731033bb7e4c9a41196a35e8b1b11b6a9ee855bd2d09887e5d80058b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:04:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0236aea81b71b2bf2a81eae3a163b6ef212639a686f61165b17e3a678d572e`  
		Last Modified: Thu, 01 Feb 2024 03:05:52 GMT  
		Size: 128.3 MB (128348880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:08456097f865fda9c193e5053627ac92c21f9e2344a17211c6ef55ac4761df8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307211401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0b61b51b05e49deb40706b9cef8f04c293f63c873e54b971da6dd3125f064`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Wed, 31 Jan 2024 23:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8a1ca907b9ef7458c126c7f50945fff6d8045755e3f4a4f1e95b5768e260fc`  
		Last Modified: Thu, 01 Feb 2024 00:00:56 GMT  
		Size: 222.2 MB (222212411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.2-sdk`

```console
$ docker pull dart@sha256:5a27bc3ef833434a5d46ec3debca6fcb301513733719bb6f230b37557de20bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5c699373db8da9377a1d0ca4920f7500fac5a70a2fa6c287a575f2c8054c6b89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d4acbe8d70dd32ea2920d45a8f05c5b03f51aeac81be8013da9cd62bf0af37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704f8df99f396b60049ca52963e733dea846a9777f6e87e1f3f35fa613a4a689`  
		Last Modified: Thu, 01 Feb 2024 06:46:38 GMT  
		Size: 223.0 MB (222961095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:1d7cbc4a9c4fcd653e05e8d0c5cd464af5b008097fad3c5c7977945dff390d54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203454992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5caa75731033bb7e4c9a41196a35e8b1b11b6a9ee855bd2d09887e5d80058b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:04:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0236aea81b71b2bf2a81eae3a163b6ef212639a686f61165b17e3a678d572e`  
		Last Modified: Thu, 01 Feb 2024 03:05:52 GMT  
		Size: 128.3 MB (128348880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:08456097f865fda9c193e5053627ac92c21f9e2344a17211c6ef55ac4761df8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307211401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0b61b51b05e49deb40706b9cef8f04c293f63c873e54b971da6dd3125f064`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Wed, 31 Jan 2024 23:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8a1ca907b9ef7458c126c7f50945fff6d8045755e3f4a4f1e95b5768e260fc`  
		Last Modified: Thu, 01 Feb 2024 00:00:56 GMT  
		Size: 222.2 MB (222212411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.2.6`

**does not exist** (yet?)

## `dart:3.2.6-sdk`

**does not exist** (yet?)

## `dart:3.3.0-279.3.beta`

**does not exist** (yet?)

## `dart:3.3.0-279.3.beta-sdk`

**does not exist** (yet?)

## `dart:beta`

```console
$ docker pull dart@sha256:30c62d243ea5fb69ed9c40def90076d966e3d9841a5107c15470b4091d99347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:3de8d548df5d9b4fd4f35335f6d9e89bf2604ddaca5d36a49f29e736a638e0c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314074055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a36a7246c16ba675537bde00d0b0cfd944999de388e5fd557f10b66f075bf76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdae9f9b5cb19b35df169b3834bf33188288c11abba0208c729656ecca2309c1`  
		Last Modified: Thu, 01 Feb 2024 06:47:32 GMT  
		Size: 228.5 MB (228468465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:07fce424083f4fbd71e38c83d93939c1787bcb84e93ba91d3b3e7500f0a4ba85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206934831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a587a839df63f08eba5e8aeffbf016463737dd155601b4287cc971bd5af882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:05:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefcf8636d0ce664273ee062ace1df536a293548b75b412ead99245ccebe0371`  
		Last Modified: Thu, 01 Feb 2024 03:06:39 GMT  
		Size: 131.8 MB (131828719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:43873a19090010019b83f37a642fec3fa37ecaee725f4bcba1f6caaaf5b63a0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312721665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce8d235337119b9422a0cf1d5b0115f4533abc440a8bf6781fa4025cd5ced9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Thu, 01 Feb 2024 00:00:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214ec7f4a499d5d9912f9d02ec94e48aab9b4fd6db88b26b3a20602cafbba07e`  
		Last Modified: Thu, 01 Feb 2024 00:01:44 GMT  
		Size: 227.7 MB (227722675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:30c62d243ea5fb69ed9c40def90076d966e3d9841a5107c15470b4091d99347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:3de8d548df5d9b4fd4f35335f6d9e89bf2604ddaca5d36a49f29e736a638e0c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314074055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a36a7246c16ba675537bde00d0b0cfd944999de388e5fd557f10b66f075bf76`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdae9f9b5cb19b35df169b3834bf33188288c11abba0208c729656ecca2309c1`  
		Last Modified: Thu, 01 Feb 2024 06:47:32 GMT  
		Size: 228.5 MB (228468465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:07fce424083f4fbd71e38c83d93939c1787bcb84e93ba91d3b3e7500f0a4ba85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206934831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a587a839df63f08eba5e8aeffbf016463737dd155601b4287cc971bd5af882`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:05:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefcf8636d0ce664273ee062ace1df536a293548b75b412ead99245ccebe0371`  
		Last Modified: Thu, 01 Feb 2024 03:06:39 GMT  
		Size: 131.8 MB (131828719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:43873a19090010019b83f37a642fec3fa37ecaee725f4bcba1f6caaaf5b63a0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312721665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce8d235337119b9422a0cf1d5b0115f4533abc440a8bf6781fa4025cd5ced9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Thu, 01 Feb 2024 00:00:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214ec7f4a499d5d9912f9d02ec94e48aab9b4fd6db88b26b3a20602cafbba07e`  
		Last Modified: Thu, 01 Feb 2024 00:01:44 GMT  
		Size: 227.7 MB (227722675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:5a27bc3ef833434a5d46ec3debca6fcb301513733719bb6f230b37557de20bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:5c699373db8da9377a1d0ca4920f7500fac5a70a2fa6c287a575f2c8054c6b89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d4acbe8d70dd32ea2920d45a8f05c5b03f51aeac81be8013da9cd62bf0af37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704f8df99f396b60049ca52963e733dea846a9777f6e87e1f3f35fa613a4a689`  
		Last Modified: Thu, 01 Feb 2024 06:46:38 GMT  
		Size: 223.0 MB (222961095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:1d7cbc4a9c4fcd653e05e8d0c5cd464af5b008097fad3c5c7977945dff390d54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203454992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5caa75731033bb7e4c9a41196a35e8b1b11b6a9ee855bd2d09887e5d80058b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:04:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0236aea81b71b2bf2a81eae3a163b6ef212639a686f61165b17e3a678d572e`  
		Last Modified: Thu, 01 Feb 2024 03:05:52 GMT  
		Size: 128.3 MB (128348880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:08456097f865fda9c193e5053627ac92c21f9e2344a17211c6ef55ac4761df8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307211401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0b61b51b05e49deb40706b9cef8f04c293f63c873e54b971da6dd3125f064`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Wed, 31 Jan 2024 23:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8a1ca907b9ef7458c126c7f50945fff6d8045755e3f4a4f1e95b5768e260fc`  
		Last Modified: Thu, 01 Feb 2024 00:00:56 GMT  
		Size: 222.2 MB (222212411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:5a27bc3ef833434a5d46ec3debca6fcb301513733719bb6f230b37557de20bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:5c699373db8da9377a1d0ca4920f7500fac5a70a2fa6c287a575f2c8054c6b89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d4acbe8d70dd32ea2920d45a8f05c5b03f51aeac81be8013da9cd62bf0af37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704f8df99f396b60049ca52963e733dea846a9777f6e87e1f3f35fa613a4a689`  
		Last Modified: Thu, 01 Feb 2024 06:46:38 GMT  
		Size: 223.0 MB (222961095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:1d7cbc4a9c4fcd653e05e8d0c5cd464af5b008097fad3c5c7977945dff390d54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203454992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5caa75731033bb7e4c9a41196a35e8b1b11b6a9ee855bd2d09887e5d80058b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:04:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0236aea81b71b2bf2a81eae3a163b6ef212639a686f61165b17e3a678d572e`  
		Last Modified: Thu, 01 Feb 2024 03:05:52 GMT  
		Size: 128.3 MB (128348880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:08456097f865fda9c193e5053627ac92c21f9e2344a17211c6ef55ac4761df8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307211401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0b61b51b05e49deb40706b9cef8f04c293f63c873e54b971da6dd3125f064`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Wed, 31 Jan 2024 23:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8a1ca907b9ef7458c126c7f50945fff6d8045755e3f4a4f1e95b5768e260fc`  
		Last Modified: Thu, 01 Feb 2024 00:00:56 GMT  
		Size: 222.2 MB (222212411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:5a27bc3ef833434a5d46ec3debca6fcb301513733719bb6f230b37557de20bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:5c699373db8da9377a1d0ca4920f7500fac5a70a2fa6c287a575f2c8054c6b89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d4acbe8d70dd32ea2920d45a8f05c5b03f51aeac81be8013da9cd62bf0af37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704f8df99f396b60049ca52963e733dea846a9777f6e87e1f3f35fa613a4a689`  
		Last Modified: Thu, 01 Feb 2024 06:46:38 GMT  
		Size: 223.0 MB (222961095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:1d7cbc4a9c4fcd653e05e8d0c5cd464af5b008097fad3c5c7977945dff390d54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203454992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5caa75731033bb7e4c9a41196a35e8b1b11b6a9ee855bd2d09887e5d80058b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:04:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0236aea81b71b2bf2a81eae3a163b6ef212639a686f61165b17e3a678d572e`  
		Last Modified: Thu, 01 Feb 2024 03:05:52 GMT  
		Size: 128.3 MB (128348880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:08456097f865fda9c193e5053627ac92c21f9e2344a17211c6ef55ac4761df8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307211401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0b61b51b05e49deb40706b9cef8f04c293f63c873e54b971da6dd3125f064`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Wed, 31 Jan 2024 23:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8a1ca907b9ef7458c126c7f50945fff6d8045755e3f4a4f1e95b5768e260fc`  
		Last Modified: Thu, 01 Feb 2024 00:00:56 GMT  
		Size: 222.2 MB (222212411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:5a27bc3ef833434a5d46ec3debca6fcb301513733719bb6f230b37557de20bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:5c699373db8da9377a1d0ca4920f7500fac5a70a2fa6c287a575f2c8054c6b89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d4acbe8d70dd32ea2920d45a8f05c5b03f51aeac81be8013da9cd62bf0af37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:45:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:45:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 06:45:10 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 06:45:10 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:45:10 GMT
WORKDIR /root
# Thu, 01 Feb 2024 06:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb856c56cc295944b3089e5d419b7da41eeba9d62af25b407f8814ac649c3f15`  
		Last Modified: Thu, 01 Feb 2024 06:46:16 GMT  
		Size: 54.7 MB (54654404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20ee8784d8b2bbcc7bebbaf905d1c12ed9e6bf1f959d041b119dd334d404b44`  
		Last Modified: Thu, 01 Feb 2024 06:46:09 GMT  
		Size: 1.8 MB (1800721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704f8df99f396b60049ca52963e733dea846a9777f6e87e1f3f35fa613a4a689`  
		Last Modified: Thu, 01 Feb 2024 06:46:38 GMT  
		Size: 223.0 MB (222961095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:1d7cbc4a9c4fcd653e05e8d0c5cd464af5b008097fad3c5c7977945dff390d54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203454992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5caa75731033bb7e4c9a41196a35e8b1b11b6a9ee855bd2d09887e5d80058b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 03:04:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 03:04:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 01 Feb 2024 03:04:42 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 01 Feb 2024 03:04:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 03:04:43 GMT
WORKDIR /root
# Thu, 01 Feb 2024 03:04:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c691e45c53bf0dcc2ff82acf359b96c8a73a1bd896d6ce6e6e94a651eec4d5`  
		Last Modified: Thu, 01 Feb 2024 03:05:39 GMT  
		Size: 49.1 MB (49137166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6767c2ba959af85f7303ac2aeea7320eec31783ce5fa0dc98b455128ba2f64e1`  
		Last Modified: Thu, 01 Feb 2024 03:05:31 GMT  
		Size: 1.2 MB (1227381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0236aea81b71b2bf2a81eae3a163b6ef212639a686f61165b17e3a678d572e`  
		Last Modified: Thu, 01 Feb 2024 03:05:52 GMT  
		Size: 128.3 MB (128348880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:08456097f865fda9c193e5053627ac92c21f9e2344a17211c6ef55ac4761df8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307211401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0b61b51b05e49deb40706b9cef8f04c293f63c873e54b971da6dd3125f064`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:59:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:59:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 31 Jan 2024 23:59:30 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 31 Jan 2024 23:59:30 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:59:30 GMT
WORKDIR /root
# Wed, 31 Jan 2024 23:59:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0935dc7e1de7a769039e0fdee30a5b625a2f5889c0d48624bca58d104abdb5`  
		Last Modified: Thu, 01 Feb 2024 00:00:39 GMT  
		Size: 54.3 MB (54324395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc5dc1b7901c1e9dd5577725986265f9dc8d15ec9403999827fb7d917152378`  
		Last Modified: Thu, 01 Feb 2024 00:00:33 GMT  
		Size: 1.5 MB (1493763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8a1ca907b9ef7458c126c7f50945fff6d8045755e3f4a4f1e95b5768e260fc`  
		Last Modified: Thu, 01 Feb 2024 00:00:56 GMT  
		Size: 222.2 MB (222212411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
