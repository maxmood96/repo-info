<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.2`](#dart32)
-	[`dart:3.2-sdk`](#dart32-sdk)
-	[`dart:3.2.5`](#dart325)
-	[`dart:3.2.5-sdk`](#dart325-sdk)
-	[`dart:3.3.0-279.1.beta`](#dart330-2791beta)
-	[`dart:3.3.0-279.1.beta-sdk`](#dart330-2791beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
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
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
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
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
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
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
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

## `dart:3.2.5`

```console
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2.5` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.5` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.5` - linux; arm64 variant v8

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

## `dart:3.2.5-sdk`

```console
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2.5-sdk` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.5-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.5-sdk` - linux; arm64 variant v8

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

## `dart:3.3.0-279.1.beta`

```console
$ docker pull dart@sha256:f7370e419ca20b8387c47e72487d7fb07b9d41e065326453a8950c16a4b3e8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.3.0-279.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:211367b234f8fcabb4528418cecae2339116d049025fcc050a2c53e83261c4b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314046377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02696d8531a72724ec6d3bc896503c95303ee4bac329fa2247947cae11f4af61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:56:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9ba3faa32de9687a547526617d1a9a9fd18cc3c955e2995fa64d3029a86e5`  
		Last Modified: Thu, 18 Jan 2024 18:57:53 GMT  
		Size: 228.5 MB (228468864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3.0-279.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:263586c1ba3339f3090239f7abd168c66dc29e7585af9e368b747c32ac7fce97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206907335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaadfbd14febdc749e05d9891b6103a3fa365eec838524695555e30db31fcaf2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a41284d464c02eff25a5f4599cbf9b0b393ea6270d9e055e94a8a47d10875`  
		Last Modified: Thu, 18 Jan 2024 19:22:53 GMT  
		Size: 131.8 MB (131828680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3.0-279.1.beta` - linux; arm64 variant v8

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

## `dart:3.3.0-279.1.beta-sdk`

```console
$ docker pull dart@sha256:f7370e419ca20b8387c47e72487d7fb07b9d41e065326453a8950c16a4b3e8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.3.0-279.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:211367b234f8fcabb4528418cecae2339116d049025fcc050a2c53e83261c4b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314046377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02696d8531a72724ec6d3bc896503c95303ee4bac329fa2247947cae11f4af61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:56:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9ba3faa32de9687a547526617d1a9a9fd18cc3c955e2995fa64d3029a86e5`  
		Last Modified: Thu, 18 Jan 2024 18:57:53 GMT  
		Size: 228.5 MB (228468864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3.0-279.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:263586c1ba3339f3090239f7abd168c66dc29e7585af9e368b747c32ac7fce97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206907335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaadfbd14febdc749e05d9891b6103a3fa365eec838524695555e30db31fcaf2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a41284d464c02eff25a5f4599cbf9b0b393ea6270d9e055e94a8a47d10875`  
		Last Modified: Thu, 18 Jan 2024 19:22:53 GMT  
		Size: 131.8 MB (131828680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.3.0-279.1.beta-sdk` - linux; arm64 variant v8

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

## `dart:beta`

```console
$ docker pull dart@sha256:f7370e419ca20b8387c47e72487d7fb07b9d41e065326453a8950c16a4b3e8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:211367b234f8fcabb4528418cecae2339116d049025fcc050a2c53e83261c4b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314046377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02696d8531a72724ec6d3bc896503c95303ee4bac329fa2247947cae11f4af61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:56:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9ba3faa32de9687a547526617d1a9a9fd18cc3c955e2995fa64d3029a86e5`  
		Last Modified: Thu, 18 Jan 2024 18:57:53 GMT  
		Size: 228.5 MB (228468864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:263586c1ba3339f3090239f7abd168c66dc29e7585af9e368b747c32ac7fce97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206907335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaadfbd14febdc749e05d9891b6103a3fa365eec838524695555e30db31fcaf2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a41284d464c02eff25a5f4599cbf9b0b393ea6270d9e055e94a8a47d10875`  
		Last Modified: Thu, 18 Jan 2024 19:22:53 GMT  
		Size: 131.8 MB (131828680 bytes)  
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
$ docker pull dart@sha256:f7370e419ca20b8387c47e72487d7fb07b9d41e065326453a8950c16a4b3e8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:211367b234f8fcabb4528418cecae2339116d049025fcc050a2c53e83261c4b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314046377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02696d8531a72724ec6d3bc896503c95303ee4bac329fa2247947cae11f4af61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:56:11 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9ba3faa32de9687a547526617d1a9a9fd18cc3c955e2995fa64d3029a86e5`  
		Last Modified: Thu, 18 Jan 2024 18:57:53 GMT  
		Size: 228.5 MB (228468864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:263586c1ba3339f3090239f7abd168c66dc29e7585af9e368b747c32ac7fce97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206907335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaadfbd14febdc749e05d9891b6103a3fa365eec838524695555e30db31fcaf2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a7ed5168acabce7cfb292de210d5fedb33a481548470a6e8142b20946ca81cfb;             SDK_ARCH="x64";;         armhf)             DART_SHA256=de28b2ab3d772026ee92d2911c0c476c147341d67a0d1f33a82ba9ba858a960e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9516c29f1261dd985685a0d1e68ec85c531795e6aed6d7da72604a9a978e9b9;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.3.0-279.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a41284d464c02eff25a5f4599cbf9b0b393ea6270d9e055e94a8a47d10875`  
		Last Modified: Thu, 18 Jan 2024 19:22:53 GMT  
		Size: 131.8 MB (131828680 bytes)  
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
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
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
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
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
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
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
$ docker pull dart@sha256:ff5c0b014b3e2f79ace8e2737c50181a6e5c24f15ee280b3fa5520d6a2f770ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:679ea0237c8458da340338baca9e61daa56f1619c6ada09c79e0bf387bc73616
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308538696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23d415b0e58dd75023a1a6c1f792617b38c9474f2142626b0bc832fd0481f12`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:28:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:28:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 05:28:12 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 05:28:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:28:12 GMT
WORKDIR /root
# Thu, 18 Jan 2024 18:55:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc143d38f00257638c6f6afde350c5dd5e5c82b5f7f1dd755ff76ef726f94c3e`  
		Last Modified: Thu, 11 Jan 2024 05:29:10 GMT  
		Size: 54.7 MB (54650943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffd9b595c430cc5ffcfec691b3fccdaedd13ec56f1222af7d606a3892410d10`  
		Last Modified: Thu, 11 Jan 2024 05:29:06 GMT  
		Size: 1.8 MB (1800649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049e845f2fe2461e2db5b811a878f0ceb7e2bfe5b1931e2a495ab0ea47973725`  
		Last Modified: Thu, 18 Jan 2024 18:56:59 GMT  
		Size: 223.0 MB (222961183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:5d76b5c6cef2ef7cb269242b7503024dbaa154c2015b90a6b80998851ac2e500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.4 MB (203427569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8a9c2a1670bcc8985572759c011985aa3b762ec39bcefd86a68277ae39a1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 19:50:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 19:50:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 11 Jan 2024 19:50:35 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 11 Jan 2024 19:50:35 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 19:50:35 GMT
WORKDIR /root
# Thu, 18 Jan 2024 19:21:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=e35e66f6cb5f511eb909fc27f9cebe81712925b6abd4494310003cdf26410ab1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=9b08a544e8e6438c136fcef04348e0b796ee4125eab291b2657b56b3df60e8dc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=aa840a615e90fc26ca0ca348be8359b254a144cff6a0e2c3f7eb361ed9aef393;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.2.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98606fa9f3adbeb573a3b9cd538f16226ba753a62994751b3f9308ee7a3c3985`  
		Last Modified: Thu, 11 Jan 2024 19:51:49 GMT  
		Size: 49.1 MB (49133316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0775197d864e5d5a2f4f33d2f5b8604f3399d6443fe0413d94896ed6b081ec`  
		Last Modified: Thu, 11 Jan 2024 19:51:38 GMT  
		Size: 1.2 MB (1227213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e408d4210b1f588ce92265e00eb2c8914f5a9a99fa0717385bf7d2fae4f77d71`  
		Last Modified: Thu, 18 Jan 2024 19:22:06 GMT  
		Size: 128.3 MB (128348914 bytes)  
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
