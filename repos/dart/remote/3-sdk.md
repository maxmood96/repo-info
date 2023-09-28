## `dart:3-sdk`

```console
$ docker pull dart@sha256:97cc20588eb7171f611606fff26bc04fb2aec5e68f7341060252a409bf7a86ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a09f09d34450002704091c7597b910c5f137526a2ad2dc309cae3a2dc1d6ac13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296112825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9b4ca91244734c598699fde8d5db901f1d5ecaeecb513a4f7703ff39f74946`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:40 GMT
ADD file:a1398394375faab8dd9e1e8d584eea96c750fb57ae4ffd2b14624f1cf263561b in / 
# Wed, 20 Sep 2023 04:55:41 GMT
CMD ["bash"]
# Thu, 28 Sep 2023 19:19:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 28 Sep 2023 19:19:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 28 Sep 2023 19:19:49 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 28 Sep 2023 19:19:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 19:19:49 GMT
WORKDIR /root
# Thu, 28 Sep 2023 19:20:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a803e7c4b030119420574a882a52b6431e160fceb7620f61b525d49bc2d58886`  
		Last Modified: Wed, 20 Sep 2023 05:00:22 GMT  
		Size: 29.1 MB (29124705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bc70eea9dee799f144b691177500016dc7f1bf559fe45d2eea099badcc9d49`  
		Last Modified: Thu, 28 Sep 2023 19:23:07 GMT  
		Size: 54.6 MB (54628213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac94b701271ce1587bc6bdf682a125139e51c5f51984984e2c1565e0a9a007ce`  
		Last Modified: Thu, 28 Sep 2023 19:23:05 GMT  
		Size: 1.8 MB (1800836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4af29d586010103c89286b0490fe3abeb765aa1d0befde60399b218453e98bb`  
		Last Modified: Thu, 28 Sep 2023 19:23:43 GMT  
		Size: 210.6 MB (210559071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6ef615d8986474437da0c048aa66cc11070752944b06c63d4dec6ce74d9d3926
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187135121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a60e03d026efaa77a7d3d50bd633c54e02d1b00f83fa83543a7ccc17dfa1d4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:17 GMT
ADD file:56b69c762bd03a9b00a1677740f7209aac08bac69a9e73563e326b9b0efbbfcc in / 
# Wed, 20 Sep 2023 04:57:17 GMT
CMD ["bash"]
# Thu, 28 Sep 2023 19:57:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 28 Sep 2023 19:57:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 28 Sep 2023 19:57:32 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 28 Sep 2023 19:57:32 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 19:57:33 GMT
WORKDIR /root
# Thu, 28 Sep 2023 19:57:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e0b5206657a67707f4c57136f811162ce89a951fec109a406df7508d59e644cb`  
		Last Modified: Wed, 20 Sep 2023 05:01:16 GMT  
		Size: 24.8 MB (24805628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df81c27c2f08cf9663bc331c61cc3989d98c47df34e6cf8cfb4d142bb33bc69`  
		Last Modified: Thu, 28 Sep 2023 20:00:10 GMT  
		Size: 49.2 MB (49175111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e87eca693679fb3824fb270e27fc240f4eaa77e848b2520ff44cf2cd11aa7e`  
		Last Modified: Thu, 28 Sep 2023 19:59:49 GMT  
		Size: 1.2 MB (1227514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa4714771f12d8c37da4deb5f36cb8b22215d8c051ef4624601769ef1d25440`  
		Last Modified: Thu, 28 Sep 2023 20:00:17 GMT  
		Size: 111.9 MB (111926868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6449f0231e2683787bdd35de0355f03e88273dfdfafb867f6fcabad05dc3067c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197989816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8ddc7edd0c4939dc05f3c1e378c67967b3ba0307bb57e7cd6bdfe7e00b31b7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:13 GMT
ADD file:ec1a6e0aedd76c8fdc8544775f8b553f58950e9435f5cfe919f39374e222cfbb in / 
# Wed, 20 Sep 2023 02:44:14 GMT
CMD ["bash"]
# Thu, 28 Sep 2023 19:39:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 28 Sep 2023 19:39:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 28 Sep 2023 19:39:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 28 Sep 2023 19:39:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 19:39:38 GMT
WORKDIR /root
# Thu, 28 Sep 2023 19:39:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:e886f0f47ef56fcadb6ecaf2116056bbdb273e0afe07ed034498b198d386c04e`  
		Last Modified: Wed, 20 Sep 2023 02:47:36 GMT  
		Size: 29.2 MB (29157221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2537385569e5e48f9f6f3bd4a3974bd39853a1b3f750237ebf646c83dd546b`  
		Last Modified: Thu, 28 Sep 2023 19:41:33 GMT  
		Size: 54.3 MB (54290946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b19c9300ae59e9cb15533b23627fcb5e0bf306d08657eedd25cbccf607ee3d`  
		Last Modified: Thu, 28 Sep 2023 19:41:37 GMT  
		Size: 1.5 MB (1494135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8b93d302fa45056cbe56027d7d43a25d42033495a0deb9ff0e2091643472f0`  
		Last Modified: Thu, 28 Sep 2023 19:42:25 GMT  
		Size: 113.0 MB (113047514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
