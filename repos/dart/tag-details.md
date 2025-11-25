<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.10`](#dart310)
-	[`dart:3.10-sdk`](#dart310-sdk)
-	[`dart:3.10.2`](#dart3102)
-	[`dart:3.10.2-sdk`](#dart3102-sdk)
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
$ docker pull dart@sha256:45e435a36a9da1422b2170dc9a91fdff21043be7f255c0348b3b59f949d5036c
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
$ docker pull dart@sha256:fa4aeb6c63fbe122446e102663a63a10b014d0107a9b43191557bd58e1105ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18729fcb2ff834aaf2ff55a539cc4cc3f5beac867ebbfb8fe0d5c8b7f83868d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 21:59:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 21:59:42 GMT
WORKDIR /root
# Tue, 18 Nov 2025 21:59:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1658fcc370faef9607684c67d9c86f881f21cfc67db6934af7f1f3b86b204`  
		Last Modified: Tue, 18 Nov 2025 22:00:46 GMT  
		Size: 42.5 MB (42494135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7318d63717dd94a619a165256471fba0d51920a1be2a23dba393193dd95cdf`  
		Last Modified: Tue, 18 Nov 2025 22:00:38 GMT  
		Size: 1.9 MB (1873622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09063cf43129eb5a67ada65d1890eb822290e7b23fb359550f75d14dbbe7cfbb`  
		Last Modified: Wed, 19 Nov 2025 00:53:59 GMT  
		Size: 213.1 MB (213121454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:f9f8e1f72fea1bbaf8804577ec38d68253e2183c19f04a13cbbc91b1795a3ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249a4f9a4efc9706dc6e60bd58708f2e62b7f2066bac0fc074baa3f9796fa291`

```dockerfile
```

-	Layers:
	-	`sha256:0b39fcea42499b23179ee0346b6d3e23219f314790b386ae0a18459fb3983923`  
		Last Modified: Wed, 19 Nov 2025 00:53:24 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb0e291a4c0b4c2f609ee143271a881bb8de1f2af7a6f706e55e106c445b995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219903719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eff55435245fcb5ad77f40a0906aa65c0bd80bb644066952ad9b67aa2e50b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:57 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c891ff91f312c704bbf333d1b15418843367b81c6b93638049944c15d532bf4`  
		Last Modified: Tue, 18 Nov 2025 22:02:58 GMT  
		Size: 37.5 MB (37498240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852375714e4e1049db217ce75acd1271f96e14b52b191e2e662730d7b616ec3`  
		Last Modified: Tue, 18 Nov 2025 22:02:54 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34517ff1c05bf15a9e61c4b87dd8232f73841d72865b047b31b625456f37c2c`  
		Last Modified: Wed, 19 Nov 2025 00:54:11 GMT  
		Size: 154.9 MB (154920365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:adde0b6ff4acf32dc018b0d6d37badeb0196e2e26b2395808878a04f83361c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77af9b3e9077badc7851b2149a4fb2b401d05d65a504f5a7957eb72a5350d55`

```dockerfile
```

-	Layers:
	-	`sha256:60325e55d4f814bbf831f4d219af19ca47382973650b36e9822294af3cd28db2`  
		Last Modified: Wed, 19 Nov 2025 00:53:27 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:03910e75eb80e0877ce681918e25ba5614dfa5d0a47be0831698c7b6523e51cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286359902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ddce5fe73a5ab577b3c0ab22071624b4e58b658b96ec99133e9c556a76d0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:47 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c282fd9d3f077502877d9bd6db1698bad289aac728ca062900cb21c7e964164`  
		Last Modified: Tue, 18 Nov 2025 22:03:17 GMT  
		Size: 42.3 MB (42293267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6c59386460b3afe249ed86ef0b7f0eb342787a6af6e3261fd1b4f8c24818e`  
		Last Modified: Tue, 18 Nov 2025 22:03:11 GMT  
		Size: 1.6 MB (1566643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f36a03cf48657a271ec16e657cb251e2094626c7fa9772b99fcc9c4c0a972`  
		Last Modified: Tue, 18 Nov 2025 22:18:31 GMT  
		Size: 212.4 MB (212361350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:88e91c39dda8324af3a2c5b906047a902708798b0d444207c49a8058e6bcf34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3711cbc9f46172d637e6f56d547a98426fbd05898d3a91009f11ed7163de37f`

```dockerfile
```

-	Layers:
	-	`sha256:7b83b5d3157271c0d042f630a42c60adf39c61ec39b32923dd56fc467a5126d9`  
		Last Modified: Wed, 19 Nov 2025 00:53:31 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:f97d4d6d26bb1216063e195bb7f5b45903dfc0ca011eee5e7a53e56e794c3c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e93eda7f17e0597108f80c4b01cf0eef8f93dd88292faa6b42f159a396373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 22:34:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 20 Nov 2025 22:34:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 22:34:59 GMT
WORKDIR /root
# Thu, 20 Nov 2025 22:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2224e8dbec4ac7444b327f03c8cb2effbf7ef809baca565fa3b7f851a157a`  
		Last Modified: Thu, 20 Nov 2025 22:40:19 GMT  
		Size: 41.6 MB (41560749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47932c01ba87b2fd89d28da4c231e8bda0b067fc21110ed989f19d9f5025f48`  
		Last Modified: Thu, 20 Nov 2025 22:40:13 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609188b99f95f73c3295f006e51f0f1e62ce3fdd70b74d7279dc9a745e93f8a7`  
		Last Modified: Thu, 20 Nov 2025 23:13:06 GMT  
		Size: 161.6 MB (161563764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:1d6d92d4991fbd675c87e8f56e0cb28fd74a122024dc43da74f7ab216582be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9389cc6325ba871c8c05c00a0c13b5691548fb3ee6ea3cf107fdf49bb721a32f`

```dockerfile
```

-	Layers:
	-	`sha256:e262f7ad459d3cf7954e10b44d17b27044153e6d6db3998efdcd3307079c06e3`  
		Last Modified: Fri, 21 Nov 2025 00:53:54 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:45e435a36a9da1422b2170dc9a91fdff21043be7f255c0348b3b59f949d5036c
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
$ docker pull dart@sha256:fa4aeb6c63fbe122446e102663a63a10b014d0107a9b43191557bd58e1105ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18729fcb2ff834aaf2ff55a539cc4cc3f5beac867ebbfb8fe0d5c8b7f83868d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 21:59:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 21:59:42 GMT
WORKDIR /root
# Tue, 18 Nov 2025 21:59:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1658fcc370faef9607684c67d9c86f881f21cfc67db6934af7f1f3b86b204`  
		Last Modified: Tue, 18 Nov 2025 22:00:46 GMT  
		Size: 42.5 MB (42494135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7318d63717dd94a619a165256471fba0d51920a1be2a23dba393193dd95cdf`  
		Last Modified: Tue, 18 Nov 2025 22:00:38 GMT  
		Size: 1.9 MB (1873622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09063cf43129eb5a67ada65d1890eb822290e7b23fb359550f75d14dbbe7cfbb`  
		Last Modified: Wed, 19 Nov 2025 00:53:59 GMT  
		Size: 213.1 MB (213121454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f9f8e1f72fea1bbaf8804577ec38d68253e2183c19f04a13cbbc91b1795a3ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249a4f9a4efc9706dc6e60bd58708f2e62b7f2066bac0fc074baa3f9796fa291`

```dockerfile
```

-	Layers:
	-	`sha256:0b39fcea42499b23179ee0346b6d3e23219f314790b386ae0a18459fb3983923`  
		Last Modified: Wed, 19 Nov 2025 00:53:24 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb0e291a4c0b4c2f609ee143271a881bb8de1f2af7a6f706e55e106c445b995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219903719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eff55435245fcb5ad77f40a0906aa65c0bd80bb644066952ad9b67aa2e50b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:57 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c891ff91f312c704bbf333d1b15418843367b81c6b93638049944c15d532bf4`  
		Last Modified: Tue, 18 Nov 2025 22:02:58 GMT  
		Size: 37.5 MB (37498240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852375714e4e1049db217ce75acd1271f96e14b52b191e2e662730d7b616ec3`  
		Last Modified: Tue, 18 Nov 2025 22:02:54 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34517ff1c05bf15a9e61c4b87dd8232f73841d72865b047b31b625456f37c2c`  
		Last Modified: Wed, 19 Nov 2025 00:54:11 GMT  
		Size: 154.9 MB (154920365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:adde0b6ff4acf32dc018b0d6d37badeb0196e2e26b2395808878a04f83361c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77af9b3e9077badc7851b2149a4fb2b401d05d65a504f5a7957eb72a5350d55`

```dockerfile
```

-	Layers:
	-	`sha256:60325e55d4f814bbf831f4d219af19ca47382973650b36e9822294af3cd28db2`  
		Last Modified: Wed, 19 Nov 2025 00:53:27 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:03910e75eb80e0877ce681918e25ba5614dfa5d0a47be0831698c7b6523e51cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286359902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ddce5fe73a5ab577b3c0ab22071624b4e58b658b96ec99133e9c556a76d0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:47 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c282fd9d3f077502877d9bd6db1698bad289aac728ca062900cb21c7e964164`  
		Last Modified: Tue, 18 Nov 2025 22:03:17 GMT  
		Size: 42.3 MB (42293267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6c59386460b3afe249ed86ef0b7f0eb342787a6af6e3261fd1b4f8c24818e`  
		Last Modified: Tue, 18 Nov 2025 22:03:11 GMT  
		Size: 1.6 MB (1566643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f36a03cf48657a271ec16e657cb251e2094626c7fa9772b99fcc9c4c0a972`  
		Last Modified: Tue, 18 Nov 2025 22:18:31 GMT  
		Size: 212.4 MB (212361350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:88e91c39dda8324af3a2c5b906047a902708798b0d444207c49a8058e6bcf34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3711cbc9f46172d637e6f56d547a98426fbd05898d3a91009f11ed7163de37f`

```dockerfile
```

-	Layers:
	-	`sha256:7b83b5d3157271c0d042f630a42c60adf39c61ec39b32923dd56fc467a5126d9`  
		Last Modified: Wed, 19 Nov 2025 00:53:31 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f97d4d6d26bb1216063e195bb7f5b45903dfc0ca011eee5e7a53e56e794c3c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e93eda7f17e0597108f80c4b01cf0eef8f93dd88292faa6b42f159a396373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 22:34:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 20 Nov 2025 22:34:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 22:34:59 GMT
WORKDIR /root
# Thu, 20 Nov 2025 22:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2224e8dbec4ac7444b327f03c8cb2effbf7ef809baca565fa3b7f851a157a`  
		Last Modified: Thu, 20 Nov 2025 22:40:19 GMT  
		Size: 41.6 MB (41560749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47932c01ba87b2fd89d28da4c231e8bda0b067fc21110ed989f19d9f5025f48`  
		Last Modified: Thu, 20 Nov 2025 22:40:13 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609188b99f95f73c3295f006e51f0f1e62ce3fdd70b74d7279dc9a745e93f8a7`  
		Last Modified: Thu, 20 Nov 2025 23:13:06 GMT  
		Size: 161.6 MB (161563764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1d6d92d4991fbd675c87e8f56e0cb28fd74a122024dc43da74f7ab216582be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9389cc6325ba871c8c05c00a0c13b5691548fb3ee6ea3cf107fdf49bb721a32f`

```dockerfile
```

-	Layers:
	-	`sha256:e262f7ad459d3cf7954e10b44d17b27044153e6d6db3998efdcd3307079c06e3`  
		Last Modified: Fri, 21 Nov 2025 00:53:54 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10`

```console
$ docker pull dart@sha256:45e435a36a9da1422b2170dc9a91fdff21043be7f255c0348b3b59f949d5036c
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

### `dart:3.10` - linux; amd64

```console
$ docker pull dart@sha256:fa4aeb6c63fbe122446e102663a63a10b014d0107a9b43191557bd58e1105ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18729fcb2ff834aaf2ff55a539cc4cc3f5beac867ebbfb8fe0d5c8b7f83868d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 21:59:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 21:59:42 GMT
WORKDIR /root
# Tue, 18 Nov 2025 21:59:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1658fcc370faef9607684c67d9c86f881f21cfc67db6934af7f1f3b86b204`  
		Last Modified: Tue, 18 Nov 2025 22:00:46 GMT  
		Size: 42.5 MB (42494135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7318d63717dd94a619a165256471fba0d51920a1be2a23dba393193dd95cdf`  
		Last Modified: Tue, 18 Nov 2025 22:00:38 GMT  
		Size: 1.9 MB (1873622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09063cf43129eb5a67ada65d1890eb822290e7b23fb359550f75d14dbbe7cfbb`  
		Last Modified: Wed, 19 Nov 2025 00:53:59 GMT  
		Size: 213.1 MB (213121454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:f9f8e1f72fea1bbaf8804577ec38d68253e2183c19f04a13cbbc91b1795a3ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249a4f9a4efc9706dc6e60bd58708f2e62b7f2066bac0fc074baa3f9796fa291`

```dockerfile
```

-	Layers:
	-	`sha256:0b39fcea42499b23179ee0346b6d3e23219f314790b386ae0a18459fb3983923`  
		Last Modified: Wed, 19 Nov 2025 00:53:24 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb0e291a4c0b4c2f609ee143271a881bb8de1f2af7a6f706e55e106c445b995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219903719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eff55435245fcb5ad77f40a0906aa65c0bd80bb644066952ad9b67aa2e50b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:57 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c891ff91f312c704bbf333d1b15418843367b81c6b93638049944c15d532bf4`  
		Last Modified: Tue, 18 Nov 2025 22:02:58 GMT  
		Size: 37.5 MB (37498240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852375714e4e1049db217ce75acd1271f96e14b52b191e2e662730d7b616ec3`  
		Last Modified: Tue, 18 Nov 2025 22:02:54 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34517ff1c05bf15a9e61c4b87dd8232f73841d72865b047b31b625456f37c2c`  
		Last Modified: Wed, 19 Nov 2025 00:54:11 GMT  
		Size: 154.9 MB (154920365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:adde0b6ff4acf32dc018b0d6d37badeb0196e2e26b2395808878a04f83361c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77af9b3e9077badc7851b2149a4fb2b401d05d65a504f5a7957eb72a5350d55`

```dockerfile
```

-	Layers:
	-	`sha256:60325e55d4f814bbf831f4d219af19ca47382973650b36e9822294af3cd28db2`  
		Last Modified: Wed, 19 Nov 2025 00:53:27 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:03910e75eb80e0877ce681918e25ba5614dfa5d0a47be0831698c7b6523e51cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286359902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ddce5fe73a5ab577b3c0ab22071624b4e58b658b96ec99133e9c556a76d0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:47 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c282fd9d3f077502877d9bd6db1698bad289aac728ca062900cb21c7e964164`  
		Last Modified: Tue, 18 Nov 2025 22:03:17 GMT  
		Size: 42.3 MB (42293267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6c59386460b3afe249ed86ef0b7f0eb342787a6af6e3261fd1b4f8c24818e`  
		Last Modified: Tue, 18 Nov 2025 22:03:11 GMT  
		Size: 1.6 MB (1566643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f36a03cf48657a271ec16e657cb251e2094626c7fa9772b99fcc9c4c0a972`  
		Last Modified: Tue, 18 Nov 2025 22:18:31 GMT  
		Size: 212.4 MB (212361350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:88e91c39dda8324af3a2c5b906047a902708798b0d444207c49a8058e6bcf34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3711cbc9f46172d637e6f56d547a98426fbd05898d3a91009f11ed7163de37f`

```dockerfile
```

-	Layers:
	-	`sha256:7b83b5d3157271c0d042f630a42c60adf39c61ec39b32923dd56fc467a5126d9`  
		Last Modified: Wed, 19 Nov 2025 00:53:31 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10` - linux; riscv64

```console
$ docker pull dart@sha256:f97d4d6d26bb1216063e195bb7f5b45903dfc0ca011eee5e7a53e56e794c3c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e93eda7f17e0597108f80c4b01cf0eef8f93dd88292faa6b42f159a396373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 22:34:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 20 Nov 2025 22:34:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 22:34:59 GMT
WORKDIR /root
# Thu, 20 Nov 2025 22:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2224e8dbec4ac7444b327f03c8cb2effbf7ef809baca565fa3b7f851a157a`  
		Last Modified: Thu, 20 Nov 2025 22:40:19 GMT  
		Size: 41.6 MB (41560749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47932c01ba87b2fd89d28da4c231e8bda0b067fc21110ed989f19d9f5025f48`  
		Last Modified: Thu, 20 Nov 2025 22:40:13 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609188b99f95f73c3295f006e51f0f1e62ce3fdd70b74d7279dc9a745e93f8a7`  
		Last Modified: Thu, 20 Nov 2025 23:13:06 GMT  
		Size: 161.6 MB (161563764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10` - unknown; unknown

```console
$ docker pull dart@sha256:1d6d92d4991fbd675c87e8f56e0cb28fd74a122024dc43da74f7ab216582be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9389cc6325ba871c8c05c00a0c13b5691548fb3ee6ea3cf107fdf49bb721a32f`

```dockerfile
```

-	Layers:
	-	`sha256:e262f7ad459d3cf7954e10b44d17b27044153e6d6db3998efdcd3307079c06e3`  
		Last Modified: Fri, 21 Nov 2025 00:53:54 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10-sdk`

```console
$ docker pull dart@sha256:45e435a36a9da1422b2170dc9a91fdff21043be7f255c0348b3b59f949d5036c
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

### `dart:3.10-sdk` - linux; amd64

```console
$ docker pull dart@sha256:fa4aeb6c63fbe122446e102663a63a10b014d0107a9b43191557bd58e1105ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18729fcb2ff834aaf2ff55a539cc4cc3f5beac867ebbfb8fe0d5c8b7f83868d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 21:59:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 21:59:42 GMT
WORKDIR /root
# Tue, 18 Nov 2025 21:59:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1658fcc370faef9607684c67d9c86f881f21cfc67db6934af7f1f3b86b204`  
		Last Modified: Tue, 18 Nov 2025 22:00:46 GMT  
		Size: 42.5 MB (42494135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7318d63717dd94a619a165256471fba0d51920a1be2a23dba393193dd95cdf`  
		Last Modified: Tue, 18 Nov 2025 22:00:38 GMT  
		Size: 1.9 MB (1873622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09063cf43129eb5a67ada65d1890eb822290e7b23fb359550f75d14dbbe7cfbb`  
		Last Modified: Wed, 19 Nov 2025 00:53:59 GMT  
		Size: 213.1 MB (213121454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f9f8e1f72fea1bbaf8804577ec38d68253e2183c19f04a13cbbc91b1795a3ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249a4f9a4efc9706dc6e60bd58708f2e62b7f2066bac0fc074baa3f9796fa291`

```dockerfile
```

-	Layers:
	-	`sha256:0b39fcea42499b23179ee0346b6d3e23219f314790b386ae0a18459fb3983923`  
		Last Modified: Wed, 19 Nov 2025 00:53:24 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb0e291a4c0b4c2f609ee143271a881bb8de1f2af7a6f706e55e106c445b995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219903719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eff55435245fcb5ad77f40a0906aa65c0bd80bb644066952ad9b67aa2e50b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:57 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c891ff91f312c704bbf333d1b15418843367b81c6b93638049944c15d532bf4`  
		Last Modified: Tue, 18 Nov 2025 22:02:58 GMT  
		Size: 37.5 MB (37498240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852375714e4e1049db217ce75acd1271f96e14b52b191e2e662730d7b616ec3`  
		Last Modified: Tue, 18 Nov 2025 22:02:54 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34517ff1c05bf15a9e61c4b87dd8232f73841d72865b047b31b625456f37c2c`  
		Last Modified: Wed, 19 Nov 2025 00:54:11 GMT  
		Size: 154.9 MB (154920365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:adde0b6ff4acf32dc018b0d6d37badeb0196e2e26b2395808878a04f83361c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77af9b3e9077badc7851b2149a4fb2b401d05d65a504f5a7957eb72a5350d55`

```dockerfile
```

-	Layers:
	-	`sha256:60325e55d4f814bbf831f4d219af19ca47382973650b36e9822294af3cd28db2`  
		Last Modified: Wed, 19 Nov 2025 00:53:27 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:03910e75eb80e0877ce681918e25ba5614dfa5d0a47be0831698c7b6523e51cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286359902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ddce5fe73a5ab577b3c0ab22071624b4e58b658b96ec99133e9c556a76d0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:47 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c282fd9d3f077502877d9bd6db1698bad289aac728ca062900cb21c7e964164`  
		Last Modified: Tue, 18 Nov 2025 22:03:17 GMT  
		Size: 42.3 MB (42293267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6c59386460b3afe249ed86ef0b7f0eb342787a6af6e3261fd1b4f8c24818e`  
		Last Modified: Tue, 18 Nov 2025 22:03:11 GMT  
		Size: 1.6 MB (1566643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f36a03cf48657a271ec16e657cb251e2094626c7fa9772b99fcc9c4c0a972`  
		Last Modified: Tue, 18 Nov 2025 22:18:31 GMT  
		Size: 212.4 MB (212361350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:88e91c39dda8324af3a2c5b906047a902708798b0d444207c49a8058e6bcf34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3711cbc9f46172d637e6f56d547a98426fbd05898d3a91009f11ed7163de37f`

```dockerfile
```

-	Layers:
	-	`sha256:7b83b5d3157271c0d042f630a42c60adf39c61ec39b32923dd56fc467a5126d9`  
		Last Modified: Wed, 19 Nov 2025 00:53:31 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.10-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f97d4d6d26bb1216063e195bb7f5b45903dfc0ca011eee5e7a53e56e794c3c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e93eda7f17e0597108f80c4b01cf0eef8f93dd88292faa6b42f159a396373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 22:34:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 20 Nov 2025 22:34:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 22:34:59 GMT
WORKDIR /root
# Thu, 20 Nov 2025 22:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2224e8dbec4ac7444b327f03c8cb2effbf7ef809baca565fa3b7f851a157a`  
		Last Modified: Thu, 20 Nov 2025 22:40:19 GMT  
		Size: 41.6 MB (41560749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47932c01ba87b2fd89d28da4c231e8bda0b067fc21110ed989f19d9f5025f48`  
		Last Modified: Thu, 20 Nov 2025 22:40:13 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609188b99f95f73c3295f006e51f0f1e62ce3fdd70b74d7279dc9a745e93f8a7`  
		Last Modified: Thu, 20 Nov 2025 23:13:06 GMT  
		Size: 161.6 MB (161563764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.10-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1d6d92d4991fbd675c87e8f56e0cb28fd74a122024dc43da74f7ab216582be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9389cc6325ba871c8c05c00a0c13b5691548fb3ee6ea3cf107fdf49bb721a32f`

```dockerfile
```

-	Layers:
	-	`sha256:e262f7ad459d3cf7954e10b44d17b27044153e6d6db3998efdcd3307079c06e3`  
		Last Modified: Fri, 21 Nov 2025 00:53:54 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.10.2`

**does not exist** (yet?)

## `dart:3.10.2-sdk`

**does not exist** (yet?)

## `dart:3.11.0-93.2.beta`

```console
$ docker pull dart@sha256:f65f34c54c2fd57e115449046af8fe8b640a099682f01c7d459ad52e2aca8a10
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
$ docker pull dart@sha256:d65d30ccbc3e6b00cbbc83946b9ef517cb5531c0fc4da4a60644b9bc331a989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288383491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbb20cd91f9204144cebebc27862fe183455e029fa759e2474c717099e7d38f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 05:14:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 05:15:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2529f5cef81aeecc09c6572e1e0dbe33c3a22307a223b8ecfaa82bcf21743`  
		Last Modified: Tue, 18 Nov 2025 05:15:37 GMT  
		Size: 42.5 MB (42494038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4313a42c948bf5c26bf4c6050453a911eb2d1fa3107407e270ee2fc2fddfe5d4`  
		Last Modified: Tue, 18 Nov 2025 05:15:34 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0620f90d617bf0c728028c0832e588717bfb0641da01c0676a65d98fc0e15d28`  
		Last Modified: Tue, 18 Nov 2025 06:54:57 GMT  
		Size: 214.2 MB (214239319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:eec7307ccf0361b096c0a867fb42fb8f3f9123a6428875bbe63b49e42ee69397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f1187cf959d77b60c4506ad50860db4d263a3ec5c50464909798c4f5f649d0`

```dockerfile
```

-	Layers:
	-	`sha256:70542988e68a4f1c5f95cdbb38138b9b2408e2b300f5a99dd2d30926f4d268da`  
		Last Modified: Tue, 18 Nov 2025 06:54:25 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:cf7925494803272669575b769293f708d5084d4656bd9b0bd6a4086dbc5837ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220613957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08ed827579b12c3c097073fae9c6474dd75c4777bc26a85d1044472db8cd6a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 04:19:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 04:19:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c356f9e9c92c891333fb1ae718cd8215415ca2152ac62bfc037b5d3045f73`  
		Last Modified: Tue, 18 Nov 2025 04:20:30 GMT  
		Size: 37.5 MB (37498324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7540b58924232b2bb1574d0d8b1e8e792b566628223cfa20c25ed7987eb2a5`  
		Last Modified: Tue, 18 Nov 2025 04:20:28 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee1e2ebe1daf3426bddce8a256b002bc05a59760884fa8994ce596195c497e`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 155.6 MB (155630520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:184a6022b83f622547a2495a9e796bcce797395c321ac0cedb07ceddb26413a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dec425e6b4e3da0dbb5b06398ba32a1f19354510341b5670411f4e32c4f539`

```dockerfile
```

-	Layers:
	-	`sha256:fe6ca29c93fdd0ab41d450123bb49aaa9219b9def1ab330ad7870ff006b06a08`  
		Last Modified: Tue, 18 Nov 2025 06:54:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05f3c539161d72c4a364d2cd1ac4bd997582ef4a623b37dd90c444f53e7829a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287457827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e4810f2701354a5cf718dfbe5a0c2fa0e1fb7fab8bdd19574834e5f02ce71e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 03:37:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:37:33 GMT
WORKDIR /root
# Tue, 18 Nov 2025 03:37:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723c2ae08eef5cb2b007a95641953958457fb3609dbec7cbc9f221c7f47368fe`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 42.3 MB (42293339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818d083b0084d331d2dec2a8191772898e5557a265bb0a65f8aa0e63564bd0d1`  
		Last Modified: Tue, 18 Nov 2025 03:38:24 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1f46bc6c5aefeb405bb3a5c492c869e77e8556d5bbefe9b2005976f225b9`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 213.5 MB (213459193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:8be7b70e1b0b7cad4606e8af8d02cff66089a484b78b502df69af450319f7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd364dcaae13777b5e5251bc5b5e5b05f97ca3e0b3fd2e3d2898bc4c3ff6e72a`

```dockerfile
```

-	Layers:
	-	`sha256:d2284a78f7db258f1faaa3a1107c2b8f864af5d22ee7b6054345d72569e663c5`  
		Last Modified: Tue, 18 Nov 2025 06:54:31 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta` - linux; riscv64

```console
$ docker pull dart@sha256:c8bc712f21347aad6d0c3cd39199111ddf4f3f137f3e426e43d5b6d1493f430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233891852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7e6980b4837f225aa4f6cc3b93df3c987671b42740652105262f71ef524029`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:40:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 19 Nov 2025 19:40:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 19:40:39 GMT
WORKDIR /root
# Wed, 19 Nov 2025 19:41:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da213c1ee21f21efd577e634d99a65798e6b0e7656870692da1c2eac8842158`  
		Last Modified: Wed, 19 Nov 2025 19:45:54 GMT  
		Size: 41.6 MB (41560760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96193f29a66f7bd8c31765af875186499b40ca5be5f023e0d948d4ed85acebad`  
		Last Modified: Wed, 19 Nov 2025 19:45:49 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae03974c01b46162db481a23a9a00ce9f9556d82e65b3d1eca98a03262e076d`  
		Last Modified: Wed, 19 Nov 2025 19:51:06 GMT  
		Size: 162.5 MB (162490863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:925a00e6fd4c2ba95b31054816561b23857dfc1ef77f90e32875f2f24c7e79f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a99264debe5bf763c4c469cd7486c94416c4ab90cf4a2ef0e7fe13710378bf`

```dockerfile
```

-	Layers:
	-	`sha256:0b5b69fa5afb5567e074aaee573dfb695d0d597c3ca22938865f5519004a7e9d`  
		Last Modified: Wed, 19 Nov 2025 21:53:30 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.0-93.2.beta-sdk`

```console
$ docker pull dart@sha256:f65f34c54c2fd57e115449046af8fe8b640a099682f01c7d459ad52e2aca8a10
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
$ docker pull dart@sha256:d65d30ccbc3e6b00cbbc83946b9ef517cb5531c0fc4da4a60644b9bc331a989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288383491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbb20cd91f9204144cebebc27862fe183455e029fa759e2474c717099e7d38f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 05:14:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 05:15:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2529f5cef81aeecc09c6572e1e0dbe33c3a22307a223b8ecfaa82bcf21743`  
		Last Modified: Tue, 18 Nov 2025 05:15:37 GMT  
		Size: 42.5 MB (42494038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4313a42c948bf5c26bf4c6050453a911eb2d1fa3107407e270ee2fc2fddfe5d4`  
		Last Modified: Tue, 18 Nov 2025 05:15:34 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0620f90d617bf0c728028c0832e588717bfb0641da01c0676a65d98fc0e15d28`  
		Last Modified: Tue, 18 Nov 2025 06:54:57 GMT  
		Size: 214.2 MB (214239319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:eec7307ccf0361b096c0a867fb42fb8f3f9123a6428875bbe63b49e42ee69397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f1187cf959d77b60c4506ad50860db4d263a3ec5c50464909798c4f5f649d0`

```dockerfile
```

-	Layers:
	-	`sha256:70542988e68a4f1c5f95cdbb38138b9b2408e2b300f5a99dd2d30926f4d268da`  
		Last Modified: Tue, 18 Nov 2025 06:54:25 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:cf7925494803272669575b769293f708d5084d4656bd9b0bd6a4086dbc5837ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220613957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08ed827579b12c3c097073fae9c6474dd75c4777bc26a85d1044472db8cd6a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 04:19:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 04:19:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c356f9e9c92c891333fb1ae718cd8215415ca2152ac62bfc037b5d3045f73`  
		Last Modified: Tue, 18 Nov 2025 04:20:30 GMT  
		Size: 37.5 MB (37498324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7540b58924232b2bb1574d0d8b1e8e792b566628223cfa20c25ed7987eb2a5`  
		Last Modified: Tue, 18 Nov 2025 04:20:28 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee1e2ebe1daf3426bddce8a256b002bc05a59760884fa8994ce596195c497e`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 155.6 MB (155630520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:184a6022b83f622547a2495a9e796bcce797395c321ac0cedb07ceddb26413a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dec425e6b4e3da0dbb5b06398ba32a1f19354510341b5670411f4e32c4f539`

```dockerfile
```

-	Layers:
	-	`sha256:fe6ca29c93fdd0ab41d450123bb49aaa9219b9def1ab330ad7870ff006b06a08`  
		Last Modified: Tue, 18 Nov 2025 06:54:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05f3c539161d72c4a364d2cd1ac4bd997582ef4a623b37dd90c444f53e7829a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287457827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e4810f2701354a5cf718dfbe5a0c2fa0e1fb7fab8bdd19574834e5f02ce71e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 03:37:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:37:33 GMT
WORKDIR /root
# Tue, 18 Nov 2025 03:37:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723c2ae08eef5cb2b007a95641953958457fb3609dbec7cbc9f221c7f47368fe`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 42.3 MB (42293339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818d083b0084d331d2dec2a8191772898e5557a265bb0a65f8aa0e63564bd0d1`  
		Last Modified: Tue, 18 Nov 2025 03:38:24 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1f46bc6c5aefeb405bb3a5c492c869e77e8556d5bbefe9b2005976f225b9`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 213.5 MB (213459193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8be7b70e1b0b7cad4606e8af8d02cff66089a484b78b502df69af450319f7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd364dcaae13777b5e5251bc5b5e5b05f97ca3e0b3fd2e3d2898bc4c3ff6e72a`

```dockerfile
```

-	Layers:
	-	`sha256:d2284a78f7db258f1faaa3a1107c2b8f864af5d22ee7b6054345d72569e663c5`  
		Last Modified: Tue, 18 Nov 2025 06:54:31 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.0-93.2.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c8bc712f21347aad6d0c3cd39199111ddf4f3f137f3e426e43d5b6d1493f430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233891852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7e6980b4837f225aa4f6cc3b93df3c987671b42740652105262f71ef524029`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:40:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 19 Nov 2025 19:40:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 19:40:39 GMT
WORKDIR /root
# Wed, 19 Nov 2025 19:41:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da213c1ee21f21efd577e634d99a65798e6b0e7656870692da1c2eac8842158`  
		Last Modified: Wed, 19 Nov 2025 19:45:54 GMT  
		Size: 41.6 MB (41560760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96193f29a66f7bd8c31765af875186499b40ca5be5f023e0d948d4ed85acebad`  
		Last Modified: Wed, 19 Nov 2025 19:45:49 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae03974c01b46162db481a23a9a00ce9f9556d82e65b3d1eca98a03262e076d`  
		Last Modified: Wed, 19 Nov 2025 19:51:06 GMT  
		Size: 162.5 MB (162490863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.0-93.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:925a00e6fd4c2ba95b31054816561b23857dfc1ef77f90e32875f2f24c7e79f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a99264debe5bf763c4c469cd7486c94416c4ab90cf4a2ef0e7fe13710378bf`

```dockerfile
```

-	Layers:
	-	`sha256:0b5b69fa5afb5567e074aaee573dfb695d0d597c3ca22938865f5519004a7e9d`  
		Last Modified: Wed, 19 Nov 2025 21:53:30 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:f65f34c54c2fd57e115449046af8fe8b640a099682f01c7d459ad52e2aca8a10
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
$ docker pull dart@sha256:d65d30ccbc3e6b00cbbc83946b9ef517cb5531c0fc4da4a60644b9bc331a989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288383491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbb20cd91f9204144cebebc27862fe183455e029fa759e2474c717099e7d38f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 05:14:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 05:15:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2529f5cef81aeecc09c6572e1e0dbe33c3a22307a223b8ecfaa82bcf21743`  
		Last Modified: Tue, 18 Nov 2025 05:15:37 GMT  
		Size: 42.5 MB (42494038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4313a42c948bf5c26bf4c6050453a911eb2d1fa3107407e270ee2fc2fddfe5d4`  
		Last Modified: Tue, 18 Nov 2025 05:15:34 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0620f90d617bf0c728028c0832e588717bfb0641da01c0676a65d98fc0e15d28`  
		Last Modified: Tue, 18 Nov 2025 06:54:57 GMT  
		Size: 214.2 MB (214239319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:eec7307ccf0361b096c0a867fb42fb8f3f9123a6428875bbe63b49e42ee69397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f1187cf959d77b60c4506ad50860db4d263a3ec5c50464909798c4f5f649d0`

```dockerfile
```

-	Layers:
	-	`sha256:70542988e68a4f1c5f95cdbb38138b9b2408e2b300f5a99dd2d30926f4d268da`  
		Last Modified: Tue, 18 Nov 2025 06:54:25 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:cf7925494803272669575b769293f708d5084d4656bd9b0bd6a4086dbc5837ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220613957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08ed827579b12c3c097073fae9c6474dd75c4777bc26a85d1044472db8cd6a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 04:19:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 04:19:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c356f9e9c92c891333fb1ae718cd8215415ca2152ac62bfc037b5d3045f73`  
		Last Modified: Tue, 18 Nov 2025 04:20:30 GMT  
		Size: 37.5 MB (37498324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7540b58924232b2bb1574d0d8b1e8e792b566628223cfa20c25ed7987eb2a5`  
		Last Modified: Tue, 18 Nov 2025 04:20:28 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee1e2ebe1daf3426bddce8a256b002bc05a59760884fa8994ce596195c497e`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 155.6 MB (155630520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:184a6022b83f622547a2495a9e796bcce797395c321ac0cedb07ceddb26413a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dec425e6b4e3da0dbb5b06398ba32a1f19354510341b5670411f4e32c4f539`

```dockerfile
```

-	Layers:
	-	`sha256:fe6ca29c93fdd0ab41d450123bb49aaa9219b9def1ab330ad7870ff006b06a08`  
		Last Modified: Tue, 18 Nov 2025 06:54:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05f3c539161d72c4a364d2cd1ac4bd997582ef4a623b37dd90c444f53e7829a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287457827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e4810f2701354a5cf718dfbe5a0c2fa0e1fb7fab8bdd19574834e5f02ce71e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 03:37:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:37:33 GMT
WORKDIR /root
# Tue, 18 Nov 2025 03:37:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723c2ae08eef5cb2b007a95641953958457fb3609dbec7cbc9f221c7f47368fe`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 42.3 MB (42293339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818d083b0084d331d2dec2a8191772898e5557a265bb0a65f8aa0e63564bd0d1`  
		Last Modified: Tue, 18 Nov 2025 03:38:24 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1f46bc6c5aefeb405bb3a5c492c869e77e8556d5bbefe9b2005976f225b9`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 213.5 MB (213459193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:8be7b70e1b0b7cad4606e8af8d02cff66089a484b78b502df69af450319f7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd364dcaae13777b5e5251bc5b5e5b05f97ca3e0b3fd2e3d2898bc4c3ff6e72a`

```dockerfile
```

-	Layers:
	-	`sha256:d2284a78f7db258f1faaa3a1107c2b8f864af5d22ee7b6054345d72569e663c5`  
		Last Modified: Tue, 18 Nov 2025 06:54:31 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:c8bc712f21347aad6d0c3cd39199111ddf4f3f137f3e426e43d5b6d1493f430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233891852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7e6980b4837f225aa4f6cc3b93df3c987671b42740652105262f71ef524029`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:40:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 19 Nov 2025 19:40:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 19:40:39 GMT
WORKDIR /root
# Wed, 19 Nov 2025 19:41:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da213c1ee21f21efd577e634d99a65798e6b0e7656870692da1c2eac8842158`  
		Last Modified: Wed, 19 Nov 2025 19:45:54 GMT  
		Size: 41.6 MB (41560760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96193f29a66f7bd8c31765af875186499b40ca5be5f023e0d948d4ed85acebad`  
		Last Modified: Wed, 19 Nov 2025 19:45:49 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae03974c01b46162db481a23a9a00ce9f9556d82e65b3d1eca98a03262e076d`  
		Last Modified: Wed, 19 Nov 2025 19:51:06 GMT  
		Size: 162.5 MB (162490863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:925a00e6fd4c2ba95b31054816561b23857dfc1ef77f90e32875f2f24c7e79f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a99264debe5bf763c4c469cd7486c94416c4ab90cf4a2ef0e7fe13710378bf`

```dockerfile
```

-	Layers:
	-	`sha256:0b5b69fa5afb5567e074aaee573dfb695d0d597c3ca22938865f5519004a7e9d`  
		Last Modified: Wed, 19 Nov 2025 21:53:30 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:f65f34c54c2fd57e115449046af8fe8b640a099682f01c7d459ad52e2aca8a10
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
$ docker pull dart@sha256:d65d30ccbc3e6b00cbbc83946b9ef517cb5531c0fc4da4a60644b9bc331a989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288383491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbb20cd91f9204144cebebc27862fe183455e029fa759e2474c717099e7d38f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 05:14:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 05:14:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:14:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 05:15:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c2529f5cef81aeecc09c6572e1e0dbe33c3a22307a223b8ecfaa82bcf21743`  
		Last Modified: Tue, 18 Nov 2025 05:15:37 GMT  
		Size: 42.5 MB (42494038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4313a42c948bf5c26bf4c6050453a911eb2d1fa3107407e270ee2fc2fddfe5d4`  
		Last Modified: Tue, 18 Nov 2025 05:15:34 GMT  
		Size: 1.9 MB (1873618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0620f90d617bf0c728028c0832e588717bfb0641da01c0676a65d98fc0e15d28`  
		Last Modified: Tue, 18 Nov 2025 06:54:57 GMT  
		Size: 214.2 MB (214239319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:eec7307ccf0361b096c0a867fb42fb8f3f9123a6428875bbe63b49e42ee69397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f1187cf959d77b60c4506ad50860db4d263a3ec5c50464909798c4f5f649d0`

```dockerfile
```

-	Layers:
	-	`sha256:70542988e68a4f1c5f95cdbb38138b9b2408e2b300f5a99dd2d30926f4d268da`  
		Last Modified: Tue, 18 Nov 2025 06:54:25 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:cf7925494803272669575b769293f708d5084d4656bd9b0bd6a4086dbc5837ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220613957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08ed827579b12c3c097073fae9c6474dd75c4777bc26a85d1044472db8cd6a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 04:19:49 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 04:19:49 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:49 GMT
WORKDIR /root
# Tue, 18 Nov 2025 04:19:58 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c356f9e9c92c891333fb1ae718cd8215415ca2152ac62bfc037b5d3045f73`  
		Last Modified: Tue, 18 Nov 2025 04:20:30 GMT  
		Size: 37.5 MB (37498324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7540b58924232b2bb1574d0d8b1e8e792b566628223cfa20c25ed7987eb2a5`  
		Last Modified: Tue, 18 Nov 2025 04:20:28 GMT  
		Size: 1.3 MB (1275121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee1e2ebe1daf3426bddce8a256b002bc05a59760884fa8994ce596195c497e`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 155.6 MB (155630520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:184a6022b83f622547a2495a9e796bcce797395c321ac0cedb07ceddb26413a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dec425e6b4e3da0dbb5b06398ba32a1f19354510341b5670411f4e32c4f539`

```dockerfile
```

-	Layers:
	-	`sha256:fe6ca29c93fdd0ab41d450123bb49aaa9219b9def1ab330ad7870ff006b06a08`  
		Last Modified: Tue, 18 Nov 2025 06:54:29 GMT  
		Size: 19.0 KB (19024 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:05f3c539161d72c4a364d2cd1ac4bd997582ef4a623b37dd90c444f53e7829a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287457827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e4810f2701354a5cf718dfbe5a0c2fa0e1fb7fab8bdd19574834e5f02ce71e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 03:37:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 03:37:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:37:33 GMT
WORKDIR /root
# Tue, 18 Nov 2025 03:37:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723c2ae08eef5cb2b007a95641953958457fb3609dbec7cbc9f221c7f47368fe`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 42.3 MB (42293339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818d083b0084d331d2dec2a8191772898e5557a265bb0a65f8aa0e63564bd0d1`  
		Last Modified: Tue, 18 Nov 2025 03:38:24 GMT  
		Size: 1.6 MB (1566653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1f46bc6c5aefeb405bb3a5c492c869e77e8556d5bbefe9b2005976f225b9`  
		Last Modified: Tue, 18 Nov 2025 06:54:59 GMT  
		Size: 213.5 MB (213459193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8be7b70e1b0b7cad4606e8af8d02cff66089a484b78b502df69af450319f7943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd364dcaae13777b5e5251bc5b5e5b05f97ca3e0b3fd2e3d2898bc4c3ff6e72a`

```dockerfile
```

-	Layers:
	-	`sha256:d2284a78f7db258f1faaa3a1107c2b8f864af5d22ee7b6054345d72569e663c5`  
		Last Modified: Tue, 18 Nov 2025 06:54:31 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:c8bc712f21347aad6d0c3cd39199111ddf4f3f137f3e426e43d5b6d1493f430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233891852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7e6980b4837f225aa4f6cc3b93df3c987671b42740652105262f71ef524029`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:40:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 19 Nov 2025 19:40:39 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 19 Nov 2025 19:40:39 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 19:40:39 GMT
WORKDIR /root
# Wed, 19 Nov 2025 19:41:23 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=1874c0ced93244389bd4e91617856c5677839e02d8c3ab66e473bd9632fc235d;             SDK_ARCH="x64";;         armhf)             DART_SHA256=729d2b5486db8606d973084e1036739396b4556834c03c75940e36ca6a7ce276;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9273ebe3bda6e1ab009b0a4c446d2e33db5f30142939bf0534d89c6dee40285e;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f4a5a6b131b4d32cc6014b97c53d75f9f7b44b33993c96868dd0b7d17debde69;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.11.0-93.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da213c1ee21f21efd577e634d99a65798e6b0e7656870692da1c2eac8842158`  
		Last Modified: Wed, 19 Nov 2025 19:45:54 GMT  
		Size: 41.6 MB (41560760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96193f29a66f7bd8c31765af875186499b40ca5be5f023e0d948d4ed85acebad`  
		Last Modified: Wed, 19 Nov 2025 19:45:49 GMT  
		Size: 1.6 MB (1567071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae03974c01b46162db481a23a9a00ce9f9556d82e65b3d1eca98a03262e076d`  
		Last Modified: Wed, 19 Nov 2025 19:51:06 GMT  
		Size: 162.5 MB (162490863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:925a00e6fd4c2ba95b31054816561b23857dfc1ef77f90e32875f2f24c7e79f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a99264debe5bf763c4c469cd7486c94416c4ab90cf4a2ef0e7fe13710378bf`

```dockerfile
```

-	Layers:
	-	`sha256:0b5b69fa5afb5567e074aaee573dfb695d0d597c3ca22938865f5519004a7e9d`  
		Last Modified: Wed, 19 Nov 2025 21:53:30 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:45e435a36a9da1422b2170dc9a91fdff21043be7f255c0348b3b59f949d5036c
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
$ docker pull dart@sha256:fa4aeb6c63fbe122446e102663a63a10b014d0107a9b43191557bd58e1105ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18729fcb2ff834aaf2ff55a539cc4cc3f5beac867ebbfb8fe0d5c8b7f83868d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 21:59:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 21:59:42 GMT
WORKDIR /root
# Tue, 18 Nov 2025 21:59:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1658fcc370faef9607684c67d9c86f881f21cfc67db6934af7f1f3b86b204`  
		Last Modified: Tue, 18 Nov 2025 22:00:46 GMT  
		Size: 42.5 MB (42494135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7318d63717dd94a619a165256471fba0d51920a1be2a23dba393193dd95cdf`  
		Last Modified: Tue, 18 Nov 2025 22:00:38 GMT  
		Size: 1.9 MB (1873622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09063cf43129eb5a67ada65d1890eb822290e7b23fb359550f75d14dbbe7cfbb`  
		Last Modified: Wed, 19 Nov 2025 00:53:59 GMT  
		Size: 213.1 MB (213121454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:f9f8e1f72fea1bbaf8804577ec38d68253e2183c19f04a13cbbc91b1795a3ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249a4f9a4efc9706dc6e60bd58708f2e62b7f2066bac0fc074baa3f9796fa291`

```dockerfile
```

-	Layers:
	-	`sha256:0b39fcea42499b23179ee0346b6d3e23219f314790b386ae0a18459fb3983923`  
		Last Modified: Wed, 19 Nov 2025 00:53:24 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb0e291a4c0b4c2f609ee143271a881bb8de1f2af7a6f706e55e106c445b995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219903719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eff55435245fcb5ad77f40a0906aa65c0bd80bb644066952ad9b67aa2e50b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:57 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c891ff91f312c704bbf333d1b15418843367b81c6b93638049944c15d532bf4`  
		Last Modified: Tue, 18 Nov 2025 22:02:58 GMT  
		Size: 37.5 MB (37498240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852375714e4e1049db217ce75acd1271f96e14b52b191e2e662730d7b616ec3`  
		Last Modified: Tue, 18 Nov 2025 22:02:54 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34517ff1c05bf15a9e61c4b87dd8232f73841d72865b047b31b625456f37c2c`  
		Last Modified: Wed, 19 Nov 2025 00:54:11 GMT  
		Size: 154.9 MB (154920365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:adde0b6ff4acf32dc018b0d6d37badeb0196e2e26b2395808878a04f83361c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77af9b3e9077badc7851b2149a4fb2b401d05d65a504f5a7957eb72a5350d55`

```dockerfile
```

-	Layers:
	-	`sha256:60325e55d4f814bbf831f4d219af19ca47382973650b36e9822294af3cd28db2`  
		Last Modified: Wed, 19 Nov 2025 00:53:27 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:03910e75eb80e0877ce681918e25ba5614dfa5d0a47be0831698c7b6523e51cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286359902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ddce5fe73a5ab577b3c0ab22071624b4e58b658b96ec99133e9c556a76d0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:47 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c282fd9d3f077502877d9bd6db1698bad289aac728ca062900cb21c7e964164`  
		Last Modified: Tue, 18 Nov 2025 22:03:17 GMT  
		Size: 42.3 MB (42293267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6c59386460b3afe249ed86ef0b7f0eb342787a6af6e3261fd1b4f8c24818e`  
		Last Modified: Tue, 18 Nov 2025 22:03:11 GMT  
		Size: 1.6 MB (1566643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f36a03cf48657a271ec16e657cb251e2094626c7fa9772b99fcc9c4c0a972`  
		Last Modified: Tue, 18 Nov 2025 22:18:31 GMT  
		Size: 212.4 MB (212361350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:88e91c39dda8324af3a2c5b906047a902708798b0d444207c49a8058e6bcf34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3711cbc9f46172d637e6f56d547a98426fbd05898d3a91009f11ed7163de37f`

```dockerfile
```

-	Layers:
	-	`sha256:7b83b5d3157271c0d042f630a42c60adf39c61ec39b32923dd56fc467a5126d9`  
		Last Modified: Wed, 19 Nov 2025 00:53:31 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:f97d4d6d26bb1216063e195bb7f5b45903dfc0ca011eee5e7a53e56e794c3c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e93eda7f17e0597108f80c4b01cf0eef8f93dd88292faa6b42f159a396373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 22:34:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 20 Nov 2025 22:34:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 22:34:59 GMT
WORKDIR /root
# Thu, 20 Nov 2025 22:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2224e8dbec4ac7444b327f03c8cb2effbf7ef809baca565fa3b7f851a157a`  
		Last Modified: Thu, 20 Nov 2025 22:40:19 GMT  
		Size: 41.6 MB (41560749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47932c01ba87b2fd89d28da4c231e8bda0b067fc21110ed989f19d9f5025f48`  
		Last Modified: Thu, 20 Nov 2025 22:40:13 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609188b99f95f73c3295f006e51f0f1e62ce3fdd70b74d7279dc9a745e93f8a7`  
		Last Modified: Thu, 20 Nov 2025 23:13:06 GMT  
		Size: 161.6 MB (161563764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:1d6d92d4991fbd675c87e8f56e0cb28fd74a122024dc43da74f7ab216582be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9389cc6325ba871c8c05c00a0c13b5691548fb3ee6ea3cf107fdf49bb721a32f`

```dockerfile
```

-	Layers:
	-	`sha256:e262f7ad459d3cf7954e10b44d17b27044153e6d6db3998efdcd3307079c06e3`  
		Last Modified: Fri, 21 Nov 2025 00:53:54 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:45e435a36a9da1422b2170dc9a91fdff21043be7f255c0348b3b59f949d5036c
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
$ docker pull dart@sha256:fa4aeb6c63fbe122446e102663a63a10b014d0107a9b43191557bd58e1105ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18729fcb2ff834aaf2ff55a539cc4cc3f5beac867ebbfb8fe0d5c8b7f83868d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 21:59:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 21:59:42 GMT
WORKDIR /root
# Tue, 18 Nov 2025 21:59:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1658fcc370faef9607684c67d9c86f881f21cfc67db6934af7f1f3b86b204`  
		Last Modified: Tue, 18 Nov 2025 22:00:46 GMT  
		Size: 42.5 MB (42494135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7318d63717dd94a619a165256471fba0d51920a1be2a23dba393193dd95cdf`  
		Last Modified: Tue, 18 Nov 2025 22:00:38 GMT  
		Size: 1.9 MB (1873622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09063cf43129eb5a67ada65d1890eb822290e7b23fb359550f75d14dbbe7cfbb`  
		Last Modified: Wed, 19 Nov 2025 00:53:59 GMT  
		Size: 213.1 MB (213121454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f9f8e1f72fea1bbaf8804577ec38d68253e2183c19f04a13cbbc91b1795a3ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249a4f9a4efc9706dc6e60bd58708f2e62b7f2066bac0fc074baa3f9796fa291`

```dockerfile
```

-	Layers:
	-	`sha256:0b39fcea42499b23179ee0346b6d3e23219f314790b386ae0a18459fb3983923`  
		Last Modified: Wed, 19 Nov 2025 00:53:24 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb0e291a4c0b4c2f609ee143271a881bb8de1f2af7a6f706e55e106c445b995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219903719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eff55435245fcb5ad77f40a0906aa65c0bd80bb644066952ad9b67aa2e50b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:57 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c891ff91f312c704bbf333d1b15418843367b81c6b93638049944c15d532bf4`  
		Last Modified: Tue, 18 Nov 2025 22:02:58 GMT  
		Size: 37.5 MB (37498240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852375714e4e1049db217ce75acd1271f96e14b52b191e2e662730d7b616ec3`  
		Last Modified: Tue, 18 Nov 2025 22:02:54 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34517ff1c05bf15a9e61c4b87dd8232f73841d72865b047b31b625456f37c2c`  
		Last Modified: Wed, 19 Nov 2025 00:54:11 GMT  
		Size: 154.9 MB (154920365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:adde0b6ff4acf32dc018b0d6d37badeb0196e2e26b2395808878a04f83361c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77af9b3e9077badc7851b2149a4fb2b401d05d65a504f5a7957eb72a5350d55`

```dockerfile
```

-	Layers:
	-	`sha256:60325e55d4f814bbf831f4d219af19ca47382973650b36e9822294af3cd28db2`  
		Last Modified: Wed, 19 Nov 2025 00:53:27 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:03910e75eb80e0877ce681918e25ba5614dfa5d0a47be0831698c7b6523e51cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286359902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ddce5fe73a5ab577b3c0ab22071624b4e58b658b96ec99133e9c556a76d0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:47 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c282fd9d3f077502877d9bd6db1698bad289aac728ca062900cb21c7e964164`  
		Last Modified: Tue, 18 Nov 2025 22:03:17 GMT  
		Size: 42.3 MB (42293267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6c59386460b3afe249ed86ef0b7f0eb342787a6af6e3261fd1b4f8c24818e`  
		Last Modified: Tue, 18 Nov 2025 22:03:11 GMT  
		Size: 1.6 MB (1566643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f36a03cf48657a271ec16e657cb251e2094626c7fa9772b99fcc9c4c0a972`  
		Last Modified: Tue, 18 Nov 2025 22:18:31 GMT  
		Size: 212.4 MB (212361350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:88e91c39dda8324af3a2c5b906047a902708798b0d444207c49a8058e6bcf34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3711cbc9f46172d637e6f56d547a98426fbd05898d3a91009f11ed7163de37f`

```dockerfile
```

-	Layers:
	-	`sha256:7b83b5d3157271c0d042f630a42c60adf39c61ec39b32923dd56fc467a5126d9`  
		Last Modified: Wed, 19 Nov 2025 00:53:31 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f97d4d6d26bb1216063e195bb7f5b45903dfc0ca011eee5e7a53e56e794c3c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e93eda7f17e0597108f80c4b01cf0eef8f93dd88292faa6b42f159a396373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 22:34:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 20 Nov 2025 22:34:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 22:34:59 GMT
WORKDIR /root
# Thu, 20 Nov 2025 22:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2224e8dbec4ac7444b327f03c8cb2effbf7ef809baca565fa3b7f851a157a`  
		Last Modified: Thu, 20 Nov 2025 22:40:19 GMT  
		Size: 41.6 MB (41560749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47932c01ba87b2fd89d28da4c231e8bda0b067fc21110ed989f19d9f5025f48`  
		Last Modified: Thu, 20 Nov 2025 22:40:13 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609188b99f95f73c3295f006e51f0f1e62ce3fdd70b74d7279dc9a745e93f8a7`  
		Last Modified: Thu, 20 Nov 2025 23:13:06 GMT  
		Size: 161.6 MB (161563764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1d6d92d4991fbd675c87e8f56e0cb28fd74a122024dc43da74f7ab216582be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9389cc6325ba871c8c05c00a0c13b5691548fb3ee6ea3cf107fdf49bb721a32f`

```dockerfile
```

-	Layers:
	-	`sha256:e262f7ad459d3cf7954e10b44d17b27044153e6d6db3998efdcd3307079c06e3`  
		Last Modified: Fri, 21 Nov 2025 00:53:54 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:45e435a36a9da1422b2170dc9a91fdff21043be7f255c0348b3b59f949d5036c
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
$ docker pull dart@sha256:fa4aeb6c63fbe122446e102663a63a10b014d0107a9b43191557bd58e1105ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18729fcb2ff834aaf2ff55a539cc4cc3f5beac867ebbfb8fe0d5c8b7f83868d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 21:59:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 21:59:42 GMT
WORKDIR /root
# Tue, 18 Nov 2025 21:59:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1658fcc370faef9607684c67d9c86f881f21cfc67db6934af7f1f3b86b204`  
		Last Modified: Tue, 18 Nov 2025 22:00:46 GMT  
		Size: 42.5 MB (42494135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7318d63717dd94a619a165256471fba0d51920a1be2a23dba393193dd95cdf`  
		Last Modified: Tue, 18 Nov 2025 22:00:38 GMT  
		Size: 1.9 MB (1873622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09063cf43129eb5a67ada65d1890eb822290e7b23fb359550f75d14dbbe7cfbb`  
		Last Modified: Wed, 19 Nov 2025 00:53:59 GMT  
		Size: 213.1 MB (213121454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:f9f8e1f72fea1bbaf8804577ec38d68253e2183c19f04a13cbbc91b1795a3ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249a4f9a4efc9706dc6e60bd58708f2e62b7f2066bac0fc074baa3f9796fa291`

```dockerfile
```

-	Layers:
	-	`sha256:0b39fcea42499b23179ee0346b6d3e23219f314790b386ae0a18459fb3983923`  
		Last Modified: Wed, 19 Nov 2025 00:53:24 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb0e291a4c0b4c2f609ee143271a881bb8de1f2af7a6f706e55e106c445b995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219903719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eff55435245fcb5ad77f40a0906aa65c0bd80bb644066952ad9b67aa2e50b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:57 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c891ff91f312c704bbf333d1b15418843367b81c6b93638049944c15d532bf4`  
		Last Modified: Tue, 18 Nov 2025 22:02:58 GMT  
		Size: 37.5 MB (37498240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852375714e4e1049db217ce75acd1271f96e14b52b191e2e662730d7b616ec3`  
		Last Modified: Tue, 18 Nov 2025 22:02:54 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34517ff1c05bf15a9e61c4b87dd8232f73841d72865b047b31b625456f37c2c`  
		Last Modified: Wed, 19 Nov 2025 00:54:11 GMT  
		Size: 154.9 MB (154920365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:adde0b6ff4acf32dc018b0d6d37badeb0196e2e26b2395808878a04f83361c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77af9b3e9077badc7851b2149a4fb2b401d05d65a504f5a7957eb72a5350d55`

```dockerfile
```

-	Layers:
	-	`sha256:60325e55d4f814bbf831f4d219af19ca47382973650b36e9822294af3cd28db2`  
		Last Modified: Wed, 19 Nov 2025 00:53:27 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:03910e75eb80e0877ce681918e25ba5614dfa5d0a47be0831698c7b6523e51cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286359902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ddce5fe73a5ab577b3c0ab22071624b4e58b658b96ec99133e9c556a76d0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:47 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c282fd9d3f077502877d9bd6db1698bad289aac728ca062900cb21c7e964164`  
		Last Modified: Tue, 18 Nov 2025 22:03:17 GMT  
		Size: 42.3 MB (42293267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6c59386460b3afe249ed86ef0b7f0eb342787a6af6e3261fd1b4f8c24818e`  
		Last Modified: Tue, 18 Nov 2025 22:03:11 GMT  
		Size: 1.6 MB (1566643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f36a03cf48657a271ec16e657cb251e2094626c7fa9772b99fcc9c4c0a972`  
		Last Modified: Tue, 18 Nov 2025 22:18:31 GMT  
		Size: 212.4 MB (212361350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:88e91c39dda8324af3a2c5b906047a902708798b0d444207c49a8058e6bcf34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3711cbc9f46172d637e6f56d547a98426fbd05898d3a91009f11ed7163de37f`

```dockerfile
```

-	Layers:
	-	`sha256:7b83b5d3157271c0d042f630a42c60adf39c61ec39b32923dd56fc467a5126d9`  
		Last Modified: Wed, 19 Nov 2025 00:53:31 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:f97d4d6d26bb1216063e195bb7f5b45903dfc0ca011eee5e7a53e56e794c3c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e93eda7f17e0597108f80c4b01cf0eef8f93dd88292faa6b42f159a396373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 22:34:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 20 Nov 2025 22:34:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 22:34:59 GMT
WORKDIR /root
# Thu, 20 Nov 2025 22:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2224e8dbec4ac7444b327f03c8cb2effbf7ef809baca565fa3b7f851a157a`  
		Last Modified: Thu, 20 Nov 2025 22:40:19 GMT  
		Size: 41.6 MB (41560749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47932c01ba87b2fd89d28da4c231e8bda0b067fc21110ed989f19d9f5025f48`  
		Last Modified: Thu, 20 Nov 2025 22:40:13 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609188b99f95f73c3295f006e51f0f1e62ce3fdd70b74d7279dc9a745e93f8a7`  
		Last Modified: Thu, 20 Nov 2025 23:13:06 GMT  
		Size: 161.6 MB (161563764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:1d6d92d4991fbd675c87e8f56e0cb28fd74a122024dc43da74f7ab216582be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9389cc6325ba871c8c05c00a0c13b5691548fb3ee6ea3cf107fdf49bb721a32f`

```dockerfile
```

-	Layers:
	-	`sha256:e262f7ad459d3cf7954e10b44d17b27044153e6d6db3998efdcd3307079c06e3`  
		Last Modified: Fri, 21 Nov 2025 00:53:54 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:45e435a36a9da1422b2170dc9a91fdff21043be7f255c0348b3b59f949d5036c
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
$ docker pull dart@sha256:fa4aeb6c63fbe122446e102663a63a10b014d0107a9b43191557bd58e1105ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 MB (287265727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18729fcb2ff834aaf2ff55a539cc4cc3f5beac867ebbfb8fe0d5c8b7f83868d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 21:59:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 21:59:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 21:59:42 GMT
WORKDIR /root
# Tue, 18 Nov 2025 21:59:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1658fcc370faef9607684c67d9c86f881f21cfc67db6934af7f1f3b86b204`  
		Last Modified: Tue, 18 Nov 2025 22:00:46 GMT  
		Size: 42.5 MB (42494135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7318d63717dd94a619a165256471fba0d51920a1be2a23dba393193dd95cdf`  
		Last Modified: Tue, 18 Nov 2025 22:00:38 GMT  
		Size: 1.9 MB (1873622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09063cf43129eb5a67ada65d1890eb822290e7b23fb359550f75d14dbbe7cfbb`  
		Last Modified: Wed, 19 Nov 2025 00:53:59 GMT  
		Size: 213.1 MB (213121454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f9f8e1f72fea1bbaf8804577ec38d68253e2183c19f04a13cbbc91b1795a3ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249a4f9a4efc9706dc6e60bd58708f2e62b7f2066bac0fc074baa3f9796fa291`

```dockerfile
```

-	Layers:
	-	`sha256:0b39fcea42499b23179ee0346b6d3e23219f314790b386ae0a18459fb3983923`  
		Last Modified: Wed, 19 Nov 2025 00:53:24 GMT  
		Size: 20.6 KB (20615 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:bb0e291a4c0b4c2f609ee143271a881bb8de1f2af7a6f706e55e106c445b995f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219903719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21eff55435245fcb5ad77f40a0906aa65c0bd80bb644066952ad9b67aa2e50b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:57 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:57 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:57 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:07 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c891ff91f312c704bbf333d1b15418843367b81c6b93638049944c15d532bf4`  
		Last Modified: Tue, 18 Nov 2025 22:02:58 GMT  
		Size: 37.5 MB (37498240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852375714e4e1049db217ce75acd1271f96e14b52b191e2e662730d7b616ec3`  
		Last Modified: Tue, 18 Nov 2025 22:02:54 GMT  
		Size: 1.3 MB (1275122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34517ff1c05bf15a9e61c4b87dd8232f73841d72865b047b31b625456f37c2c`  
		Last Modified: Wed, 19 Nov 2025 00:54:11 GMT  
		Size: 154.9 MB (154920365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:adde0b6ff4acf32dc018b0d6d37badeb0196e2e26b2395808878a04f83361c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77af9b3e9077badc7851b2149a4fb2b401d05d65a504f5a7957eb72a5350d55`

```dockerfile
```

-	Layers:
	-	`sha256:60325e55d4f814bbf831f4d219af19ca47382973650b36e9822294af3cd28db2`  
		Last Modified: Wed, 19 Nov 2025 00:53:27 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:03910e75eb80e0877ce681918e25ba5614dfa5d0a47be0831698c7b6523e51cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286359902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ddce5fe73a5ab577b3c0ab22071624b4e58b658b96ec99133e9c556a76d0b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Nov 2025 22:01:47 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Nov 2025 22:01:47 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 22:01:47 GMT
WORKDIR /root
# Tue, 18 Nov 2025 22:02:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c282fd9d3f077502877d9bd6db1698bad289aac728ca062900cb21c7e964164`  
		Last Modified: Tue, 18 Nov 2025 22:03:17 GMT  
		Size: 42.3 MB (42293267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd6c59386460b3afe249ed86ef0b7f0eb342787a6af6e3261fd1b4f8c24818e`  
		Last Modified: Tue, 18 Nov 2025 22:03:11 GMT  
		Size: 1.6 MB (1566643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f36a03cf48657a271ec16e657cb251e2094626c7fa9772b99fcc9c4c0a972`  
		Last Modified: Tue, 18 Nov 2025 22:18:31 GMT  
		Size: 212.4 MB (212361350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:88e91c39dda8324af3a2c5b906047a902708798b0d444207c49a8058e6bcf34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3711cbc9f46172d637e6f56d547a98426fbd05898d3a91009f11ed7163de37f`

```dockerfile
```

-	Layers:
	-	`sha256:7b83b5d3157271c0d042f630a42c60adf39c61ec39b32923dd56fc467a5126d9`  
		Last Modified: Wed, 19 Nov 2025 00:53:31 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f97d4d6d26bb1216063e195bb7f5b45903dfc0ca011eee5e7a53e56e794c3c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232964741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46e93eda7f17e0597108f80c4b01cf0eef8f93dd88292faa6b42f159a396373`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 22:34:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 20 Nov 2025 22:34:59 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 20 Nov 2025 22:34:59 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 22:34:59 GMT
WORKDIR /root
# Thu, 20 Nov 2025 22:35:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=a352fd18e0c07aab694bba9cf57e431eddce390550a90449b1ff880fee7736f4;             SDK_ARCH="x64";;         armhf)             DART_SHA256=4b2e148019dfa1c1703ccc86aea45fe711ed09f190d853a26c172b5b962bf5bd;             SDK_ARCH="arm";;         arm64)             DART_SHA256=60d33687806781175723f4cb7def7adf83ee0f981ca997d2eece40f975526b4c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=1c21d9b9223a19b356a493b06b16000645cc45a56dce51db0de96eda8be5381e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.10.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb2224e8dbec4ac7444b327f03c8cb2effbf7ef809baca565fa3b7f851a157a`  
		Last Modified: Thu, 20 Nov 2025 22:40:19 GMT  
		Size: 41.6 MB (41560749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47932c01ba87b2fd89d28da4c231e8bda0b067fc21110ed989f19d9f5025f48`  
		Last Modified: Thu, 20 Nov 2025 22:40:13 GMT  
		Size: 1.6 MB (1567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609188b99f95f73c3295f006e51f0f1e62ce3fdd70b74d7279dc9a745e93f8a7`  
		Last Modified: Thu, 20 Nov 2025 23:13:06 GMT  
		Size: 161.6 MB (161563764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:1d6d92d4991fbd675c87e8f56e0cb28fd74a122024dc43da74f7ab216582be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9389cc6325ba871c8c05c00a0c13b5691548fb3ee6ea3cf107fdf49bb721a32f`

```dockerfile
```

-	Layers:
	-	`sha256:e262f7ad459d3cf7954e10b44d17b27044153e6d6db3998efdcd3307079c06e3`  
		Last Modified: Fri, 21 Nov 2025 00:53:54 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json
