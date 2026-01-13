## `dart:beta`

```console
$ docker pull dart@sha256:b76a68ed11e34e77d10eabf2f030ee61e5516b20c2a1a99542ab273c4c3dbb22
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

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:6f1f83062a2e18c7f25274ccae6b8d032a0e4771ac9dbb4a187c621f0088d324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307095113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c567583ca44c78a8a4ea64fa4c79231c02930145d40522171278e922ea4907`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:18:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:18:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:18:39 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:18:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:18:39 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:18:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab3084e87930151d7aed530bbb1bf2c8a24f3087ad9e16bb222a589c9b730c`  
		Last Modified: Tue, 13 Jan 2026 02:19:31 GMT  
		Size: 42.5 MB (42496039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6365420d51d2b6ba23eb3b86a834f1430856916db5082f05852c279b53b499`  
		Last Modified: Tue, 13 Jan 2026 02:19:28 GMT  
		Size: 1.9 MB (1870165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae29fd97922bf83189a8f61d1673ca03d22a630f2057bd2afbd5a08381fe0f66`  
		Last Modified: Tue, 13 Jan 2026 02:19:37 GMT  
		Size: 233.0 MB (232955192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:6ddecf1cbe40e76b1debeab4d1f6a75acf6a6261ff2703b57d13655ff387193b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba740fc9c0c310a69d95c6f8b05bf840e58bc5d769d8da60859fe6ff9f89bd4`

```dockerfile
```

-	Layers:
	-	`sha256:bae18b819cdd2663c79709acfdf57e41fbfbb08e41d5cfce6808806a425c5e64`  
		Last Modified: Tue, 13 Jan 2026 03:54:32 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:b8c79fcaef46f6877092d936e8f7f8daf5728cc9e8bd8513360418ce689f1afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222895680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785e7f2454e3019594e2bc3851b597efd74544febe620f85964f6a92f838899b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:05:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:05:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 03:05:25 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 03:05:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:05:25 GMT
WORKDIR /root
# Tue, 13 Jan 2026 03:05:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957583ed8fcdaa998dc06645e341fbfc24ab26ab8562d1dc6cdcc88d2201c62e`  
		Last Modified: Tue, 13 Jan 2026 03:06:07 GMT  
		Size: 37.5 MB (37497709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1786de50aa83185ce894c4e3f8e9311f08767b0111fa1a4f16cd282d8156609`  
		Last Modified: Tue, 13 Jan 2026 03:06:03 GMT  
		Size: 1.3 MB (1273158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6249c63e5f13e917efed16d0ea9050c22ee9735e5ee8e44bfc65a28238379296`  
		Last Modified: Tue, 13 Jan 2026 03:06:15 GMT  
		Size: 157.9 MB (157916203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:0d5cb9c1b02a11a681c5d467527b9989cffd2ae633546689537bebe3eadccb3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c812f6d3a6ec27b0e362192a4b4f09010c0641c8a9e1dbd9a45b6bdf53812559`

```dockerfile
```

-	Layers:
	-	`sha256:9f9974f21138c8780edda9e1aabe2b61aa394e6805118715be77db4473b9b2d5`  
		Last Modified: Tue, 13 Jan 2026 03:54:35 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ec48e9d6d4931de4151322971d76a2f1d48444811238f005d62202fbce0f7903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305469520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0315b8318b9946bef43db6762f4bfc8741ddeb82fc33440d4879c8ed03d627b5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:23:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:23:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 13 Jan 2026 02:23:41 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 13 Jan 2026 02:23:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:23:41 GMT
WORKDIR /root
# Tue, 13 Jan 2026 02:23:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b54eb21223789e2fa9a8d33b8925f7224a598f8beb030d3488442472aaab43`  
		Last Modified: Tue, 13 Jan 2026 03:56:02 GMT  
		Size: 42.3 MB (42292867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d82efa0dda122393dd41946835f8d58cb49d4bde45d76fdf251bd46b6411b9`  
		Last Modified: Tue, 13 Jan 2026 02:24:34 GMT  
		Size: 1.6 MB (1564522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d0899c6548d7cd6f75dcbee200472ee14c5994d5f8dc2c5a205076414ee6`  
		Last Modified: Tue, 13 Jan 2026 02:24:43 GMT  
		Size: 231.5 MB (231478057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:f2095d6e715596a40936aae990509a05677f58d13e8ae77e305945fb43d03878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e736b26bf7449ad338ba0eedb83f7db5911276908639d6524fa1380d2c18d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9cf3078c4cce3a36c0e77e6f09187c38897fefdf194ee55114cad9574f6a2ad`  
		Last Modified: Tue, 13 Jan 2026 03:54:41 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:2cfdd54bdc709dd57f5e9967e59dcf202795d53070353a674b7466068ed75939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251894743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b877615a26388ddead16a06e335acd030c2aaa08ad3ed4964cf6845f15b057d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 17:53:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 07 Jan 2026 17:53:21 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 07 Jan 2026 17:53:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Jan 2026 17:53:21 GMT
WORKDIR /root
# Thu, 08 Jan 2026 19:03:50 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=edd704e758363f4e91f7e331e8c0c1dd6f65459a2c45a12ca8800c98ea6aa994;             SDK_ARCH="x64";;         armhf)             DART_SHA256=668f984cb8252e3b1ad067a1fee4985a58453ac8575042d4c12781297f8b7f65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=30b6e1e200a55108989e52094186fbb3f71819c1d75ba1fe9f084f8b77930415;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=ac3fd240cb4ad31e7b64d33f11a266e007f80a4554d6e53c2accf57f57a2d396;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-296.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7371402766e4abc95eaf0d0fca5d28b341ec201064383d231f20c9f6c9cbfd42`  
		Last Modified: Wed, 07 Jan 2026 17:59:02 GMT  
		Size: 41.6 MB (41560755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33684bab959ef2a5be84df6d39f37456a938f2f54f81fa698516adc65104c8b`  
		Last Modified: Wed, 07 Jan 2026 17:58:56 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20287815c4db5622d2036c3b61c21b86ac227bcbfc7a019cc23c3d372c0027`  
		Last Modified: Thu, 08 Jan 2026 19:09:04 GMT  
		Size: 180.5 MB (180493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:9ffb45d7609846f4cdfeec23d2d0f8a0f20aa8ff3b1abc4e57712587b0a74a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac32ba00dccfda38803d938d9c652855a1927a5b4ed811dc448294c7c79d096`

```dockerfile
```

-	Layers:
	-	`sha256:05c7bb5d7458d535a1e4271e1e71355be0072e8f31152f6a4ecca5a2c3a14823`  
		Last Modified: Thu, 08 Jan 2026 21:53:39 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json
