<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.5`](#dart35)
-	[`dart:3.5-sdk`](#dart35-sdk)
-	[`dart:3.5.4`](#dart354)
-	[`dart:3.5.4-sdk`](#dart354-sdk)
-	[`dart:3.6.0-334.3.beta`](#dart360-3343beta)
-	[`dart:3.6.0-334.3.beta-sdk`](#dart360-3343beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
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
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
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
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.5`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.5` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.5-sdk`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.5-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.5.4`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.5.4` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5.4` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5.4` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5.4` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5.4` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5.4` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.5.4-sdk`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.5.4-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5.4-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.5.4-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.5.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6.0-334.3.beta`

```console
$ docker pull dart@sha256:c1ccee418424907a452806bb70b366c01c776c04e1e1bbef1bd0ff6d61ee8aaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6.0-334.3.beta` - linux; amd64

```console
$ docker pull dart@sha256:f3dea11af7197fde7a5ebd3c819f5c925a3a5322cc030222ab836c68b94021ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313017973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dea51a24fbaaae1e0f3e3992f5ea9e0a02717d950cc8b2819f7db1b56a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a12dff24c7c1e153368b11ae120799d6e42e9829416389f52e18a0cd6a98b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 54.9 MB (54905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba69c9a2872567a537db226c706878b04571e5f4be750b3a819ab47ff64a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d231c89557df1bfa479abe883fd21f055dd7ed06f85d42bd062212aaae9f991`  
		Last Modified: Tue, 12 Nov 2024 02:39:14 GMT  
		Size: 227.2 MB (227187287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-334.3.beta` - unknown; unknown

```console
$ docker pull dart@sha256:ad2825732d0564cd2f68bee6364c5e22924e7292b382917f0539927e9ba3725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f02612f6357876164d4af0ce78cfff9959f68c2728a8becad2dcd77fe8e7d4a`

```dockerfile
```

-	Layers:
	-	`sha256:55230a211b499ca64e3b03449d2900f9b32952714f5cdf67565aff7a53cb20c7`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0-334.3.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:94e78a6f9e143cf3876708306b518306994f53b733cd73435609ea6ecafe5320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211194167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba5883ed11f9a3bacb5e738ccb2e1fc0954ae868b7807ce2e17a467a0c9f90f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6586f76f894e31923a8da624a38e50456c7a3171d53144c78048f8f3721b53`  
		Last Modified: Tue, 12 Nov 2024 16:08:31 GMT  
		Size: 135.7 MB (135691747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-334.3.beta` - unknown; unknown

```console
$ docker pull dart@sha256:0020895eadb5e732e4a6b65d3daa74e4628add07db4ee8aabc1d24dee5a9edda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dbf30d6d8c0fcb7fbaa85f9b6db1119157bce2e9330e200dad3f91bab3bdc0`

```dockerfile
```

-	Layers:
	-	`sha256:4e195fc24eefd1e3c1a1926bbe5229a682437235cd80171c7f39f32f0ec98f25`  
		Last Modified: Tue, 12 Nov 2024 16:08:27 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0-334.3.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86dc7be81abb33732792a7dd8bb8aa9eb643199871f3939e5f29296e5c441de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311661236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578a9e832648fa82a1bb5b547f789a49b83c75576b7b73e1c692a01a3d073449`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41075dbe0c552f8c8190f3158065f6e421d6f964452c788ef104b0da777da906`  
		Last Modified: Tue, 12 Nov 2024 11:25:50 GMT  
		Size: 226.3 MB (226343524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-334.3.beta` - unknown; unknown

```console
$ docker pull dart@sha256:c241f0df5694bf7b7e36c7a929aaef16a82f0c7b4b1c24dbbfd2e3ce439a871b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed40ec059cd0a11104875905449c1b2e75e0626e09fce91c141bca35b65ee7f`

```dockerfile
```

-	Layers:
	-	`sha256:d13c8c85bfa0d3c12cb8d2b432ae84f37b33b08e3c97d5b1a48441c19e864812`  
		Last Modified: Tue, 12 Nov 2024 11:25:40 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.6.0-334.3.beta-sdk`

```console
$ docker pull dart@sha256:c1ccee418424907a452806bb70b366c01c776c04e1e1bbef1bd0ff6d61ee8aaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.6.0-334.3.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f3dea11af7197fde7a5ebd3c819f5c925a3a5322cc030222ab836c68b94021ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313017973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dea51a24fbaaae1e0f3e3992f5ea9e0a02717d950cc8b2819f7db1b56a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a12dff24c7c1e153368b11ae120799d6e42e9829416389f52e18a0cd6a98b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 54.9 MB (54905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba69c9a2872567a537db226c706878b04571e5f4be750b3a819ab47ff64a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d231c89557df1bfa479abe883fd21f055dd7ed06f85d42bd062212aaae9f991`  
		Last Modified: Tue, 12 Nov 2024 02:39:14 GMT  
		Size: 227.2 MB (227187287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-334.3.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ad2825732d0564cd2f68bee6364c5e22924e7292b382917f0539927e9ba3725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f02612f6357876164d4af0ce78cfff9959f68c2728a8becad2dcd77fe8e7d4a`

```dockerfile
```

-	Layers:
	-	`sha256:55230a211b499ca64e3b03449d2900f9b32952714f5cdf67565aff7a53cb20c7`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0-334.3.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:94e78a6f9e143cf3876708306b518306994f53b733cd73435609ea6ecafe5320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211194167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba5883ed11f9a3bacb5e738ccb2e1fc0954ae868b7807ce2e17a467a0c9f90f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6586f76f894e31923a8da624a38e50456c7a3171d53144c78048f8f3721b53`  
		Last Modified: Tue, 12 Nov 2024 16:08:31 GMT  
		Size: 135.7 MB (135691747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-334.3.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0020895eadb5e732e4a6b65d3daa74e4628add07db4ee8aabc1d24dee5a9edda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dbf30d6d8c0fcb7fbaa85f9b6db1119157bce2e9330e200dad3f91bab3bdc0`

```dockerfile
```

-	Layers:
	-	`sha256:4e195fc24eefd1e3c1a1926bbe5229a682437235cd80171c7f39f32f0ec98f25`  
		Last Modified: Tue, 12 Nov 2024 16:08:27 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.6.0-334.3.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86dc7be81abb33732792a7dd8bb8aa9eb643199871f3939e5f29296e5c441de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311661236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578a9e832648fa82a1bb5b547f789a49b83c75576b7b73e1c692a01a3d073449`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41075dbe0c552f8c8190f3158065f6e421d6f964452c788ef104b0da777da906`  
		Last Modified: Tue, 12 Nov 2024 11:25:50 GMT  
		Size: 226.3 MB (226343524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.6.0-334.3.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c241f0df5694bf7b7e36c7a929aaef16a82f0c7b4b1c24dbbfd2e3ce439a871b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed40ec059cd0a11104875905449c1b2e75e0626e09fce91c141bca35b65ee7f`

```dockerfile
```

-	Layers:
	-	`sha256:d13c8c85bfa0d3c12cb8d2b432ae84f37b33b08e3c97d5b1a48441c19e864812`  
		Last Modified: Tue, 12 Nov 2024 11:25:40 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:c1ccee418424907a452806bb70b366c01c776c04e1e1bbef1bd0ff6d61ee8aaa
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
$ docker pull dart@sha256:f3dea11af7197fde7a5ebd3c819f5c925a3a5322cc030222ab836c68b94021ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313017973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dea51a24fbaaae1e0f3e3992f5ea9e0a02717d950cc8b2819f7db1b56a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a12dff24c7c1e153368b11ae120799d6e42e9829416389f52e18a0cd6a98b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 54.9 MB (54905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba69c9a2872567a537db226c706878b04571e5f4be750b3a819ab47ff64a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d231c89557df1bfa479abe883fd21f055dd7ed06f85d42bd062212aaae9f991`  
		Last Modified: Tue, 12 Nov 2024 02:39:14 GMT  
		Size: 227.2 MB (227187287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:ad2825732d0564cd2f68bee6364c5e22924e7292b382917f0539927e9ba3725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f02612f6357876164d4af0ce78cfff9959f68c2728a8becad2dcd77fe8e7d4a`

```dockerfile
```

-	Layers:
	-	`sha256:55230a211b499ca64e3b03449d2900f9b32952714f5cdf67565aff7a53cb20c7`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:94e78a6f9e143cf3876708306b518306994f53b733cd73435609ea6ecafe5320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211194167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba5883ed11f9a3bacb5e738ccb2e1fc0954ae868b7807ce2e17a467a0c9f90f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6586f76f894e31923a8da624a38e50456c7a3171d53144c78048f8f3721b53`  
		Last Modified: Tue, 12 Nov 2024 16:08:31 GMT  
		Size: 135.7 MB (135691747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:0020895eadb5e732e4a6b65d3daa74e4628add07db4ee8aabc1d24dee5a9edda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dbf30d6d8c0fcb7fbaa85f9b6db1119157bce2e9330e200dad3f91bab3bdc0`

```dockerfile
```

-	Layers:
	-	`sha256:4e195fc24eefd1e3c1a1926bbe5229a682437235cd80171c7f39f32f0ec98f25`  
		Last Modified: Tue, 12 Nov 2024 16:08:27 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86dc7be81abb33732792a7dd8bb8aa9eb643199871f3939e5f29296e5c441de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311661236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578a9e832648fa82a1bb5b547f789a49b83c75576b7b73e1c692a01a3d073449`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41075dbe0c552f8c8190f3158065f6e421d6f964452c788ef104b0da777da906`  
		Last Modified: Tue, 12 Nov 2024 11:25:50 GMT  
		Size: 226.3 MB (226343524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:c241f0df5694bf7b7e36c7a929aaef16a82f0c7b4b1c24dbbfd2e3ce439a871b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed40ec059cd0a11104875905449c1b2e75e0626e09fce91c141bca35b65ee7f`

```dockerfile
```

-	Layers:
	-	`sha256:d13c8c85bfa0d3c12cb8d2b432ae84f37b33b08e3c97d5b1a48441c19e864812`  
		Last Modified: Tue, 12 Nov 2024 11:25:40 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:c1ccee418424907a452806bb70b366c01c776c04e1e1bbef1bd0ff6d61ee8aaa
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
$ docker pull dart@sha256:f3dea11af7197fde7a5ebd3c819f5c925a3a5322cc030222ab836c68b94021ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313017973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dea51a24fbaaae1e0f3e3992f5ea9e0a02717d950cc8b2819f7db1b56a6e0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410a12dff24c7c1e153368b11ae120799d6e42e9829416389f52e18a0cd6a98b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 54.9 MB (54905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba69c9a2872567a537db226c706878b04571e5f4be750b3a819ab47ff64a9`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 1.8 MB (1796912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d231c89557df1bfa479abe883fd21f055dd7ed06f85d42bd062212aaae9f991`  
		Last Modified: Tue, 12 Nov 2024 02:39:14 GMT  
		Size: 227.2 MB (227187287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ad2825732d0564cd2f68bee6364c5e22924e7292b382917f0539927e9ba3725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f02612f6357876164d4af0ce78cfff9959f68c2728a8becad2dcd77fe8e7d4a`

```dockerfile
```

-	Layers:
	-	`sha256:55230a211b499ca64e3b03449d2900f9b32952714f5cdf67565aff7a53cb20c7`  
		Last Modified: Tue, 12 Nov 2024 02:39:11 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:94e78a6f9e143cf3876708306b518306994f53b733cd73435609ea6ecafe5320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211194167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba5883ed11f9a3bacb5e738ccb2e1fc0954ae868b7807ce2e17a467a0c9f90f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6586f76f894e31923a8da624a38e50456c7a3171d53144c78048f8f3721b53`  
		Last Modified: Tue, 12 Nov 2024 16:08:31 GMT  
		Size: 135.7 MB (135691747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0020895eadb5e732e4a6b65d3daa74e4628add07db4ee8aabc1d24dee5a9edda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dbf30d6d8c0fcb7fbaa85f9b6db1119157bce2e9330e200dad3f91bab3bdc0`

```dockerfile
```

-	Layers:
	-	`sha256:4e195fc24eefd1e3c1a1926bbe5229a682437235cd80171c7f39f32f0ec98f25`  
		Last Modified: Tue, 12 Nov 2024 16:08:27 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:86dc7be81abb33732792a7dd8bb8aa9eb643199871f3939e5f29296e5c441de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311661236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578a9e832648fa82a1bb5b547f789a49b83c75576b7b73e1c692a01a3d073449`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=12d8e0258fbf50cb08fcf79dcb4aeec24c26341c97519ce8de8d48009e9867c4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b0b37a0f05a11890b41e5840d6ed9cfcddafb28ad38481f56a8b423588bd0b40;             SDK_ARCH="arm";;         arm64)             DART_SHA256=1e8e40d5faf45f16067b90f618043a51bf7d8d939f5fe52eb40d0adf9887cf4d;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.6.0-334.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41075dbe0c552f8c8190f3158065f6e421d6f964452c788ef104b0da777da906`  
		Last Modified: Tue, 12 Nov 2024 11:25:50 GMT  
		Size: 226.3 MB (226343524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c241f0df5694bf7b7e36c7a929aaef16a82f0c7b4b1c24dbbfd2e3ce439a871b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed40ec059cd0a11104875905449c1b2e75e0626e09fce91c141bca35b65ee7f`

```dockerfile
```

-	Layers:
	-	`sha256:d13c8c85bfa0d3c12cb8d2b432ae84f37b33b08e3c97d5b1a48441c19e864812`  
		Last Modified: Tue, 12 Nov 2024 11:25:40 GMT  
		Size: 18.0 KB (18043 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
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
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
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
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
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
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:6489a269e878813bf5a8fe66256c1a3e552d3a3c53eef9c1b224e2d8d737ca6d
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
$ docker pull dart@sha256:1f0a26577243364176f8c7fc785c586e72527023a7442d51ca55b44c4316622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303190865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e979f74bc066edacc023528a452dda9df0b83ce69ac12d76e05f5def4d0057`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7270511d35536be9f105b273a5f9ddc8192670a054297a2f8e176683a4d442`  
		Last Modified: Tue, 12 Nov 2024 02:38:51 GMT  
		Size: 54.9 MB (54905578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49923a2bba5c87e4d3eaae2a2b65428bf4ee36736635ccb632fb303e4d0db9ab`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 1.8 MB (1796918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06df19e64459c06fab10a305657457e5fff92d3b8bb1aacb66c65a796d89a8`  
		Last Modified: Tue, 12 Nov 2024 02:38:53 GMT  
		Size: 217.4 MB (217360342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:11e13c1a715102e76b390ae5be68b8ae5949da3134594df2233a0c914b6b38f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35acca8ddb386f256741d2d34d7d570f2c39f44a3666c6e2d7ae96f06479f0cd`

```dockerfile
```

-	Layers:
	-	`sha256:487e9abb444ed306a8f0c111f08bebb4a2646628e4fb24a55a9d172a42e0c760`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e336aee1554670eb0aef18629a08c5f38cb585c9e8827ab653038206d4f84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203576027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7acb47379da6d32d6bef42d9390f29eddfb0f60d502359644c0a14435094f722`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026296b948440807345fd883605a8035045580aed9363aa9e4cdf994b62320ea`  
		Last Modified: Tue, 12 Nov 2024 16:07:31 GMT  
		Size: 49.6 MB (49561808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efbb6e2cf001213dcb354c309335c8db029d50f3ba7dcc1c9047ac5c4d788f`  
		Last Modified: Tue, 12 Nov 2024 16:07:30 GMT  
		Size: 1.2 MB (1221671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743609a4f34fb8a7ab1e13eaa14c04d84c06516ea701c38ffe26baabce869b8`  
		Last Modified: Tue, 12 Nov 2024 16:07:33 GMT  
		Size: 128.1 MB (128073607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7b2e9ebd396ec79647170045358b373d8202b4b62c1d521a0d09373c136d12e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06352ef483fc7cf2fc5fae585fe57fe1963be3019e50a963a7e321b32acd684`

```dockerfile
```

-	Layers:
	-	`sha256:813b3dadc858eda55ab45f22f278dd4ccbdf7a81e9d5dd1ce52db2ccbc3515a7`  
		Last Modified: Tue, 12 Nov 2024 16:07:29 GMT  
		Size: 19.8 KB (19750 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:bc24793951eb3fc64cfabf691e595a0815b2b0377c728e1fce52e5edd74d242d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b856a0a12c690e999a2aae650dc05eca05b068aa343e21f779042fe35fbdd13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 16:13:27 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Oct 2024 16:13:27 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Oct 2024 16:13:27 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 16:13:27 GMT
WORKDIR /root
# Thu, 17 Oct 2024 16:13:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=8d0c5e34f2a9d6b9f5ebf05252ae1703893f6087d547c631b390aef2d0cd6967;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f56d635ae4119f78ed887eaf8fb5e7821405fc10816d8ef42d3a9105c7ffb1f4;             SDK_ARCH="arm";;         arm64)             DART_SHA256=a91d64dd3173349cee58c82f5ebf18bb9670f65eecc26d5684124c3def3f83ec;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.5.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30788698cf66de5527ab11fdf6360cfbc0afaa650a7c6760e0b65aee939b94f`  
		Last Modified: Tue, 12 Nov 2024 11:24:43 GMT  
		Size: 54.7 MB (54672293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e618fc32cc4ac27b04f196b54833b2e942604e13cf31b088c0f7bd901279`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ce1f36765666b3e1463de410930979bef5184d6b2deede6b108fbc86f1ef29`  
		Last Modified: Tue, 12 Nov 2024 11:24:46 GMT  
		Size: 216.5 MB (216517607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fe5db58723d2c1cf926b818da48243e995a9851162b528d6c50e1486a96acf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00921ea8aa4b02ae24416fa7015e910339d31343b6c2f1566e1232765b3c2f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a721b1096de50136f98ef52136e5f8bdab8f59db539808f818a3546bf3b86`  
		Last Modified: Tue, 12 Nov 2024 11:24:41 GMT  
		Size: 19.8 KB (19805 bytes)  
		MIME: application/vnd.in-toto+json
