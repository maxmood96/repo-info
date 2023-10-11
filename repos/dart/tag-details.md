<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.1`](#dart31)
-	[`dart:3.1-sdk`](#dart31-sdk)
-	[`dart:3.1.3`](#dart313)
-	[`dart:3.1.3-sdk`](#dart313-sdk)
-	[`dart:3.2.0-210.2.beta`](#dart320-2102beta)
-	[`dart:3.2.0-210.2.beta-sdk`](#dart320-2102beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

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

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

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

## `dart:3-sdk`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
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
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
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

## `dart:3.1`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1` - linux; amd64

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

### `dart:3.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1` - linux; arm64 variant v8

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

## `dart:3.1-sdk`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1-sdk` - linux; amd64

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

### `dart:3.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1-sdk` - linux; arm64 variant v8

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

## `dart:3.1.3`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1.3` - linux; amd64

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

### `dart:3.1.3` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.3` - linux; arm64 variant v8

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

## `dart:3.1.3-sdk`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.1.3-sdk` - linux; amd64

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

### `dart:3.1.3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.1.3-sdk` - linux; arm64 variant v8

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

## `dart:3.2.0-210.2.beta`

```console
$ docker pull dart@sha256:7ce6034969b691cd4a0cde715420a61c9b2dab0b0c9d7a44389fb45f79f1753a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2.0-210.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:b4c1be73a7a406190e0acb5b72588ee33848a40756f377873ea9ce889109ccdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308530587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cf5181b6b6a85215a5570d3e9d8c0a02aef2112723f0e5c298fbd638c175bf`
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
# Wed, 11 Oct 2023 18:06:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:6e91fc38b4414125d1d6c862d5f1dccd178387c0db953689c5fc34bdc19bd207`  
		Last Modified: Wed, 11 Oct 2023 18:07:33 GMT  
		Size: 223.0 MB (222976833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ede85687279822075d16747f1222a81d80f931307ee6b160f98abfeac00fcba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203555939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f354b348ae2f142e7f4c47565c17fe5ac1982fb54ed45a68458742a6d55ad6`
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
# Wed, 11 Oct 2023 17:31:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:3d7e5bf42641d09d5266abb5afb8685db5aca09ea3acc6bff92ec8f99ca76b04`  
		Last Modified: Wed, 11 Oct 2023 17:32:01 GMT  
		Size: 128.3 MB (128347686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:06e5ef47321c93ccae86e5e9072e51394c009088302cc88e000d0652ace4b6e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213672417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b71e3a5f335b83d349ca1f9203527cd1676ae2fd9e2a3119770cc6aa35854c8`
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
# Wed, 11 Oct 2023 17:32:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:b205fa0520f71cb8f6e294b78c89589ce4467e52c0070bd0c40aaa44c46a5642`  
		Last Modified: Wed, 11 Oct 2023 17:33:02 GMT  
		Size: 128.7 MB (128730115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.2.0-210.2.beta-sdk`

```console
$ docker pull dart@sha256:4114c03ec9c203ec4c17bf81ad33c2b063dfd96861dda9ba794949d76cef9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.2.0-210.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b4c1be73a7a406190e0acb5b72588ee33848a40756f377873ea9ce889109ccdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308530587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cf5181b6b6a85215a5570d3e9d8c0a02aef2112723f0e5c298fbd638c175bf`
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
# Wed, 11 Oct 2023 18:06:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:6e91fc38b4414125d1d6c862d5f1dccd178387c0db953689c5fc34bdc19bd207`  
		Last Modified: Wed, 11 Oct 2023 18:07:33 GMT  
		Size: 223.0 MB (222976833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c6cffacd175ecb80015fedfdd7bf3bc6e1bea0c8ea49a186139a16614bf5f1b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203521137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0b1af82226a721b8c03657e35195dbf25ab7536b284eef034faad5a5c39e6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42aca3211574cba3a679289c44f735c5b1b4ba07df25dab2e4e8c4e34bee6ba9`  
		Last Modified: Wed, 11 Oct 2023 18:23:20 GMT  
		Size: 128.3 MB (128347623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.2.0-210.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:06e5ef47321c93ccae86e5e9072e51394c009088302cc88e000d0652ace4b6e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213672417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b71e3a5f335b83d349ca1f9203527cd1676ae2fd9e2a3119770cc6aa35854c8`
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
# Wed, 11 Oct 2023 17:32:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:b205fa0520f71cb8f6e294b78c89589ce4467e52c0070bd0c40aaa44c46a5642`  
		Last Modified: Wed, 11 Oct 2023 17:33:02 GMT  
		Size: 128.7 MB (128730115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:4114c03ec9c203ec4c17bf81ad33c2b063dfd96861dda9ba794949d76cef9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:b4c1be73a7a406190e0acb5b72588ee33848a40756f377873ea9ce889109ccdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308530587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cf5181b6b6a85215a5570d3e9d8c0a02aef2112723f0e5c298fbd638c175bf`
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
# Wed, 11 Oct 2023 18:06:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:6e91fc38b4414125d1d6c862d5f1dccd178387c0db953689c5fc34bdc19bd207`  
		Last Modified: Wed, 11 Oct 2023 18:07:33 GMT  
		Size: 223.0 MB (222976833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:c6cffacd175ecb80015fedfdd7bf3bc6e1bea0c8ea49a186139a16614bf5f1b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203521137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0b1af82226a721b8c03657e35195dbf25ab7536b284eef034faad5a5c39e6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42aca3211574cba3a679289c44f735c5b1b4ba07df25dab2e4e8c4e34bee6ba9`  
		Last Modified: Wed, 11 Oct 2023 18:23:20 GMT  
		Size: 128.3 MB (128347623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:06e5ef47321c93ccae86e5e9072e51394c009088302cc88e000d0652ace4b6e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213672417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b71e3a5f335b83d349ca1f9203527cd1676ae2fd9e2a3119770cc6aa35854c8`
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
# Wed, 11 Oct 2023 17:32:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:b205fa0520f71cb8f6e294b78c89589ce4467e52c0070bd0c40aaa44c46a5642`  
		Last Modified: Wed, 11 Oct 2023 17:33:02 GMT  
		Size: 128.7 MB (128730115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:4114c03ec9c203ec4c17bf81ad33c2b063dfd96861dda9ba794949d76cef9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b4c1be73a7a406190e0acb5b72588ee33848a40756f377873ea9ce889109ccdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.5 MB (308530587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cf5181b6b6a85215a5570d3e9d8c0a02aef2112723f0e5c298fbd638c175bf`
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
# Wed, 11 Oct 2023 18:06:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:6e91fc38b4414125d1d6c862d5f1dccd178387c0db953689c5fc34bdc19bd207`  
		Last Modified: Wed, 11 Oct 2023 18:07:33 GMT  
		Size: 223.0 MB (222976833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c6cffacd175ecb80015fedfdd7bf3bc6e1bea0c8ea49a186139a16614bf5f1b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203521137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0b1af82226a721b8c03657e35195dbf25ab7536b284eef034faad5a5c39e6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42aca3211574cba3a679289c44f735c5b1b4ba07df25dab2e4e8c4e34bee6ba9`  
		Last Modified: Wed, 11 Oct 2023 18:23:20 GMT  
		Size: 128.3 MB (128347623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:06e5ef47321c93ccae86e5e9072e51394c009088302cc88e000d0652ace4b6e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213672417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b71e3a5f335b83d349ca1f9203527cd1676ae2fd9e2a3119770cc6aa35854c8`
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
# Wed, 11 Oct 2023 17:32:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=d10d4aa2daf2afc43397ea4c4106a9965c2930bed022ee4d9e8f195cb856af41;             SDK_ARCH="x64";;         armhf)             DART_SHA256=070729edebd45adca5f7c023df7b887787452bdc4417682fbbf366712bd7d338;             SDK_ARCH="arm";;         arm64)             DART_SHA256=305ca5698e0399bc5cb96c394d158ceb83be59e9dc83b761c2b4dac2769e2af0;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.2.0-210.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:b205fa0520f71cb8f6e294b78c89589ce4467e52c0070bd0c40aaa44c46a5642`  
		Last Modified: Wed, 11 Oct 2023 17:33:02 GMT  
		Size: 128.7 MB (128730115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

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

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

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

## `dart:sdk`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

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

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

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

## `dart:stable`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

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

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

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

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:f5613d4ae97eb6ae324c3c3271b2bd5f8b8997cb74197064ea271a155c1fd867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

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

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2f7245226858ea86fffbdbb30de8333a45a3a14e26352eff89420b0c9de62385
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187100537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c112737de71b07ef8bd0713cba469929b87fba3e4b1c87f1b802f86c0c273d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:11 GMT
ADD file:da08fed31a161a2210fd920a1b5e43aa3f4199985cdeaa0d5d24c0a0f19044aa in / 
# Wed, 11 Oct 2023 17:42:11 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:21:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 11 Oct 2023 18:21:22 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Oct 2023 18:21:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:21:23 GMT
WORKDIR /root
# Wed, 11 Oct 2023 18:21:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0150dff731ac017646941ebfa46ca2a7bbe5c634be0928262d524420341fc739;             SDK_ARCH="x64";;         armhf)             DART_SHA256=0edf3fe2f5b8d212468de67b08fd1f27e5a775ef10e4e8bbef811a083cf15650;             SDK_ARCH="arm";;         arm64)             DART_SHA256=2b2830001cd8732d356c4beee7be25c947e6cb6e8ca7b8ea748da47f6cc9d222;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.1.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2f11c34abc7b59f09b58bb6e2cf54f260f4b4142ecf8023a114e281ea4b532d1`  
		Last Modified: Wed, 11 Oct 2023 17:46:22 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96df7c1334c06ce61f50070f4f0982f1670c0f9ce6d68f66c53d97df089773bd`  
		Last Modified: Wed, 11 Oct 2023 18:22:22 GMT  
		Size: 49.2 MB (49197359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43deeabde0db6379fcbf973ad8d851910371d49793774b9e405fb517bcb5efe0`  
		Last Modified: Wed, 11 Oct 2023 18:22:15 GMT  
		Size: 1.2 MB (1227230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb99db0b9128df9e023e75b3fa7d423af28f024665d023d1a422869d8b613407`  
		Last Modified: Wed, 11 Oct 2023 18:22:33 GMT  
		Size: 111.9 MB (111927023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

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
