## `dart:beta`

```console
$ docker pull dart@sha256:7ac742a1e454216aabf1ade7ed19797a39d8049da5f47bc5224adebe5ae3e745
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
$ docker pull dart@sha256:ee5dcb135870b1a039b0132d5d1cbda179a89997e9a13b0e49e53ab7710431e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285674344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc9e4c9ab79478de68a3f80d5d72ccdc122fc746b377384f1fd3279cacf3851`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6048941f04ffda44cec4bccd989475c7c9cc95d7f4f2c1ddbd7d3047bd690c`  
		Last Modified: Tue, 30 Sep 2025 00:13:23 GMT  
		Size: 42.5 MB (42482645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4405596079890b306cff94599c654c78fe673b9caefbb013194dbafbc745fc5`  
		Last Modified: Tue, 30 Sep 2025 00:13:20 GMT  
		Size: 1.9 MB (1873614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689ad9fb8fc0849199be3d8997eacf3c486e55d332b38557f3577beded0f33c0`  
		Last Modified: Tue, 30 Sep 2025 20:55:15 GMT  
		Size: 211.5 MB (211540287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:cbcf95105d26a32c8258fcd36a5ecfc710a5c015b15c1614c3cbfae9862654f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f1da3c2640cb6cf9f3a2334ef9938f91247d05d7151b9531c8f47ffe689568`

```dockerfile
```

-	Layers:
	-	`sha256:80be05639a1d1fdb163237c48b4d415a1b17626c8328a09817de72259212e640`  
		Last Modified: Tue, 30 Sep 2025 20:53:20 GMT  
		Size: 19.0 KB (18965 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:3654b35cd12c3c67b1f2889a41685c5e04d1af75a61b9e0cc3acbbca116a8992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218749936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54149911be75a340d0cd6a1a3f7e2f68888adea6b9c1e8c0d96fb5ca523195ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a15304957cc1bb2c69a0e494bd2cac4ad18323eb25d15bc69c2dbfe072901`  
		Last Modified: Tue, 30 Sep 2025 01:12:30 GMT  
		Size: 37.5 MB (37478684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0730404d0906bd6947fbad5d60403bc685459df20004f7068c4e8d5b809419b5`  
		Last Modified: Tue, 30 Sep 2025 01:12:24 GMT  
		Size: 1.3 MB (1275114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e60f62aea3e617f1e730f178db409a13680b008a813a394fdee92d983c0f011`  
		Last Modified: Wed, 01 Oct 2025 20:53:59 GMT  
		Size: 153.8 MB (153783348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:9dc4c08bf4c3fc04d2e7f9a68800f1bc4ae254ca702f326eb50f382f7cc7d836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec30c0d350586f3da754bd02c970de9d300b83c3286383885dfb705327810fa0`

```dockerfile
```

-	Layers:
	-	`sha256:df975dc94acba86d746bdd921be5b690264ca414239a1553b7f6312fbdaece5c`  
		Last Modified: Wed, 01 Oct 2025 20:53:38 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:ca6ff3f563dd97d20a5cb187aa0e13ed434c633b187a519bd4f726d21c2d0fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284893012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e03f36a240aa049732473e5a5e67004bd277535834eb4a49413919b3a7e18b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a0025da7a49d97100d3f5038b6bb022624ad7c985d0c64a092ba12a27846af`  
		Last Modified: Tue, 30 Sep 2025 00:17:16 GMT  
		Size: 42.3 MB (42270040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94a2f736f4fa64461dcba879ceedadd508d4a16a740d2c64f37507c903f787`  
		Last Modified: Tue, 30 Sep 2025 00:17:04 GMT  
		Size: 1.6 MB (1566647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc11c7d6b6d336fa2200e0b2ce7d63c00ddbab38e8207ba8e6420cf3e874158`  
		Last Modified: Tue, 30 Sep 2025 11:53:46 GMT  
		Size: 210.9 MB (210915451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:988242dd7712cbdb760f47a0c5c68b8833d1ca815f58673ecce3397b7478a213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc19f751acef5f9681150218b0042e39f345f05a7ad8520d9ad14040f66a397`

```dockerfile
```

-	Layers:
	-	`sha256:e0bd59ac11bb3579ed3f6d8d5f66a720df54d30fc178a4030a674a6671258abd`  
		Last Modified: Tue, 30 Sep 2025 11:53:24 GMT  
		Size: 19.1 KB (19100 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:35c70cfc78b46cdb595854fb5823b9fcd9e38eb37888da75239850a392848a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231823810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0642fb6d57fdc6dd53ce2e6e0611c558f8eed181c6c8cd1e8145a086cbf55683`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Sep 2025 19:58:42 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 09 Sep 2025 19:58:42 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 09 Sep 2025 19:58:42 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Sep 2025 19:58:42 GMT
WORKDIR /root
# Tue, 09 Sep 2025 19:58:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1075ae8162ade585eb34ab3e11eece658b7b8b3ad292b927e8585898d67836f3`  
		Last Modified: Wed, 01 Oct 2025 11:03:02 GMT  
		Size: 41.6 MB (41553142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977b9639a3f9f96e75d41d175427ab5045f840e04c4eeaf4cb057c2470b1295`  
		Last Modified: Wed, 01 Oct 2025 11:02:59 GMT  
		Size: 1.6 MB (1567062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985f3697ba2b6a69ed2f0072e77f76f3f2f61dba2888008a99582bc243d6d4db`  
		Last Modified: Wed, 01 Oct 2025 19:09:16 GMT  
		Size: 160.4 MB (160428072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:c1b590206ee0fd2893e7e2048c43b3d4aab3a2f22bcc221ff4947f2df134d210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdf046550eb5d344ab6fcf3dec1f434164de6b2453ef2be89e157cd319dae06`

```dockerfile
```

-	Layers:
	-	`sha256:3274594d7f4444ceb75e14eed639faec499ee306324b932d91f5123e9b5100d9`  
		Last Modified: Wed, 01 Oct 2025 20:53:43 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json
