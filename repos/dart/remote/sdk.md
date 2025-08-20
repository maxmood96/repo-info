## `dart:sdk`

```console
$ docker pull dart@sha256:570376d123ff9ddc55c2f01dff3e5161b19f818f38a401c9dc19a9a9f2d12ef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:82ac018e41734030799914e5ce313b4bb5183e92b00bfc41f8dfbf00a872b543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295374189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613678f7e783d3b058408c005f02296ed76e52e9a4d5d71c2a9bed4d7c5b4862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5031e9e92260c6719209917d4471da96ea7834a5b1ed5f06031366770420e6be`  
		Last Modified: Wed, 20 Aug 2025 18:40:48 GMT  
		Size: 42.5 MB (42480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67608fd3791b8b8ed71ae6b23139605d68d89a91694d98ed76b884a527be5e61`  
		Last Modified: Wed, 20 Aug 2025 18:40:44 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9af5d5f5f5d85caab45c1a4a51397a255cc3043cefd7466f6ede61731d4dd69`  
		Last Modified: Wed, 20 Aug 2025 20:54:00 GMT  
		Size: 221.2 MB (221247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:64ebee01c9328ea81d1f56af149dedb8935cd52d634c361d341e5a007708326e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2536a7862ad6e6cc7dda23caec94a04b41457ec469b9a66908b9164bb28b6e3f`

```dockerfile
```

-	Layers:
	-	`sha256:acee13f2ab0384617440f06cf80f206d4ee1a4368e93f7c55561fc9f7b758507`  
		Last Modified: Wed, 20 Aug 2025 20:53:25 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:3ab948fc8a4111b30b2f3e06ec0e727a00edb82801448e09464bba399cf02016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220749423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff87cc1c4a359c39d0ad5e80c413bf8bfc130e7c61fd0f6adaad858756c9867`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97637b80b152bf1acb3dae7b2d3f4c272d6fe5352fbdb3919889a4081924f07`  
		Last Modified: Thu, 14 Aug 2025 17:53:40 GMT  
		Size: 37.5 MB (37478412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd21b12715dcd82b36216f964ba5790eb12ffa810e4bf0bfb70d7fcdbca353`  
		Last Modified: Thu, 14 Aug 2025 17:01:31 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c3f0397f1d937d5a38e1358aba4d36d9ba500998ef860accc552fe3497e7`  
		Last Modified: Wed, 20 Aug 2025 20:53:59 GMT  
		Size: 155.8 MB (155788378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e4c983586796ae482a8d08fd869ebc4fe81598480dac82150563cfdeb8af4a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae47e2e9245dd792c3707f05e4b6f621e08119ce28c47842d4fc4b749608ed`

```dockerfile
```

-	Layers:
	-	`sha256:59e0656aea816b79011f210a7c61f20286a9051dc5287618b0cefb7f6551022a`  
		Last Modified: Wed, 20 Aug 2025 20:53:29 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:b9702758244f57cd486772ce4b75de8594ba32ba8ef93f3997d3982760e8ff9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294657088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e0b67af315f8ffab171d684724a3b24ad5fda09a835e36f01e906247b06922`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 Aug 2025 13:12:00 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Aug 2025 13:12:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Aug 2025 13:12:00 GMT
WORKDIR /root
# Wed, 20 Aug 2025 13:12:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=9e73c2dbf557b844328ada4f0b42a38f585b8226e77e3e96456267fc68ae2769;             SDK_ARCH="x64";;         armhf)             DART_SHA256=1cf6cd418109de72da92ed60e133bebcf5535adb2220ba7928d79d1d0c2a453d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=d8ec9c7f0ae8f242ea9c76b9846aaeffd484c656879befd8e8ee7fc1e8d167db;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=61ece7d18acf3479e10b4caaa50b75efc3ff3831b0d150c0e60205f242f7f6d6;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3afea05610d5e523abc7b1b80da95f86be166605de4bc50f647f30021609db`  
		Last Modified: Wed, 20 Aug 2025 18:52:15 GMT  
		Size: 42.3 MB (42265724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856a5741073f9a038c6f208b8b8c66a087d92e3f8d612594b31b217d6ae444c`  
		Last Modified: Wed, 20 Aug 2025 18:52:11 GMT  
		Size: 1.6 MB (1566645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bb9e794ad4f572aa6212cee4dfbe2b9bbbd2883af98c5affac8cabe97f4365`  
		Last Modified: Wed, 20 Aug 2025 19:40:50 GMT  
		Size: 220.7 MB (220688643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:038f1f1f145df1e762b046c8c055b7274f4f1da912cc69cccb398574f047a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb431a0375c140398c46354c8dc64d14cc3844ac74e346607b37da5bf7f0ab3`

```dockerfile
```

-	Layers:
	-	`sha256:408767754ba9a985371bfc75f67b63385f5075718510f1188664551da93a8033`  
		Last Modified: Wed, 20 Aug 2025 20:53:32 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:167e64a40bca0723a2855103c66851c56fd815593d65ec4885d88160d1bf595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232352868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28107717a0f106f1afa443c80f73599a673731c51ef2b30c511bf9a4edc8a5e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 14 Aug 2025 09:10:38 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 14 Aug 2025 09:10:38 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 09:10:38 GMT
WORKDIR /root
# Thu, 14 Aug 2025 09:10:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=75bf2badc56cd6aff829042a0112ca5f3cf50bcf7fd95c29bc76650579dc00e1;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c2bc9f74f3d77ff5e2d66b10eb9acb81e1978ef7ec88772a8a0231d0dbc526ac;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e9a028b0be5325e2cbf5118ab6c6c407d302fb220ae5dc7d9d6f5648676fb724;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=81df475711bf672ef4d04bcbef3cc563b6e9224ba0742f73cd538ff649361d74;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a1e4eb491912dc7b21fd6a73c25e90deeffc6bafa2b51bcc63bbb402c65b35`  
		Last Modified: Sun, 17 Aug 2025 07:55:48 GMT  
		Size: 41.5 MB (41549977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c887a46dde247e91dccbfb3e2a5b2739f880ec79160ee89876ed59756214067`  
		Last Modified: Sun, 17 Aug 2025 07:55:45 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92992550b3126ba3ff441f4e84d0dd756d8b7414d2d6cf8fc71947270abdc82`  
		Last Modified: Sun, 17 Aug 2025 08:07:24 GMT  
		Size: 161.0 MB (160964166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e098104ba0efa6950ccb94ceb88ed40c63088c24b8325a8a412783f4d57602d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8f479460e0e1346a48da29857aba544f754de2052708dadd0dc214d611e93`

```dockerfile
```

-	Layers:
	-	`sha256:bae4bba6c3775f017525bb113980671e82aaf3c3798e7004f3679b2afaf5dd80`  
		Last Modified: Sun, 17 Aug 2025 08:53:24 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json
