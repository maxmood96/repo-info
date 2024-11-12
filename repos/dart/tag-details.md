<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.5`](#dart35)
-	[`dart:3.5-sdk`](#dart35-sdk)
-	[`dart:3.5.4`](#dart354)
-	[`dart:3.5.4-sdk`](#dart354-sdk)
-	[`dart:3.6.0-334.3.beta`](#dart360-3343beta)
-	[`dart:3.6.0-334.3.beta-sdk`](#dart360-3343beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3-sdk`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5-sdk`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.4`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.4` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5.4` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5.4` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.4` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.4-sdk`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.4-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5.4-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.4-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.6.0-334.3.beta`

```console
$ docker pull dart@sha256:fdad7b8eed0ad11731a6554c2e1b799a2957c2c63554aa934214fea0f8bfa413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.6.0-334.3.beta` - linux; amd64

```console
$ docker pull dart@sha256:f3dea11af7197fde7a5ebd3c819f5c925a3a5322cc030222ab836c68b94021ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313017973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dea51a24fbaaae1e0f3e3992f5ea9e0a02717d950cc8b2819f7db1b56a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a12dff24c7c1e153368b11ae120799d6e42e9829416389f52e18a0cd6a98b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 54.9 MB (54905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba69c9a2872567a537db226c706878b04571e5f4be750b3a819ab47ff64a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d231c89557df1bfa479abe883fd21f055dd7ed06f85d42bd062212aaae9f991`  
		Last Modified: Tue, 12 Nov 2024 02:39:14 GMT  
		Size: 227.2 MB (227187287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-334.3.beta` - unknown; unknown

```console
$ docker pull dart@sha256:ad2825732d0564cd2f68bee6364c5e22924e7292b382917f0539927e9ba3725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f02612f6357876164d4af0ce78cfff9959f68c2728a8becad2dcd77fe8e7d4a`

```dockerfile
```

-	Layers:
	-	`sha256:55230a211b499ca64e3b03449d2900f9b32952714f5cdf67565aff7a53cb20c7`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0-334.3.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:b55fefa913eac6d194049358fba28c944305b858feeed22c63238a2e4de95a7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211200930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4fe5b34decb961d1e70e5b061869de5474ce2dbd685a33576889076ffb3935`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:00:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1223942ee36dfb20dc976411e55e67738caf86a1addb1222efd951799472679`  
		Last Modified: Fri, 18 Oct 2024 19:01:27 GMT  
		Size: 135.7 MB (135691506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-334.3.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bf0f6a693a1261e6a6d6c6299df10308bdd887f7122c15760a1c1a3ca842e60d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311667566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0921fbfc8d8f827249a25de4a83cdcb17f8254f00fc3986d8a29994d7b72fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:40:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcbe4f3f92cedede1c215853bc1faee5aa523f3bd6c8d092c891c9edc294bfb`  
		Last Modified: Fri, 18 Oct 2024 19:41:29 GMT  
		Size: 226.3 MB (226343074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.6.0-334.3.beta-sdk`

```console
$ docker pull dart@sha256:fdad7b8eed0ad11731a6554c2e1b799a2957c2c63554aa934214fea0f8bfa413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.6.0-334.3.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f3dea11af7197fde7a5ebd3c819f5c925a3a5322cc030222ab836c68b94021ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313017973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dea51a24fbaaae1e0f3e3992f5ea9e0a02717d950cc8b2819f7db1b56a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a12dff24c7c1e153368b11ae120799d6e42e9829416389f52e18a0cd6a98b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 54.9 MB (54905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba69c9a2872567a537db226c706878b04571e5f4be750b3a819ab47ff64a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d231c89557df1bfa479abe883fd21f055dd7ed06f85d42bd062212aaae9f991`  
		Last Modified: Tue, 12 Nov 2024 02:39:14 GMT  
		Size: 227.2 MB (227187287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-334.3.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ad2825732d0564cd2f68bee6364c5e22924e7292b382917f0539927e9ba3725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f02612f6357876164d4af0ce78cfff9959f68c2728a8becad2dcd77fe8e7d4a`

```dockerfile
```

-	Layers:
	-	`sha256:55230a211b499ca64e3b03449d2900f9b32952714f5cdf67565aff7a53cb20c7`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0-334.3.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:b55fefa913eac6d194049358fba28c944305b858feeed22c63238a2e4de95a7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211200930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4fe5b34decb961d1e70e5b061869de5474ce2dbd685a33576889076ffb3935`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:00:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1223942ee36dfb20dc976411e55e67738caf86a1addb1222efd951799472679`  
		Last Modified: Fri, 18 Oct 2024 19:01:27 GMT  
		Size: 135.7 MB (135691506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-334.3.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bf0f6a693a1261e6a6d6c6299df10308bdd887f7122c15760a1c1a3ca842e60d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311667566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0921fbfc8d8f827249a25de4a83cdcb17f8254f00fc3986d8a29994d7b72fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:40:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcbe4f3f92cedede1c215853bc1faee5aa523f3bd6c8d092c891c9edc294bfb`  
		Last Modified: Fri, 18 Oct 2024 19:41:29 GMT  
		Size: 226.3 MB (226343074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:fdad7b8eed0ad11731a6554c2e1b799a2957c2c63554aa934214fea0f8bfa413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:f3dea11af7197fde7a5ebd3c819f5c925a3a5322cc030222ab836c68b94021ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313017973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dea51a24fbaaae1e0f3e3992f5ea9e0a02717d950cc8b2819f7db1b56a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a12dff24c7c1e153368b11ae120799d6e42e9829416389f52e18a0cd6a98b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 54.9 MB (54905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba69c9a2872567a537db226c706878b04571e5f4be750b3a819ab47ff64a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d231c89557df1bfa479abe883fd21f055dd7ed06f85d42bd062212aaae9f991`  
		Last Modified: Tue, 12 Nov 2024 02:39:14 GMT  
		Size: 227.2 MB (227187287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:ad2825732d0564cd2f68bee6364c5e22924e7292b382917f0539927e9ba3725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f02612f6357876164d4af0ce78cfff9959f68c2728a8becad2dcd77fe8e7d4a`

```dockerfile
```

-	Layers:
	-	`sha256:55230a211b499ca64e3b03449d2900f9b32952714f5cdf67565aff7a53cb20c7`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:b55fefa913eac6d194049358fba28c944305b858feeed22c63238a2e4de95a7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211200930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4fe5b34decb961d1e70e5b061869de5474ce2dbd685a33576889076ffb3935`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:00:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1223942ee36dfb20dc976411e55e67738caf86a1addb1222efd951799472679`  
		Last Modified: Fri, 18 Oct 2024 19:01:27 GMT  
		Size: 135.7 MB (135691506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bf0f6a693a1261e6a6d6c6299df10308bdd887f7122c15760a1c1a3ca842e60d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311667566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0921fbfc8d8f827249a25de4a83cdcb17f8254f00fc3986d8a29994d7b72fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:40:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcbe4f3f92cedede1c215853bc1faee5aa523f3bd6c8d092c891c9edc294bfb`  
		Last Modified: Fri, 18 Oct 2024 19:41:29 GMT  
		Size: 226.3 MB (226343074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:fdad7b8eed0ad11731a6554c2e1b799a2957c2c63554aa934214fea0f8bfa413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f3dea11af7197fde7a5ebd3c819f5c925a3a5322cc030222ab836c68b94021ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313017973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dea51a24fbaaae1e0f3e3992f5ea9e0a02717d950cc8b2819f7db1b56a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a12dff24c7c1e153368b11ae120799d6e42e9829416389f52e18a0cd6a98b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 54.9 MB (54905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba69c9a2872567a537db226c706878b04571e5f4be750b3a819ab47ff64a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d231c89557df1bfa479abe883fd21f055dd7ed06f85d42bd062212aaae9f991`  
		Last Modified: Tue, 12 Nov 2024 02:39:14 GMT  
		Size: 227.2 MB (227187287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ad2825732d0564cd2f68bee6364c5e22924e7292b382917f0539927e9ba3725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f02612f6357876164d4af0ce78cfff9959f68c2728a8becad2dcd77fe8e7d4a`

```dockerfile
```

-	Layers:
	-	`sha256:55230a211b499ca64e3b03449d2900f9b32952714f5cdf67565aff7a53cb20c7`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:b55fefa913eac6d194049358fba28c944305b858feeed22c63238a2e4de95a7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211200930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4fe5b34decb961d1e70e5b061869de5474ce2dbd685a33576889076ffb3935`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:00:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1223942ee36dfb20dc976411e55e67738caf86a1addb1222efd951799472679`  
		Last Modified: Fri, 18 Oct 2024 19:01:27 GMT  
		Size: 135.7 MB (135691506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bf0f6a693a1261e6a6d6c6299df10308bdd887f7122c15760a1c1a3ca842e60d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311667566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0921fbfc8d8f827249a25de4a83cdcb17f8254f00fc3986d8a29994d7b72fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:40:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcbe4f3f92cedede1c215853bc1faee5aa523f3bd6c8d092c891c9edc294bfb`  
		Last Modified: Fri, 18 Oct 2024 19:41:29 GMT  
		Size: 226.3 MB (226343074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:a942a9c8757bd7d3dd6ae79938ed7098bcb4a47327f2148a6517b96d26080b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:44de2979a1e65b341036c4742d266df4d1a9b6071f56d7e616805fd6a3058e46
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203583042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270b0489b7c08302e57e162997fa2dfd5c9bad2599c5af2ade6f658630574834`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:41:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 03:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 03:41:29 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 03:41:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 03:41:29 GMT
WORKDIR /root
# Fri, 18 Oct 2024 18:59:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9156a98a1506cc5eaa39325cb70fda804b66d3d8e8dc84710c43864dfed9cf73`  
		Last Modified: Thu, 17 Oct 2024 03:42:30 GMT  
		Size: 49.6 MB (49563698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c941e93242ff85dba1bae0cfe71f142b2855aa56fed6eca21f1f0f80dc5b7a`  
		Last Modified: Thu, 17 Oct 2024 03:42:21 GMT  
		Size: 1.2 MB (1227529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880038dee00a0b4628b806d88a79ba4e5ceb84dd084dd28a5269764f436fbda3`  
		Last Modified: Fri, 18 Oct 2024 19:00:45 GMT  
		Size: 128.1 MB (128073618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b58becb6946054ca74aa8b8e4aa62ba2d054527d13fee5f670882da6d1641947
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301842080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f9f1c3d5c99ca03c7e1930c04f695d0de4973aa062517f70d0d4b3e8ecc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:39:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:39:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 04:39:50 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 04:39:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:51 GMT
WORKDIR /root
# Fri, 18 Oct 2024 19:39:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c019dfb35fa07757a4e3ab43e13177efae8aebab795daf20d67bd5b51f8201c6`  
		Last Modified: Thu, 17 Oct 2024 04:40:45 GMT  
		Size: 54.7 MB (54674274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319b297f0abf2689e4def2b1aa58f8d73b4cc12098835f6f9a1b88e86637aece`  
		Last Modified: Thu, 17 Oct 2024 04:40:40 GMT  
		Size: 1.5 MB (1493877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4b65e7af5a4e729381227db1025100116c4e681afd5ce342b067359ddaaf4b`  
		Last Modified: Fri, 18 Oct 2024 19:40:45 GMT  
		Size: 216.5 MB (216517588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
