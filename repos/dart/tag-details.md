<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.12`](#dart312)
-	[`dart:3.12-sdk`](#dart312-sdk)
-	[`dart:3.12.1`](#dart3121)
-	[`dart:3.12.1-sdk`](#dart3121-sdk)
-	[`dart:3.13.0-103.1.beta`](#dart3130-1031beta)
-	[`dart:3.13.0-103.1.beta-sdk`](#dart3130-1031beta-sdk)
-	[`dart:beta`](#dartbeta)
-	[`dart:beta-sdk`](#dartbeta-sdk)
-	[`dart:latest`](#dartlatest)
-	[`dart:sdk`](#dartsdk)
-	[`dart:stable`](#dartstable)
-	[`dart:stable-sdk`](#dartstable-sdk)

## `dart:3`

```console
$ docker pull dart@sha256:3705781e19ca2689f0358fad861087149f392e44b2058254835beca1a58b8eda
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
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:24e06ecf7d936658613dcb03c72477fa7ddc70798695a1cb8cd7feb9718c77c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248327744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4369db773cde4ecc31a6d3e5f6d3760a7fc220cc4e7bf2377c215ded4ab48a90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:05:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b240da7f78e851f44ebaad3b387956d9ae27eeb3ff3b62c7df96eb90470757f`  
		Last Modified: Thu, 21 May 2026 14:10:06 GMT  
		Size: 176.9 MB (176908111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:d8180fdca39443d0c3f6bfce415b743686ca50dc9c2ae4c5553b7fbbda4454b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb9384d09e7f62df4db0b577166165a3183947d1c0494b013b7b321cc4a773`

```dockerfile
```

-	Layers:
	-	`sha256:553bb64621759abdbfe8faa8153be1b26999eac959dca86947e53c86f0eab66d`  
		Last Modified: Thu, 21 May 2026 14:09:32 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:3705781e19ca2689f0358fad861087149f392e44b2058254835beca1a58b8eda
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
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:24e06ecf7d936658613dcb03c72477fa7ddc70798695a1cb8cd7feb9718c77c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248327744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4369db773cde4ecc31a6d3e5f6d3760a7fc220cc4e7bf2377c215ded4ab48a90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:05:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b240da7f78e851f44ebaad3b387956d9ae27eeb3ff3b62c7df96eb90470757f`  
		Last Modified: Thu, 21 May 2026 14:10:06 GMT  
		Size: 176.9 MB (176908111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d8180fdca39443d0c3f6bfce415b743686ca50dc9c2ae4c5553b7fbbda4454b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb9384d09e7f62df4db0b577166165a3183947d1c0494b013b7b321cc4a773`

```dockerfile
```

-	Layers:
	-	`sha256:553bb64621759abdbfe8faa8153be1b26999eac959dca86947e53c86f0eab66d`  
		Last Modified: Thu, 21 May 2026 14:09:32 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12`

```console
$ docker pull dart@sha256:3705781e19ca2689f0358fad861087149f392e44b2058254835beca1a58b8eda
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

### `dart:3.12` - linux; amd64

```console
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12` - linux; riscv64

```console
$ docker pull dart@sha256:24e06ecf7d936658613dcb03c72477fa7ddc70798695a1cb8cd7feb9718c77c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248327744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4369db773cde4ecc31a6d3e5f6d3760a7fc220cc4e7bf2377c215ded4ab48a90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:05:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b240da7f78e851f44ebaad3b387956d9ae27eeb3ff3b62c7df96eb90470757f`  
		Last Modified: Thu, 21 May 2026 14:10:06 GMT  
		Size: 176.9 MB (176908111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12` - unknown; unknown

```console
$ docker pull dart@sha256:d8180fdca39443d0c3f6bfce415b743686ca50dc9c2ae4c5553b7fbbda4454b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb9384d09e7f62df4db0b577166165a3183947d1c0494b013b7b321cc4a773`

```dockerfile
```

-	Layers:
	-	`sha256:553bb64621759abdbfe8faa8153be1b26999eac959dca86947e53c86f0eab66d`  
		Last Modified: Thu, 21 May 2026 14:09:32 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12-sdk`

```console
$ docker pull dart@sha256:3705781e19ca2689f0358fad861087149f392e44b2058254835beca1a58b8eda
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

### `dart:3.12-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:24e06ecf7d936658613dcb03c72477fa7ddc70798695a1cb8cd7feb9718c77c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248327744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4369db773cde4ecc31a6d3e5f6d3760a7fc220cc4e7bf2377c215ded4ab48a90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:05:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b240da7f78e851f44ebaad3b387956d9ae27eeb3ff3b62c7df96eb90470757f`  
		Last Modified: Thu, 21 May 2026 14:10:06 GMT  
		Size: 176.9 MB (176908111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d8180fdca39443d0c3f6bfce415b743686ca50dc9c2ae4c5553b7fbbda4454b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb9384d09e7f62df4db0b577166165a3183947d1c0494b013b7b321cc4a773`

```dockerfile
```

-	Layers:
	-	`sha256:553bb64621759abdbfe8faa8153be1b26999eac959dca86947e53c86f0eab66d`  
		Last Modified: Thu, 21 May 2026 14:09:32 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12.1`

```console
$ docker pull dart@sha256:f103024d92d881a8111647edea875b75024cd83760df173e04b804fef893d8ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.12.1` - linux; amd64

```console
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.1` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.1` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.1` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.1` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.1` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.12.1-sdk`

```console
$ docker pull dart@sha256:f103024d92d881a8111647edea875b75024cd83760df173e04b804fef893d8ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:3.12.1-sdk` - linux; amd64

```console
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.1-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.12.1-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.12.1-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.13.0-103.1.beta`

```console
$ docker pull dart@sha256:ed9028cc6bb0c9d2bfb7d50c257f16cb08f50b29bc5e2e6d54d78631d6bd0cbf
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

### `dart:3.13.0-103.1.beta` - linux; amd64

```console
$ docker pull dart@sha256:d81104c75faa61e9bc592dc7cc60c8ab4ffcb12db5371ab6e9ddc6992462751e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311868471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92de4785610143ad324146e9b88ed54133f6b2b3722461a075c76875e3d0ead`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:24:01 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:24:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:24:01 GMT
WORKDIR /root
# Tue, 19 May 2026 23:24:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2637e16c6e09ec72d1e2ae554f5b644f89bf58785dd17b2d9e09d216775e7b0`  
		Last Modified: Tue, 19 May 2026 23:24:45 GMT  
		Size: 42.5 MB (42504587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0391b9c8117291502f7211c501b407679110af6571981a1b1e68741437216bf3`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 1.9 MB (1869784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b407e03bd03922c379b45fd3462ef310cff5c7f7656d368f78c7de49da7056`  
		Last Modified: Tue, 19 May 2026 23:24:49 GMT  
		Size: 237.7 MB (237714142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:7c9a6af0d2e5c71425a48670acff41349acce81bb7731ee16a2dcba6e401e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478e75cee0184f8913737b51ea4b7c4b15a1c8f6329b67a6aa083130e7c6b432`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f270b49f3ebfa43ab75a653087be14e198f81706b609bc2466946a28adde`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:73703a0c4fc01c7603659d9f932646eb8fb6465551ddaa7d5e53c7f259a95c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226607635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8f17a0e40e803c7c40f3fa782153d42b6c66511317b3d744d4f8de3a63d564`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 May 2026 00:07:51 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 May 2026 00:07:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:51 GMT
WORKDIR /root
# Wed, 20 May 2026 00:08:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcb232070ef0f1260ca1db8ab9faa9460c3544d787e0fd6f8708f5e0be4a2f5`  
		Last Modified: Wed, 20 May 2026 00:08:21 GMT  
		Size: 37.5 MB (37502823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e397e0cd660862cdbd2e6a3cdbc97550fa640df55588d7f35c0b0afe9085bf`  
		Last Modified: Wed, 20 May 2026 00:08:20 GMT  
		Size: 1.3 MB (1273147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40eb28562d86ed40c23a1a217d7a99d7c7282f10719462e6d07950d1f4731d3`  
		Last Modified: Wed, 20 May 2026 00:09:01 GMT  
		Size: 161.6 MB (161625802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:cb10a187f36a3bd0e8f5216ed03204a3395215bfe28d8069e040aea49636e3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8598f847a5afe67ab30bc8b2caa36a0f0c047d9bc29cecfdf2d47ea82c954db0`

```dockerfile
```

-	Layers:
	-	`sha256:c35eb02e66ff238b7bf17deb38570ab61df64b0b07b204dd4b16369e7067a323`  
		Last Modified: Wed, 20 May 2026 00:08:56 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:50d7147ffd3c2564de733ed9dfa5e75c9a02716f4385168f3118afe434ba8869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310470172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92690a571315c8c8c9611c21ebb8d2203c2be96e084e23754d7dbc5f82abcf2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:27:34 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:27:34 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:27:34 GMT
WORKDIR /root
# Tue, 19 May 2026 23:27:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9eeb40aab4c60256acbfa8620c6a9f0c376405fa0b1fa38151ae5c49a76fc`  
		Last Modified: Tue, 19 May 2026 23:28:19 GMT  
		Size: 42.3 MB (42285492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ae340b2688c04af9ea257dff8fbc380201889d785011cf78e8365b4f8ee89`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 1.6 MB (1564379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57db52b85afca7d5c6f5c60d44beaf0167c0dc1575e6ab0b0cee7434496e7a`  
		Last Modified: Tue, 19 May 2026 23:28:23 GMT  
		Size: 236.5 MB (236478350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:84e3bdd1ad43f42e59bb613ebbf32b943d5afe370bf297f1e24fa61b8ff6acb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafd012745fa7c99f78132341076804da9c867806414fda3c2170806fa8f92d2`

```dockerfile
```

-	Layers:
	-	`sha256:0982a19342bf0fcd1105f96915f3307e4982172758aaa087f4f087b4a9781f6e`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta` - linux; riscv64

```console
$ docker pull dart@sha256:f3a93cf6014293f0768787d868cf257e85ad4396efb067d360540b8035a99231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249073469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54e50328204e0b2e95d6868108b5f2792303c8a42de7220128d20e5f014520`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:11:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a038534bab8be6a6635a8999ca6bd8824b2c385b086d8951ad743031c697a3`  
		Last Modified: Thu, 21 May 2026 14:16:09 GMT  
		Size: 177.7 MB (177653836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:cfe4807c10a5f66249c296a0e4a3aeaa884a6b711990460d2bf25f2beb47881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1596b3a51e1e388cf25c7c65bd8acd452a171bf3a3ba828d15d32efd76bd39c2`

```dockerfile
```

-	Layers:
	-	`sha256:ff67f678e6957680be542404d025cbfb52e1c695d1fe3b3504da6d99fa8db66c`  
		Last Modified: Thu, 21 May 2026 14:15:43 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.13.0-103.1.beta-sdk`

```console
$ docker pull dart@sha256:ed9028cc6bb0c9d2bfb7d50c257f16cb08f50b29bc5e2e6d54d78631d6bd0cbf
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

### `dart:3.13.0-103.1.beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:d81104c75faa61e9bc592dc7cc60c8ab4ffcb12db5371ab6e9ddc6992462751e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311868471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92de4785610143ad324146e9b88ed54133f6b2b3722461a075c76875e3d0ead`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:24:01 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:24:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:24:01 GMT
WORKDIR /root
# Tue, 19 May 2026 23:24:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2637e16c6e09ec72d1e2ae554f5b644f89bf58785dd17b2d9e09d216775e7b0`  
		Last Modified: Tue, 19 May 2026 23:24:45 GMT  
		Size: 42.5 MB (42504587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0391b9c8117291502f7211c501b407679110af6571981a1b1e68741437216bf3`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 1.9 MB (1869784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b407e03bd03922c379b45fd3462ef310cff5c7f7656d368f78c7de49da7056`  
		Last Modified: Tue, 19 May 2026 23:24:49 GMT  
		Size: 237.7 MB (237714142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7c9a6af0d2e5c71425a48670acff41349acce81bb7731ee16a2dcba6e401e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478e75cee0184f8913737b51ea4b7c4b15a1c8f6329b67a6aa083130e7c6b432`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f270b49f3ebfa43ab75a653087be14e198f81706b609bc2466946a28adde`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:73703a0c4fc01c7603659d9f932646eb8fb6465551ddaa7d5e53c7f259a95c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226607635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8f17a0e40e803c7c40f3fa782153d42b6c66511317b3d744d4f8de3a63d564`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 May 2026 00:07:51 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 May 2026 00:07:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:51 GMT
WORKDIR /root
# Wed, 20 May 2026 00:08:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcb232070ef0f1260ca1db8ab9faa9460c3544d787e0fd6f8708f5e0be4a2f5`  
		Last Modified: Wed, 20 May 2026 00:08:21 GMT  
		Size: 37.5 MB (37502823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e397e0cd660862cdbd2e6a3cdbc97550fa640df55588d7f35c0b0afe9085bf`  
		Last Modified: Wed, 20 May 2026 00:08:20 GMT  
		Size: 1.3 MB (1273147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40eb28562d86ed40c23a1a217d7a99d7c7282f10719462e6d07950d1f4731d3`  
		Last Modified: Wed, 20 May 2026 00:09:01 GMT  
		Size: 161.6 MB (161625802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cb10a187f36a3bd0e8f5216ed03204a3395215bfe28d8069e040aea49636e3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8598f847a5afe67ab30bc8b2caa36a0f0c047d9bc29cecfdf2d47ea82c954db0`

```dockerfile
```

-	Layers:
	-	`sha256:c35eb02e66ff238b7bf17deb38570ab61df64b0b07b204dd4b16369e7067a323`  
		Last Modified: Wed, 20 May 2026 00:08:56 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:50d7147ffd3c2564de733ed9dfa5e75c9a02716f4385168f3118afe434ba8869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310470172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92690a571315c8c8c9611c21ebb8d2203c2be96e084e23754d7dbc5f82abcf2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:27:34 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:27:34 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:27:34 GMT
WORKDIR /root
# Tue, 19 May 2026 23:27:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9eeb40aab4c60256acbfa8620c6a9f0c376405fa0b1fa38151ae5c49a76fc`  
		Last Modified: Tue, 19 May 2026 23:28:19 GMT  
		Size: 42.3 MB (42285492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ae340b2688c04af9ea257dff8fbc380201889d785011cf78e8365b4f8ee89`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 1.6 MB (1564379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57db52b85afca7d5c6f5c60d44beaf0167c0dc1575e6ab0b0cee7434496e7a`  
		Last Modified: Tue, 19 May 2026 23:28:23 GMT  
		Size: 236.5 MB (236478350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:84e3bdd1ad43f42e59bb613ebbf32b943d5afe370bf297f1e24fa61b8ff6acb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafd012745fa7c99f78132341076804da9c867806414fda3c2170806fa8f92d2`

```dockerfile
```

-	Layers:
	-	`sha256:0982a19342bf0fcd1105f96915f3307e4982172758aaa087f4f087b4a9781f6e`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f3a93cf6014293f0768787d868cf257e85ad4396efb067d360540b8035a99231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249073469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54e50328204e0b2e95d6868108b5f2792303c8a42de7220128d20e5f014520`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:11:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a038534bab8be6a6635a8999ca6bd8824b2c385b086d8951ad743031c697a3`  
		Last Modified: Thu, 21 May 2026 14:16:09 GMT  
		Size: 177.7 MB (177653836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cfe4807c10a5f66249c296a0e4a3aeaa884a6b711990460d2bf25f2beb47881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1596b3a51e1e388cf25c7c65bd8acd452a171bf3a3ba828d15d32efd76bd39c2`

```dockerfile
```

-	Layers:
	-	`sha256:ff67f678e6957680be542404d025cbfb52e1c695d1fe3b3504da6d99fa8db66c`  
		Last Modified: Thu, 21 May 2026 14:15:43 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:ed9028cc6bb0c9d2bfb7d50c257f16cb08f50b29bc5e2e6d54d78631d6bd0cbf
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
$ docker pull dart@sha256:d81104c75faa61e9bc592dc7cc60c8ab4ffcb12db5371ab6e9ddc6992462751e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311868471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92de4785610143ad324146e9b88ed54133f6b2b3722461a075c76875e3d0ead`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:24:01 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:24:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:24:01 GMT
WORKDIR /root
# Tue, 19 May 2026 23:24:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2637e16c6e09ec72d1e2ae554f5b644f89bf58785dd17b2d9e09d216775e7b0`  
		Last Modified: Tue, 19 May 2026 23:24:45 GMT  
		Size: 42.5 MB (42504587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0391b9c8117291502f7211c501b407679110af6571981a1b1e68741437216bf3`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 1.9 MB (1869784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b407e03bd03922c379b45fd3462ef310cff5c7f7656d368f78c7de49da7056`  
		Last Modified: Tue, 19 May 2026 23:24:49 GMT  
		Size: 237.7 MB (237714142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:7c9a6af0d2e5c71425a48670acff41349acce81bb7731ee16a2dcba6e401e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478e75cee0184f8913737b51ea4b7c4b15a1c8f6329b67a6aa083130e7c6b432`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f270b49f3ebfa43ab75a653087be14e198f81706b609bc2466946a28adde`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:73703a0c4fc01c7603659d9f932646eb8fb6465551ddaa7d5e53c7f259a95c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226607635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8f17a0e40e803c7c40f3fa782153d42b6c66511317b3d744d4f8de3a63d564`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 May 2026 00:07:51 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 May 2026 00:07:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:51 GMT
WORKDIR /root
# Wed, 20 May 2026 00:08:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcb232070ef0f1260ca1db8ab9faa9460c3544d787e0fd6f8708f5e0be4a2f5`  
		Last Modified: Wed, 20 May 2026 00:08:21 GMT  
		Size: 37.5 MB (37502823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e397e0cd660862cdbd2e6a3cdbc97550fa640df55588d7f35c0b0afe9085bf`  
		Last Modified: Wed, 20 May 2026 00:08:20 GMT  
		Size: 1.3 MB (1273147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40eb28562d86ed40c23a1a217d7a99d7c7282f10719462e6d07950d1f4731d3`  
		Last Modified: Wed, 20 May 2026 00:09:01 GMT  
		Size: 161.6 MB (161625802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:cb10a187f36a3bd0e8f5216ed03204a3395215bfe28d8069e040aea49636e3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8598f847a5afe67ab30bc8b2caa36a0f0c047d9bc29cecfdf2d47ea82c954db0`

```dockerfile
```

-	Layers:
	-	`sha256:c35eb02e66ff238b7bf17deb38570ab61df64b0b07b204dd4b16369e7067a323`  
		Last Modified: Wed, 20 May 2026 00:08:56 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:50d7147ffd3c2564de733ed9dfa5e75c9a02716f4385168f3118afe434ba8869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310470172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92690a571315c8c8c9611c21ebb8d2203c2be96e084e23754d7dbc5f82abcf2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:27:34 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:27:34 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:27:34 GMT
WORKDIR /root
# Tue, 19 May 2026 23:27:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9eeb40aab4c60256acbfa8620c6a9f0c376405fa0b1fa38151ae5c49a76fc`  
		Last Modified: Tue, 19 May 2026 23:28:19 GMT  
		Size: 42.3 MB (42285492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ae340b2688c04af9ea257dff8fbc380201889d785011cf78e8365b4f8ee89`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 1.6 MB (1564379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57db52b85afca7d5c6f5c60d44beaf0167c0dc1575e6ab0b0cee7434496e7a`  
		Last Modified: Tue, 19 May 2026 23:28:23 GMT  
		Size: 236.5 MB (236478350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:84e3bdd1ad43f42e59bb613ebbf32b943d5afe370bf297f1e24fa61b8ff6acb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafd012745fa7c99f78132341076804da9c867806414fda3c2170806fa8f92d2`

```dockerfile
```

-	Layers:
	-	`sha256:0982a19342bf0fcd1105f96915f3307e4982172758aaa087f4f087b4a9781f6e`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:f3a93cf6014293f0768787d868cf257e85ad4396efb067d360540b8035a99231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249073469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54e50328204e0b2e95d6868108b5f2792303c8a42de7220128d20e5f014520`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:11:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a038534bab8be6a6635a8999ca6bd8824b2c385b086d8951ad743031c697a3`  
		Last Modified: Thu, 21 May 2026 14:16:09 GMT  
		Size: 177.7 MB (177653836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:cfe4807c10a5f66249c296a0e4a3aeaa884a6b711990460d2bf25f2beb47881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1596b3a51e1e388cf25c7c65bd8acd452a171bf3a3ba828d15d32efd76bd39c2`

```dockerfile
```

-	Layers:
	-	`sha256:ff67f678e6957680be542404d025cbfb52e1c695d1fe3b3504da6d99fa8db66c`  
		Last Modified: Thu, 21 May 2026 14:15:43 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:ed9028cc6bb0c9d2bfb7d50c257f16cb08f50b29bc5e2e6d54d78631d6bd0cbf
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
$ docker pull dart@sha256:d81104c75faa61e9bc592dc7cc60c8ab4ffcb12db5371ab6e9ddc6992462751e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311868471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92de4785610143ad324146e9b88ed54133f6b2b3722461a075c76875e3d0ead`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:00 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:24:01 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:24:01 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:24:01 GMT
WORKDIR /root
# Tue, 19 May 2026 23:24:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2637e16c6e09ec72d1e2ae554f5b644f89bf58785dd17b2d9e09d216775e7b0`  
		Last Modified: Tue, 19 May 2026 23:24:45 GMT  
		Size: 42.5 MB (42504587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0391b9c8117291502f7211c501b407679110af6571981a1b1e68741437216bf3`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 1.9 MB (1869784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b407e03bd03922c379b45fd3462ef310cff5c7f7656d368f78c7de49da7056`  
		Last Modified: Tue, 19 May 2026 23:24:49 GMT  
		Size: 237.7 MB (237714142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7c9a6af0d2e5c71425a48670acff41349acce81bb7731ee16a2dcba6e401e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478e75cee0184f8913737b51ea4b7c4b15a1c8f6329b67a6aa083130e7c6b432`

```dockerfile
```

-	Layers:
	-	`sha256:5ae6f270b49f3ebfa43ab75a653087be14e198f81706b609bc2466946a28adde`  
		Last Modified: Tue, 19 May 2026 23:24:43 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:73703a0c4fc01c7603659d9f932646eb8fb6465551ddaa7d5e53c7f259a95c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226607635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8f17a0e40e803c7c40f3fa782153d42b6c66511317b3d744d4f8de3a63d564`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:07:51 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 20 May 2026 00:07:51 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 May 2026 00:07:51 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:51 GMT
WORKDIR /root
# Wed, 20 May 2026 00:08:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcb232070ef0f1260ca1db8ab9faa9460c3544d787e0fd6f8708f5e0be4a2f5`  
		Last Modified: Wed, 20 May 2026 00:08:21 GMT  
		Size: 37.5 MB (37502823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e397e0cd660862cdbd2e6a3cdbc97550fa640df55588d7f35c0b0afe9085bf`  
		Last Modified: Wed, 20 May 2026 00:08:20 GMT  
		Size: 1.3 MB (1273147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40eb28562d86ed40c23a1a217d7a99d7c7282f10719462e6d07950d1f4731d3`  
		Last Modified: Wed, 20 May 2026 00:09:01 GMT  
		Size: 161.6 MB (161625802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cb10a187f36a3bd0e8f5216ed03204a3395215bfe28d8069e040aea49636e3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8598f847a5afe67ab30bc8b2caa36a0f0c047d9bc29cecfdf2d47ea82c954db0`

```dockerfile
```

-	Layers:
	-	`sha256:c35eb02e66ff238b7bf17deb38570ab61df64b0b07b204dd4b16369e7067a323`  
		Last Modified: Wed, 20 May 2026 00:08:56 GMT  
		Size: 19.0 KB (19029 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:50d7147ffd3c2564de733ed9dfa5e75c9a02716f4385168f3118afe434ba8869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310470172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92690a571315c8c8c9611c21ebb8d2203c2be96e084e23754d7dbc5f82abcf2d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:34 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 19 May 2026 23:27:34 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 19 May 2026 23:27:34 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:27:34 GMT
WORKDIR /root
# Tue, 19 May 2026 23:27:47 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd9eeb40aab4c60256acbfa8620c6a9f0c376405fa0b1fa38151ae5c49a76fc`  
		Last Modified: Tue, 19 May 2026 23:28:19 GMT  
		Size: 42.3 MB (42285492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ae340b2688c04af9ea257dff8fbc380201889d785011cf78e8365b4f8ee89`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 1.6 MB (1564379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57db52b85afca7d5c6f5c60d44beaf0167c0dc1575e6ab0b0cee7434496e7a`  
		Last Modified: Tue, 19 May 2026 23:28:23 GMT  
		Size: 236.5 MB (236478350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:84e3bdd1ad43f42e59bb613ebbf32b943d5afe370bf297f1e24fa61b8ff6acb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafd012745fa7c99f78132341076804da9c867806414fda3c2170806fa8f92d2`

```dockerfile
```

-	Layers:
	-	`sha256:0982a19342bf0fcd1105f96915f3307e4982172758aaa087f4f087b4a9781f6e`  
		Last Modified: Tue, 19 May 2026 23:28:17 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:f3a93cf6014293f0768787d868cf257e85ad4396efb067d360540b8035a99231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249073469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef54e50328204e0b2e95d6868108b5f2792303c8a42de7220128d20e5f014520`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:11:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a038534bab8be6a6635a8999ca6bd8824b2c385b086d8951ad743031c697a3`  
		Last Modified: Thu, 21 May 2026 14:16:09 GMT  
		Size: 177.7 MB (177653836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cfe4807c10a5f66249c296a0e4a3aeaa884a6b711990460d2bf25f2beb47881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1596b3a51e1e388cf25c7c65bd8acd452a171bf3a3ba828d15d32efd76bd39c2`

```dockerfile
```

-	Layers:
	-	`sha256:ff67f678e6957680be542404d025cbfb52e1c695d1fe3b3504da6d99fa8db66c`  
		Last Modified: Thu, 21 May 2026 14:15:43 GMT  
		Size: 19.0 KB (18970 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:3705781e19ca2689f0358fad861087149f392e44b2058254835beca1a58b8eda
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
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:24e06ecf7d936658613dcb03c72477fa7ddc70798695a1cb8cd7feb9718c77c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248327744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4369db773cde4ecc31a6d3e5f6d3760a7fc220cc4e7bf2377c215ded4ab48a90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:05:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b240da7f78e851f44ebaad3b387956d9ae27eeb3ff3b62c7df96eb90470757f`  
		Last Modified: Thu, 21 May 2026 14:10:06 GMT  
		Size: 176.9 MB (176908111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:d8180fdca39443d0c3f6bfce415b743686ca50dc9c2ae4c5553b7fbbda4454b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb9384d09e7f62df4db0b577166165a3183947d1c0494b013b7b321cc4a773`

```dockerfile
```

-	Layers:
	-	`sha256:553bb64621759abdbfe8faa8153be1b26999eac959dca86947e53c86f0eab66d`  
		Last Modified: Thu, 21 May 2026 14:09:32 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:3705781e19ca2689f0358fad861087149f392e44b2058254835beca1a58b8eda
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
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:24e06ecf7d936658613dcb03c72477fa7ddc70798695a1cb8cd7feb9718c77c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248327744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4369db773cde4ecc31a6d3e5f6d3760a7fc220cc4e7bf2377c215ded4ab48a90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:05:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b240da7f78e851f44ebaad3b387956d9ae27eeb3ff3b62c7df96eb90470757f`  
		Last Modified: Thu, 21 May 2026 14:10:06 GMT  
		Size: 176.9 MB (176908111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d8180fdca39443d0c3f6bfce415b743686ca50dc9c2ae4c5553b7fbbda4454b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb9384d09e7f62df4db0b577166165a3183947d1c0494b013b7b321cc4a773`

```dockerfile
```

-	Layers:
	-	`sha256:553bb64621759abdbfe8faa8153be1b26999eac959dca86947e53c86f0eab66d`  
		Last Modified: Thu, 21 May 2026 14:09:32 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:3705781e19ca2689f0358fad861087149f392e44b2058254835beca1a58b8eda
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
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:24e06ecf7d936658613dcb03c72477fa7ddc70798695a1cb8cd7feb9718c77c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248327744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4369db773cde4ecc31a6d3e5f6d3760a7fc220cc4e7bf2377c215ded4ab48a90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:05:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b240da7f78e851f44ebaad3b387956d9ae27eeb3ff3b62c7df96eb90470757f`  
		Last Modified: Thu, 21 May 2026 14:10:06 GMT  
		Size: 176.9 MB (176908111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:d8180fdca39443d0c3f6bfce415b743686ca50dc9c2ae4c5553b7fbbda4454b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb9384d09e7f62df4db0b577166165a3183947d1c0494b013b7b321cc4a773`

```dockerfile
```

-	Layers:
	-	`sha256:553bb64621759abdbfe8faa8153be1b26999eac959dca86947e53c86f0eab66d`  
		Last Modified: Thu, 21 May 2026 14:09:32 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:3705781e19ca2689f0358fad861087149f392e44b2058254835beca1a58b8eda
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
$ docker pull dart@sha256:1084929f4e943f44fd86c78500d22a4339469354a374574ecc16a2aabfd2582f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310942915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee2b2dbfbebaf4146fd0560471ee6229ec6ae294c9fcaf2776f4a8eadfa8abc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:56 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:56 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:56 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f61b2fe77f050f4ca332791e970839ee640079b59c7b53688e1f1b57aeac212`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 42.5 MB (42504481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02046203169b09dd439aee7573065dfeb9a315df8eca955bff762a861c854aff`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 1.9 MB (1869790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c4abf572584d12407b08706626e143ff8cfcb141cd72bb0944c0e11ff83e5d`  
		Last Modified: Tue, 26 May 2026 20:32:46 GMT  
		Size: 236.8 MB (236788686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:7662ef2d512115d6ef2963f51fd168a2432dd186dbe29e3347d47436386cf536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66ca8e1d5016f2aea61a8dd844f5335c777dad65f65582a625d53c6c8308f1`

```dockerfile
```

-	Layers:
	-	`sha256:63c6e102192cb2c8676951b6a7cdf6229f35712d9e7412245f8b838bf6269169`  
		Last Modified: Tue, 26 May 2026 20:32:33 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:f04de8d20306fec21c148ae2fa0ebdf6da6a379262d97dafa0a7b4bb7178728b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226078344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e3dc4d47e77fb089b94f285993f313895b52ac9b8570ab2c18667941173586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:32:05 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:32:05 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:32:05 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:14 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d27d7a75151cc5bd699515a5d3097fd940446c299f659e359320f74e5ce9c9`  
		Last Modified: Tue, 26 May 2026 20:32:38 GMT  
		Size: 37.5 MB (37509460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488f84b526710261b0936f6401897f0144cdcd34a3152f8c629f7ad190e80d2`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 1.3 MB (1273153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32f7c39bac5379adb0c968d408e5921141b187eb329acb8752ba34728fe709`  
		Last Modified: Tue, 26 May 2026 20:32:41 GMT  
		Size: 161.1 MB (161089868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:e16e1be8c8d332c96675d3d53627af6df60592752947823f856bd0e871779143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d0f80676ce4d8d3bc881c4b95a688fdf49ef49e8bc528e1733113dae35bac5`

```dockerfile
```

-	Layers:
	-	`sha256:902d802aafa445250a18077914d1985faae10f00b37d254b4af45019d7bfe5cf`  
		Last Modified: Tue, 26 May 2026 20:32:36 GMT  
		Size: 20.8 KB (20769 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:df748054c761938f24bae1e3876b0a29dc0b7cfaecbb0dd0883af5d2c3c076a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.4 MB (309389795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c238a332a84f01dffc64a14ac91694e533232fb9f949b3d5229d8d4442a7941`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 26 May 2026 20:31:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 May 2026 20:31:52 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 26 May 2026 20:31:52 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 26 May 2026 20:31:52 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 20:31:52 GMT
WORKDIR /root
# Tue, 26 May 2026 20:32:04 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6a2bbf64a133c9c86a62a532dbd3e0b4db4ac365abd456e9f9d1c5df61fcdbf8;             SDK_ARCH="x64";;         armhf)             DART_SHA256=51dfead169350b452a24230b9bcbbf11ac15cda3f993dab32c63a51b3689bbb5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=b44087930108f6d7f56bf580a02d5d2a97ff94519c5a288339982202e1b4c481;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=32d0b8c2ee819ba5df76a22702bc254e3d3a460760e1e11690c17ac7877f6289;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.1/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff8a7689f6c9f14c0653099d5e198fe1a17373899dc456f3f7a333959498a3d`  
		Last Modified: Tue, 26 May 2026 20:32:37 GMT  
		Size: 42.3 MB (42285764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937db8af4819e606d38a27f0917ff9a96fc90950463b7b8e43a11c907fd734d1`  
		Last Modified: Tue, 26 May 2026 20:32:35 GMT  
		Size: 1.6 MB (1564378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f2479714efd63130d273102cb8377f276edbc3e9bd8bd0aa7676c2784a7a9`  
		Last Modified: Tue, 26 May 2026 20:32:44 GMT  
		Size: 235.4 MB (235397702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:5a848294cf6b9099bf97bd50aa7f591d0ae8d47616dc98c907b1df1c1f8f3bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3515f2b37b72250729227324cec1092d27e673f5674e6f836b942140a267119`

```dockerfile
```

-	Layers:
	-	`sha256:1290ad536f1527c5745bdce044ebf1deaaf3ee5433e731589eec822827fd26f9`  
		Last Modified: Tue, 26 May 2026 20:32:34 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:24e06ecf7d936658613dcb03c72477fa7ddc70798695a1cb8cd7feb9718c77c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248327744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4369db773cde4ecc31a6d3e5f6d3760a7fc220cc4e7bf2377c215ded4ab48a90`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:04:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 14:04:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 21 May 2026 14:04:45 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 21 May 2026 14:04:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 14:04:45 GMT
WORKDIR /root
# Thu, 21 May 2026 14:05:30 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=45773140810cfd433402a58bb2ead4f43cc55805c34d2de0641c51012591d65c;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c8919bba2fa9f72801d709485fcff27f73f0cc58d3f3f5dd056a44a317848ffc;             SDK_ARCH="arm";;         arm64)             DART_SHA256=17e901b9029c1be256c64d937595725a242b2052dab810d7d10f715bed7b6d90;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=f603a24bdaa9fc31c498c558bfeed8e3ebab84c0e085974eb5849c1cec756b3e;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.12.0/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e9c17cfea21bbbe7d24d23d566a0cf8890898dda5269a1d062f47b6f69403d`  
		Last Modified: Thu, 21 May 2026 14:09:46 GMT  
		Size: 41.6 MB (41577551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2897a726c8c88454c801e82ecafe8ef027a50157aa7b469ac730ccb5dcde9b7`  
		Last Modified: Thu, 21 May 2026 14:09:33 GMT  
		Size: 1.6 MB (1564452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b240da7f78e851f44ebaad3b387956d9ae27eeb3ff3b62c7df96eb90470757f`  
		Last Modified: Thu, 21 May 2026 14:10:06 GMT  
		Size: 176.9 MB (176908111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:d8180fdca39443d0c3f6bfce415b743686ca50dc9c2ae4c5553b7fbbda4454b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63eb9384d09e7f62df4db0b577166165a3183947d1c0494b013b7b321cc4a773`

```dockerfile
```

-	Layers:
	-	`sha256:553bb64621759abdbfe8faa8153be1b26999eac959dca86947e53c86f0eab66d`  
		Last Modified: Thu, 21 May 2026 14:09:32 GMT  
		Size: 20.7 KB (20699 bytes)  
		MIME: application/vnd.in-toto+json
