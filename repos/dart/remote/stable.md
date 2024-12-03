## `dart:stable`

```console
$ docker pull dart@sha256:3f3877b9a75a1695dd284151d2dab5787bc6cefd04313b6a8e0bee98230d347b
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
$ docker pull dart@sha256:507c2c93d1ac60c2949fb1d27dcb90931931278c640bb59961eeb6252b6b1899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302100571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e153376b5d065de282ef2d923a69bf9622475d788397b5944f51bf8e248cdf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Nov 2024 19:25:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 13 Nov 2024 19:25:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Nov 2024 19:25:25 GMT
WORKDIR /root
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cdebd16f971ed8d9d9b71733e68a59d9741782e6f256e5370805aec3713d39`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 54.7 MB (54711809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1197438a4f9100eecc69a7fbd5a5b839f1b96bf87d10b7a7030ddd588149f82d`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 1.8 MB (1796916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923d8d91b0e6e210ff527309f9cd1b783f0a6bd188dcb19570d882588a9a5a31`  
		Last Modified: Tue, 03 Dec 2024 02:30:16 GMT  
		Size: 217.4 MB (217360234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:c4b1b990b91b3d2b741f1d3fddc1031f512146399d4715b22fdd7a6183897916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21997906ea9b5afdc53a19141045d669e8cd6546b083a68842d77c64b28ed9d`

```dockerfile
```

-	Layers:
	-	`sha256:d57a02e566eab492b70f789b466187d0a51510f0ce9b97b22746c1eb5dea7ef3`  
		Last Modified: Tue, 03 Dec 2024 02:30:12 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:dc2e2aaad99fcfd4e868933d0e8f0d18f88e31586cdaa529f2adc7aa08506f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202596290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1fce26f4fc2c0ca80655a7c84ee4e5f031b36246fe982211b0430f438805b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Nov 2024 19:25:25 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 13 Nov 2024 19:25:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Nov 2024 19:25:25 GMT
WORKDIR /root
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48ebfccf8612e489a704dcaa37efa83ac6c599e5b1901d51fe9719fa5551d6`  
		Last Modified: Tue, 03 Dec 2024 07:43:22 GMT  
		Size: 49.4 MB (49367322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa56c5371336abad086b100e68ad4b0f7f581ee3779293514a5496c8ef72d16f`  
		Last Modified: Tue, 03 Dec 2024 07:43:20 GMT  
		Size: 1.2 MB (1221676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a8c6722ad097aa48eb5ea6025502607db8805f399faa90897526d5e3f77acd`  
		Last Modified: Tue, 03 Dec 2024 07:43:24 GMT  
		Size: 128.1 MB (128073672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e5dbb755358ba0dcfc9428dddffd196a070424ccffd05cb99afcb156b3dd6d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff10cfbc7945b8d288ff200f5a400966f581aeb5759ad3ca844d5ef8797c54be`

```dockerfile
```

-	Layers:
	-	`sha256:710ff15821f65db2a5f04984ff1fadc1d99271f977172570ec1777e8ba94947a`  
		Last Modified: Tue, 03 Dec 2024 07:43:20 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:41138b3771cb6cb69ebaa18f0c4c8e781bb8751a0b9ebab765f4a15ffe7fd523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300543045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c630722bec02bac3143256632c06a3920d1760beffb002ee6b34b618e6b7cd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 Nov 2024 19:25:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 13 Nov 2024 19:25:25 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 13 Nov 2024 19:25:25 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Nov 2024 19:25:25 GMT
WORKDIR /root
# Wed, 13 Nov 2024 19:25:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e45794817221bd49021987489346cac977817b0783fd67f0ccb1a46ef65baaa`  
		Last Modified: Tue, 03 Dec 2024 05:46:37 GMT  
		Size: 54.5 MB (54478859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91d4c3b279a7e9c8c1be335fb15b0681241f02f4746137c99cc2c52981eba83`  
		Last Modified: Tue, 03 Dec 2024 05:46:35 GMT  
		Size: 1.5 MB (1488032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c695b1284a230492def115def668536a5f7430bce7c2661a30c2c94ca3b9b507`  
		Last Modified: Tue, 03 Dec 2024 05:46:40 GMT  
		Size: 216.5 MB (216517312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:3155b862d3718e735a8417b43fc43058338ce57209d72ed1957277dff92850e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedd522efb6437dcaacdec93234c4f17b0972f5e7f751b39be8906ba6e8d463c`

```dockerfile
```

-	Layers:
	-	`sha256:075ead30da310efd57ba9e962fd18b1c392e9ad28ef372c74fb6091a8e23f89a`  
		Last Modified: Tue, 03 Dec 2024 05:46:35 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
