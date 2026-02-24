## `dart:beta-sdk`

```console
$ docker pull dart@sha256:b5cfb124ff9f86ca6c51af77e5af364ef93a4f6d20d7c4497e5710434c88f5f4
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

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:8688d0284b9370c63530f574bd75e28b55ebc0f5220c15b1a05a23d6c5a0a3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309460330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83aea4e297ce922152ee3391e96f655ac6c082d11d250ab95ef902fa77233a2a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 24 Feb 2026 17:35:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 17:35:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 17:35:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 17:35:46 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 17:35:46 GMT
WORKDIR /root
# Tue, 24 Feb 2026 17:36:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e83ea8446bb5b2aee78b2226c164d6225076764207a9016b820a575194bd3e`  
		Last Modified: Tue, 24 Feb 2026 17:36:25 GMT  
		Size: 42.5 MB (42492425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641a076f24eb4d31fe67a975b987f76389eba01572792f72ec7bf69bea57601`  
		Last Modified: Tue, 24 Feb 2026 17:36:23 GMT  
		Size: 1.9 MB (1870173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e45719416203712456355c1966db24cae5e2bb1b484dddb2e2a1f21ec072e5`  
		Last Modified: Tue, 24 Feb 2026 17:37:16 GMT  
		Size: 235.3 MB (235319104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:95dcec104415085895192b2a7bf02856bdbda39d32cd25a6836ea6b83070bac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b27a68273829a8309621103b0fce5efd8b2eea0439cbbac7ae5970c9da779d`

```dockerfile
```

-	Layers:
	-	`sha256:cdafd4cc093a849bb6882ef4113252741e441887d72c056cb918193f83b02c40`  
		Last Modified: Tue, 24 Feb 2026 17:37:11 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d1b0d3c9d58e00ec06da92c78231657f34e33e5cb44be4660f06cf69a97d53fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224225957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bea35e5b6116daaedace14fa4f56a451227226bd68b746e727a0cc459824c53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 24 Feb 2026 17:35:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 17:35:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 17:35:53 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 17:35:53 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 17:35:53 GMT
WORKDIR /root
# Tue, 24 Feb 2026 17:36:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66ec589fc9697f0d717fa7c73918963aab74ab10faeebaafef01baa094e2cee`  
		Last Modified: Tue, 24 Feb 2026 17:36:22 GMT  
		Size: 37.5 MB (37494589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c20d1e9cbeac670b35f42d52b3be888bfe4b629cc321907842849b064062ac`  
		Last Modified: Tue, 24 Feb 2026 17:36:21 GMT  
		Size: 1.3 MB (1273154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f436de2e1f8f97c5f080da50bec9e0a6c5b3312500d8265ee77b3a95bcdc9`  
		Last Modified: Tue, 24 Feb 2026 17:37:01 GMT  
		Size: 159.2 MB (159244434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:503385bc20b02f1b35be930edc2fda16ac1f77a921d4fa3c4f68da0cd1692928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fee868aeb5b17ad83473d4f9a0736f1710dcbcd0122b9f52d94606bd013cb0`

```dockerfile
```

-	Layers:
	-	`sha256:b3c9d1897615c25acedee729e2e10588d6deae83bf7e1829143e0b0a40f966e2`  
		Last Modified: Tue, 24 Feb 2026 17:36:57 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:636048725d33845bd5c8ec16957328ef0bdbb03148e4cd72007fe7ff0cc67620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307847029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5ea697afa998a55aedb98c1d1d465f9b0ea81290e10010dd08ac9ad34bc1c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 24 Feb 2026 17:35:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 17:35:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 17:35:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 17:35:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 17:35:45 GMT
WORKDIR /root
# Tue, 24 Feb 2026 17:36:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889b7673a83c1154ac289d57384142aa387438e52c2605a2b5b19e4e524e76cf`  
		Last Modified: Tue, 24 Feb 2026 17:36:29 GMT  
		Size: 42.3 MB (42291957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e96f47cf3613b0bdb90f0c448b3578d3fd54843035767141c17c77f8dc8b9e`  
		Last Modified: Tue, 24 Feb 2026 17:36:27 GMT  
		Size: 1.6 MB (1564522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66188dc7b634eecf71945baec3d9040609403313939fec44b9e2fe4de9edde9d`  
		Last Modified: Tue, 24 Feb 2026 17:37:31 GMT  
		Size: 233.9 MB (233850454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1a164123f6c215e6f35bcb5cdc5438581f2e6673a2ce4c155a7941e10b9f4b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965ce99f29040a9f19c22a46d9ad38f68b3d603b28ca6c72f85b173d875b7e52`

```dockerfile
```

-	Layers:
	-	`sha256:5b8bde39b694071abad6e920d592a163667e6e0649a04e38379ead5e3dd966ae`  
		Last Modified: Tue, 24 Feb 2026 17:37:21 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:56272621b4380711de1c27999b81bbd8f25f15b6394da1248f8cf4c6a9acd998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253221880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48abe794e5744f16997ef397ec4941f0f8c3eac26d8bc9e5a5031492a63a22c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Tue, 24 Feb 2026 17:36:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 17:36:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 17:36:22 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 17:36:22 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 17:36:22 GMT
WORKDIR /root
# Tue, 24 Feb 2026 17:43:01 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b1ffb5d54515c9205f5aa5b80f611aabd2400fab85d7920cddf64ce77f4b24`  
		Last Modified: Tue, 24 Feb 2026 17:41:27 GMT  
		Size: 41.6 MB (41560908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d700e76008c419c1f10155a84068cb1db35d3aa1389becf195da577452287ba5`  
		Last Modified: Tue, 24 Feb 2026 17:41:14 GMT  
		Size: 1.6 MB (1564666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed5c6185812682fd8347b0b353cf6cbcc9ca2365b1f849dadd603e16b2e8d5d`  
		Last Modified: Tue, 24 Feb 2026 17:47:41 GMT  
		Size: 181.8 MB (181819885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:155008f15fd799c11c6f2cc42a1d19cdc629ffcfdde5d974beb67f0f51a5093e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d60df2f9528914b123ed6dc2a03674bd446921e695a2404fbffda75a500be60`

```dockerfile
```

-	Layers:
	-	`sha256:269fa9bf69870f232e7a28e563ec3be03d34d0976135e358d6db48a27c745ba8`  
		Last Modified: Tue, 24 Feb 2026 17:47:15 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json
