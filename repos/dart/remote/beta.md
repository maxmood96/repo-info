## `dart:beta`

```console
$ docker pull dart@sha256:a9f5b93205e6cbf53910db5f9a0a2d37ff33e01b64a1d13591f709bb83181c5a
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
$ docker pull dart@sha256:5084c7a1fed4cadc13c7c867e160748f0d8c08eb1c40a4420d6c97140a5a73e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296619863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7489a2443fa4b82dbd1bd94013a63eef90c98d0c4f2f5b768864c553ae1fea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9e550785035dcff2df32a0bed7ff284e976b218b003bc4ab115107868712`  
		Last Modified: Mon, 17 Mar 2025 23:14:31 GMT  
		Size: 54.9 MB (54908151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c63fead5de115fd918f08ab4ac8f058af8cd4fc6007b965aa9f8c55b78b982`  
		Last Modified: Mon, 17 Mar 2025 23:14:30 GMT  
		Size: 1.8 MB (1785446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247b71fb811807d5c0e71c827722d1f4c80904e5652bc688769e7e8eb513b96b`  
		Last Modified: Mon, 17 Mar 2025 23:14:33 GMT  
		Size: 211.7 MB (211721369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:ef0fbcca2ea768445bf58a153927a1ff71cf0b648b3d591d84cc71fe069fd42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6d023a713f9fa8b42a4f44a4a1dae84c572bdf8a99857595465737757f0345`

```dockerfile
```

-	Layers:
	-	`sha256:cc4cc1a711a4b44c7d9e01e42d0d865ccfefc5d7c770e71f6b202e4e9f4df89a`  
		Last Modified: Mon, 17 Mar 2025 23:14:30 GMT  
		Size: 17.9 KB (17906 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:6d745ba2c62a5390a0cb36e8316c4b673f8244d29409c121397cbe44c456a237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219311621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c255acae4e8e210333d8bc47eba0e7abeaa72eda330577e5db5cfa9c08693d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9360e16b8287d9e7cce502fbb1dabc9b4fdece658d3131f00f86e5c3041351`  
		Last Modified: Tue, 18 Mar 2025 06:13:51 GMT  
		Size: 49.6 MB (49562108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f19fcfca0e0eb3fd6966080c85aed47ea82f507c0bc2d962979594dfcf82c4`  
		Last Modified: Tue, 18 Mar 2025 06:13:50 GMT  
		Size: 1.2 MB (1221947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26c07ab65b9c9a16fda4ae08c7af791316f18f99e625fb98f2ae213de0580e3`  
		Last Modified: Tue, 18 Mar 2025 06:13:54 GMT  
		Size: 144.6 MB (144612446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:5dababe640d0ee146b66a31d4236bbafdc6e6e7d4e8250e84ab3ecee9f2852fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b5ba2582af4f3f56fc31b5d567a6b7f65d4182a35f808480182e1e681820bf`

```dockerfile
```

-	Layers:
	-	`sha256:e7b8d03af067d900d72873da1694cd702d823306463984967da847afbe8aea58`  
		Last Modified: Tue, 18 Mar 2025 06:13:49 GMT  
		Size: 18.0 KB (18008 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:6d638efd160b119fd44786db528698d15ae742da2cff3210359d70a35124fea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295552034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ffdbbd91d74ffd057cca0143a4294846ec37f2ea52548519dde0db4090d062`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Mar 2025 10:36:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Mar 2025 10:36:55 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Mar 2025 10:36:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Mar 2025 10:36:55 GMT
WORKDIR /root
# Wed, 12 Mar 2025 10:36:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=c1b1d66c0fd37a432b268e43b06520b824ada88b268e9e0a3d0e244ba4f3abe4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=38ccb0abd0f754a7d3b95106cdccd54899a749be7833e49455eadf689941256c;             SDK_ARCH="arm";;         arm64)             DART_SHA256=86ce086fb32bceed703e6f460a1c9835aaa421b83ee960d6dfee809d527b5e09;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-70.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387d928a318fc9806cbd845acf2fdccedc9302e7e8e65177c2aa8a4b9dee0984`  
		Last Modified: Tue, 18 Mar 2025 05:26:59 GMT  
		Size: 54.7 MB (54678842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0013f41ef3c1c0739a092d918efdb7b1b49a0e0d3302213f91f347fa3479601f`  
		Last Modified: Tue, 18 Mar 2025 05:26:58 GMT  
		Size: 1.5 MB (1488211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f5abb1e61c9fe22c55dafbde2ba68140d8bb72d9bbf6627efcadc935ef299`  
		Last Modified: Tue, 18 Mar 2025 05:27:03 GMT  
		Size: 211.3 MB (211340912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:f157b0d055f01dc5ca477f25813e90ca2e9fc6f91c36802d73d257d6f691df93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26efbf1f35518196d3dd85814acbed3502d1912f8f58cf10f60c5b8c1eb8365a`

```dockerfile
```

-	Layers:
	-	`sha256:3c14b76c91ae367b8e5a2cbead3cf9450cd2805ffe2159945a59c5cc8a0ab896`  
		Last Modified: Tue, 18 Mar 2025 05:26:57 GMT  
		Size: 18.0 KB (18040 bytes)  
		MIME: application/vnd.in-toto+json
