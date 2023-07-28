## `dart:stable`

```console
$ docker pull dart@sha256:faf300f790cadb2e34182dd75c5f14642e21c625396055a16aa967170dfb71d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:d04faa9da103974a42a73915ba28f443aa3430b39656469bf95caa15f4506db5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296613757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e7e005e696996ffd7f611ec502bf9f115806d620c0f1fc0f088dd994b10cbf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:57:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:57:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 28 Jul 2023 00:57:24 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 28 Jul 2023 00:57:25 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 00:57:25 GMT
WORKDIR /root
# Fri, 28 Jul 2023 00:57:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cccd5300faa5a9abce12a5f77586e26350028cea82bb4ff8eeb55641b58a2e1d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a15d42cb1677ac5e50a23045cafe3bf5db2855a5287a3e9019b849fe8477897;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2c8eeaf0d3da60c4e14beec45ce3b39aca754f71b9fa3fb0c635ee28d6f44708;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f327e85d0d085fa1b66e19f223e26d295b0112f5b3118b186eedd566e3cbe4a`  
		Last Modified: Fri, 28 Jul 2023 00:58:22 GMT  
		Size: 45.1 MB (45101672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da22ff9cae25bc9894d49f8004c09cacc8c88a7125b197633206cbdfaaee088`  
		Last Modified: Fri, 28 Jul 2023 00:58:16 GMT  
		Size: 2.2 MB (2160697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905f02fff62812e055e6557c81eb1ca0d0726af9da10708d7d23671e2c0dd4c6`  
		Last Modified: Fri, 28 Jul 2023 00:58:43 GMT  
		Size: 217.9 MB (217933786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:6c532fcde08cd3645d8210f682d183a4ae4664c91eeae0a7076514780dc99d17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191284063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af009fac56f668ce82a2b90afbc0ad264c5069bfb9478135196d91a94204e8c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:58:18 GMT
ADD file:480cada6975fa477736805a1834cca05d1e18de255c6cc0cca13df01fdb44253 in / 
# Thu, 27 Jul 2023 23:58:18 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:55:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:55:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 28 Jul 2023 01:55:27 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 28 Jul 2023 01:55:27 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 01:55:27 GMT
WORKDIR /root
# Fri, 28 Jul 2023 01:55:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cccd5300faa5a9abce12a5f77586e26350028cea82bb4ff8eeb55641b58a2e1d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a15d42cb1677ac5e50a23045cafe3bf5db2855a5287a3e9019b849fe8477897;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2c8eeaf0d3da60c4e14beec45ce3b39aca754f71b9fa3fb0c635ee28d6f44708;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1236490553984befd7be19a151a0489729a35a66c4aaf5d799cd87d2c738371a`  
		Last Modified: Fri, 28 Jul 2023 00:03:56 GMT  
		Size: 26.6 MB (26578603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7323e5a974514854e652831281e0fd7bd1d80513b94656cb181796634cc819f4`  
		Last Modified: Fri, 28 Jul 2023 01:56:17 GMT  
		Size: 41.0 MB (40988395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183ec55d0b3582530c58a4c9ca20596e636b9679a53bcc4a10af114cdb53f25b`  
		Last Modified: Fri, 28 Jul 2023 01:56:11 GMT  
		Size: 1.3 MB (1287725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e92c96224b5c4c0d1752d9c4586fd46b04c1894af6dac7b40937da7fcd5201`  
		Last Modified: Fri, 28 Jul 2023 01:56:29 GMT  
		Size: 122.4 MB (122429340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:69ebebe7f9b145aa49a9e1f3a873a58960f84af74f4991c38282f81af5d53ad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200470199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92246d2c5512c4b72ca39cecb925e7819cadfda3962eb668a346f25f0c57f81`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:57:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:57:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 28 Jul 2023 01:57:21 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 28 Jul 2023 01:57:21 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 01:57:21 GMT
WORKDIR /root
# Fri, 28 Jul 2023 01:57:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cccd5300faa5a9abce12a5f77586e26350028cea82bb4ff8eeb55641b58a2e1d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a15d42cb1677ac5e50a23045cafe3bf5db2855a5287a3e9019b849fe8477897;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2c8eeaf0d3da60c4e14beec45ce3b39aca754f71b9fa3fb0c635ee28d6f44708;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.0.7/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e281d1226aaec284b99b66f0b9755f4c095b9838af34edef5767fceb41c974c3`  
		Last Modified: Fri, 28 Jul 2023 01:58:07 GMT  
		Size: 45.0 MB (45011814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15fe0151f7dbcdfc9a9b9dfab3428243f2e7f9eb30015a557f4f55057509cc9a`  
		Last Modified: Fri, 28 Jul 2023 01:58:03 GMT  
		Size: 1.6 MB (1560885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667b132ba042d61bb8ed29bf80ad2c2de81858044cf9a9fed204ce822a8398a4`  
		Last Modified: Fri, 28 Jul 2023 01:58:16 GMT  
		Size: 123.8 MB (123834669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
