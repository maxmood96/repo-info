<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.7`](#dart37)
-	[`dart:3.7-sdk`](#dart37-sdk)
-	[`dart:3.7.3`](#dart373)
-	[`dart:3.7.3-sdk`](#dart373-sdk)
-	[`dart:3.8.0-278.2.beta`](#dart380-2782beta)
-	[`dart:3.8.0-278.2.beta-sdk`](#dart380-2782beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
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
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
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
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7` - linux; amd64

```console
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7-sdk`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.3`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.3` - linux; amd64

```console
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.3` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.3` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.3` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.3` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.7.3-sdk`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.7.3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.7.3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.7.3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0-278.2.beta`

```console
$ docker pull dart@sha256:36ff8e8122e785662da594ada68d9dd0ee4c618efe55443bd97e5b1eaeca2130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.0-278.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:755789239f8e0835fcd92aeb540cda0ab03289397ecd31321c92251be9b61734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288117188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a5da5d7ebffdaef0813ed7c622ca29f069fda579665061170fa08b35b56901`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1821e9ec7964abb30bbd28cfb6e2046c54b59b9e3912cc6541ab6d6cc178d141`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754ed7fd1364abf68e23d376fb3b8dd74e40f7cbfd5fe2e1930e9023055e322d`  
		Last Modified: Thu, 17 Apr 2025 18:29:02 GMT  
		Size: 200.9 MB (200868261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-278.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:b7d31f952ca384e084b68bac03cd4a8d94c7f1d88cd656405bd6817aedef4d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca30c9a056d38247b3d1db72316d24a5759073126b8631a965b67b51da8c12e9`

```dockerfile
```

-	Layers:
	-	`sha256:b6a10844e7fe10ad3e608df97dc1373f2c3bde1709559ddb63057e9d78820bd9`  
		Last Modified: Thu, 17 Apr 2025 18:28:55 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-278.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:fcb47073dc94621c6ee4d513866089c33fd9893d25126149f2c1e70da55b3373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216564329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f8af776f699b9124d934d1173111f12cf206f113e253191f482cb27930f8ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c9675305586ea17ae1bd95e07c9e788b32963793efccdf9ab297de4f1d357`  
		Last Modified: Thu, 17 Apr 2025 18:51:27 GMT  
		Size: 139.7 MB (139723555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-278.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:be4678b09c641f67f4b19cd85aad2b186c33406b672afae4bdf7da3e224c687a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47386101b1d0dffefb59ddd5a9a1d9591b880c9dba256c4a7d74d23c2c1c4a21`

```dockerfile
```

-	Layers:
	-	`sha256:54fc3aece1519b5e1abdae77d66a61e8447fd4c981d48dc5aaef1d86811bd383`  
		Last Modified: Thu, 17 Apr 2025 18:51:23 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-278.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f9621984605a97e45161dce06d8ede6a6f8564baf5c6d9c2a62bf9e37d2b5a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286624838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4730ca61f6c14f7dc16632ba527dbb68c06f40bf5405e009546b3982ef83e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e41e5b9170f5ef4469004795bdb5d6c8daf9ce7caec4c0440fa2f8b8a8cf8`  
		Last Modified: Thu, 17 Apr 2025 18:54:16 GMT  
		Size: 200.1 MB (200126516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-278.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:357ebbe44ef68afe36703bef276ae735361ec0f4f6dc95b64fe6016ddbb07534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7f6ec38a3630af168ebe1066bf0afe2303fd4b91a5188282f7b613d5a084bc`

```dockerfile
```

-	Layers:
	-	`sha256:0a820c2eb9f30b9693d721b611121f5e4440f0de136ee144e9010d4e6810fb75`  
		Last Modified: Thu, 17 Apr 2025 18:54:09 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.8.0-278.2.beta-sdk`

```console
$ docker pull dart@sha256:36ff8e8122e785662da594ada68d9dd0ee4c618efe55443bd97e5b1eaeca2130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.8.0-278.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:755789239f8e0835fcd92aeb540cda0ab03289397ecd31321c92251be9b61734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288117188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a5da5d7ebffdaef0813ed7c622ca29f069fda579665061170fa08b35b56901`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1821e9ec7964abb30bbd28cfb6e2046c54b59b9e3912cc6541ab6d6cc178d141`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754ed7fd1364abf68e23d376fb3b8dd74e40f7cbfd5fe2e1930e9023055e322d`  
		Last Modified: Thu, 17 Apr 2025 18:29:02 GMT  
		Size: 200.9 MB (200868261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-278.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b7d31f952ca384e084b68bac03cd4a8d94c7f1d88cd656405bd6817aedef4d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca30c9a056d38247b3d1db72316d24a5759073126b8631a965b67b51da8c12e9`

```dockerfile
```

-	Layers:
	-	`sha256:b6a10844e7fe10ad3e608df97dc1373f2c3bde1709559ddb63057e9d78820bd9`  
		Last Modified: Thu, 17 Apr 2025 18:28:55 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-278.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fcb47073dc94621c6ee4d513866089c33fd9893d25126149f2c1e70da55b3373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216564329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f8af776f699b9124d934d1173111f12cf206f113e253191f482cb27930f8ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c9675305586ea17ae1bd95e07c9e788b32963793efccdf9ab297de4f1d357`  
		Last Modified: Thu, 17 Apr 2025 18:51:27 GMT  
		Size: 139.7 MB (139723555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-278.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:be4678b09c641f67f4b19cd85aad2b186c33406b672afae4bdf7da3e224c687a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47386101b1d0dffefb59ddd5a9a1d9591b880c9dba256c4a7d74d23c2c1c4a21`

```dockerfile
```

-	Layers:
	-	`sha256:54fc3aece1519b5e1abdae77d66a61e8447fd4c981d48dc5aaef1d86811bd383`  
		Last Modified: Thu, 17 Apr 2025 18:51:23 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.8.0-278.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f9621984605a97e45161dce06d8ede6a6f8564baf5c6d9c2a62bf9e37d2b5a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286624838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4730ca61f6c14f7dc16632ba527dbb68c06f40bf5405e009546b3982ef83e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e41e5b9170f5ef4469004795bdb5d6c8daf9ce7caec4c0440fa2f8b8a8cf8`  
		Last Modified: Thu, 17 Apr 2025 18:54:16 GMT  
		Size: 200.1 MB (200126516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.8.0-278.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:357ebbe44ef68afe36703bef276ae735361ec0f4f6dc95b64fe6016ddbb07534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7f6ec38a3630af168ebe1066bf0afe2303fd4b91a5188282f7b613d5a084bc`

```dockerfile
```

-	Layers:
	-	`sha256:0a820c2eb9f30b9693d721b611121f5e4440f0de136ee144e9010d4e6810fb75`  
		Last Modified: Thu, 17 Apr 2025 18:54:09 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:36ff8e8122e785662da594ada68d9dd0ee4c618efe55443bd97e5b1eaeca2130
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
$ docker pull dart@sha256:755789239f8e0835fcd92aeb540cda0ab03289397ecd31321c92251be9b61734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288117188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a5da5d7ebffdaef0813ed7c622ca29f069fda579665061170fa08b35b56901`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1821e9ec7964abb30bbd28cfb6e2046c54b59b9e3912cc6541ab6d6cc178d141`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754ed7fd1364abf68e23d376fb3b8dd74e40f7cbfd5fe2e1930e9023055e322d`  
		Last Modified: Thu, 17 Apr 2025 18:29:02 GMT  
		Size: 200.9 MB (200868261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:b7d31f952ca384e084b68bac03cd4a8d94c7f1d88cd656405bd6817aedef4d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca30c9a056d38247b3d1db72316d24a5759073126b8631a965b67b51da8c12e9`

```dockerfile
```

-	Layers:
	-	`sha256:b6a10844e7fe10ad3e608df97dc1373f2c3bde1709559ddb63057e9d78820bd9`  
		Last Modified: Thu, 17 Apr 2025 18:28:55 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:fcb47073dc94621c6ee4d513866089c33fd9893d25126149f2c1e70da55b3373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216564329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f8af776f699b9124d934d1173111f12cf206f113e253191f482cb27930f8ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c9675305586ea17ae1bd95e07c9e788b32963793efccdf9ab297de4f1d357`  
		Last Modified: Thu, 17 Apr 2025 18:51:27 GMT  
		Size: 139.7 MB (139723555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:be4678b09c641f67f4b19cd85aad2b186c33406b672afae4bdf7da3e224c687a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47386101b1d0dffefb59ddd5a9a1d9591b880c9dba256c4a7d74d23c2c1c4a21`

```dockerfile
```

-	Layers:
	-	`sha256:54fc3aece1519b5e1abdae77d66a61e8447fd4c981d48dc5aaef1d86811bd383`  
		Last Modified: Thu, 17 Apr 2025 18:51:23 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f9621984605a97e45161dce06d8ede6a6f8564baf5c6d9c2a62bf9e37d2b5a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286624838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4730ca61f6c14f7dc16632ba527dbb68c06f40bf5405e009546b3982ef83e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e41e5b9170f5ef4469004795bdb5d6c8daf9ce7caec4c0440fa2f8b8a8cf8`  
		Last Modified: Thu, 17 Apr 2025 18:54:16 GMT  
		Size: 200.1 MB (200126516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:357ebbe44ef68afe36703bef276ae735361ec0f4f6dc95b64fe6016ddbb07534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7f6ec38a3630af168ebe1066bf0afe2303fd4b91a5188282f7b613d5a084bc`

```dockerfile
```

-	Layers:
	-	`sha256:0a820c2eb9f30b9693d721b611121f5e4440f0de136ee144e9010d4e6810fb75`  
		Last Modified: Thu, 17 Apr 2025 18:54:09 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:36ff8e8122e785662da594ada68d9dd0ee4c618efe55443bd97e5b1eaeca2130
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
$ docker pull dart@sha256:755789239f8e0835fcd92aeb540cda0ab03289397ecd31321c92251be9b61734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288117188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a5da5d7ebffdaef0813ed7c622ca29f069fda579665061170fa08b35b56901`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1821e9ec7964abb30bbd28cfb6e2046c54b59b9e3912cc6541ab6d6cc178d141`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754ed7fd1364abf68e23d376fb3b8dd74e40f7cbfd5fe2e1930e9023055e322d`  
		Last Modified: Thu, 17 Apr 2025 18:29:02 GMT  
		Size: 200.9 MB (200868261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b7d31f952ca384e084b68bac03cd4a8d94c7f1d88cd656405bd6817aedef4d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca30c9a056d38247b3d1db72316d24a5759073126b8631a965b67b51da8c12e9`

```dockerfile
```

-	Layers:
	-	`sha256:b6a10844e7fe10ad3e608df97dc1373f2c3bde1709559ddb63057e9d78820bd9`  
		Last Modified: Thu, 17 Apr 2025 18:28:55 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fcb47073dc94621c6ee4d513866089c33fd9893d25126149f2c1e70da55b3373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 MB (216564329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f8af776f699b9124d934d1173111f12cf206f113e253191f482cb27930f8ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c9675305586ea17ae1bd95e07c9e788b32963793efccdf9ab297de4f1d357`  
		Last Modified: Thu, 17 Apr 2025 18:51:27 GMT  
		Size: 139.7 MB (139723555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:be4678b09c641f67f4b19cd85aad2b186c33406b672afae4bdf7da3e224c687a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47386101b1d0dffefb59ddd5a9a1d9591b880c9dba256c4a7d74d23c2c1c4a21`

```dockerfile
```

-	Layers:
	-	`sha256:54fc3aece1519b5e1abdae77d66a61e8447fd4c981d48dc5aaef1d86811bd383`  
		Last Modified: Thu, 17 Apr 2025 18:51:23 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:f9621984605a97e45161dce06d8ede6a6f8564baf5c6d9c2a62bf9e37d2b5a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286624838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4730ca61f6c14f7dc16632ba527dbb68c06f40bf5405e009546b3982ef83e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6f53574f123efcf43659030f18038f460fa976ed1b12e66bffa991f7d5ad87c3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=6456bfdd97f3c0ea76890aa0847fb1ea90c5a95551481db7f1bc98fcefde9368;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9576dcf1595514b434b65620d7dae86df1813e2be084c176233031e0848cdc69;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-278.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e41e5b9170f5ef4469004795bdb5d6c8daf9ce7caec4c0440fa2f8b8a8cf8`  
		Last Modified: Thu, 17 Apr 2025 18:54:16 GMT  
		Size: 200.1 MB (200126516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:357ebbe44ef68afe36703bef276ae735361ec0f4f6dc95b64fe6016ddbb07534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7f6ec38a3630af168ebe1066bf0afe2303fd4b91a5188282f7b613d5a084bc`

```dockerfile
```

-	Layers:
	-	`sha256:0a820c2eb9f30b9693d721b611121f5e4440f0de136ee144e9010d4e6810fb75`  
		Last Modified: Thu, 17 Apr 2025 18:54:09 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
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
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
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
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
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
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:52497b20476fd84cb9f0d63a008b306d75f56f44e54431e510b8cf0e4cc4534a
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
$ docker pull dart@sha256:f4a6c9309e31c102d735d7140ba018251ae127a865ce7b1e1e0431c86f691547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307713248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5d03087f1b50d27487cff7f629021eec8691a0613e9fde3404696b09be59b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fd3330382be9a8c5dfcd8819f5fe3ff52cd09b49ac87b5df73a9e79be6e2b3`  
		Last Modified: Thu, 17 Apr 2025 18:28:58 GMT  
		Size: 57.2 MB (57236170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac76fda0f1251d90abf3cfb001c78c5fa3c9beaa15f508ed7a060d64958689ae`  
		Last Modified: Thu, 17 Apr 2025 18:28:56 GMT  
		Size: 1.8 MB (1785448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ed721d73a924eb4278d70355aba60ea198e58a08954fb2506921d1accd30d`  
		Last Modified: Thu, 17 Apr 2025 18:29:01 GMT  
		Size: 220.5 MB (220464339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70f1163a6c3d697a08f081ab5ab912f0bd54ca2706c61e0807e09b11d4b57271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4d714f0cfa96f103df0cffefa0bcdaa4bc350ccbad9d8c7353d13b9c6f1b26`

```dockerfile
```

-	Layers:
	-	`sha256:2cc886a55857e76eeac8aa86c34be7baec3e9240a1c3b3f49f61c34cb75dbdcc`  
		Last Modified: Thu, 17 Apr 2025 18:28:57 GMT  
		Size: 19.6 KB (19600 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:fa5f01498124bfc93a26439dcf18337f8c39eabe33c81a65754c687e0b3042fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228435602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ed14046d61d7c42e7587c103375c0f48ecf86dd214519144ea99799fae8107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330b2381da106ae28676390c114d27603e3d27780aa9cf44a256c87c17d3f73`  
		Last Modified: Thu, 17 Apr 2025 18:50:34 GMT  
		Size: 51.7 MB (51680929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa2189d0ec2c0aa10e7cd73369cd1a292f801f44dae53b2dca0bfc1de42f32b`  
		Last Modified: Thu, 17 Apr 2025 18:50:33 GMT  
		Size: 1.2 MB (1221946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7f0fbeee15e07c6f2dbd37cc4288a12b1ffeec74ae9f0db7559cc82f3cb070`  
		Last Modified: Thu, 17 Apr 2025 18:50:37 GMT  
		Size: 151.6 MB (151594828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c1705a576066009b8acd8340f301e35c3586a5e494d4c97a95f4210fa520dd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 KB (19749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed8a1f7a28dd3dc02b86835f8a5e30ec682670bb62ce8239c953083d86e9410`

```dockerfile
```

-	Layers:
	-	`sha256:80b02523c75524fd9b92278f18632f57254f9409b1c39c6b0b4f490e0b5774e9`  
		Last Modified: Thu, 17 Apr 2025 18:50:32 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:812b98b726872dae8c1483ee265b1f19f228e5131842579df2b43db9716f3eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306124161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26529ee0f584c548a4440d406943549cf4f55633d617fc010c40e6a0729a162a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 17 Apr 2025 07:27:52 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 17 Apr 2025 07:27:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Apr 2025 07:27:52 GMT
WORKDIR /root
# Thu, 17 Apr 2025 07:27:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b772a2807d2fcf08b4edcff998123b0e87391c12067ad0cf11f7c50ca31982b2;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c518909142c6c3110ff8818445d2359103deb20d9136188c8ca3529403b84a4d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=16546f4cd27fca883eee7f1e7597f409a67e0254174443aff6f62c35c9ff78ad;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.7.3/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121cece50d49eba8634dea84f9d28d9736feef46609fad36256ab2fc13bda939`  
		Last Modified: Thu, 17 Apr 2025 18:53:22 GMT  
		Size: 56.9 MB (56943757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d5a6d2921a02dc94eeacce2d2369f9b7aec957f761943a2539a79879077d8c`  
		Last Modified: Thu, 17 Apr 2025 18:53:21 GMT  
		Size: 1.5 MB (1488213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57fd26eb5fbcba6aa861a9c32d3c013a73bc5c4a741a57e8904c3a4bcc1377`  
		Last Modified: Thu, 17 Apr 2025 18:53:26 GMT  
		Size: 219.6 MB (219625839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b03379937fb175ee272b89dc853a9e0e5c221c70bd147b1457ead9780f6faf95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 KB (19806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd1c1576f94fd71f3ecb9e55edba76a3be147801166cc600dfac85031eb987`

```dockerfile
```

-	Layers:
	-	`sha256:e246be64a680f145b32cef04396c800732646b703a40b6cf9f0f4199530d9579`  
		Last Modified: Thu, 17 Apr 2025 18:53:20 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json
