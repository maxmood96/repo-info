## `dart:3-sdk`

```console
$ docker pull dart@sha256:4598f4a37cda764808c931d9e1d77f8eb2aa283439702d7bc11205dd50846239
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
$ docker pull dart@sha256:46f76404a63829a6352f58fabea528e67f9fd21f22b73a541239b29581936c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311926530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44eba4602897befa7306ed6243189770b19c2e2f3ef6b2bddf2b4230ac66a81c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Dec 2024 15:15:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6f5fa97b705363b2ca334014be14c89bd94486df654d9c1f7a072070be7882`  
		Last Modified: Tue, 24 Dec 2024 22:26:51 GMT  
		Size: 54.7 MB (54712110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a70b52f6e336b8413c2bc4d145049fdcd35e67e0062a48039b1dccfcd257f50`  
		Size: 1.8 MB (1796915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a503a0422de76312935fdb92beebb6e2c5b12699354d237b4b7da14e8ee36e0`  
		Last Modified: Tue, 24 Dec 2024 22:26:53 GMT  
		Size: 227.2 MB (227185892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0a116a80ae759b7ce84e52fdab8ebe2388f65455b41c9228054100f50cb05f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c26b35a28082d63fd24ae8f0e81199d8ce32fc59c1a743ec90af3d19e7bfc8e`

```dockerfile
```

-	Layers:
	-	`sha256:b312583301bd3ea9a0978c990cb865ae6f99b0db423b1991153bc94b080fea9e`  
		Last Modified: Tue, 24 Dec 2024 22:26:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

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

### `dart:3-sdk` - unknown; unknown

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
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:646068950440e75924bbb0b2de9906ee0a577166959a9be9b3d7f98acd66c133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310386886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfeedc47aad766dabe1a7bf8b5e225ef303a01aa62884bf6b5f80e184cf6e337`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Dec 2024 15:15:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350b8ee3c923617f751426999c11c9ebb6d18fea5bdfbe043c10d7ab794508e0`  
		Last Modified: Wed, 25 Dec 2024 01:56:24 GMT  
		Size: 54.5 MB (54478718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644c7934a85b5386cf1664e7edcefe7194b3a4e888f05f1e989c0e505590ecfc`  
		Last Modified: Wed, 25 Dec 2024 01:56:23 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ff579ad83ddd814f587cea728fc823044072f2760cc2f25d34b5f5d6894210`  
		Last Modified: Wed, 25 Dec 2024 01:56:28 GMT  
		Size: 226.4 MB (226361382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d25f5d5c5fb126575459ab60a63e78169b34030c0391c4827232c553f73ca0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d549f87a1a8e9848dcb8dd139636ec367adcbd25cb2c61da96f215c675ef77f`

```dockerfile
```

-	Layers:
	-	`sha256:39b83ee156bb0106023f413d84ad1d5143d001bcd61e40f3c9cf1eaf02600641`  
		Last Modified: Wed, 25 Dec 2024 01:56:22 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json
