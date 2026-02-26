<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.11`](#dart311)
-	[`dart:3.11-sdk`](#dart311-sdk)
-	[`dart:3.11.1`](#dart3111)
-	[`dart:3.11.1-sdk`](#dart3111-sdk)
-	[`dart:3.12.0-113.2.beta`](#dart3120-1132beta)
-	[`dart:3.12.0-113.2.beta-sdk`](#dart3120-1132beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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

### `dart:3.11` - linux; amd64

```console
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11-sdk`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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

### `dart:3.11-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.1`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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

### `dart:3.11.1` - linux; amd64

```console
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.1` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.1` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.1` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.1` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.1` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.1-sdk`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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

### `dart:3.11.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.1-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12.0-113.2.beta`

```console
$ docker pull dart@sha256:e4d80d890d29ed8184ba242310dd19ab966e93e3580c86d6e9a39aef4d17b775
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

### `dart:3.12.0-113.2.beta` - linux; amd64

```console
$ docker pull dart@sha256:a0958dfffc4400fbe4cae115af46959b7264e86780e9dd24fd6056a3e71eb91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309460253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e525f21eb51f88244f60e1fb36799d6cbbd2bd9068d164d8a9b99ee8a6891247`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:55 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26d5c75a49729dcb3a500c6b135aa554b3875b482c1053c382bb4c1d06bf2`  
		Last Modified: Tue, 24 Feb 2026 19:22:34 GMT  
		Size: 42.5 MB (42492318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639caeb9c2422b00b4a0104d4c820b5e0ae24f4f57e2ea62ecd93238dbf2f346`  
		Last Modified: Tue, 24 Feb 2026 19:22:32 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6243cf8ec8caa0c3fb5f04ab4d019e1a69784de86ffe24ee48e3fe05a054e`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 235.3 MB (235319097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:3616ca0e82ecd87c917d972133917347d1ee4441a38753e8b203c38801241d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c2e651e2272ecec10eb06b84bdf7acf864cd691963223203da49e1485e29f`

```dockerfile
```

-	Layers:
	-	`sha256:12d5aa3859a6ffeaa1f25d274c39fc4b038012adfdc8d0580b68e78de3e9df45`  
		Last Modified: Tue, 24 Feb 2026 19:22:32 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.2.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:893ca3ad1080e110dd552b3afb25a87d1f863c6dc96352bb924f44ee98b69610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224226020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f225c735516c83bd5503a2976813bcd9803a766d12a39364128e62ea6ed997ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:08 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:08 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:08 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5dad2eef2ec67d1d2234fcdf51527fc9340b40fa926552e853c3d8ee01701`  
		Last Modified: Tue, 24 Feb 2026 20:08:37 GMT  
		Size: 37.5 MB (37494629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0602bf8cd2b4f8cc0ff62f57cba5590594aa4771c26bcbacaf56e4fa586edd7e`  
		Last Modified: Tue, 24 Feb 2026 20:08:35 GMT  
		Size: 1.3 MB (1273168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9185498e604b8c26f524c864ff93504057594d6f9cdf29a88c4dd1f09b2184dc`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 159.2 MB (159244446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:e0e5a4ef74307f5a07bc18e8dfc2dda1d0ca6d27411fa6b09854cd1457db8c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdd3934e69aeedd82fd25839106d759c5943a8eec9e63f2c7abd8cc0deb3138`

```dockerfile
```

-	Layers:
	-	`sha256:3d858f19a858c40ea9539a4ab1961ccfefbac29ab98ed7c05a31c0c59e89e366`  
		Last Modified: Tue, 24 Feb 2026 20:08:35 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.2.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c39ffa192a593b6e61cadb71a34a2da842682816e56888679729656760427e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e803af2068ed8873aec0aaedc9dbe0b587e17f8f73655f96697887127ec6c81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:33 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275ce614eff7bfd6dd4a8f0b4ee9dc1946a530cd0eea82e6a31308984aac8861`  
		Last Modified: Tue, 24 Feb 2026 19:27:14 GMT  
		Size: 42.3 MB (42291968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fcc034e7ca757f47c03df7d06bdaf892e1f6c56f1057b94fbd897ced9a80e0`  
		Last Modified: Tue, 24 Feb 2026 19:27:13 GMT  
		Size: 1.6 MB (1564524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e7cc156019f686116aa5c63c229c3ba0e43343a7696578793e295384ccc287`  
		Last Modified: Tue, 24 Feb 2026 19:27:18 GMT  
		Size: 233.9 MB (233850335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:6568d58f4f97408249ed785e2f1f6e1ec2ee05112d564a668888215a52f5e0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eb93a998152652877d7edfaf88a534fd638554fca04da080fbf8297816a62f`

```dockerfile
```

-	Layers:
	-	`sha256:bd5a884ddbaed2129272ec6af9b5eebe76e53a6dd16a31fb242e7cf2b1987b53`  
		Last Modified: Tue, 24 Feb 2026 19:27:12 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.2.beta` - linux; riscv64

```console
$ docker pull dart@sha256:acf96245efe2823a10de32c3e177477022a188f24db2777d6b846c23ba0ddfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253221364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff7a27ee39f7e6197b62ff0ebc8091478b6412a97ca047658e29ee4a2a1aaed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:53:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd42cf2d325d135018ebbd1f57ce19f308a6bdb4b79bb7c78b871e3febd5ba`  
		Last Modified: Thu, 26 Feb 2026 21:58:39 GMT  
		Size: 181.8 MB (181819528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.2.beta` - unknown; unknown

```console
$ docker pull dart@sha256:be74cb80505517e1e57a186d757c3d237e367248ab2c5d1b8f4350164236cec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bfa732734865735afaa5293919b43717c39b1176d0b57ef30dd90c8e2174d4`

```dockerfile
```

-	Layers:
	-	`sha256:ae0cdf1926dc673af79d7728957d4c0a1ffd5762dfc9f188e0945f7578f64e53`  
		Last Modified: Thu, 26 Feb 2026 21:58:11 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12.0-113.2.beta-sdk`

```console
$ docker pull dart@sha256:e4d80d890d29ed8184ba242310dd19ab966e93e3580c86d6e9a39aef4d17b775
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

### `dart:3.12.0-113.2.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:a0958dfffc4400fbe4cae115af46959b7264e86780e9dd24fd6056a3e71eb91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309460253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e525f21eb51f88244f60e1fb36799d6cbbd2bd9068d164d8a9b99ee8a6891247`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:55 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26d5c75a49729dcb3a500c6b135aa554b3875b482c1053c382bb4c1d06bf2`  
		Last Modified: Tue, 24 Feb 2026 19:22:34 GMT  
		Size: 42.5 MB (42492318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639caeb9c2422b00b4a0104d4c820b5e0ae24f4f57e2ea62ecd93238dbf2f346`  
		Last Modified: Tue, 24 Feb 2026 19:22:32 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6243cf8ec8caa0c3fb5f04ab4d019e1a69784de86ffe24ee48e3fe05a054e`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 235.3 MB (235319097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3616ca0e82ecd87c917d972133917347d1ee4441a38753e8b203c38801241d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c2e651e2272ecec10eb06b84bdf7acf864cd691963223203da49e1485e29f`

```dockerfile
```

-	Layers:
	-	`sha256:12d5aa3859a6ffeaa1f25d274c39fc4b038012adfdc8d0580b68e78de3e9df45`  
		Last Modified: Tue, 24 Feb 2026 19:22:32 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.2.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:893ca3ad1080e110dd552b3afb25a87d1f863c6dc96352bb924f44ee98b69610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224226020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f225c735516c83bd5503a2976813bcd9803a766d12a39364128e62ea6ed997ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:08 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:08 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:08 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5dad2eef2ec67d1d2234fcdf51527fc9340b40fa926552e853c3d8ee01701`  
		Last Modified: Tue, 24 Feb 2026 20:08:37 GMT  
		Size: 37.5 MB (37494629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0602bf8cd2b4f8cc0ff62f57cba5590594aa4771c26bcbacaf56e4fa586edd7e`  
		Last Modified: Tue, 24 Feb 2026 20:08:35 GMT  
		Size: 1.3 MB (1273168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9185498e604b8c26f524c864ff93504057594d6f9cdf29a88c4dd1f09b2184dc`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 159.2 MB (159244446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e0e5a4ef74307f5a07bc18e8dfc2dda1d0ca6d27411fa6b09854cd1457db8c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdd3934e69aeedd82fd25839106d759c5943a8eec9e63f2c7abd8cc0deb3138`

```dockerfile
```

-	Layers:
	-	`sha256:3d858f19a858c40ea9539a4ab1961ccfefbac29ab98ed7c05a31c0c59e89e366`  
		Last Modified: Tue, 24 Feb 2026 20:08:35 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.2.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c39ffa192a593b6e61cadb71a34a2da842682816e56888679729656760427e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e803af2068ed8873aec0aaedc9dbe0b587e17f8f73655f96697887127ec6c81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:33 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275ce614eff7bfd6dd4a8f0b4ee9dc1946a530cd0eea82e6a31308984aac8861`  
		Last Modified: Tue, 24 Feb 2026 19:27:14 GMT  
		Size: 42.3 MB (42291968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fcc034e7ca757f47c03df7d06bdaf892e1f6c56f1057b94fbd897ced9a80e0`  
		Last Modified: Tue, 24 Feb 2026 19:27:13 GMT  
		Size: 1.6 MB (1564524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e7cc156019f686116aa5c63c229c3ba0e43343a7696578793e295384ccc287`  
		Last Modified: Tue, 24 Feb 2026 19:27:18 GMT  
		Size: 233.9 MB (233850335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6568d58f4f97408249ed785e2f1f6e1ec2ee05112d564a668888215a52f5e0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eb93a998152652877d7edfaf88a534fd638554fca04da080fbf8297816a62f`

```dockerfile
```

-	Layers:
	-	`sha256:bd5a884ddbaed2129272ec6af9b5eebe76e53a6dd16a31fb242e7cf2b1987b53`  
		Last Modified: Tue, 24 Feb 2026 19:27:12 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.0-113.2.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:acf96245efe2823a10de32c3e177477022a188f24db2777d6b846c23ba0ddfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253221364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff7a27ee39f7e6197b62ff0ebc8091478b6412a97ca047658e29ee4a2a1aaed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:53:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd42cf2d325d135018ebbd1f57ce19f308a6bdb4b79bb7c78b871e3febd5ba`  
		Last Modified: Thu, 26 Feb 2026 21:58:39 GMT  
		Size: 181.8 MB (181819528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.0-113.2.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:be74cb80505517e1e57a186d757c3d237e367248ab2c5d1b8f4350164236cec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bfa732734865735afaa5293919b43717c39b1176d0b57ef30dd90c8e2174d4`

```dockerfile
```

-	Layers:
	-	`sha256:ae0cdf1926dc673af79d7728957d4c0a1ffd5762dfc9f188e0945f7578f64e53`  
		Last Modified: Thu, 26 Feb 2026 21:58:11 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:e4d80d890d29ed8184ba242310dd19ab966e93e3580c86d6e9a39aef4d17b775
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
$ docker pull dart@sha256:a0958dfffc4400fbe4cae115af46959b7264e86780e9dd24fd6056a3e71eb91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309460253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e525f21eb51f88244f60e1fb36799d6cbbd2bd9068d164d8a9b99ee8a6891247`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:55 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26d5c75a49729dcb3a500c6b135aa554b3875b482c1053c382bb4c1d06bf2`  
		Last Modified: Tue, 24 Feb 2026 19:22:34 GMT  
		Size: 42.5 MB (42492318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639caeb9c2422b00b4a0104d4c820b5e0ae24f4f57e2ea62ecd93238dbf2f346`  
		Last Modified: Tue, 24 Feb 2026 19:22:32 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6243cf8ec8caa0c3fb5f04ab4d019e1a69784de86ffe24ee48e3fe05a054e`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 235.3 MB (235319097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:3616ca0e82ecd87c917d972133917347d1ee4441a38753e8b203c38801241d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c2e651e2272ecec10eb06b84bdf7acf864cd691963223203da49e1485e29f`

```dockerfile
```

-	Layers:
	-	`sha256:12d5aa3859a6ffeaa1f25d274c39fc4b038012adfdc8d0580b68e78de3e9df45`  
		Last Modified: Tue, 24 Feb 2026 19:22:32 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:893ca3ad1080e110dd552b3afb25a87d1f863c6dc96352bb924f44ee98b69610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224226020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f225c735516c83bd5503a2976813bcd9803a766d12a39364128e62ea6ed997ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:08 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:08 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:08 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5dad2eef2ec67d1d2234fcdf51527fc9340b40fa926552e853c3d8ee01701`  
		Last Modified: Tue, 24 Feb 2026 20:08:37 GMT  
		Size: 37.5 MB (37494629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0602bf8cd2b4f8cc0ff62f57cba5590594aa4771c26bcbacaf56e4fa586edd7e`  
		Last Modified: Tue, 24 Feb 2026 20:08:35 GMT  
		Size: 1.3 MB (1273168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9185498e604b8c26f524c864ff93504057594d6f9cdf29a88c4dd1f09b2184dc`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 159.2 MB (159244446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:e0e5a4ef74307f5a07bc18e8dfc2dda1d0ca6d27411fa6b09854cd1457db8c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdd3934e69aeedd82fd25839106d759c5943a8eec9e63f2c7abd8cc0deb3138`

```dockerfile
```

-	Layers:
	-	`sha256:3d858f19a858c40ea9539a4ab1961ccfefbac29ab98ed7c05a31c0c59e89e366`  
		Last Modified: Tue, 24 Feb 2026 20:08:35 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c39ffa192a593b6e61cadb71a34a2da842682816e56888679729656760427e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e803af2068ed8873aec0aaedc9dbe0b587e17f8f73655f96697887127ec6c81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:33 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275ce614eff7bfd6dd4a8f0b4ee9dc1946a530cd0eea82e6a31308984aac8861`  
		Last Modified: Tue, 24 Feb 2026 19:27:14 GMT  
		Size: 42.3 MB (42291968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fcc034e7ca757f47c03df7d06bdaf892e1f6c56f1057b94fbd897ced9a80e0`  
		Last Modified: Tue, 24 Feb 2026 19:27:13 GMT  
		Size: 1.6 MB (1564524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e7cc156019f686116aa5c63c229c3ba0e43343a7696578793e295384ccc287`  
		Last Modified: Tue, 24 Feb 2026 19:27:18 GMT  
		Size: 233.9 MB (233850335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:6568d58f4f97408249ed785e2f1f6e1ec2ee05112d564a668888215a52f5e0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eb93a998152652877d7edfaf88a534fd638554fca04da080fbf8297816a62f`

```dockerfile
```

-	Layers:
	-	`sha256:bd5a884ddbaed2129272ec6af9b5eebe76e53a6dd16a31fb242e7cf2b1987b53`  
		Last Modified: Tue, 24 Feb 2026 19:27:12 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:acf96245efe2823a10de32c3e177477022a188f24db2777d6b846c23ba0ddfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253221364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff7a27ee39f7e6197b62ff0ebc8091478b6412a97ca047658e29ee4a2a1aaed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:53:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd42cf2d325d135018ebbd1f57ce19f308a6bdb4b79bb7c78b871e3febd5ba`  
		Last Modified: Thu, 26 Feb 2026 21:58:39 GMT  
		Size: 181.8 MB (181819528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:be74cb80505517e1e57a186d757c3d237e367248ab2c5d1b8f4350164236cec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bfa732734865735afaa5293919b43717c39b1176d0b57ef30dd90c8e2174d4`

```dockerfile
```

-	Layers:
	-	`sha256:ae0cdf1926dc673af79d7728957d4c0a1ffd5762dfc9f188e0945f7578f64e53`  
		Last Modified: Thu, 26 Feb 2026 21:58:11 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:e4d80d890d29ed8184ba242310dd19ab966e93e3580c86d6e9a39aef4d17b775
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
$ docker pull dart@sha256:a0958dfffc4400fbe4cae115af46959b7264e86780e9dd24fd6056a3e71eb91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309460253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e525f21eb51f88244f60e1fb36799d6cbbd2bd9068d164d8a9b99ee8a6891247`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:55 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:55 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:55 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:55 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26d5c75a49729dcb3a500c6b135aa554b3875b482c1053c382bb4c1d06bf2`  
		Last Modified: Tue, 24 Feb 2026 19:22:34 GMT  
		Size: 42.5 MB (42492318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639caeb9c2422b00b4a0104d4c820b5e0ae24f4f57e2ea62ecd93238dbf2f346`  
		Last Modified: Tue, 24 Feb 2026 19:22:32 GMT  
		Size: 1.9 MB (1870174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6243cf8ec8caa0c3fb5f04ab4d019e1a69784de86ffe24ee48e3fe05a054e`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 235.3 MB (235319097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3616ca0e82ecd87c917d972133917347d1ee4441a38753e8b203c38801241d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c2e651e2272ecec10eb06b84bdf7acf864cd691963223203da49e1485e29f`

```dockerfile
```

-	Layers:
	-	`sha256:12d5aa3859a6ffeaa1f25d274c39fc4b038012adfdc8d0580b68e78de3e9df45`  
		Last Modified: Tue, 24 Feb 2026 19:22:32 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:893ca3ad1080e110dd552b3afb25a87d1f863c6dc96352bb924f44ee98b69610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224226020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f225c735516c83bd5503a2976813bcd9803a766d12a39364128e62ea6ed997ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:08 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:08 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:08 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:08 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:16 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5dad2eef2ec67d1d2234fcdf51527fc9340b40fa926552e853c3d8ee01701`  
		Last Modified: Tue, 24 Feb 2026 20:08:37 GMT  
		Size: 37.5 MB (37494629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0602bf8cd2b4f8cc0ff62f57cba5590594aa4771c26bcbacaf56e4fa586edd7e`  
		Last Modified: Tue, 24 Feb 2026 20:08:35 GMT  
		Size: 1.3 MB (1273168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9185498e604b8c26f524c864ff93504057594d6f9cdf29a88c4dd1f09b2184dc`  
		Last Modified: Tue, 24 Feb 2026 20:08:39 GMT  
		Size: 159.2 MB (159244446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e0e5a4ef74307f5a07bc18e8dfc2dda1d0ca6d27411fa6b09854cd1457db8c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdd3934e69aeedd82fd25839106d759c5943a8eec9e63f2c7abd8cc0deb3138`

```dockerfile
```

-	Layers:
	-	`sha256:3d858f19a858c40ea9539a4ab1961ccfefbac29ab98ed7c05a31c0c59e89e366`  
		Last Modified: Tue, 24 Feb 2026 20:08:35 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:c39ffa192a593b6e61cadb71a34a2da842682816e56888679729656760427e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307846957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e803af2068ed8873aec0aaedc9dbe0b587e17f8f73655f96697887127ec6c81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:33 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:33 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:33 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:33 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:46 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275ce614eff7bfd6dd4a8f0b4ee9dc1946a530cd0eea82e6a31308984aac8861`  
		Last Modified: Tue, 24 Feb 2026 19:27:14 GMT  
		Size: 42.3 MB (42291968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fcc034e7ca757f47c03df7d06bdaf892e1f6c56f1057b94fbd897ced9a80e0`  
		Last Modified: Tue, 24 Feb 2026 19:27:13 GMT  
		Size: 1.6 MB (1564524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e7cc156019f686116aa5c63c229c3ba0e43343a7696578793e295384ccc287`  
		Last Modified: Tue, 24 Feb 2026 19:27:18 GMT  
		Size: 233.9 MB (233850335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6568d58f4f97408249ed785e2f1f6e1ec2ee05112d564a668888215a52f5e0a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eb93a998152652877d7edfaf88a534fd638554fca04da080fbf8297816a62f`

```dockerfile
```

-	Layers:
	-	`sha256:bd5a884ddbaed2129272ec6af9b5eebe76e53a6dd16a31fb242e7cf2b1987b53`  
		Last Modified: Tue, 24 Feb 2026 19:27:12 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:acf96245efe2823a10de32c3e177477022a188f24db2777d6b846c23ba0ddfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253221364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff7a27ee39f7e6197b62ff0ebc8091478b6412a97ca047658e29ee4a2a1aaed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:53:57 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=0cde5d4d710532c9ff01dbbf94c7bcdcff46cdd7f376ca10befa0c697ad05c3c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=f1d8494c38e400c484f697aecf97da0a2dc584cf4104dc18012ff5511af4db39;             SDK_ARCH="arm";;         arm64)             DART_SHA256=5eda41ac9adb63fb887b7d4b2a1def316560b8ac3c06b80860e8fd589a0d5150;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3addb48c46e41044ba186c184c2ae575cd3029236395d5b2d3c548d276302401;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-113.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd42cf2d325d135018ebbd1f57ce19f308a6bdb4b79bb7c78b871e3febd5ba`  
		Last Modified: Thu, 26 Feb 2026 21:58:39 GMT  
		Size: 181.8 MB (181819528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:be74cb80505517e1e57a186d757c3d237e367248ab2c5d1b8f4350164236cec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bfa732734865735afaa5293919b43717c39b1176d0b57ef30dd90c8e2174d4`

```dockerfile
```

-	Layers:
	-	`sha256:ae0cdf1926dc673af79d7728957d4c0a1ffd5762dfc9f188e0945f7578f64e53`  
		Last Modified: Thu, 26 Feb 2026 21:58:11 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:e3ea62cbe54470e5cc4c31cbc85693aa9b0b01723521baf0be634ea3597e1f5d
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
$ docker pull dart@sha256:a65a122371697a370b0d92494153849b975a1b3b31439d5e00a10adc1cb68cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307078454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d716c55938b238835332951a00bd2eb59ba6d2ee453f7116b9330cbcce0944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:21:54 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:21:54 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:21:54 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:22:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cca34bbfa78544772171ad6feb31a703cdfcf16bd7c4bcb7887be1a80847e`  
		Last Modified: Tue, 24 Feb 2026 19:22:33 GMT  
		Size: 42.5 MB (42492297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096946df2b65a1445800d274da6d6d968eff32522f27fa501c1ffe41b68a3e49`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 1.9 MB (1870163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad851a2efa89a226d1dd2de3c2ee267ceceecd4af60a25fa03fe99e33b7e71ec`  
		Last Modified: Tue, 24 Feb 2026 19:22:37 GMT  
		Size: 232.9 MB (232937330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8faf56f2168cec7a44f4dd88c7503275c17e3f418cdeb65bb8a47efa7aaaff34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b6af7f53ec82afc087f7a93c977ea0fe2ed30b56e484a88d980e8ee572ee4`

```dockerfile
```

-	Layers:
	-	`sha256:d24dc0dfdb2fff39856f19b0f469413dc9acd620f72c8e9c0c3a5a11170ea53c`  
		Last Modified: Tue, 24 Feb 2026 19:22:31 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:9b51681f24ce0021c7425228dff567d12ea224cbe1c4d92ea8a91460b5cb2b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222903041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144150cff24fee0d4e64effbe4d507924f146c6338cb1f95a74ebbec1319801d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 20:08:02 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:02 GMT
WORKDIR /root
# Tue, 24 Feb 2026 20:08:10 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6c691e32f18bfa78558b54a419af4c094ac4f646129f5a304d57094b3a133e`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 37.5 MB (37494610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6dccb597ee6ded5ec69bb8232a71a0dac91030b7b89cc91e30a4617716c2a`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 MB (1273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f78bc4992a9cc0a71ad4359e45d32c02e836e66b1f18908ea46a8643f30a61`  
		Last Modified: Tue, 24 Feb 2026 20:08:33 GMT  
		Size: 157.9 MB (157921498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:f83ec5644f8b2b5c3c8c3c9c8641f3c517bd29eef1a10422e7fd7cf3ea625a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fa860ebbe31412d1b796484530c8977632f46901c40e959b5954b17b0aeb72`

```dockerfile
```

-	Layers:
	-	`sha256:9cad6fbe4758047e7694049f647722cb6fac1d7998a8ba88238059ecb934aefc`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:75b7d635e8017bedfb7558b673e86d06d296c5e2e4928094d361dea08a2e33d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305432790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08262d25efa06630d26613096ad8569fcbae1e4a76c6282c25b7fed371ff2c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 24 Feb 2026 19:26:13 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 24 Feb 2026 19:26:13 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:13 GMT
WORKDIR /root
# Tue, 24 Feb 2026 19:26:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0817a6b12277453cbb8c6769167bda699e33a67c6b6f7728471333fd409234b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 42.3 MB (42291780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd117eca6678bea966f82c3670c899371d76ab1831faf88cca36aba6a9b152`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 1.6 MB (1564525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974025aa8251e00a687a16e8110c92efa7be829da96a4fc60097c79eba30b243`  
		Last Modified: Tue, 24 Feb 2026 19:26:56 GMT  
		Size: 231.4 MB (231436355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:41f5ea01f073f96696a4d8066ab95d06db8ce516293223eef647fe73f5cdf873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcac1eeaf18c60b98ddb7c4a70d4c07f54262ee40fe793278c498cf642574f0`

```dockerfile
```

-	Layers:
	-	`sha256:ec630e8c02811815587c511be77ff5b26e883a970894a3cac50f4178a4c75d49`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:3c50bd3f77c48dabf0745da10733e901a29f50f48375204ffce8b1f8cb3d26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251885792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbe8353f4bf2c2b74bbfc9d6cd971f71c61c6e854327256bd0e0dfeeb70fb2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:47:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 26 Feb 2026 21:47:17 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 26 Feb 2026 21:47:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 21:47:17 GMT
WORKDIR /root
# Thu, 26 Feb 2026 21:48:05 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=cffb8fa4afb777c2630c66311bf59eb034cd3ea0c7f94ad326e1a62c6aa9c272;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69afd778175725c9ef25a7d6ca52c1a84f0e803cd8e8c39b76ff7667e7933d0a;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17645c94014b1b46a100e4135b64235cf9c19f9c9a3fb814959ae8293f35e98c;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=7acca59fa74b057b78e4e8a1c3dba32cd5f8dceead5e7a04dd2e472ecc52e11c;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8005b5410669f900e219d8f1011496036e8e069aa48a198a6760555d1e565862`  
		Last Modified: Thu, 26 Feb 2026 21:52:24 GMT  
		Size: 41.6 MB (41560724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b398538cbb3cf53074f900bb3c39189de10e24ab8ad79bc08944898c0008d0`  
		Last Modified: Thu, 26 Feb 2026 21:52:08 GMT  
		Size: 1.6 MB (1564663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb387d36d548d74ab36773195694e1529dca0153f6b401118c2fad500d6a3be`  
		Last Modified: Thu, 26 Feb 2026 21:52:43 GMT  
		Size: 180.5 MB (180483956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:b2100c2dbdb91555037b5c28a91c8690920255dd893f5c37769d0ed072fce4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de089cc2eb0543729a77991a9982b076142756be16a0561e5b7d667a651270`

```dockerfile
```

-	Layers:
	-	`sha256:36a836d347e4af15c77b9ab5afc85d735357d7d81cfc4fd67d121798ac3a6a2c`  
		Last Modified: Thu, 26 Feb 2026 21:52:05 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json
