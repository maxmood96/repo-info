## `dart:latest`

```console
$ docker pull dart@sha256:b143c2f2ba9264aa2c531e80c6131b2fc8a47164471cb1f1368ad5509bd29e52
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
$ docker pull dart@sha256:ffc3c01e484010f25b6bee22cb71880bb1eac52b8bdafa8cdedf164c1cdb690f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311934255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233713d067ef3307134d5669f8047d2915bdbfc5cf407f67838e6685e1057b28`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43639dd324b6b5894f1cc406950f2c70d89617ad051ff862bde9fd40570e5192`  
		Last Modified: Wed, 08 Jan 2025 23:31:52 GMT  
		Size: 54.7 MB (54711790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c33f045c0949d13dc511e819dd1f659cdb84d5b013a0a0a5dd022281685ce5`  
		Last Modified: Wed, 08 Jan 2025 23:31:51 GMT  
		Size: 1.8 MB (1796919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19e6ccd46b54cc3b2a5d9f7f41aef5a4eef1eab745ad6143980766ff73c77c9`  
		Last Modified: Wed, 08 Jan 2025 23:31:54 GMT  
		Size: 227.2 MB (227193933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:01f387b98bdfe1ae560735fc7c785346ee9de99f9e7047d8cdbdd45855bb1a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e7a32a4def00d8345d5a5cfb637eec157fa8386bcd6b8e707d0511ce6982ce`

```dockerfile
```

-	Layers:
	-	`sha256:b97c0ea7c31b6119580a3f3dccef00b492dba9a91fd7d9aa68671b92a08d7d7e`  
		Last Modified: Wed, 08 Jan 2025 23:31:51 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:5f2487069072dd8c4f200cce135da1572af180b018b428ac7c7e1c4da757e308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210219204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e603ac81eb9bc69166a9570cd539319c0c34aad902c689350f162a928ef0cf0c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Dec 2024 15:15:24 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8e14ff436e1eec72618dabc94f421a97251f2068c9cc9ad2d3bb9d232d6155a3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=7281158159d65d35d0bee46a97eb425f3efcb53ca3e52fd4901aac47da8af3fc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=0f82f10f808c7003d0d03294ae9220b5e0824ab3d2d19b4929d4fa735254e7bf;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689318bf76a8dd4043ce70c82f26289471b16ae5819c010091389de80431b97b`  
		Last Modified: Wed, 25 Dec 2024 03:49:08 GMT  
		Size: 49.4 MB (49367345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c84d81f266ec2585355bd2e2ed55d6cd30d49f3236885c32df91cdf54f35ba`  
		Last Modified: Wed, 25 Dec 2024 03:49:06 GMT  
		Size: 1.2 MB (1221682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71626ea2bd04f4e757e6b3e4d35487afb3287484e7f2fffeffa992b84825ed8b`  
		Last Modified: Wed, 25 Dec 2024 03:49:10 GMT  
		Size: 135.7 MB (135696623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1f6f85ba40f1e37dfad8db488614c78a5a940a857693c3ef98ac1515ed2e391f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de9f27ca5f8c0a7af0725a2274031c5057d38e2127fead851aeccbd5ce54bf7`

```dockerfile
```

-	Layers:
	-	`sha256:1dc75df2864c0e798ecb465403d97d7dfa9d243e7603576620c0629d6cc05cd9`  
		Last Modified: Wed, 25 Dec 2024 03:49:06 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:993bfdc17a168ab0ce0b9628c28ba512b46efa8266ba8c4f22137e27392d3658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310385749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11a419f3f0ea79ae52c720c569bb307f20065fcef04e2947556d840acb9229b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=fbed37419784149c93f3ae444b9a9d1b5d5b73a521cbce731899d601d9b435b4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2792acd3abfba7f3d61fef7d0973bbd8069f5f0ebaa3a4bc47222cbf8d4811bf;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9192cc5efe2af1ff91aae692950550ae4eb649656e5e003c76b4ed55c328154e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.6.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa8c1c3b12a53353279d393f47b32f7d821fe90f459256db76e188171c89470`  
		Last Modified: Thu, 09 Jan 2025 06:52:23 GMT  
		Size: 54.5 MB (54478973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ca35b8af208b4cb83ffa0f8e224eec123321c5c743daf0863c50cad72cc851`  
		Last Modified: Thu, 09 Jan 2025 06:52:21 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86596cf895deb6e1c697222d9909a546a232393dcd29d546d464b0522c254bf7`  
		Last Modified: Thu, 09 Jan 2025 06:52:26 GMT  
		Size: 226.4 MB (226359990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:0e1768f381072f721e6919909d6af2f0e5be26d745bc5a57d26818a58ec7d0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51f23dd96332a92d8cd25042a78015bf61e120e66a6f223b694c2d21b64834f`

```dockerfile
```

-	Layers:
	-	`sha256:8a102958d6fa0c649ee6936812079551a8d69535fc4cbbc1d151c1175fec41a5`  
		Last Modified: Thu, 09 Jan 2025 06:52:21 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
