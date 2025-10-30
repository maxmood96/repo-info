<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10.0-290.4.beta`](#dart3100-2904beta)
-	[`dart:3.10.0-290.4.beta-sdk`](#dart3100-2904beta-sdk)
-	[`dart:3.9`](#dart39)
-	[`dart:3.9-sdk`](#dart39-sdk)
-	[`dart:3.9.4`](#dart394)
-	[`dart:3.9.4-sdk`](#dart394-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:3` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:3-sdk` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-290.4.beta`

**does not exist** (yet?)

## `dart:3.10.0-290.4.beta-sdk`

**does not exist** (yet?)

## `dart:3.9`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:3.9` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9-sdk`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:3.9-sdk` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.4`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:3.9.4` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.9.4-sdk`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:3.9.4-sdk` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.9.4-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.9.4-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:2f3ca2d9b2f5e8cdff963d4346240057429c41154a3f4bc64c937c4c4961ae5d
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
$ docker pull dart@sha256:0af8739f0f090490699c92dab18e6832e63f8aee7c8f961334a4119eae25bdda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287259464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f32f25b1e454510c487cd38eef1143e9b4b296b8dcfa4860699a556c11916e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:25:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 22:25:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 28 Oct 2025 22:25:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 28 Oct 2025 22:25:46 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Oct 2025 22:25:46 GMT
WORKDIR /root
# Tue, 28 Oct 2025 22:25:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5781c0ac40b0f1357e1cfc4164a01d9fbfe1824c489ee268d8808af5d38c53d`  
		Last Modified: Tue, 28 Oct 2025 22:26:36 GMT  
		Size: 42.5 MB (42493503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d344e3845e6145d3bcd057a0f28b94a04bda53029941eb6315d3014f0eed19`  
		Last Modified: Tue, 28 Oct 2025 22:26:33 GMT  
		Size: 1.9 MB (1873623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aef94fde277c060843046ca4d8bdd5041faae464de3b28d7f839c085f64ec`  
		Last Modified: Tue, 28 Oct 2025 23:54:07 GMT  
		Size: 213.1 MB (213114382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:2c42f0e481d8467a3ea2fc1b34b5fc784bf6e21ca10c0a14ecc8f9792c9c4759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64405a621de4b05eabd11c41db005ddb64425c288f2678d6fa1dc72ae4592fa2`

```dockerfile
```

-	Layers:
	-	`sha256:dd8af3d504259b5865fba52115e0d365ea5e99724b8f69e62de4c255dc1603cf`  
		Last Modified: Tue, 28 Oct 2025 23:53:25 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:6529dbbc2fce6376c7d6768e946a093b77ed738d60b0460c9a9c93b6e89db1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219898369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bd55cc3420ddb98ac7a6dac66543b2474a59c61bd83143e548dd8bd7452705`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:25:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 22:25:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 28 Oct 2025 22:25:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 28 Oct 2025 22:25:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Oct 2025 22:25:45 GMT
WORKDIR /root
# Tue, 28 Oct 2025 22:25:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae209e09fa6c360792c585f0387e6c5b0041ba800c61a226f19e07b125ba803`  
		Last Modified: Tue, 28 Oct 2025 22:26:24 GMT  
		Size: 37.5 MB (37498608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d96875a73d98a8d1a434d8f24bf2bbbeed942e24731617fc74e5cba920a6a5`  
		Last Modified: Tue, 28 Oct 2025 22:26:22 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ee01f6e03f5ec6baa2082c5505c86eafd1065aea17da1ed18b3e90c3a22e85`  
		Last Modified: Tue, 28 Oct 2025 23:53:53 GMT  
		Size: 154.9 MB (154911716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:d0e05f4ff0c733a1f7b353b6b1903142f592c921a89fbe9db471f657c57747f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2f29e2b1962ca389527012e2c74d140f3ee7459e0181a8fef88ae36be588a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f9595d633a10830c15d9944ce758e32ca0a78b1296db280f764d155dc4f92fc`  
		Last Modified: Tue, 28 Oct 2025 23:53:27 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5a94146bf98409e23561a248975c88d064f5b720cc4099db2387e5211d06d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286339084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9887d094b4af23b1b792ecaf536485d54f97ce660a4850ea644110c26600053`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:42:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 22:42:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 28 Oct 2025 22:42:44 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 28 Oct 2025 22:42:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Oct 2025 22:42:44 GMT
WORKDIR /root
# Tue, 28 Oct 2025 22:42:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c936ec72e3b42040d7546e2220ef63b18fa3ee4f6e9dfff83338e97d076ca3d8`  
		Last Modified: Tue, 28 Oct 2025 22:43:34 GMT  
		Size: 42.3 MB (42293169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967125d8b8c0ba242421201ee7b493e6e45b40e9e150724a004840f6bed2fed6`  
		Last Modified: Tue, 28 Oct 2025 22:43:33 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1e4a70be59e636b458900e431b58f81cff6b3de1e42ce16f4d2e7eb3ea6cf9`  
		Last Modified: Tue, 28 Oct 2025 22:45:49 GMT  
		Size: 212.3 MB (212337103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:a99f048a1dfb575468d56afceef594b550d7a6328023ebb20bad0e7eecd48f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369dba964e4a033ab5de12121d14caf237d17fcefb39983858a85f3636a6c591`

```dockerfile
```

-	Layers:
	-	`sha256:34f0bd5425cc53f111a8c25d3f0afbb770d392b3195238a90daf8e34d6271897`  
		Last Modified: Tue, 28 Oct 2025 23:53:30 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:05b4c6aae0a3400ee04d484431c490d1afe77bf23b999d4fa55737dd0805470d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232962711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fa70fae02db8c1a7c9beb26aa8444bf951d0918bdf4314fd5fef418cff8855`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 29 Oct 2025 16:10:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Oct 2025 16:10:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 29 Oct 2025 16:10:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 29 Oct 2025 16:10:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Oct 2025 16:10:43 GMT
WORKDIR /root
# Wed, 29 Oct 2025 16:11:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a506f531a9b378b37a57e69ce88af552bafd4f8861debc3cd60759cc0ce24b`  
		Last Modified: Wed, 29 Oct 2025 16:15:46 GMT  
		Size: 41.6 MB (41560624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061570a1fc4dd384af969a49f50fbaa0fdeccf08dfd02e2e5ba2a45039aa23bc`  
		Last Modified: Wed, 29 Oct 2025 16:15:41 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4cdfd96c6e003bf90afc1efa87426ad5e5bc5e5f29044a223762914495bc7`  
		Last Modified: Wed, 29 Oct 2025 17:53:57 GMT  
		Size: 161.6 MB (161559334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:b2a28b6768da7d5db12dd0d4454c8fee4b8753f0dd1fa94aa98283fc68595f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e9724afdeec2f2053bd463a147e902eec2506acd108b13cbef298382c7a634`

```dockerfile
```

-	Layers:
	-	`sha256:da2f1a18510427cb052371790e2df0d2f270b32b723b61166655135fac3d6911`  
		Last Modified: Wed, 29 Oct 2025 17:53:24 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:2f3ca2d9b2f5e8cdff963d4346240057429c41154a3f4bc64c937c4c4961ae5d
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
$ docker pull dart@sha256:0af8739f0f090490699c92dab18e6832e63f8aee7c8f961334a4119eae25bdda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287259464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f32f25b1e454510c487cd38eef1143e9b4b296b8dcfa4860699a556c11916e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:25:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 22:25:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 28 Oct 2025 22:25:46 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 28 Oct 2025 22:25:46 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Oct 2025 22:25:46 GMT
WORKDIR /root
# Tue, 28 Oct 2025 22:25:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5781c0ac40b0f1357e1cfc4164a01d9fbfe1824c489ee268d8808af5d38c53d`  
		Last Modified: Tue, 28 Oct 2025 22:26:36 GMT  
		Size: 42.5 MB (42493503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d344e3845e6145d3bcd057a0f28b94a04bda53029941eb6315d3014f0eed19`  
		Last Modified: Tue, 28 Oct 2025 22:26:33 GMT  
		Size: 1.9 MB (1873623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916aef94fde277c060843046ca4d8bdd5041faae464de3b28d7f839c085f64ec`  
		Last Modified: Tue, 28 Oct 2025 23:54:07 GMT  
		Size: 213.1 MB (213114382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2c42f0e481d8467a3ea2fc1b34b5fc784bf6e21ca10c0a14ecc8f9792c9c4759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64405a621de4b05eabd11c41db005ddb64425c288f2678d6fa1dc72ae4592fa2`

```dockerfile
```

-	Layers:
	-	`sha256:dd8af3d504259b5865fba52115e0d365ea5e99724b8f69e62de4c255dc1603cf`  
		Last Modified: Tue, 28 Oct 2025 23:53:25 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6529dbbc2fce6376c7d6768e946a093b77ed738d60b0460c9a9c93b6e89db1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219898369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bd55cc3420ddb98ac7a6dac66543b2474a59c61bd83143e548dd8bd7452705`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:25:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 22:25:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 28 Oct 2025 22:25:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 28 Oct 2025 22:25:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Oct 2025 22:25:45 GMT
WORKDIR /root
# Tue, 28 Oct 2025 22:25:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae209e09fa6c360792c585f0387e6c5b0041ba800c61a226f19e07b125ba803`  
		Last Modified: Tue, 28 Oct 2025 22:26:24 GMT  
		Size: 37.5 MB (37498608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d96875a73d98a8d1a434d8f24bf2bbbeed942e24731617fc74e5cba920a6a5`  
		Last Modified: Tue, 28 Oct 2025 22:26:22 GMT  
		Size: 1.3 MB (1275119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ee01f6e03f5ec6baa2082c5505c86eafd1065aea17da1ed18b3e90c3a22e85`  
		Last Modified: Tue, 28 Oct 2025 23:53:53 GMT  
		Size: 154.9 MB (154911716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d0e05f4ff0c733a1f7b353b6b1903142f592c921a89fbe9db471f657c57747f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2f29e2b1962ca389527012e2c74d140f3ee7459e0181a8fef88ae36be588a4`

```dockerfile
```

-	Layers:
	-	`sha256:2f9595d633a10830c15d9944ce758e32ca0a78b1296db280f764d155dc4f92fc`  
		Last Modified: Tue, 28 Oct 2025 23:53:27 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:5a94146bf98409e23561a248975c88d064f5b720cc4099db2387e5211d06d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286339084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9887d094b4af23b1b792ecaf536485d54f97ce660a4850ea644110c26600053`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 28 Oct 2025 22:42:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 22:42:44 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 28 Oct 2025 22:42:44 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 28 Oct 2025 22:42:44 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Oct 2025 22:42:44 GMT
WORKDIR /root
# Tue, 28 Oct 2025 22:42:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c936ec72e3b42040d7546e2220ef63b18fa3ee4f6e9dfff83338e97d076ca3d8`  
		Last Modified: Tue, 28 Oct 2025 22:43:34 GMT  
		Size: 42.3 MB (42293169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967125d8b8c0ba242421201ee7b493e6e45b40e9e150724a004840f6bed2fed6`  
		Last Modified: Tue, 28 Oct 2025 22:43:33 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1e4a70be59e636b458900e431b58f81cff6b3de1e42ce16f4d2e7eb3ea6cf9`  
		Last Modified: Tue, 28 Oct 2025 22:45:49 GMT  
		Size: 212.3 MB (212337103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:a99f048a1dfb575468d56afceef594b550d7a6328023ebb20bad0e7eecd48f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369dba964e4a033ab5de12121d14caf237d17fcefb39983858a85f3636a6c591`

```dockerfile
```

-	Layers:
	-	`sha256:34f0bd5425cc53f111a8c25d3f0afbb770d392b3195238a90daf8e34d6271897`  
		Last Modified: Tue, 28 Oct 2025 23:53:30 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:05b4c6aae0a3400ee04d484431c490d1afe77bf23b999d4fa55737dd0805470d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232962711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fa70fae02db8c1a7c9beb26aa8444bf951d0918bdf4314fd5fef418cff8855`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 29 Oct 2025 16:10:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Oct 2025 16:10:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 29 Oct 2025 16:10:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 29 Oct 2025 16:10:43 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Oct 2025 16:10:43 GMT
WORKDIR /root
# Wed, 29 Oct 2025 16:11:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=f34786de7578862d7d8718f1d70c983b90e7ecfaea29599d7826649be7f0efd3;             SDK_ARCH="x64";;         armhf)             DART_SHA256=649d5e6e31f6189ab216214c0f286e6e5eb74c2ed7e0977f9594d9742afdae5e;             SDK_ARCH="arm";;         arm64)             DART_SHA256=868e2f477c4bfc7c894fec2dddd061a4edb12d7b7ac39d2052e83ac9bfce5bf9;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=b411452a247b672e87477f60e82ede0a9207a289fac9e544b6089e2dc29a8f1c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-290.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a506f531a9b378b37a57e69ce88af552bafd4f8861debc3cd60759cc0ce24b`  
		Last Modified: Wed, 29 Oct 2025 16:15:46 GMT  
		Size: 41.6 MB (41560624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061570a1fc4dd384af969a49f50fbaa0fdeccf08dfd02e2e5ba2a45039aa23bc`  
		Last Modified: Wed, 29 Oct 2025 16:15:41 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4cdfd96c6e003bf90afc1efa87426ad5e5bc5e5f29044a223762914495bc7`  
		Last Modified: Wed, 29 Oct 2025 17:53:57 GMT  
		Size: 161.6 MB (161559334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2a28b6768da7d5db12dd0d4454c8fee4b8753f0dd1fa94aa98283fc68595f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e9724afdeec2f2053bd463a147e902eec2506acd108b13cbef298382c7a634`

```dockerfile
```

-	Layers:
	-	`sha256:da2f1a18510427cb052371790e2df0d2f270b32b723b61166655135fac3d6911`  
		Last Modified: Wed, 29 Oct 2025 17:53:24 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:latest` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:sdk` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:stable` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:653505558d4698efd16e14c0cd26413d3d163d4dca95fa1a69805f3f6d276180
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

### `dart:stable-sdk` - linux; amd64

```console
$ docker pull dart@sha256:041a2a2d8b51a7cf54ce8b8056baed05b58f86e42c0ad23d9edf7d6f2e935900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295380156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd830304f7f5b328eebcd252abbd38920c2028ffbdd50e88cc76b115982833c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdeb6101aa34c5f5517b85d8983916329495b9d7a48ab21cddfaf71c5773e93`  
		Last Modified: Tue, 21 Oct 2025 01:44:37 GMT  
		Size: 42.5 MB (42482261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf38e81456ef336d8df2b1018deef84aa7f8d99233a661a32497f246287726da`  
		Last Modified: Tue, 21 Oct 2025 01:44:36 GMT  
		Size: 1.9 MB (1873590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d035b6a727e3f3a5fc1b6d0364b7c617c5d575b36edba70947da21d8869b98`  
		Last Modified: Tue, 21 Oct 2025 08:54:17 GMT  
		Size: 221.2 MB (221246349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:200f91ed227e132b1037c1f3d0a9cd0393db2949aaf0bf323cefdfbf2bd42a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2cfdadac72be0df4ed31ede4b7566b7997f6611ca574e3e1a23d488c1eaf0b`

```dockerfile
```

-	Layers:
	-	`sha256:74a65f4cd1cf3b7f0f521421f93f3eaaabba0abdd9e8342f4fd61d9df47a38c2`  
		Last Modified: Tue, 21 Oct 2025 08:53:23 GMT  
		Size: 20.6 KB (20649 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c7fd4901bf4a5b12b5fb20b456f50a4205b70ef36db559a7213e0491b5be27dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220771571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ccdba16fcca36efc0a0e5ebf5d69bcdab079a85e1fbef8e5239486f463914`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e9925968c4f79c0da7ec16de559b2e2c7f4acda91440ec5b6b549bc0cf914a`  
		Last Modified: Tue, 21 Oct 2025 08:53:40 GMT  
		Size: 37.5 MB (37478452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af730c8c59196b728272a2ae8be14b68c8912f9448d25d1af953a1ea95b1bb3`  
		Last Modified: Tue, 21 Oct 2025 02:51:47 GMT  
		Size: 1.3 MB (1275113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265eeb6ec0990a084e9144c6a8ff3c3ead8320a6b34b0b3f8a92913b10d146ec`  
		Last Modified: Tue, 21 Oct 2025 08:53:48 GMT  
		Size: 155.8 MB (155805080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8317954cc9946d25f336e22198fd6c6f847c81b6bb5ad8453e74b928777bb112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46615811d269db256bd7f9fd5b3985ea7fb4c30fe885b40d7fd97697c7bf0925`

```dockerfile
```

-	Layers:
	-	`sha256:5fb0aef44100b73db59a6e88443bdcd0b9109f75f0ea4c5b8b6813649310d55b`  
		Last Modified: Tue, 21 Oct 2025 08:53:26 GMT  
		Size: 20.8 KB (20803 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:773602927f62ea5efdc1ac755ff0a7dd75f81d897dca51cbacd017578c756aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294673983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae2f21c596788f36acb709cc19eba3c97b726972e1edad9a4405bf0a7482900`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b6a9ae70d6ba17466e6bcbb860bf4bfb34dec69d5edaca49d4fb27466f46b`  
		Last Modified: Tue, 21 Oct 2025 01:49:36 GMT  
		Size: 42.3 MB (42269752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba1c06b7ed648c1bd015f2d6becde752da90d1ea8c84dcdf75ec57e7d42aff`  
		Last Modified: Tue, 21 Oct 2025 01:49:32 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0016541012e067f4b25d52b0dba7a4b74179144b8340acf154e21af7cdd65dc9`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 220.7 MB (220695420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:75b0f59042d3164a1e85fe174a4764ce6b03870c2907e856d47dc5709a058bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a32d22c9ee8b46ea51aa4cc8ec563ad38a258d8a31818f3f80df657c45fa4cd`

```dockerfile
```

-	Layers:
	-	`sha256:be10d217e786c8e8f42bd6468cbf8eb8445c620f7787a2958b71aa6e4a5f3e8d`  
		Last Modified: Tue, 21 Oct 2025 08:53:28 GMT  
		Size: 20.9 KB (20856 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:782aaa891a78b71910165672904b9e3fe158b8163dcc2a922fc15f77bfca9a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232360171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63eda4a3e3578973795edc7f66f903e507e370e67028f4a560bea5cdc6d2167`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 Oct 2025 20:09:49 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 14 Oct 2025 20:09:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 14 Oct 2025 20:09:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 20:09:49 GMT
WORKDIR /root
# Tue, 14 Oct 2025 20:09:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958c5096be531df462c49fbc4cb7bab5d41c2d0aff8fc92382548b907142234`  
		Last Modified: Wed, 22 Oct 2025 18:16:40 GMT  
		Size: 41.6 MB (41553161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa886b4e6fbe4b3e8b90d86ff42f203ba82388dd3833c8084ebf49af4a1d067`  
		Last Modified: Wed, 22 Oct 2025 18:16:37 GMT  
		Size: 1.6 MB (1567075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50651d783b0bd383210185abbf53fca0946f9f122a0f50d833b1ff850663f586`  
		Last Modified: Wed, 22 Oct 2025 20:54:02 GMT  
		Size: 161.0 MB (160964253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:097f61a0fb7dfe67cf61594df8e56c12faa2ee4ee07cb78dcfb2bea8b3df9dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecd394742ffe902326c12248a9724cc9c84691a5c6b5862b113a8e13ae35094`

```dockerfile
```

-	Layers:
	-	`sha256:5e716bb2d9c1b95ba3bfa8be7eb282f99f4ffbe2b3002e19ab881b1d2eccb29b`  
		Last Modified: Wed, 22 Oct 2025 20:53:22 GMT  
		Size: 20.7 KB (20734 bytes)  
		MIME: application/vnd.in-toto+json
