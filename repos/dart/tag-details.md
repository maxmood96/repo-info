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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5-sdk` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.2` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.5.2-sdk` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.5.2-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
$ docker pull dart@sha256:e46822a14fbbf1583b2dff053689229e0a5053fb512067cc2484d2a79b8421bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.6.0-216.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:c51b472157e1e8c6c0d6fbc9e775a6fb7845ecfd36d1a8cfb0f656aca5865ff0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307806990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d4484820eaccbd263cb3432cb4981806ffc60d383684c13e528be07576ef61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092edec8ccf1c323bb4c0189865f58ebca4445030d9581b6ae81b75c584b7788`  
		Last Modified: Thu, 17 Oct 2024 01:16:28 GMT  
		Size: 222.0 MB (221974654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-216.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:93e922b2244821f4489228488086aa76b5980aeb211c7626514fcc00994e3bcf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206409027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63629c7984313c9fc3d8330a978bdcece687d0a4d489f46b36b9f21cc5d14390`
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
# Thu, 17 Oct 2024 03:42:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:d3652f6aff0f3baa032663b1c4f0277fb8492c76592676b6351759198210ffc6`  
		Last Modified: Thu, 17 Oct 2024 03:43:29 GMT  
		Size: 130.9 MB (130899603 bytes)  
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
$ docker pull dart@sha256:e46822a14fbbf1583b2dff053689229e0a5053fb512067cc2484d2a79b8421bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:3.6.0-216.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:c51b472157e1e8c6c0d6fbc9e775a6fb7845ecfd36d1a8cfb0f656aca5865ff0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307806990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d4484820eaccbd263cb3432cb4981806ffc60d383684c13e528be07576ef61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092edec8ccf1c323bb4c0189865f58ebca4445030d9581b6ae81b75c584b7788`  
		Last Modified: Thu, 17 Oct 2024 01:16:28 GMT  
		Size: 222.0 MB (221974654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:3.6.0-216.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:93e922b2244821f4489228488086aa76b5980aeb211c7626514fcc00994e3bcf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206409027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63629c7984313c9fc3d8330a978bdcece687d0a4d489f46b36b9f21cc5d14390`
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
# Thu, 17 Oct 2024 03:42:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:d3652f6aff0f3baa032663b1c4f0277fb8492c76592676b6351759198210ffc6`  
		Last Modified: Thu, 17 Oct 2024 03:43:29 GMT  
		Size: 130.9 MB (130899603 bytes)  
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
$ docker pull dart@sha256:e46822a14fbbf1583b2dff053689229e0a5053fb512067cc2484d2a79b8421bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:c51b472157e1e8c6c0d6fbc9e775a6fb7845ecfd36d1a8cfb0f656aca5865ff0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307806990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d4484820eaccbd263cb3432cb4981806ffc60d383684c13e528be07576ef61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092edec8ccf1c323bb4c0189865f58ebca4445030d9581b6ae81b75c584b7788`  
		Last Modified: Thu, 17 Oct 2024 01:16:28 GMT  
		Size: 222.0 MB (221974654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:93e922b2244821f4489228488086aa76b5980aeb211c7626514fcc00994e3bcf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206409027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63629c7984313c9fc3d8330a978bdcece687d0a4d489f46b36b9f21cc5d14390`
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
# Thu, 17 Oct 2024 03:42:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:d3652f6aff0f3baa032663b1c4f0277fb8492c76592676b6351759198210ffc6`  
		Last Modified: Thu, 17 Oct 2024 03:43:29 GMT  
		Size: 130.9 MB (130899603 bytes)  
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
$ docker pull dart@sha256:e46822a14fbbf1583b2dff053689229e0a5053fb512067cc2484d2a79b8421bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:c51b472157e1e8c6c0d6fbc9e775a6fb7845ecfd36d1a8cfb0f656aca5865ff0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307806990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d4484820eaccbd263cb3432cb4981806ffc60d383684c13e528be07576ef61`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092edec8ccf1c323bb4c0189865f58ebca4445030d9581b6ae81b75c584b7788`  
		Last Modified: Thu, 17 Oct 2024 01:16:28 GMT  
		Size: 222.0 MB (221974654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:93e922b2244821f4489228488086aa76b5980aeb211c7626514fcc00994e3bcf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206409027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63629c7984313c9fc3d8330a978bdcece687d0a4d489f46b36b9f21cc5d14390`
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
# Thu, 17 Oct 2024 03:42:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9cd1436875df2299df48e238b3353678f620ac066e706c35c805403099733b52;             SDK_ARCH="x64";;         armhf)             DART_SHA256=76931a9e6e354a63b3ec7243c1c99d0bd4c5425d71b48f3b2fdcf933d12ea8b1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a592f8b23d62b5ff902525bb0c47ab7f82aee0ce27588ea559717998b262cc57;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-216.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:d3652f6aff0f3baa032663b1c4f0277fb8492c76592676b6351759198210ffc6`  
		Last Modified: Thu, 17 Oct 2024 03:43:29 GMT  
		Size: 130.9 MB (130899603 bytes)  
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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
$ docker pull dart@sha256:9b7b8e5bc033862858cd0cae9bec360864517820dc4338c4dd537dd2e2f39f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:928ddd4eab9fffc49967086b1d705eb97f3ac63a53a6f0b5d28d19593f43de3a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303189867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6c90553ad636b5c60c788b672e36b878705e7fa92f9ba3d1b31775d2a7b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:14:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 01:14:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 17 Oct 2024 01:14:22 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 01:14:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 01:14:23 GMT
WORKDIR /root
# Thu, 17 Oct 2024 01:14:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d5be6e18ffd64548b00c5115fef591f54ba52496bcdbdaffdc7490d304c09`  
		Last Modified: Thu, 17 Oct 2024 01:15:19 GMT  
		Size: 54.9 MB (54905125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ad2a3cb28900d04f3adafc044bdbffafd503d01542f48a4e461f4839bbfcd4`  
		Last Modified: Thu, 17 Oct 2024 01:15:11 GMT  
		Size: 1.8 MB (1800922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b300af3d1e818609187e4607db97dfe11d459cdf20156b149d72ce99226ae5e`  
		Last Modified: Thu, 17 Oct 2024 01:15:39 GMT  
		Size: 217.4 MB (217357531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc157ea099b53126a167b8b0be9810851c6fbb342573028ee16d86aa1e392ed2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203582963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12f38ba3325383c3d8dfc3a7ab353afe376c2925e14d915ead785a0d18ed65`
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
# Thu, 17 Oct 2024 03:41:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0b50f0523eb1cdaa3c18bcb88f78b4dddfad9e3abced0aef05b0fd765b980d98;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6be11d8bf7e9f4b9a04ba3169be9af7f407f73c0eee60c0081c5f3871762489c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0a382412154fc12ce6dd6d25903281e3c33922b0d3857bc541baea054f09a1f2;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.2/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
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
	-	`sha256:dd4ddcf827aa03e72e193ca0088e8d319c9a678216c43ebe8d43639287137da0`  
		Last Modified: Thu, 17 Oct 2024 03:42:45 GMT  
		Size: 128.1 MB (128073539 bytes)  
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
