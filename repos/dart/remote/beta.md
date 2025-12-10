## `dart:beta`

```console
$ docker pull dart@sha256:0d8592ebfdd9f8787ee862cc7e44c02a8207a6154021d9afa3dd58b1dc691678
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
$ docker pull dart@sha256:20519089835056cab79b0380d0890ecf43937e577beb78091ac185ad7cd52b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305114145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dd14fb6d806a264112b7e71647d76fbd99f9a26728c22edfdb9c8726442326`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:09:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:09:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 08 Dec 2025 23:09:07 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 08 Dec 2025 23:09:07 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:09:07 GMT
WORKDIR /root
# Mon, 08 Dec 2025 23:09:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581329b06a199392f585d8b78f555e6a16564525937ff4dc487383e8d8f947d5`  
		Last Modified: Mon, 08 Dec 2025 23:10:18 GMT  
		Size: 42.5 MB (42494103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff929d39f7136aba46a1f6a2a094ece872c5ada290f5ef31c6f6b4f69642d7d`  
		Last Modified: Mon, 08 Dec 2025 23:10:14 GMT  
		Size: 1.9 MB (1873623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b7a27a31d539105f131c9a89bfc45345b120c67bb77fe96ca6ccfa83a15d2`  
		Last Modified: Mon, 08 Dec 2025 23:10:19 GMT  
		Size: 231.0 MB (230969891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:494ce442aae576fb62f74e58b61b329b22312c5cb1172f41bbca46c9e6a7229b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d93f052751dcaf7b81bda20eea14d2ed85a0b962e27a1fdf5da0f4d7d6f239`

```dockerfile
```

-	Layers:
	-	`sha256:fce368f3531398c73d5552681ffa410a67ba1e944aac69e142843c18c9b62f31`  
		Last Modified: Tue, 09 Dec 2025 00:54:25 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:9ed2778af698e0bf57de8aa27626043a404bf2a2ed06cd4c44de8c8fe9eb2e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221092314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608cc59d9642ba75c1134ea383620bdb698760d765c25134d596e11678844b4c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:12:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:12:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Dec 2025 00:12:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Dec 2025 00:12:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:12:05 GMT
WORKDIR /root
# Tue, 09 Dec 2025 00:12:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0bde31488d6bd56a51952609027f33616c1eccb2ff4775c18a41ae63886fb`  
		Last Modified: Tue, 09 Dec 2025 00:12:55 GMT  
		Size: 37.5 MB (37498295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48160cca2f3e40fb4d84d90b19ee96d5cefdd88d48b88711f35bfb2a1ebcfe46`  
		Last Modified: Tue, 09 Dec 2025 00:12:52 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e77619ec2d71fe6c4c64add4e6c620eee2ecb974d5a07fe3edabaaecdccc3a8`  
		Last Modified: Tue, 09 Dec 2025 01:17:47 GMT  
		Size: 156.1 MB (156108855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:71396abeeb1690717e26590dd45f3e323f54a02c664f9f8978c0b2e27dc7423f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595ffbbe51ea670003858fec8f8c78c517234fd17648a706a49b205ff6b13cd7`

```dockerfile
```

-	Layers:
	-	`sha256:767f734302c8cbf5908d7aa38c5b7a0a86658da931fb9b001c017e3434342196`  
		Last Modified: Tue, 09 Dec 2025 03:53:58 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:066ee8ce165a8cafd2502ed76f67db1eb7b9db5d5ae679cd7cdbf85dffcf7c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303583484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac234390be29f1968b465e510547f689fc3c8b3322adc1a730e0f5d908201450`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:12:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 08 Dec 2025 23:13:00 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 08 Dec 2025 23:13:00 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:13:00 GMT
WORKDIR /root
# Mon, 08 Dec 2025 23:13:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d899d4f9f9fa77838090813d15d475c0af6266a7ef487646c1188beb39c3ea1`  
		Last Modified: Mon, 08 Dec 2025 23:14:08 GMT  
		Size: 42.3 MB (42293408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd90d3bc1c1a39ba19625e95151b82f5364e00ada2ba33833adde99e7a225388`  
		Last Modified: Mon, 08 Dec 2025 23:14:03 GMT  
		Size: 1.6 MB (1566649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a08ce233cddb8b525043a2c2824cbf80885f8582a66710863b48b95f3e6d08f`  
		Last Modified: Mon, 08 Dec 2025 23:14:28 GMT  
		Size: 229.6 MB (229584767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:9031081999e2d837f4c7a03d51748d6e53f1bbdd82f77eae793e120b78ad7419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfa39258186f796946f337eb5bd4edf385c1b3dfff1bf7f0fdf0e708a577300`

```dockerfile
```

-	Layers:
	-	`sha256:a2c5d5429eefdf5915b30edf09857013467c46ac2cf90f1b20bcd1d91829a778`  
		Last Modified: Tue, 09 Dec 2025 03:54:01 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:a9e74eaabdd530247853823149e2cd262f518ccc9771e814e20ac41053f4a6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249840551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9abc3994de87045e100e2fc90a9798cbab311e4ca8afaf8cebb347d1706abd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 18:21:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:21:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Dec 2025 18:21:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Dec 2025 18:21:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:21:05 GMT
WORKDIR /root
# Fri, 05 Dec 2025 07:37:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b313c517bbfa7a5b726c6a766d6aa3a74fbef75b6ae8435a341a6c892a1a28c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=783cb6bdb7dd7991d15b2cf1c31eaf69d29f1bd3469fc4d511b7599eafc9305d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=4ba60cf02bc68bc524dc5f75fdb3e65f36d07b4698bed1df1de5b4584c3872c2;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=8a38056f963876e8249df1f7099fc2b07995a9be25244b4571cd6662a84e5803;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-200.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d187aa75d6411bfc9c015781547398506ff8a5d8e0c4ee5c89cba4597dca7658`  
		Last Modified: Tue, 02 Dec 2025 18:26:43 GMT  
		Size: 41.6 MB (41560771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1041beabf784b9a8a14f47ab8166f4c0734faf36f7141b1c5273529ee215bb06`  
		Last Modified: Tue, 02 Dec 2025 18:26:40 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755d03422fc004be8f0bec8c81c7e1ef9e85b1f57722e3638979aca86923f189`  
		Last Modified: Fri, 05 Dec 2025 09:53:55 GMT  
		Size: 178.4 MB (178439551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:1abf61397be53470d13360aff1ae9c183a6c11ea7814f9d6e5ddd1ccc6805b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448ed0099e84c07e0c8d5b721f84cca2e0f3bb660df0690ac7af9c779b281b35`

```dockerfile
```

-	Layers:
	-	`sha256:55ca52a37e43f49c8533fdf07f2cd97c1556ab831523105c5efe422cf29c8507`  
		Last Modified: Fri, 05 Dec 2025 09:53:27 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json
