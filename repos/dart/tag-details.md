<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.5`](#dart35)
-	[`dart:3.5-sdk`](#dart35-sdk)
-	[`dart:3.5.2`](#dart352)
-	[`dart:3.5.2-sdk`](#dart352-sdk)
-	[`dart:3.6.0-216.1.beta`](#dart360-2161beta)
-	[`dart:3.6.0-216.1.beta-sdk`](#dart360-2161beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3-sdk`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5-sdk`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.2`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.2` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.5.2-sdk`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.6.0-216.1.beta`

```console
$ docker pull dart@sha256:e5eaf03c6be13cbd1bc02e87de7c4ff3d4a5764a791f05ed12bb634fc9c8805e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.6.0-216.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:22503ed220c413433a8423b33748afb0c6c8f316af8517f872b66eb368797d5a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307807198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3ae5f21074c1b05b07f1434755ca8d8ae7dcd55215c6c126b4d7cf50072764`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777d772871c682f0836f381b897716852007fe31a8370b06e0005906fddeb118`  
		Last Modified: Fri, 27 Sep 2024 05:21:03 GMT  
		Size: 222.0 MB (221974636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-216.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:dbe0dfac5358af831b1f28cdf47720ce64337359cc6af52b6300dfcdbc75ee03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206408861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa11975b565294485ac90984c0f160b8b35df9ffc4ff28a96fe4c8a350b0bdd9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab8d5201bcd6477e74fd21579517dbb42d719f742cb05537891af27165f54e`  
		Last Modified: Fri, 27 Sep 2024 07:45:50 GMT  
		Size: 130.9 MB (130899388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-216.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ffb70ac7b55331c71c1f1a24a42867fa1de78b807f2ee29c315c558e95551770
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306528962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a8121e3e491911339d9f976105bef6ad654795e50ad9c0e69f0fcac7fb99c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fe3af9353c0f5d8438c5e038017df864189a36615a4e6948bce6c5883ff118`  
		Last Modified: Fri, 27 Sep 2024 05:30:51 GMT  
		Size: 221.2 MB (221204336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:3.6.0-216.1.beta-sdk`

```console
$ docker pull dart@sha256:e5eaf03c6be13cbd1bc02e87de7c4ff3d4a5764a791f05ed12bb634fc9c8805e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.6.0-216.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:22503ed220c413433a8423b33748afb0c6c8f316af8517f872b66eb368797d5a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307807198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3ae5f21074c1b05b07f1434755ca8d8ae7dcd55215c6c126b4d7cf50072764`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777d772871c682f0836f381b897716852007fe31a8370b06e0005906fddeb118`  
		Last Modified: Fri, 27 Sep 2024 05:21:03 GMT  
		Size: 222.0 MB (221974636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-216.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:dbe0dfac5358af831b1f28cdf47720ce64337359cc6af52b6300dfcdbc75ee03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206408861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa11975b565294485ac90984c0f160b8b35df9ffc4ff28a96fe4c8a350b0bdd9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab8d5201bcd6477e74fd21579517dbb42d719f742cb05537891af27165f54e`  
		Last Modified: Fri, 27 Sep 2024 07:45:50 GMT  
		Size: 130.9 MB (130899388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-216.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ffb70ac7b55331c71c1f1a24a42867fa1de78b807f2ee29c315c558e95551770
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306528962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a8121e3e491911339d9f976105bef6ad654795e50ad9c0e69f0fcac7fb99c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fe3af9353c0f5d8438c5e038017df864189a36615a4e6948bce6c5883ff118`  
		Last Modified: Fri, 27 Sep 2024 05:30:51 GMT  
		Size: 221.2 MB (221204336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta`

```console
$ docker pull dart@sha256:e5eaf03c6be13cbd1bc02e87de7c4ff3d4a5764a791f05ed12bb634fc9c8805e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:22503ed220c413433a8423b33748afb0c6c8f316af8517f872b66eb368797d5a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307807198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3ae5f21074c1b05b07f1434755ca8d8ae7dcd55215c6c126b4d7cf50072764`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777d772871c682f0836f381b897716852007fe31a8370b06e0005906fddeb118`  
		Last Modified: Fri, 27 Sep 2024 05:21:03 GMT  
		Size: 222.0 MB (221974636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:dbe0dfac5358af831b1f28cdf47720ce64337359cc6af52b6300dfcdbc75ee03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206408861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa11975b565294485ac90984c0f160b8b35df9ffc4ff28a96fe4c8a350b0bdd9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab8d5201bcd6477e74fd21579517dbb42d719f742cb05537891af27165f54e`  
		Last Modified: Fri, 27 Sep 2024 07:45:50 GMT  
		Size: 130.9 MB (130899388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ffb70ac7b55331c71c1f1a24a42867fa1de78b807f2ee29c315c558e95551770
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306528962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a8121e3e491911339d9f976105bef6ad654795e50ad9c0e69f0fcac7fb99c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fe3af9353c0f5d8438c5e038017df864189a36615a4e6948bce6c5883ff118`  
		Last Modified: Fri, 27 Sep 2024 05:30:51 GMT  
		Size: 221.2 MB (221204336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:e5eaf03c6be13cbd1bc02e87de7c4ff3d4a5764a791f05ed12bb634fc9c8805e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:22503ed220c413433a8423b33748afb0c6c8f316af8517f872b66eb368797d5a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307807198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3ae5f21074c1b05b07f1434755ca8d8ae7dcd55215c6c126b4d7cf50072764`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777d772871c682f0836f381b897716852007fe31a8370b06e0005906fddeb118`  
		Last Modified: Fri, 27 Sep 2024 05:21:03 GMT  
		Size: 222.0 MB (221974636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:dbe0dfac5358af831b1f28cdf47720ce64337359cc6af52b6300dfcdbc75ee03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206408861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa11975b565294485ac90984c0f160b8b35df9ffc4ff28a96fe4c8a350b0bdd9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab8d5201bcd6477e74fd21579517dbb42d719f742cb05537891af27165f54e`  
		Last Modified: Fri, 27 Sep 2024 07:45:50 GMT  
		Size: 130.9 MB (130899388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ffb70ac7b55331c71c1f1a24a42867fa1de78b807f2ee29c315c558e95551770
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306528962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a8121e3e491911339d9f976105bef6ad654795e50ad9c0e69f0fcac7fb99c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fe3af9353c0f5d8438c5e038017df864189a36615a4e6948bce6c5883ff118`  
		Last Modified: Fri, 27 Sep 2024 05:30:51 GMT  
		Size: 221.2 MB (221204336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:latest`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:sdk`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:93ce3d39d7ec4914f9035e853ebb6c09eb7c5ea20d06a62f28abb807d3513391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:b10b8f779d94cabaa50cc1e8f3a9e20410ef21be6ce022aa6b3a9f45a352725c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e9cc58c524b5ea983ba484455d7b7b747139c6192b305d3833c635f137f45`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:18:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:18:50 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:18:50 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:18:50 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:19:03 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc3e11bf2773260f8b61c545f8d8c7e3e23acae593418e59b3bd2cb80b5a0f`  
		Last Modified: Fri, 27 Sep 2024 05:19:51 GMT  
		Size: 54.9 MB (54905369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4178dd10d5867511d413354ebdf00a40f32ab39bdbe9df6ac2a25e2ab3fc811b`  
		Last Modified: Fri, 27 Sep 2024 05:19:44 GMT  
		Size: 1.8 MB (1800917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b138ee684ccf3e44427551135578db5090a205de6d7e2786fef03aff10ff3d54`  
		Last Modified: Fri, 27 Sep 2024 05:20:15 GMT  
		Size: 217.4 MB (217357416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:8bce93a751c66e0e33dd327ece958f306a4f70948c2d9dde693106fd01931058
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1e89d11ba56548c09950a9afcadeea9d13de5f13881832d4abee4a33d3204f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:46 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Fri, 27 Sep 2024 05:13:46 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:43:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:43:48 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 07:43:49 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 07:43:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 07:43:49 GMT
WORKDIR /root
# Fri, 27 Sep 2024 07:44:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321b8c842057e0577b08f45bcff78c340340f797bfc2b390158f4b10b5e9a58b`  
		Last Modified: Fri, 27 Sep 2024 07:44:56 GMT  
		Size: 49.6 MB (49563797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a990cbbf1b1878f43011d53321ce977e3ebfe19a81c00eb9d8efea4fc1f592`  
		Last Modified: Fri, 27 Sep 2024 07:44:49 GMT  
		Size: 1.2 MB (1227531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c99d4528046710aaf579fb545cffce079c55c306c1bc95867d94cff90ab8859`  
		Last Modified: Fri, 27 Sep 2024 07:45:08 GMT  
		Size: 128.1 MB (128073504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:1dc071a167995809e2e62772d4b24f8d3d18e47341dad146187ceca698725086
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301841631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7116a00e590177dc08e27fab9bb9707d159046dcfba0231d495ba929f98c3699`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:28:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:28:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Fri, 27 Sep 2024 05:28:51 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 27 Sep 2024 05:28:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:28:51 GMT
WORKDIR /root
# Fri, 27 Sep 2024 05:29:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0f6698a98b6fd1fb9fc3230149c5a9ffcd19e26aed8a8dc258ae8bde65af`  
		Last Modified: Fri, 27 Sep 2024 05:29:51 GMT  
		Size: 54.7 MB (54674383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db99aa8d04a45b99135f32350dad29ddca681e99f32389febc30dbd9b10d1ecc`  
		Last Modified: Fri, 27 Sep 2024 05:29:46 GMT  
		Size: 1.5 MB (1493874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0f52fb99f07e8894b4b049abb39d01178975cccc98b72526b825e14e250ee`  
		Last Modified: Fri, 27 Sep 2024 05:30:08 GMT  
		Size: 216.5 MB (216517005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
