<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.1`](#dart31)
-	[`dart:3.1-sdk`](#dart31-sdk)
-	[`dart:3.1.5`](#dart315)
-	[`dart:3.1.5-sdk`](#dart315-sdk)
-	[`dart:3.2.0-210.4.beta`](#dart320-2104beta)
-	[`dart:3.2.0-210.4.beta-sdk`](#dart320-2104beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3-sdk`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.1`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.1-sdk`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.1.5`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1.5` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.5` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.5` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.1.5-sdk`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1.5-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.5-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.5-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.2.0-210.4.beta`

```console
$ docker pull dart@sha256:88ced76ff4a63e565872df26fe2442f060e3ecf828a272090ad10c79e9d044af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2.0-210.4.beta` - linux; amd64

```console
$ docker pull dart@sha256:608b36471e0e3d54df75269cb4032b7d96eb25bff6f58bdf27b80095d8a30ed5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70722bcd1d8fd247e946b658e4d832fb3008b3e9ddee6e50564779c8bf3f78e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:02:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eeba4fd84a02b713056ed88331e747d8cca0740eddb942a1b21f22a97fa1e0`  
		Last Modified: Thu, 02 Nov 2023 00:02:53 GMT  
		Size: 223.0 MB (222975978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.4.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:d16230978bdb16891e814fb5dd078d3ff1d9add142515c2a6c91fc095d9156d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203523800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3a9564203fc3dba630f2aed86b09987daa6206a4f4c391772308ab265f52dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:14:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa56b684c2e6e61ddc9c09b7348f03d6c56c8eb1319dd25ce98764245871782`  
		Last Modified: Thu, 02 Nov 2023 00:14:53 GMT  
		Size: 128.4 MB (128350762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.4.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cd50157262b5ddc58ade39e30cb71af75839bbdaa97f49c1290c9638e89b2c1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307149309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73a800bf45ac8a8389f9475eec9a2cfe0bfac3d7e4ec6b89567484a3b301c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:28:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8995e171951212f5b8fb5c52697a82c57269a5dd6fedc6af35e6e7e40cbdf5e`  
		Last Modified: Thu, 02 Nov 2023 00:29:01 GMT  
		Size: 222.2 MB (222159647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.2.0-210.4.beta-sdk`

```console
$ docker pull dart@sha256:88ced76ff4a63e565872df26fe2442f060e3ecf828a272090ad10c79e9d044af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2.0-210.4.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:608b36471e0e3d54df75269cb4032b7d96eb25bff6f58bdf27b80095d8a30ed5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70722bcd1d8fd247e946b658e4d832fb3008b3e9ddee6e50564779c8bf3f78e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:02:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eeba4fd84a02b713056ed88331e747d8cca0740eddb942a1b21f22a97fa1e0`  
		Last Modified: Thu, 02 Nov 2023 00:02:53 GMT  
		Size: 223.0 MB (222975978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.4.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d16230978bdb16891e814fb5dd078d3ff1d9add142515c2a6c91fc095d9156d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203523800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3a9564203fc3dba630f2aed86b09987daa6206a4f4c391772308ab265f52dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:14:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa56b684c2e6e61ddc9c09b7348f03d6c56c8eb1319dd25ce98764245871782`  
		Last Modified: Thu, 02 Nov 2023 00:14:53 GMT  
		Size: 128.4 MB (128350762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.4.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cd50157262b5ddc58ade39e30cb71af75839bbdaa97f49c1290c9638e89b2c1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307149309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73a800bf45ac8a8389f9475eec9a2cfe0bfac3d7e4ec6b89567484a3b301c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:28:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8995e171951212f5b8fb5c52697a82c57269a5dd6fedc6af35e6e7e40cbdf5e`  
		Last Modified: Thu, 02 Nov 2023 00:29:01 GMT  
		Size: 222.2 MB (222159647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:88ced76ff4a63e565872df26fe2442f060e3ecf828a272090ad10c79e9d044af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:608b36471e0e3d54df75269cb4032b7d96eb25bff6f58bdf27b80095d8a30ed5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70722bcd1d8fd247e946b658e4d832fb3008b3e9ddee6e50564779c8bf3f78e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:02:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eeba4fd84a02b713056ed88331e747d8cca0740eddb942a1b21f22a97fa1e0`  
		Last Modified: Thu, 02 Nov 2023 00:02:53 GMT  
		Size: 223.0 MB (222975978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:d16230978bdb16891e814fb5dd078d3ff1d9add142515c2a6c91fc095d9156d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203523800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3a9564203fc3dba630f2aed86b09987daa6206a4f4c391772308ab265f52dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:14:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa56b684c2e6e61ddc9c09b7348f03d6c56c8eb1319dd25ce98764245871782`  
		Last Modified: Thu, 02 Nov 2023 00:14:53 GMT  
		Size: 128.4 MB (128350762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cd50157262b5ddc58ade39e30cb71af75839bbdaa97f49c1290c9638e89b2c1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307149309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73a800bf45ac8a8389f9475eec9a2cfe0bfac3d7e4ec6b89567484a3b301c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:28:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8995e171951212f5b8fb5c52697a82c57269a5dd6fedc6af35e6e7e40cbdf5e`  
		Last Modified: Thu, 02 Nov 2023 00:29:01 GMT  
		Size: 222.2 MB (222159647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:88ced76ff4a63e565872df26fe2442f060e3ecf828a272090ad10c79e9d044af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:608b36471e0e3d54df75269cb4032b7d96eb25bff6f58bdf27b80095d8a30ed5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308566231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70722bcd1d8fd247e946b658e4d832fb3008b3e9ddee6e50564779c8bf3f78e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:02:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eeba4fd84a02b713056ed88331e747d8cca0740eddb942a1b21f22a97fa1e0`  
		Last Modified: Thu, 02 Nov 2023 00:02:53 GMT  
		Size: 223.0 MB (222975978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d16230978bdb16891e814fb5dd078d3ff1d9add142515c2a6c91fc095d9156d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203523800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3a9564203fc3dba630f2aed86b09987daa6206a4f4c391772308ab265f52dc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:14:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa56b684c2e6e61ddc9c09b7348f03d6c56c8eb1319dd25ce98764245871782`  
		Last Modified: Thu, 02 Nov 2023 00:14:53 GMT  
		Size: 128.4 MB (128350762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cd50157262b5ddc58ade39e30cb71af75839bbdaa97f49c1290c9638e89b2c1a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307149309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee73a800bf45ac8a8389f9475eec9a2cfe0bfac3d7e4ec6b89567484a3b301c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Thu, 02 Nov 2023 00:28:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=345fc18e2c2ab39db94fa9da34afb7d2f6bc7dff35cba66fc30429a68b4b52c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b563fa1e44f847b552417c5a651ded4a508fc3379916e1ca2417bd0cdc5b61e8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f2592ee85cab72c74b20e0f138f3acc023e9dc0e04e6aede25dd97ed78311873;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.4.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8995e171951212f5b8fb5c52697a82c57269a5dd6fedc6af35e6e7e40cbdf5e`  
		Last Modified: Thu, 02 Nov 2023 00:29:01 GMT  
		Size: 222.2 MB (222159647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:2432c3e2162542ee9d701b9d8524a3220f0182d37407382efa8fd782d1273e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b4182019ffa05ae868d140333e864f470b1613912a9afc3b903665e1b560bc16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296144873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25befd0141f69e6d4f28f11302d4f76e7de328e7bde39d70f353c88f91d15bfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:40:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:40:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:40:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:40:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:40:55 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:41:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443e1238ad5605aa2993fca352f33ae02c9200eab79655b252839c43fe789acd`  
		Last Modified: Wed, 01 Nov 2023 02:41:56 GMT  
		Size: 54.6 MB (54639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd56d85c13e7d3e2dd85b2c440c609473fb411d99ab1979010a0729b628fd64`  
		Last Modified: Wed, 01 Nov 2023 02:41:49 GMT  
		Size: 1.8 MB (1800640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2facbcebf557d97b6383fcdee4cc12245f77c91d0565e6cfca8049374f7907f5`  
		Last Modified: Wed, 01 Nov 2023 02:42:15 GMT  
		Size: 210.6 MB (210554620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:62a6240a9f49f3f08d906d00de125ca7f0a7ea78eef6d11c88ca489beb778df5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff741b944a76e418abcc40545a8e35e2cb3f216e2052889df239bee930ef6bc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:57:53 GMT
ADD file:fbe34fcf46c7cb91e83b67f7381d8971c97842aadd3e081994eaee4c08043106 in / 
# Wed, 01 Nov 2023 00:57:53 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:23:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:23:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 01:23:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 01:23:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:23:38 GMT
WORKDIR /root
# Wed, 01 Nov 2023 01:23:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:0a684901cedc28e6abb4cde4579d23d26345d871acd708a5bf266c562fe15b4d`  
		Last Modified: Wed, 01 Nov 2023 01:02:13 GMT  
		Size: 24.7 MB (24748900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980e17089e9c2528fd7907032247f990aadbd6d926d8b31b18828324b670bc8`  
		Last Modified: Wed, 01 Nov 2023 01:24:39 GMT  
		Size: 49.2 MB (49196919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e0afdcc924dc50a02f4ebad19ef1b19c57a1a9fd0852ea6146359d21a75cef`  
		Last Modified: Wed, 01 Nov 2023 01:24:30 GMT  
		Size: 1.2 MB (1227219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2662a770b8d54b50c52ab80d9dde1247a2a6eb1c59c9a110f0d52486c1d87ae9`  
		Last Modified: Wed, 01 Nov 2023 01:24:52 GMT  
		Size: 111.9 MB (111927111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ed6f8ac7dc0834ee58243e25d8bd4b4f0cfa13111c694ee3de088290be51d756
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1bedf9a9b53f9c86225159442d9f856b62d5b12453308f2296b042fc0dc4c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:41 GMT
ADD file:c58f86cd28b3a97f884e2a46f8fe60a2c5c1f443e198bd10e3277b4f3653736a in / 
# Wed, 01 Nov 2023 00:39:41 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:56:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:56:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 01 Nov 2023 02:56:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 01 Nov 2023 02:56:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 02:56:28 GMT
WORKDIR /root
# Wed, 01 Nov 2023 02:56:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=4342ba274a4e9f8057079cf9de43b1c7bdb002016ad538313e8ebe942b61bba8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b4f326bd045aae1d4b00a6a74b11d70937fc41291a9d8d62a123dab8bc3ac7d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f0e19c276c99fa3efd6428ea4bef1502f742f2a1f9772959637eec775c10ba0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.5/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:31ce7ceb6d443e2ab4ae91695fea10e1443417fd94c40a46994d5a96940ea1ca`  
		Last Modified: Wed, 01 Nov 2023 00:43:07 GMT  
		Size: 29.2 MB (29179119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5551d2ab4bed7b04d3e7e9a3d7c2465c554002d3607e6f27cf388d0954556c`  
		Last Modified: Wed, 01 Nov 2023 02:57:31 GMT  
		Size: 54.3 MB (54316968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaac47fb8ef03efc0ead0893fdd0607531115deca4329de0512c8a0fdc1cc30e`  
		Last Modified: Wed, 01 Nov 2023 02:57:25 GMT  
		Size: 1.5 MB (1493575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b841f603ae44ee2472c360559adcb93dcdea959c5ef8661bfa976f0920ee199c`  
		Last Modified: Wed, 01 Nov 2023 02:57:47 GMT  
		Size: 209.7 MB (209677848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
