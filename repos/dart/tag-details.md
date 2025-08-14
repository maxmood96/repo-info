<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10.0-75.1.beta`](#dart3100-751beta)
-	[`dart:3.10.0-75.1.beta-sdk`](#dart3100-751beta-sdk)
-	[`dart:3.9`](#dart39)
-	[`dart:3.9-sdk`](#dart39-sdk)
-	[`dart:3.9.0`](#dart390)
-	[`dart:3.9.0-sdk`](#dart390-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-75.1.beta`

```console
$ docker pull dart@sha256:ac752a2db1111d945ed4c374d96b368d41a6e36f996f43d94b3cc5c5c4fc5fba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.10.0-75.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:e37f7117b38bb692aa9f26a15c92cdd1f09ae79ecc6c8920e53c8b149ba5f836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282109417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e03d86faca4f2b4a88ff768fc7cb6dc4e9a33a1f1bae1c4c51e94ea82d97b4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe9d72cb6b8ef54bc8a95fba754c0fef4dc3d8cddc41549dcc5456c1be7f693`  
		Last Modified: Thu, 14 Aug 2025 16:53:39 GMT  
		Size: 42.5 MB (42479916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960a711161dad1205d7a3a696a360d15bef4319d795b5ca9732d0fc82cf04676`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc57f3d4b6d83f9ad980aad6cd261aa91a25a647333d551f861af74e1681443d`  
		Last Modified: Thu, 14 Aug 2025 17:54:09 GMT  
		Size: 208.0 MB (207982577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:75d6bf7c43e61c779f73769592d5fdad01d93ad045c9d9526d93194719da968d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2d3ca565ce26f2e9894eab4d254c44dd9304dcd494834e92f6f67a6cc02147`

```dockerfile
```

-	Layers:
	-	`sha256:9dc890b3ff810caffc0c8c7ca9d309aa19434324a14f157410bfdabb5f71197d`  
		Last Modified: Thu, 14 Aug 2025 17:53:29 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:af1c38749636032f178190215574e23ec7cbb47d6c129ee497591b76e7c7b12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215045861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9059d630c6873c8fcb396338bf23122f70c589b9025dfabc37f56a88833f6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:0fb4fa6977669275d5f401b41e87cb33168d059da5da784a076289946c67b0f5`  
		Last Modified: Thu, 14 Aug 2025 17:53:59 GMT  
		Size: 150.1 MB (150084816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:d5bffaeb13f68d9b458968fb051c7e918ef8f9af8dbb9a0fbbace5d0c9df7fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86619cd55204299bf6e2870ca3b3b8031c8311e8b9484f700785e19216eadf27`

```dockerfile
```

-	Layers:
	-	`sha256:76312dee563d79f32fac703b94fb5bdbcceb6b66103a81f067ca5df68c83a9fc`  
		Last Modified: Thu, 14 Aug 2025 17:53:32 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:57501f3fdb8cdf9c48ce51afa306bc9b24058e35466ad8525126f85db2bc931a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281270046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad193395f3bb869e500748eba96df90c447bab010a9e9c4344417b675276020`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c50d8b6df0886b100244a376c57d178edd5a90d9b9bb55cc2635a925df620a7`  
		Last Modified: Thu, 14 Aug 2025 20:54:03 GMT  
		Size: 207.3 MB (207301561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:3fa656bb99bfcbaa8f1e3840f46dbb2c3284abc76e4712d1bc2bb85ced9a4ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09910c0ae5475672034439bc645f5d8a3e0f6c932b0fc14948e6f739063c2e8`

```dockerfile
```

-	Layers:
	-	`sha256:8f26996bf38ef9bb6552b4f5322b1adf933267c2b01475dd6bb19615d078271c`  
		Last Modified: Thu, 14 Aug 2025 20:53:28 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-75.1.beta-sdk`

```console
$ docker pull dart@sha256:ac752a2db1111d945ed4c374d96b368d41a6e36f996f43d94b3cc5c5c4fc5fba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.10.0-75.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e37f7117b38bb692aa9f26a15c92cdd1f09ae79ecc6c8920e53c8b149ba5f836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282109417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e03d86faca4f2b4a88ff768fc7cb6dc4e9a33a1f1bae1c4c51e94ea82d97b4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe9d72cb6b8ef54bc8a95fba754c0fef4dc3d8cddc41549dcc5456c1be7f693`  
		Last Modified: Thu, 14 Aug 2025 16:53:39 GMT  
		Size: 42.5 MB (42479916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960a711161dad1205d7a3a696a360d15bef4319d795b5ca9732d0fc82cf04676`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc57f3d4b6d83f9ad980aad6cd261aa91a25a647333d551f861af74e1681443d`  
		Last Modified: Thu, 14 Aug 2025 17:54:09 GMT  
		Size: 208.0 MB (207982577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:75d6bf7c43e61c779f73769592d5fdad01d93ad045c9d9526d93194719da968d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2d3ca565ce26f2e9894eab4d254c44dd9304dcd494834e92f6f67a6cc02147`

```dockerfile
```

-	Layers:
	-	`sha256:9dc890b3ff810caffc0c8c7ca9d309aa19434324a14f157410bfdabb5f71197d`  
		Last Modified: Thu, 14 Aug 2025 17:53:29 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:af1c38749636032f178190215574e23ec7cbb47d6c129ee497591b76e7c7b12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215045861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9059d630c6873c8fcb396338bf23122f70c589b9025dfabc37f56a88833f6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:0fb4fa6977669275d5f401b41e87cb33168d059da5da784a076289946c67b0f5`  
		Last Modified: Thu, 14 Aug 2025 17:53:59 GMT  
		Size: 150.1 MB (150084816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d5bffaeb13f68d9b458968fb051c7e918ef8f9af8dbb9a0fbbace5d0c9df7fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86619cd55204299bf6e2870ca3b3b8031c8311e8b9484f700785e19216eadf27`

```dockerfile
```

-	Layers:
	-	`sha256:76312dee563d79f32fac703b94fb5bdbcceb6b66103a81f067ca5df68c83a9fc`  
		Last Modified: Thu, 14 Aug 2025 17:53:32 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-75.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:57501f3fdb8cdf9c48ce51afa306bc9b24058e35466ad8525126f85db2bc931a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281270046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad193395f3bb869e500748eba96df90c447bab010a9e9c4344417b675276020`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c50d8b6df0886b100244a376c57d178edd5a90d9b9bb55cc2635a925df620a7`  
		Last Modified: Thu, 14 Aug 2025 20:54:03 GMT  
		Size: 207.3 MB (207301561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-75.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3fa656bb99bfcbaa8f1e3840f46dbb2c3284abc76e4712d1bc2bb85ced9a4ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09910c0ae5475672034439bc645f5d8a3e0f6c932b0fc14948e6f739063c2e8`

```dockerfile
```

-	Layers:
	-	`sha256:8f26996bf38ef9bb6552b4f5322b1adf933267c2b01475dd6bb19615d078271c`  
		Last Modified: Thu, 14 Aug 2025 20:53:28 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9-sdk`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.0-sdk`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.9.0-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.0-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:ac752a2db1111d945ed4c374d96b368d41a6e36f996f43d94b3cc5c5c4fc5fba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:e37f7117b38bb692aa9f26a15c92cdd1f09ae79ecc6c8920e53c8b149ba5f836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282109417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e03d86faca4f2b4a88ff768fc7cb6dc4e9a33a1f1bae1c4c51e94ea82d97b4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe9d72cb6b8ef54bc8a95fba754c0fef4dc3d8cddc41549dcc5456c1be7f693`  
		Last Modified: Thu, 14 Aug 2025 16:53:39 GMT  
		Size: 42.5 MB (42479916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960a711161dad1205d7a3a696a360d15bef4319d795b5ca9732d0fc82cf04676`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc57f3d4b6d83f9ad980aad6cd261aa91a25a647333d551f861af74e1681443d`  
		Last Modified: Thu, 14 Aug 2025 17:54:09 GMT  
		Size: 208.0 MB (207982577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:75d6bf7c43e61c779f73769592d5fdad01d93ad045c9d9526d93194719da968d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2d3ca565ce26f2e9894eab4d254c44dd9304dcd494834e92f6f67a6cc02147`

```dockerfile
```

-	Layers:
	-	`sha256:9dc890b3ff810caffc0c8c7ca9d309aa19434324a14f157410bfdabb5f71197d`  
		Last Modified: Thu, 14 Aug 2025 17:53:29 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:af1c38749636032f178190215574e23ec7cbb47d6c129ee497591b76e7c7b12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215045861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9059d630c6873c8fcb396338bf23122f70c589b9025dfabc37f56a88833f6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:0fb4fa6977669275d5f401b41e87cb33168d059da5da784a076289946c67b0f5`  
		Last Modified: Thu, 14 Aug 2025 17:53:59 GMT  
		Size: 150.1 MB (150084816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:d5bffaeb13f68d9b458968fb051c7e918ef8f9af8dbb9a0fbbace5d0c9df7fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86619cd55204299bf6e2870ca3b3b8031c8311e8b9484f700785e19216eadf27`

```dockerfile
```

-	Layers:
	-	`sha256:76312dee563d79f32fac703b94fb5bdbcceb6b66103a81f067ca5df68c83a9fc`  
		Last Modified: Thu, 14 Aug 2025 17:53:32 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:57501f3fdb8cdf9c48ce51afa306bc9b24058e35466ad8525126f85db2bc931a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281270046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad193395f3bb869e500748eba96df90c447bab010a9e9c4344417b675276020`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c50d8b6df0886b100244a376c57d178edd5a90d9b9bb55cc2635a925df620a7`  
		Last Modified: Thu, 14 Aug 2025 20:54:03 GMT  
		Size: 207.3 MB (207301561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:3fa656bb99bfcbaa8f1e3840f46dbb2c3284abc76e4712d1bc2bb85ced9a4ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09910c0ae5475672034439bc645f5d8a3e0f6c932b0fc14948e6f739063c2e8`

```dockerfile
```

-	Layers:
	-	`sha256:8f26996bf38ef9bb6552b4f5322b1adf933267c2b01475dd6bb19615d078271c`  
		Last Modified: Thu, 14 Aug 2025 20:53:28 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:ac752a2db1111d945ed4c374d96b368d41a6e36f996f43d94b3cc5c5c4fc5fba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:e37f7117b38bb692aa9f26a15c92cdd1f09ae79ecc6c8920e53c8b149ba5f836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282109417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e03d86faca4f2b4a88ff768fc7cb6dc4e9a33a1f1bae1c4c51e94ea82d97b4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe9d72cb6b8ef54bc8a95fba754c0fef4dc3d8cddc41549dcc5456c1be7f693`  
		Last Modified: Thu, 14 Aug 2025 16:53:39 GMT  
		Size: 42.5 MB (42479916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960a711161dad1205d7a3a696a360d15bef4319d795b5ca9732d0fc82cf04676`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc57f3d4b6d83f9ad980aad6cd261aa91a25a647333d551f861af74e1681443d`  
		Last Modified: Thu, 14 Aug 2025 17:54:09 GMT  
		Size: 208.0 MB (207982577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:75d6bf7c43e61c779f73769592d5fdad01d93ad045c9d9526d93194719da968d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2d3ca565ce26f2e9894eab4d254c44dd9304dcd494834e92f6f67a6cc02147`

```dockerfile
```

-	Layers:
	-	`sha256:9dc890b3ff810caffc0c8c7ca9d309aa19434324a14f157410bfdabb5f71197d`  
		Last Modified: Thu, 14 Aug 2025 17:53:29 GMT  
		Size: 19.0 KB (18961 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:af1c38749636032f178190215574e23ec7cbb47d6c129ee497591b76e7c7b12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215045861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9059d630c6873c8fcb396338bf23122f70c589b9025dfabc37f56a88833f6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
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
	-	`sha256:0fb4fa6977669275d5f401b41e87cb33168d059da5da784a076289946c67b0f5`  
		Last Modified: Thu, 14 Aug 2025 17:53:59 GMT  
		Size: 150.1 MB (150084816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d5bffaeb13f68d9b458968fb051c7e918ef8f9af8dbb9a0fbbace5d0c9df7fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86619cd55204299bf6e2870ca3b3b8031c8311e8b9484f700785e19216eadf27`

```dockerfile
```

-	Layers:
	-	`sha256:76312dee563d79f32fac703b94fb5bdbcceb6b66103a81f067ca5df68c83a9fc`  
		Last Modified: Thu, 14 Aug 2025 17:53:32 GMT  
		Size: 19.1 KB (19063 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:57501f3fdb8cdf9c48ce51afa306bc9b24058e35466ad8525126f85db2bc931a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281270046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad193395f3bb869e500748eba96df90c447bab010a9e9c4344417b675276020`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6611ef00903d500efd0bc74a910b01c818ed5c685f77b980c505b8a1b03f8c53;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c878444a937d23344b9bcb95a052a3b2c2709e51369a88b4bcf6edbadfc070df;             SDK_ARCH="arm";;         arm64)             DART_SHA256=313fbe03e064742ddac0f46c78b0a1c5e1e51c5040cc447e0c17b54885f77f51;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b330ac3c76aec2d823056b65bdbb768cb49d95f9451528a4295509294443cb28;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-75.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c50d8b6df0886b100244a376c57d178edd5a90d9b9bb55cc2635a925df620a7`  
		Last Modified: Thu, 14 Aug 2025 20:54:03 GMT  
		Size: 207.3 MB (207301561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3fa656bb99bfcbaa8f1e3840f46dbb2c3284abc76e4712d1bc2bb85ced9a4ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09910c0ae5475672034439bc645f5d8a3e0f6c932b0fc14948e6f739063c2e8`

```dockerfile
```

-	Layers:
	-	`sha256:8f26996bf38ef9bb6552b4f5322b1adf933267c2b01475dd6bb19615d078271c`  
		Last Modified: Thu, 14 Aug 2025 20:53:28 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:bb7ee3bd0d370d6f54f4f701cf8eec10ad8a9d726f9073ad3586b2128ad78771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1e23c4499590b111854fad3665a36433f573211a5fc399d8f5e09ef8b97ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2cf067d7afc1167bb69d22e79905a493a6b691aeeb9448a261e223539b7909`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110950d2e4c073c7c80791997693f35b31a16108a688544bbbe8029bb2660c1`  
		Last Modified: Thu, 14 Aug 2025 16:53:42 GMT  
		Size: 42.5 MB (42479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d19522797224714ecd6a243503a9c388d808929e0bb2550811a410a2d54b7`  
		Last Modified: Thu, 14 Aug 2025 16:53:33 GMT  
		Size: 1.9 MB (1873600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5629e970a5c74974188cb416df5d2791b7d6dd02e22e9256e6a3a3ce8f3b053`  
		Last Modified: Thu, 14 Aug 2025 17:53:57 GMT  
		Size: 221.3 MB (221253182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:10a1ec12399410bfefd6753146ce45481998e2347d02cbebb66c913fd997d962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547c29ad742d58c9796648ee56d9f7837166bcba5fcb2e800d43afe8419ebd4`

```dockerfile
```

-	Layers:
	-	`sha256:e5eaddee557e6264c436de59ce6d2c76c37251b302af5fbd080e33b5f1c935df`  
		Last Modified: Thu, 14 Aug 2025 17:53:23 GMT  
		Size: 20.6 KB (20650 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:2fda5d27f4be70470322470658dd84363012349e35018af2c35b3d5d741353b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220742597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de82f9e6eae794d8087a95a3110b73f3426c3c0222744ec7d5a88b9b3937b33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
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
	-	`sha256:bd9a3d97dea3b3ee391039ad6f72a22e05c54dfd67493074a5bd242db4519080`  
		Last Modified: Thu, 14 Aug 2025 17:53:49 GMT  
		Size: 155.8 MB (155781552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0f765baea28386fbb97cb7d967726213424610d5fe98d9f67b972d382caed8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b4cd5637dc586571196f82f130f587a70e125d517cd53b6d468b01d8e2526`

```dockerfile
```

-	Layers:
	-	`sha256:1beed90db3e9da2a3657c659b7f89fdcc3669a9c1f10bd8488a05e9fd6db7f5b`  
		Last Modified: Thu, 14 Aug 2025 17:53:26 GMT  
		Size: 20.8 KB (20800 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cb2445d720c8d24f3debd3acbab024607d953d24e2f6b3e0be2bd22f8491ee9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294652531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57be5b1749c7b480c614f4a3e729ea40048149f7e83cc01ac0f533b33c265b9e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18287c360d1688b0e600d87c5823779357babf2a466e30908bae9b439aaee0cf`  
		Last Modified: Thu, 14 Aug 2025 19:37:06 GMT  
		Size: 42.3 MB (42265768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b0ce991ee7dfa825eff9ab0d1c769604247e53e91ab7833da23126e435a804`  
		Last Modified: Thu, 14 Aug 2025 19:37:02 GMT  
		Size: 1.6 MB (1566641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d4691e1cb782c18055c26e4e84bc4d91b6a7f00e825ccced31be6abaa7a2f8`  
		Last Modified: Thu, 14 Aug 2025 20:08:28 GMT  
		Size: 220.7 MB (220684046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b6cc183cfb9d956230f32ff33a4ba250100799cd6da2c2be1bcb334e67e62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d968731bd0f6001d5a4e2718d987264e43e41f1288f2fb12932ff05d3f742e`

```dockerfile
```

-	Layers:
	-	`sha256:fad8d8e854d9a8c7bf806f35dfa0bc27885f9e34d74ea306d29419e0d2421bac`  
		Last Modified: Thu, 14 Aug 2025 20:53:21 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json
