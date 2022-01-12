<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:2`](#dart2)
-	[`dart:2-sdk`](#dart2-sdk)
-	[`dart:2.15`](#dart215)
-	[`dart:2.15-sdk`](#dart215-sdk)
-	[`dart:2.15.1`](#dart2151)
-	[`dart:2.15.1-sdk`](#dart2151-sdk)
-	[`dart:2.16.0-134.1.beta`](#dart2160-1341beta)
-	[`dart:2.16.0-134.1.beta-sdk`](#dart2160-1341beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:2`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2-sdk`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.15` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15-sdk`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.15-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15.1`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.15.1` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.15.1-sdk`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:2.15.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:2.15.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:2.16.0-134.1.beta`

**does not exist** (yet?)

## `dart:2.16.0-134.1.beta-sdk`

**does not exist** (yet?)

## `dart:beta`

```console
$ docker pull dart@sha256:e8de80bbe0751030dd6f006b8297b5ff193a6111efd5c54774b78ba90e2cdb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:1c24661ac875e11b2a31c7abe1f3bc81b62de5d068b18252ca2f6d3eb1e3cedf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283568777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8cb35c3be994f9da66a4f3a3dcbf498c8437a84db891ba9e9771b4b5e413b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad35e7d39210bebff8e8cb87bda3d96226d6582f5461f9e8328f06cf2b8505d`  
		Last Modified: Tue, 21 Dec 2021 02:14:38 GMT  
		Size: 204.5 MB (204472423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:badc3664b9436b52b57a443dd8d80c070361256410bb754085863fab740cc194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190590750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775e46517a6b43baa5d988c24d92a45b8908db8bad29bec9401dfeb044cc62b3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc690b285a9d6422dcb01834f5e29ba4c48745d2b25f4dfc904afedd15d09a1`  
		Last Modified: Tue, 21 Dec 2021 03:37:20 GMT  
		Size: 122.1 MB (122081562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:123316efda5dded883b46b48c5f0a63cd20967636faaab349949884bcb05b5c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200774042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b458d64b107ef292fdd5e0d50f81d1a48eba71978fc79b98ab99adf698746e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ab21c3eaccc7125daa5a6d7c9438c3cd1d15cc8eb241b617529050493cc78a`  
		Last Modified: Tue, 21 Dec 2021 10:44:16 GMT  
		Size: 123.6 MB (123579961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:e8de80bbe0751030dd6f006b8297b5ff193a6111efd5c54774b78ba90e2cdb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1c24661ac875e11b2a31c7abe1f3bc81b62de5d068b18252ca2f6d3eb1e3cedf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283568777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc8cb35c3be994f9da66a4f3a3dcbf498c8437a84db891ba9e9771b4b5e413b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad35e7d39210bebff8e8cb87bda3d96226d6582f5461f9e8328f06cf2b8505d`  
		Last Modified: Tue, 21 Dec 2021 02:14:38 GMT  
		Size: 204.5 MB (204472423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:badc3664b9436b52b57a443dd8d80c070361256410bb754085863fab740cc194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.6 MB (190590750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775e46517a6b43baa5d988c24d92a45b8908db8bad29bec9401dfeb044cc62b3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc690b285a9d6422dcb01834f5e29ba4c48745d2b25f4dfc904afedd15d09a1`  
		Last Modified: Tue, 21 Dec 2021 03:37:20 GMT  
		Size: 122.1 MB (122081562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:123316efda5dded883b46b48c5f0a63cd20967636faaab349949884bcb05b5c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200774042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b458d64b107ef292fdd5e0d50f81d1a48eba71978fc79b98ab99adf698746e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b758aefce016c0dfdc8b4e2941c88e0a5c0d29339c4432abd58fab4ef076d2dc;             SDK_ARCH="x64";;         armhf)             DART_SHA256=a6db5eae93c894effda6aeac737a304a31f56c48dcea21ab80fb7b16febbaa53;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1427731141075364bc2f6b2c89c3db28e781048b05149ab8d336ab213382aea6;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.16.0-80.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ab21c3eaccc7125daa5a6d7c9438c3cd1d15cc8eb241b617529050493cc78a`  
		Last Modified: Tue, 21 Dec 2021 10:44:16 GMT  
		Size: 123.6 MB (123579961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:9043b377c0448fb27052f30ab8504c2e76730cc30c12cc5b5c9eb3981b5ef252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e4427c7e48cc0aa02672d25dd2e9ea9c99604e711710941a1ed6586d388e9e57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276273063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5f7394762039f22f3f575801707a62dfae886321aa40995d77b9c8b30161e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:12:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:12:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 02:12:11 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 02:12:11 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:12:11 GMT
WORKDIR /root
# Tue, 21 Dec 2021 02:12:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc662689f4adb433a913e6d893c92c5fde897581ac0f2fd8a961247559923984`  
		Last Modified: Tue, 21 Dec 2021 02:13:15 GMT  
		Size: 49.6 MB (49583489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704f11b6b5127161ce1f81555ab9fd12a7c019851b026d5551e7c1fef269278`  
		Last Modified: Tue, 21 Dec 2021 02:13:07 GMT  
		Size: 2.4 MB (2359142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73862d93e27af5ad2d89066699c3e2b89718547f6161e0f833715ea325090086`  
		Last Modified: Tue, 21 Dec 2021 02:13:37 GMT  
		Size: 197.2 MB (197176709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e214892b10b121595eabe9b2c093b38b8ffeeecc94ab382a92c06bcbb2f72887
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183687340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee867e1b13e6f0fc7de5626cf76776c2ec7c8e0cee56319d99bb2a5bcd034a4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:00:52 GMT
ADD file:1381e18e2847f24ebd16d8e83ad940adeff45aca2c327d4e07d7451816f29420 in / 
# Tue, 21 Dec 2021 02:00:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:31:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:31:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 03:31:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 03:31:49 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 03:31:50 GMT
WORKDIR /root
# Tue, 21 Dec 2021 03:32:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:b597e1a6bc27aa2a24a587cb687c9551dfbcfa730a11d48c5a44ff77ff6fdd75`  
		Last Modified: Tue, 21 Dec 2021 02:16:50 GMT  
		Size: 22.8 MB (22754324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724933b2255953150dd8ff394645661fd54951a61361422bd95093fe5e0a5b6f`  
		Last Modified: Tue, 21 Dec 2021 03:34:31 GMT  
		Size: 44.4 MB (44398962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df35a6fcdd7a30ac0a37835fb1e33934c2468b5f30d08368ae3bf49f7bfa461`  
		Last Modified: Tue, 21 Dec 2021 03:34:06 GMT  
		Size: 1.4 MB (1355902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446c54f72d5347582c556d2537f97460e566a4199eca6f9d6cacc983738576`  
		Last Modified: Tue, 21 Dec 2021 03:35:19 GMT  
		Size: 115.2 MB (115178152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f5ec034c53c3f93765d86d9b85201e6360ae5b4991adfe0d688b34576050de06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335738f0f8d990c39816d0e69eefd7b7c9efb18fe48d71e874383963ce10821b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:42:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 21 Dec 2021 10:42:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 21 Dec 2021 10:42:06 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 10:42:07 GMT
WORKDIR /root
# Tue, 21 Dec 2021 10:42:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727522a568dd0f19904269187584697524c2ca41951cceb1d2c0e2b5cca2b237`  
		Last Modified: Tue, 21 Dec 2021 10:43:15 GMT  
		Size: 49.6 MB (49639004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb72aa07e1e9efbca3d1261e042e1fbe1bb24e1c06e0ec46137338ad38ee1cc`  
		Last Modified: Tue, 21 Dec 2021 10:43:07 GMT  
		Size: 1.6 MB (1631928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ed7d23e8421ea3a339f708bc20d733065ce343fbd9eb0324bd1da256bd1c8c`  
		Last Modified: Tue, 21 Dec 2021 10:43:24 GMT  
		Size: 116.6 MB (116567341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
