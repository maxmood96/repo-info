## `dart:stable-sdk`

```console
$ docker pull dart@sha256:093af7b5701910004117c19e7432571e0569edb2cd4fa0ed4b856be6ee2ed9cb
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
$ docker pull dart@sha256:0f892ee2369111c1ca2f022b589706133e7d298ce42a244f54e8b63825df24c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193761564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2e249c37e65aa4de53e7dc8fd39b717a7cdfe925bad33d1a992c85e7ccf3e2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:10:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:10:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 02 Dec 2021 10:10:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 02 Dec 2021 10:10:36 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:10:37 GMT
WORKDIR /root
# Tue, 14 Dec 2021 20:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0f45dcaa53b4090b69b277b885ea9a4cb3a41589c9119113e1b978ad55ce335f;             SDK_ARCH="x64";;         armhf)             DART_SHA256=751935fc08dec2121410c3f2f33de8215d8a4e5f21192a4c42c4b81dd00f8659;             SDK_ARCH="arm";;         arm64)             DART_SHA256=8836c294234352cc53e8aea4a1ce0442ebbb769a536ce7f309579da5020a2395;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/2.15.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9514eec777ef806660e5c8a0e2019db098e460e313b3212baad2d9a3c74a04`  
		Last Modified: Thu, 02 Dec 2021 10:11:47 GMT  
		Size: 49.6 MB (49639089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bd4fe19302b8d33de0926bafa96b46c46ec80d6bf5e69467b4b18f388e9e6d`  
		Last Modified: Thu, 02 Dec 2021 10:11:40 GMT  
		Size: 1.6 MB (1631924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8370c262418045f2747607696d072a6bbc5c9efb084a466711d003cab8eee4f5`  
		Last Modified: Tue, 14 Dec 2021 20:40:46 GMT  
		Size: 116.6 MB (116567407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
