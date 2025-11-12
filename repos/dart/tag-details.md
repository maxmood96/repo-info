<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10`](#dart310)
-	[`dart:3.10-sdk`](#dart310-sdk)
-	[`dart:3.10.0`](#dart3100)
-	[`dart:3.10.0-sdk`](#dart3100-sdk)
-	[`dart:3.11.0-93.2.beta`](#dart3110-932beta)
-	[`dart:3.11.0-93.2.beta-sdk`](#dart3110-932beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:9e72ff17956a600cc028732f040a5e51f7910840fa4679cb4261a065b1a65f9d
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
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:9e46a406614705bd3d47c1be1afe629fdb4c87d4fa923ab33e07ddf4bc7fe117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08fa7f7d62fa729c627cfe94bc12fc0e11f92d7d1fbae438c9a829d96aeb04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 12:06:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 12:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 12:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 12:06:29 GMT
WORKDIR /root
# Thu, 06 Nov 2025 07:41:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec87d9e6fe2a6c3d564b97ec749845500d1eb36d011fa27e67400daca20cad51`  
		Last Modified: Wed, 05 Nov 2025 12:15:22 GMT  
		Size: 41.6 MB (41560904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12241236d8e9213dd7db34ee23bd2fa4fe14911c837e542a2a0765c13d09ee31`  
		Last Modified: Wed, 05 Nov 2025 12:15:19 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81373d5bf99f9327fc756e8b4595aa20a086584c9af210bcc6545d96488afe68`  
		Last Modified: Thu, 06 Nov 2025 09:53:50 GMT  
		Size: 161.0 MB (160964291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:2a1530fc9402398181623e1f0f3ba717dceff941e28759bdbc1ee786dba0d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d229c0a98fa31d37805411d1f4fd045710e182c07fe507b550d0d10620c9d1de`

```dockerfile
```

-	Layers:
	-	`sha256:db9d4c9c047e25be7ac912026f41b0e7c2f7fabc4cac0d08d52c7c3c6a28827f`  
		Last Modified: Thu, 06 Nov 2025 09:53:22 GMT  
		Size: 20.7 KB (20689 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:9e72ff17956a600cc028732f040a5e51f7910840fa4679cb4261a065b1a65f9d
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
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:9e46a406614705bd3d47c1be1afe629fdb4c87d4fa923ab33e07ddf4bc7fe117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08fa7f7d62fa729c627cfe94bc12fc0e11f92d7d1fbae438c9a829d96aeb04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 12:06:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 12:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 12:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 12:06:29 GMT
WORKDIR /root
# Thu, 06 Nov 2025 07:41:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec87d9e6fe2a6c3d564b97ec749845500d1eb36d011fa27e67400daca20cad51`  
		Last Modified: Wed, 05 Nov 2025 12:15:22 GMT  
		Size: 41.6 MB (41560904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12241236d8e9213dd7db34ee23bd2fa4fe14911c837e542a2a0765c13d09ee31`  
		Last Modified: Wed, 05 Nov 2025 12:15:19 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81373d5bf99f9327fc756e8b4595aa20a086584c9af210bcc6545d96488afe68`  
		Last Modified: Thu, 06 Nov 2025 09:53:50 GMT  
		Size: 161.0 MB (160964291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2a1530fc9402398181623e1f0f3ba717dceff941e28759bdbc1ee786dba0d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d229c0a98fa31d37805411d1f4fd045710e182c07fe507b550d0d10620c9d1de`

```dockerfile
```

-	Layers:
	-	`sha256:db9d4c9c047e25be7ac912026f41b0e7c2f7fabc4cac0d08d52c7c3c6a28827f`  
		Last Modified: Thu, 06 Nov 2025 09:53:22 GMT  
		Size: 20.7 KB (20689 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10`

```console
$ docker pull dart@sha256:2b4ac3974f4315f107d0a19a2aafbcb6f03bb1b577e8472ee82f198e2263cb73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `dart:3.10` - linux; amd64

```console
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10-sdk`

```console
$ docker pull dart@sha256:2b4ac3974f4315f107d0a19a2aafbcb6f03bb1b577e8472ee82f198e2263cb73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `dart:3.10-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0`

```console
$ docker pull dart@sha256:2b4ac3974f4315f107d0a19a2aafbcb6f03bb1b577e8472ee82f198e2263cb73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `dart:3.10.0` - linux; amd64

```console
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.0-sdk`

```console
$ docker pull dart@sha256:2b4ac3974f4315f107d0a19a2aafbcb6f03bb1b577e8472ee82f198e2263cb73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown

### `dart:3.10.0-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10.0-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10.0-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-93.2.beta`

```console
$ docker pull dart@sha256:6a431a6e21ab5314345d608bfe7b41408821bebadb774d65516ece61ef773b2f
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

### `dart:3.11.0-93.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:33d0ca1bc0880f023f75c69a86a9d1c81b13881ac6a763393588cb936a979163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288384401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a924e0b9c4cad527b5acd6cb90fda46b95f9bdf65cd06ed8ed16f06e74930e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:14 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:14 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae19ab0b2391e3242ed12efa17c83d8ac6c48802e6a8c1f632d7143b5721b3`  
		Last Modified: Tue, 11 Nov 2025 22:16:09 GMT  
		Size: 42.5 MB (42493487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6d9e659e528761eca391ab6142adad2bea9035ea701227cea6c0d69cfc7230`  
		Last Modified: Tue, 11 Nov 2025 22:16:07 GMT  
		Size: 1.9 MB (1873619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b24e8d4912cd087463372e7fc9754faedbb79c4077960d5bc44bb4e243893cf`  
		Last Modified: Wed, 12 Nov 2025 00:54:48 GMT  
		Size: 214.2 MB (214239159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:4887ef98ebb6c16cd74270bb39bfbd3b08374163da0c625c8732e8897df11ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e846850968c870af509c4c4659b2834bf01da7640b9ec2f98e938723ae568c`

```dockerfile
```

-	Layers:
	-	`sha256:734da6fb45bc4347c1442ec4765b9a810523cfc0f06d9b09bee95a5aecda06f5`  
		Last Modified: Wed, 12 Nov 2025 00:53:26 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:eb532338a2caa8666446075930a5afb7575e03232e9e7f3dd24a2e619aa10ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220617534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e24ad689f22fb55c4e907bdc54494d2cf8918a22943989549ef3257611cf38d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:28 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8a0e3673d3f3dd91177a058ce7a80d8c11656917a9723053456c0ea1daaf91`  
		Last Modified: Tue, 11 Nov 2025 22:16:14 GMT  
		Size: 37.5 MB (37498739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28c299936895e6e7c678360d65ddf9bcc10d991bf9d5ac38acba1bf0633f366`  
		Last Modified: Tue, 11 Nov 2025 22:16:13 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d391fc01102844a7f6ac7c68c3b6cdfa8b75c5d885bf34221925d1e59c20d98`  
		Last Modified: Wed, 12 Nov 2025 09:57:58 GMT  
		Size: 155.6 MB (155630604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:c69a37e1315d5cbc986a26ea182473dc93e571216e0dde5a9eca1baffd14e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316a76cbae0bbff8a04a4c13df598035674a3c4a19aa43ac85c0c877f0e775d0`

```dockerfile
```

-	Layers:
	-	`sha256:878d79baeb2edea66f080d0ae62ae9864a42908b3ac5a63f4d73edf2d9529563`  
		Last Modified: Wed, 12 Nov 2025 00:53:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c588906dd1bfa1d1f5c23c0e5ba61196c87cb3444e3580489fe12542caef0f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287460575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d1cc0f662d9e99097c9082442ba1c871409475d9339c256105664ead2afe0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:14 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:14 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029f67d0772e2784f3a9ce97116fa13626753db2df6a764af45aabfac06935c`  
		Last Modified: Tue, 11 Nov 2025 22:16:16 GMT  
		Size: 42.3 MB (42292501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6cb4c90d5106963daf20bdea42e32fa5212942072bcd78921bc494a71597fd`  
		Last Modified: Tue, 11 Nov 2025 22:16:14 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d3566d67a811fffeabc9cb48ecd0ad8fb6dbd599c8f7c2c052b2c80468cc06`  
		Last Modified: Wed, 12 Nov 2025 00:54:18 GMT  
		Size: 213.5 MB (213459092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:2d3b3e76744d794ea46b6286481ca3cfc4bbefe339a98e190e4827e92fce6454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0085728b81c3ea8f83182e0c7402225e75cf60b06e6cc0a7694fb94daee4127b`

```dockerfile
```

-	Layers:
	-	`sha256:12c066a294761cc4ffa0ae3ad115944c49d52e9d6e79ab66dffbb275fb5a29f8`  
		Last Modified: Wed, 12 Nov 2025 00:53:33 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta` - linux; riscv64

```console
$ docker pull dart@sha256:7c11f0bfea444c2db3fe3e41b543ebaa631b93f4243c16b3203b38067894fd02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233894084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1454d64d0067d809d3c414bd0ffa5912e9ab0bce08897581102f42f7ace52e6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:16:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:16:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:16:04 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:16:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c197f3fb63a08d839b0be1ce3d42db3af7f54f27346b95f111b82b21cc267fa8`  
		Last Modified: Tue, 11 Nov 2025 22:21:21 GMT  
		Size: 41.6 MB (41560559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bf767ca6af272d9eb378bc7d2f7a727579f404cc0d6158b26873863458f082`  
		Last Modified: Tue, 11 Nov 2025 22:21:09 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7cc814bd47aaf1e0dea94600169b3e15079b07a4f0205613785de0d3536cba`  
		Last Modified: Wed, 12 Nov 2025 00:54:13 GMT  
		Size: 162.5 MB (162490635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:230a706ab7179ce03490b0532cb65f3d8c64ce391ade3058f64249d507cf80ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0019f5ad603db58065c81ebc4d233ab6c2f380da38a967a60e20fba3972868a8`

```dockerfile
```

-	Layers:
	-	`sha256:0c5d6c11ae9d41d20cc5b5b8efd6bd400229ffe9acb1047c039d218bc04b5c2f`  
		Last Modified: Wed, 12 Nov 2025 00:53:36 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-93.2.beta-sdk`

```console
$ docker pull dart@sha256:6a431a6e21ab5314345d608bfe7b41408821bebadb774d65516ece61ef773b2f
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

### `dart:3.11.0-93.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:33d0ca1bc0880f023f75c69a86a9d1c81b13881ac6a763393588cb936a979163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288384401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a924e0b9c4cad527b5acd6cb90fda46b95f9bdf65cd06ed8ed16f06e74930e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:14 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:14 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae19ab0b2391e3242ed12efa17c83d8ac6c48802e6a8c1f632d7143b5721b3`  
		Last Modified: Tue, 11 Nov 2025 22:16:09 GMT  
		Size: 42.5 MB (42493487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6d9e659e528761eca391ab6142adad2bea9035ea701227cea6c0d69cfc7230`  
		Last Modified: Tue, 11 Nov 2025 22:16:07 GMT  
		Size: 1.9 MB (1873619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b24e8d4912cd087463372e7fc9754faedbb79c4077960d5bc44bb4e243893cf`  
		Last Modified: Wed, 12 Nov 2025 00:54:48 GMT  
		Size: 214.2 MB (214239159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4887ef98ebb6c16cd74270bb39bfbd3b08374163da0c625c8732e8897df11ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e846850968c870af509c4c4659b2834bf01da7640b9ec2f98e938723ae568c`

```dockerfile
```

-	Layers:
	-	`sha256:734da6fb45bc4347c1442ec4765b9a810523cfc0f06d9b09bee95a5aecda06f5`  
		Last Modified: Wed, 12 Nov 2025 00:53:26 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:eb532338a2caa8666446075930a5afb7575e03232e9e7f3dd24a2e619aa10ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220617534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e24ad689f22fb55c4e907bdc54494d2cf8918a22943989549ef3257611cf38d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:28 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8a0e3673d3f3dd91177a058ce7a80d8c11656917a9723053456c0ea1daaf91`  
		Last Modified: Tue, 11 Nov 2025 22:16:14 GMT  
		Size: 37.5 MB (37498739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28c299936895e6e7c678360d65ddf9bcc10d991bf9d5ac38acba1bf0633f366`  
		Last Modified: Tue, 11 Nov 2025 22:16:13 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d391fc01102844a7f6ac7c68c3b6cdfa8b75c5d885bf34221925d1e59c20d98`  
		Last Modified: Wed, 12 Nov 2025 09:57:58 GMT  
		Size: 155.6 MB (155630604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c69a37e1315d5cbc986a26ea182473dc93e571216e0dde5a9eca1baffd14e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316a76cbae0bbff8a04a4c13df598035674a3c4a19aa43ac85c0c877f0e775d0`

```dockerfile
```

-	Layers:
	-	`sha256:878d79baeb2edea66f080d0ae62ae9864a42908b3ac5a63f4d73edf2d9529563`  
		Last Modified: Wed, 12 Nov 2025 00:53:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c588906dd1bfa1d1f5c23c0e5ba61196c87cb3444e3580489fe12542caef0f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287460575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d1cc0f662d9e99097c9082442ba1c871409475d9339c256105664ead2afe0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:14 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:14 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029f67d0772e2784f3a9ce97116fa13626753db2df6a764af45aabfac06935c`  
		Last Modified: Tue, 11 Nov 2025 22:16:16 GMT  
		Size: 42.3 MB (42292501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6cb4c90d5106963daf20bdea42e32fa5212942072bcd78921bc494a71597fd`  
		Last Modified: Tue, 11 Nov 2025 22:16:14 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d3566d67a811fffeabc9cb48ecd0ad8fb6dbd599c8f7c2c052b2c80468cc06`  
		Last Modified: Wed, 12 Nov 2025 00:54:18 GMT  
		Size: 213.5 MB (213459092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2d3b3e76744d794ea46b6286481ca3cfc4bbefe339a98e190e4827e92fce6454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0085728b81c3ea8f83182e0c7402225e75cf60b06e6cc0a7694fb94daee4127b`

```dockerfile
```

-	Layers:
	-	`sha256:12c066a294761cc4ffa0ae3ad115944c49d52e9d6e79ab66dffbb275fb5a29f8`  
		Last Modified: Wed, 12 Nov 2025 00:53:33 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:7c11f0bfea444c2db3fe3e41b543ebaa631b93f4243c16b3203b38067894fd02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233894084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1454d64d0067d809d3c414bd0ffa5912e9ab0bce08897581102f42f7ace52e6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:16:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:16:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:16:04 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:16:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c197f3fb63a08d839b0be1ce3d42db3af7f54f27346b95f111b82b21cc267fa8`  
		Last Modified: Tue, 11 Nov 2025 22:21:21 GMT  
		Size: 41.6 MB (41560559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bf767ca6af272d9eb378bc7d2f7a727579f404cc0d6158b26873863458f082`  
		Last Modified: Tue, 11 Nov 2025 22:21:09 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7cc814bd47aaf1e0dea94600169b3e15079b07a4f0205613785de0d3536cba`  
		Last Modified: Wed, 12 Nov 2025 00:54:13 GMT  
		Size: 162.5 MB (162490635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:230a706ab7179ce03490b0532cb65f3d8c64ce391ade3058f64249d507cf80ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0019f5ad603db58065c81ebc4d233ab6c2f380da38a967a60e20fba3972868a8`

```dockerfile
```

-	Layers:
	-	`sha256:0c5d6c11ae9d41d20cc5b5b8efd6bd400229ffe9acb1047c039d218bc04b5c2f`  
		Last Modified: Wed, 12 Nov 2025 00:53:36 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:6a431a6e21ab5314345d608bfe7b41408821bebadb774d65516ece61ef773b2f
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
$ docker pull dart@sha256:33d0ca1bc0880f023f75c69a86a9d1c81b13881ac6a763393588cb936a979163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288384401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a924e0b9c4cad527b5acd6cb90fda46b95f9bdf65cd06ed8ed16f06e74930e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:14 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:14 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae19ab0b2391e3242ed12efa17c83d8ac6c48802e6a8c1f632d7143b5721b3`  
		Last Modified: Tue, 11 Nov 2025 22:16:09 GMT  
		Size: 42.5 MB (42493487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6d9e659e528761eca391ab6142adad2bea9035ea701227cea6c0d69cfc7230`  
		Last Modified: Tue, 11 Nov 2025 22:16:07 GMT  
		Size: 1.9 MB (1873619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b24e8d4912cd087463372e7fc9754faedbb79c4077960d5bc44bb4e243893cf`  
		Last Modified: Wed, 12 Nov 2025 00:54:48 GMT  
		Size: 214.2 MB (214239159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:4887ef98ebb6c16cd74270bb39bfbd3b08374163da0c625c8732e8897df11ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e846850968c870af509c4c4659b2834bf01da7640b9ec2f98e938723ae568c`

```dockerfile
```

-	Layers:
	-	`sha256:734da6fb45bc4347c1442ec4765b9a810523cfc0f06d9b09bee95a5aecda06f5`  
		Last Modified: Wed, 12 Nov 2025 00:53:26 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:eb532338a2caa8666446075930a5afb7575e03232e9e7f3dd24a2e619aa10ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220617534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e24ad689f22fb55c4e907bdc54494d2cf8918a22943989549ef3257611cf38d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:28 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8a0e3673d3f3dd91177a058ce7a80d8c11656917a9723053456c0ea1daaf91`  
		Last Modified: Tue, 11 Nov 2025 22:16:14 GMT  
		Size: 37.5 MB (37498739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28c299936895e6e7c678360d65ddf9bcc10d991bf9d5ac38acba1bf0633f366`  
		Last Modified: Tue, 11 Nov 2025 22:16:13 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d391fc01102844a7f6ac7c68c3b6cdfa8b75c5d885bf34221925d1e59c20d98`  
		Last Modified: Wed, 12 Nov 2025 09:57:58 GMT  
		Size: 155.6 MB (155630604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:c69a37e1315d5cbc986a26ea182473dc93e571216e0dde5a9eca1baffd14e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316a76cbae0bbff8a04a4c13df598035674a3c4a19aa43ac85c0c877f0e775d0`

```dockerfile
```

-	Layers:
	-	`sha256:878d79baeb2edea66f080d0ae62ae9864a42908b3ac5a63f4d73edf2d9529563`  
		Last Modified: Wed, 12 Nov 2025 00:53:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c588906dd1bfa1d1f5c23c0e5ba61196c87cb3444e3580489fe12542caef0f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287460575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d1cc0f662d9e99097c9082442ba1c871409475d9339c256105664ead2afe0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:14 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:14 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029f67d0772e2784f3a9ce97116fa13626753db2df6a764af45aabfac06935c`  
		Last Modified: Tue, 11 Nov 2025 22:16:16 GMT  
		Size: 42.3 MB (42292501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6cb4c90d5106963daf20bdea42e32fa5212942072bcd78921bc494a71597fd`  
		Last Modified: Tue, 11 Nov 2025 22:16:14 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d3566d67a811fffeabc9cb48ecd0ad8fb6dbd599c8f7c2c052b2c80468cc06`  
		Last Modified: Wed, 12 Nov 2025 00:54:18 GMT  
		Size: 213.5 MB (213459092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:2d3b3e76744d794ea46b6286481ca3cfc4bbefe339a98e190e4827e92fce6454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0085728b81c3ea8f83182e0c7402225e75cf60b06e6cc0a7694fb94daee4127b`

```dockerfile
```

-	Layers:
	-	`sha256:12c066a294761cc4ffa0ae3ad115944c49d52e9d6e79ab66dffbb275fb5a29f8`  
		Last Modified: Wed, 12 Nov 2025 00:53:33 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:7c11f0bfea444c2db3fe3e41b543ebaa631b93f4243c16b3203b38067894fd02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233894084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1454d64d0067d809d3c414bd0ffa5912e9ab0bce08897581102f42f7ace52e6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:16:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:16:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:16:04 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:16:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c197f3fb63a08d839b0be1ce3d42db3af7f54f27346b95f111b82b21cc267fa8`  
		Last Modified: Tue, 11 Nov 2025 22:21:21 GMT  
		Size: 41.6 MB (41560559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bf767ca6af272d9eb378bc7d2f7a727579f404cc0d6158b26873863458f082`  
		Last Modified: Tue, 11 Nov 2025 22:21:09 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7cc814bd47aaf1e0dea94600169b3e15079b07a4f0205613785de0d3536cba`  
		Last Modified: Wed, 12 Nov 2025 00:54:13 GMT  
		Size: 162.5 MB (162490635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:230a706ab7179ce03490b0532cb65f3d8c64ce391ade3058f64249d507cf80ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0019f5ad603db58065c81ebc4d233ab6c2f380da38a967a60e20fba3972868a8`

```dockerfile
```

-	Layers:
	-	`sha256:0c5d6c11ae9d41d20cc5b5b8efd6bd400229ffe9acb1047c039d218bc04b5c2f`  
		Last Modified: Wed, 12 Nov 2025 00:53:36 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:6a431a6e21ab5314345d608bfe7b41408821bebadb774d65516ece61ef773b2f
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
$ docker pull dart@sha256:33d0ca1bc0880f023f75c69a86a9d1c81b13881ac6a763393588cb936a979163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288384401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a924e0b9c4cad527b5acd6cb90fda46b95f9bdf65cd06ed8ed16f06e74930e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:14 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:14 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae19ab0b2391e3242ed12efa17c83d8ac6c48802e6a8c1f632d7143b5721b3`  
		Last Modified: Tue, 11 Nov 2025 22:16:09 GMT  
		Size: 42.5 MB (42493487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6d9e659e528761eca391ab6142adad2bea9035ea701227cea6c0d69cfc7230`  
		Last Modified: Tue, 11 Nov 2025 22:16:07 GMT  
		Size: 1.9 MB (1873619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b24e8d4912cd087463372e7fc9754faedbb79c4077960d5bc44bb4e243893cf`  
		Last Modified: Wed, 12 Nov 2025 00:54:48 GMT  
		Size: 214.2 MB (214239159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4887ef98ebb6c16cd74270bb39bfbd3b08374163da0c625c8732e8897df11ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e846850968c870af509c4c4659b2834bf01da7640b9ec2f98e938723ae568c`

```dockerfile
```

-	Layers:
	-	`sha256:734da6fb45bc4347c1442ec4765b9a810523cfc0f06d9b09bee95a5aecda06f5`  
		Last Modified: Wed, 12 Nov 2025 00:53:26 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:eb532338a2caa8666446075930a5afb7575e03232e9e7f3dd24a2e619aa10ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220617534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e24ad689f22fb55c4e907bdc54494d2cf8918a22943989549ef3257611cf38d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:28 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:28 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:37 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8a0e3673d3f3dd91177a058ce7a80d8c11656917a9723053456c0ea1daaf91`  
		Last Modified: Tue, 11 Nov 2025 22:16:14 GMT  
		Size: 37.5 MB (37498739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28c299936895e6e7c678360d65ddf9bcc10d991bf9d5ac38acba1bf0633f366`  
		Last Modified: Tue, 11 Nov 2025 22:16:13 GMT  
		Size: 1.3 MB (1275120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d391fc01102844a7f6ac7c68c3b6cdfa8b75c5d885bf34221925d1e59c20d98`  
		Last Modified: Wed, 12 Nov 2025 09:57:58 GMT  
		Size: 155.6 MB (155630604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:c69a37e1315d5cbc986a26ea182473dc93e571216e0dde5a9eca1baffd14e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316a76cbae0bbff8a04a4c13df598035674a3c4a19aa43ac85c0c877f0e775d0`

```dockerfile
```

-	Layers:
	-	`sha256:878d79baeb2edea66f080d0ae62ae9864a42908b3ac5a63f4d73edf2d9529563`  
		Last Modified: Wed, 12 Nov 2025 00:53:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c588906dd1bfa1d1f5c23c0e5ba61196c87cb3444e3580489fe12542caef0f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287460575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d1cc0f662d9e99097c9082442ba1c871409475d9339c256105664ead2afe0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:15:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:15:14 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:15:14 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:15:14 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:15:27 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029f67d0772e2784f3a9ce97116fa13626753db2df6a764af45aabfac06935c`  
		Last Modified: Tue, 11 Nov 2025 22:16:16 GMT  
		Size: 42.3 MB (42292501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6cb4c90d5106963daf20bdea42e32fa5212942072bcd78921bc494a71597fd`  
		Last Modified: Tue, 11 Nov 2025 22:16:14 GMT  
		Size: 1.6 MB (1566652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d3566d67a811fffeabc9cb48ecd0ad8fb6dbd599c8f7c2c052b2c80468cc06`  
		Last Modified: Wed, 12 Nov 2025 00:54:18 GMT  
		Size: 213.5 MB (213459092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2d3b3e76744d794ea46b6286481ca3cfc4bbefe339a98e190e4827e92fce6454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0085728b81c3ea8f83182e0c7402225e75cf60b06e6cc0a7694fb94daee4127b`

```dockerfile
```

-	Layers:
	-	`sha256:12c066a294761cc4ffa0ae3ad115944c49d52e9d6e79ab66dffbb275fb5a29f8`  
		Last Modified: Wed, 12 Nov 2025 00:53:33 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:7c11f0bfea444c2db3fe3e41b543ebaa631b93f4243c16b3203b38067894fd02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233894084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1454d64d0067d809d3c414bd0ffa5912e9ab0bce08897581102f42f7ace52e6b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 11 Nov 2025 22:16:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 11 Nov 2025 22:16:04 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 11 Nov 2025 22:16:04 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 22:16:04 GMT
WORKDIR /root
# Tue, 11 Nov 2025 22:16:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c197f3fb63a08d839b0be1ce3d42db3af7f54f27346b95f111b82b21cc267fa8`  
		Last Modified: Tue, 11 Nov 2025 22:21:21 GMT  
		Size: 41.6 MB (41560559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bf767ca6af272d9eb378bc7d2f7a727579f404cc0d6158b26873863458f082`  
		Last Modified: Tue, 11 Nov 2025 22:21:09 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7cc814bd47aaf1e0dea94600169b3e15079b07a4f0205613785de0d3536cba`  
		Last Modified: Wed, 12 Nov 2025 00:54:13 GMT  
		Size: 162.5 MB (162490635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:230a706ab7179ce03490b0532cb65f3d8c64ce391ade3058f64249d507cf80ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0019f5ad603db58065c81ebc4d233ab6c2f380da38a967a60e20fba3972868a8`

```dockerfile
```

-	Layers:
	-	`sha256:0c5d6c11ae9d41d20cc5b5b8efd6bd400229ffe9acb1047c039d218bc04b5c2f`  
		Last Modified: Wed, 12 Nov 2025 00:53:36 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:9e72ff17956a600cc028732f040a5e51f7910840fa4679cb4261a065b1a65f9d
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
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:9e46a406614705bd3d47c1be1afe629fdb4c87d4fa923ab33e07ddf4bc7fe117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08fa7f7d62fa729c627cfe94bc12fc0e11f92d7d1fbae438c9a829d96aeb04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 12:06:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 12:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 12:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 12:06:29 GMT
WORKDIR /root
# Thu, 06 Nov 2025 07:41:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec87d9e6fe2a6c3d564b97ec749845500d1eb36d011fa27e67400daca20cad51`  
		Last Modified: Wed, 05 Nov 2025 12:15:22 GMT  
		Size: 41.6 MB (41560904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12241236d8e9213dd7db34ee23bd2fa4fe14911c837e542a2a0765c13d09ee31`  
		Last Modified: Wed, 05 Nov 2025 12:15:19 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81373d5bf99f9327fc756e8b4595aa20a086584c9af210bcc6545d96488afe68`  
		Last Modified: Thu, 06 Nov 2025 09:53:50 GMT  
		Size: 161.0 MB (160964291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:2a1530fc9402398181623e1f0f3ba717dceff941e28759bdbc1ee786dba0d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d229c0a98fa31d37805411d1f4fd045710e182c07fe507b550d0d10620c9d1de`

```dockerfile
```

-	Layers:
	-	`sha256:db9d4c9c047e25be7ac912026f41b0e7c2f7fabc4cac0d08d52c7c3c6a28827f`  
		Last Modified: Thu, 06 Nov 2025 09:53:22 GMT  
		Size: 20.7 KB (20689 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:9e72ff17956a600cc028732f040a5e51f7910840fa4679cb4261a065b1a65f9d
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
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:9e46a406614705bd3d47c1be1afe629fdb4c87d4fa923ab33e07ddf4bc7fe117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08fa7f7d62fa729c627cfe94bc12fc0e11f92d7d1fbae438c9a829d96aeb04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 12:06:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 12:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 12:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 12:06:29 GMT
WORKDIR /root
# Thu, 06 Nov 2025 07:41:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec87d9e6fe2a6c3d564b97ec749845500d1eb36d011fa27e67400daca20cad51`  
		Last Modified: Wed, 05 Nov 2025 12:15:22 GMT  
		Size: 41.6 MB (41560904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12241236d8e9213dd7db34ee23bd2fa4fe14911c837e542a2a0765c13d09ee31`  
		Last Modified: Wed, 05 Nov 2025 12:15:19 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81373d5bf99f9327fc756e8b4595aa20a086584c9af210bcc6545d96488afe68`  
		Last Modified: Thu, 06 Nov 2025 09:53:50 GMT  
		Size: 161.0 MB (160964291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2a1530fc9402398181623e1f0f3ba717dceff941e28759bdbc1ee786dba0d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d229c0a98fa31d37805411d1f4fd045710e182c07fe507b550d0d10620c9d1de`

```dockerfile
```

-	Layers:
	-	`sha256:db9d4c9c047e25be7ac912026f41b0e7c2f7fabc4cac0d08d52c7c3c6a28827f`  
		Last Modified: Thu, 06 Nov 2025 09:53:22 GMT  
		Size: 20.7 KB (20689 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:9e72ff17956a600cc028732f040a5e51f7910840fa4679cb4261a065b1a65f9d
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
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:9e46a406614705bd3d47c1be1afe629fdb4c87d4fa923ab33e07ddf4bc7fe117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08fa7f7d62fa729c627cfe94bc12fc0e11f92d7d1fbae438c9a829d96aeb04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 12:06:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 12:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 12:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 12:06:29 GMT
WORKDIR /root
# Thu, 06 Nov 2025 07:41:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec87d9e6fe2a6c3d564b97ec749845500d1eb36d011fa27e67400daca20cad51`  
		Last Modified: Wed, 05 Nov 2025 12:15:22 GMT  
		Size: 41.6 MB (41560904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12241236d8e9213dd7db34ee23bd2fa4fe14911c837e542a2a0765c13d09ee31`  
		Last Modified: Wed, 05 Nov 2025 12:15:19 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81373d5bf99f9327fc756e8b4595aa20a086584c9af210bcc6545d96488afe68`  
		Last Modified: Thu, 06 Nov 2025 09:53:50 GMT  
		Size: 161.0 MB (160964291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:2a1530fc9402398181623e1f0f3ba717dceff941e28759bdbc1ee786dba0d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d229c0a98fa31d37805411d1f4fd045710e182c07fe507b550d0d10620c9d1de`

```dockerfile
```

-	Layers:
	-	`sha256:db9d4c9c047e25be7ac912026f41b0e7c2f7fabc4cac0d08d52c7c3c6a28827f`  
		Last Modified: Thu, 06 Nov 2025 09:53:22 GMT  
		Size: 20.7 KB (20689 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:9e72ff17956a600cc028732f040a5e51f7910840fa4679cb4261a065b1a65f9d
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
$ docker pull dart@sha256:a01a638bf7d4707d606d9c6fb17975eeed63b888607197309e89d0fa816484a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287267609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3892461526385750e7457f2f6c5246f2347025e761fe3d88ce7bf62c4b7dd7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:28 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:28 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3003c70db2a9f2039ddc7da75b0d7235bae857133770b66f0cf731fa74428328`  
		Last Modified: Wed, 12 Nov 2025 18:36:40 GMT  
		Size: 42.5 MB (42493515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1fa6912e6ffd2fa18dae02684c0b684b98206f1c35af09f005b2cd1d699edc`  
		Last Modified: Wed, 12 Nov 2025 18:36:31 GMT  
		Size: 1.9 MB (1873621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b92483aa7a5bc4ba942381384205bb120718ab71c9fc2beeadf54ce622ebe4`  
		Last Modified: Wed, 12 Nov 2025 18:53:47 GMT  
		Size: 213.1 MB (213122337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:fc87d30077585f41fcd338cdb1e7d4672596b884e46794f130cffedddae15f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce26f6ae62799910afa4957fb295cc2c6fc9c1b06ca741d274524833ea09ba94`

```dockerfile
```

-	Layers:
	-	`sha256:c3a79ad2a5bb909466fc5f26905c3d750d02616ac018f8e65ee4b4ef538f20b4`  
		Last Modified: Wed, 12 Nov 2025 18:53:20 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:03c1d7142b61062d08ec7edd69e49a707e3e4c816e0b2d8d5a5e9f61438b30b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219900272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff900fe5f1e5e9a0ba7dbaea04cfdd76e8fd1166d863333e75eef5f1b26329e4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 12 Nov 2025 18:35:23 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 12 Nov 2025 18:35:23 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:35:23 GMT
WORKDIR /root
# Wed, 12 Nov 2025 18:35:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a27681be873c3891692285db8d656e7494ca80c74e86613b8085fc6cffa3e31d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b91536edbcafc0d6389b8db6d1677bac0c608a1578fdf7c919b47b439aa044f1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=688603283b9a9e7833da53eb5b3a07d78fea9c51fdd925bbfd922775d4ba5ea3;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=dafc564768e0063170e5f0c663b90c3b4570ad3cd39c9bff3790f03e6b8554bb;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74f539c89eb39fb5123fd5f832cbb522d4f2fbbce503c1aa7689dc5d239395`  
		Last Modified: Wed, 12 Nov 2025 18:37:07 GMT  
		Size: 37.5 MB (37498727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d72ec58e49925670e37d5d3fdd8dd48f2d570be34c9fa541a5342015dab1e`  
		Last Modified: Wed, 12 Nov 2025 18:37:04 GMT  
		Size: 1.3 MB (1275117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395ad3197e7b5339ad187d66cd6b5fd4c3836ac71dd7983bd42211ae8795bbe`  
		Last Modified: Wed, 12 Nov 2025 18:53:50 GMT  
		Size: 154.9 MB (154913357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:77143b98362270e95b6dea4d584a7298ab29cd4180be7b230efc2b4832145f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30de7b48ed399fd89823fff86deffd06484e6386db33a44835f47f924390bc68`

```dockerfile
```

-	Layers:
	-	`sha256:96e7d1bc92abdd1deb6f599f381b6064f09e26e5f74ec69dadc1798514867f29`  
		Last Modified: Wed, 12 Nov 2025 18:53:24 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:27c76dc5e4d5795728c51823b70ad37c5d61abc6b4bacf193ffbc0a8e168184f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294697869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5436563b26ada7ab7f72d03f9f86025314b116359b8b2be15411e14fcb1185`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 04 Nov 2025 01:30:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 04 Nov 2025 01:30:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:30:02 GMT
WORKDIR /root
# Tue, 04 Nov 2025 01:30:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08a1ebe82316959af68cf4b727956b0c0e2aeb525a983b4c26d2c64674717b`  
		Last Modified: Tue, 04 Nov 2025 01:30:56 GMT  
		Size: 42.3 MB (42293074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb592177dd76edb97117a226c9263b70f4c8f6e45adcbce1abcb2e29e65442`  
		Last Modified: Tue, 04 Nov 2025 01:30:52 GMT  
		Size: 1.6 MB (1566648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece4f3619d34dd8cabf51e267e6ec54211b93188e46b45879188c8d2f5d538cb`  
		Last Modified: Tue, 04 Nov 2025 09:54:15 GMT  
		Size: 220.7 MB (220695817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5780ce3fbde29f136929657df3320974e5f30194f61758647be810fe59d0e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537cb701cdcecee1335d58a4396b69c165117a02c53b45a63bf1b347826fd6b`

```dockerfile
```

-	Layers:
	-	`sha256:98e52a980356515c72ae926934bdf15ed52fe3052ab4dd746f27bfa5d9d7af9f`  
		Last Modified: Tue, 04 Nov 2025 09:53:50 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:9e46a406614705bd3d47c1be1afe629fdb4c87d4fa923ab33e07ddf4bc7fe117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08fa7f7d62fa729c627cfe94bc12fc0e11f92d7d1fbae438c9a829d96aeb04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:06:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 12:06:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 05 Nov 2025 12:06:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 05 Nov 2025 12:06:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 12:06:29 GMT
WORKDIR /root
# Thu, 06 Nov 2025 07:41:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=61b4b9488e1b4255b94be17ad48ae2ddb23c6fbe67824cf8103d0b28fa8ab816;             SDK_ARCH="x64";;         armhf)             DART_SHA256=8490f1d4a137e6b9edc628f7fe56bfa2d93ea22d07981b37bcb08c4248f03be8;             SDK_ARCH="arm";;         arm64)             DART_SHA256=21790958b6c65cb57a1a3c3fb508f44ddcfb77b822a090039ee47e583fcde0e8;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=9f1c7fb1d742c2962a19d09e9698f601e001855ddc63a5ecc5ae5732144c88be;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.9.4/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec87d9e6fe2a6c3d564b97ec749845500d1eb36d011fa27e67400daca20cad51`  
		Last Modified: Wed, 05 Nov 2025 12:15:22 GMT  
		Size: 41.6 MB (41560904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12241236d8e9213dd7db34ee23bd2fa4fe14911c837e542a2a0765c13d09ee31`  
		Last Modified: Wed, 05 Nov 2025 12:15:19 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81373d5bf99f9327fc756e8b4595aa20a086584c9af210bcc6545d96488afe68`  
		Last Modified: Thu, 06 Nov 2025 09:53:50 GMT  
		Size: 161.0 MB (160964291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2a1530fc9402398181623e1f0f3ba717dceff941e28759bdbc1ee786dba0d041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d229c0a98fa31d37805411d1f4fd045710e182c07fe507b550d0d10620c9d1de`

```dockerfile
```

-	Layers:
	-	`sha256:db9d4c9c047e25be7ac912026f41b0e7c2f7fabc4cac0d08d52c7c3c6a28827f`  
		Last Modified: Thu, 06 Nov 2025 09:53:22 GMT  
		Size: 20.7 KB (20689 bytes)  
		MIME: application/vnd.in-toto+json
