## `dart:beta-sdk`

```console
$ docker pull dart@sha256:77cda94da2b0c5ac5396e7fd8bcd401ab5f1315308340f41c7d8873a9a6302bf
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

### `dart:beta-sdk` - unknown; unknown

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

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:c606212d22f4b2078cf2a2e440b8d924cef6ae10e3a0c7afe0ed17ca25522e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218745426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95188e190071230b9cb0b13dbfc08319b425985af33a3feaf59414b4a949e07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Sep 2025 11:42:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:42:45 GMT
WORKDIR /root
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbab51fd941bfbf6894d5ee7b1ae01abfb3076cfdb1e3f4371f13b39a54dddbe`  
		Last Modified: Mon, 08 Sep 2025 23:54:03 GMT  
		Size: 37.5 MB (37479176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206df88050e16bafd852282e462194d8df0920b42252c3bd860ca91615777cf5`  
		Last Modified: Mon, 08 Sep 2025 22:47:14 GMT  
		Size: 1.3 MB (1275115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800bb6b7413bbcd1380ad6590e1cf724afce7386c7bcd4c3d5db32a864c06ae7`  
		Last Modified: Tue, 09 Sep 2025 09:53:27 GMT  
		Size: 153.8 MB (153783256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:964c33d7f39661cd706ac0561d400307f98caf0747c9d5394a8ededaa0cd6b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a785ccf4475420b72e572cda89bbdc900326c006a6c0f57bf51276152f63ff8`

```dockerfile
```

-	Layers:
	-	`sha256:fb2e25bc7affa0449ceae956cb65e3851ed6e2a746a1fab0a8350dd619e2d5c1`  
		Last Modified: Mon, 08 Sep 2025 23:53:39 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:cc6e1efe0ccaf82e263bef608e143aedf4c3c6b73e573d0250c04f67be1d895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284888716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8275d4bc438c73cdbf73aac3fb00b5a9a1825aaf89e358db879fb193fed2d9fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Sep 2025 11:42:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 02 Sep 2025 11:42:45 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 02 Sep 2025 11:42:45 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:42:45 GMT
WORKDIR /root
# Tue, 02 Sep 2025 11:42:45 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=aff507c0c17e4b749b72ecba0f42030f1541fc3dd52daf8c2bf29a9478537800;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3d4a719368dd8705e95c3ffc71201048ded208b64e4fa39be7d93da2b3297b65;             SDK_ARCH="arm";;         arm64)             DART_SHA256=9e231c949e010a4576df1afa9a00e15d5e58a4094ebad071420183ee34a8ad46;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=3b7711289aee528aa080739008aae92800b1b9612a3ad3713eeb4ab040bb61a7;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.10.0-162.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f89d69a51684f84a0769ff272a135e820627c2f0d17635b87386b8556e7d03`  
		Last Modified: Mon, 08 Sep 2025 22:31:10 GMT  
		Size: 42.3 MB (42270008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123341c443b49228dd642399a401a37640a47e145ee3cf26c2402c466c8c6d5`  
		Last Modified: Mon, 08 Sep 2025 22:04:04 GMT  
		Size: 1.6 MB (1566646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8403eae81c4d4bd441ef47eb5297d3bc2f977e25307b11ab670d34e0c66d28c7`  
		Last Modified: Mon, 08 Sep 2025 22:31:08 GMT  
		Size: 210.9 MB (210915399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:28ca783d7f1d813039c444aed686b2eb0dbacb7806380bf87096fd81174450ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561fbee50dd68f2c0ece118c7559db733590306ffe98169e8df0f8d519087bf9`

```dockerfile
```

-	Layers:
	-	`sha256:b17277cd2be2f2c0dd838ac93c5c9486658a66d53c105f82bcfe37c72efaf468`  
		Last Modified: Mon, 08 Sep 2025 23:53:43 GMT  
		Size: 19.1 KB (19100 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:0824896c3635178640a866888571670fde47cb5f94701c9c664235b5e1ceca6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231819901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40450849884f7fcbe60b8c33d9b55b1c6c21cc100ef257f99869d9afbb3e0e3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
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
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7109b7e9bd6ab41707df02c7d0e4f792f522902a928d58b1c0061eb1fe108a43`  
		Last Modified: Thu, 11 Sep 2025 01:52:01 GMT  
		Size: 41.6 MB (41553255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c5150a8a2900e580473fbfa46ae631ad996da8e9dead53e064607a8d06e010`  
		Last Modified: Thu, 11 Sep 2025 01:51:57 GMT  
		Size: 1.6 MB (1567072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa771d564a3f34dc85c1a96c0bea55a3c71e4d4be67d3b2fd4fed468955e503`  
		Last Modified: Thu, 11 Sep 2025 02:53:44 GMT  
		Size: 160.4 MB (160428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:831cdc4dbee079bd9df32f9c777e715bf45cc481d282e8f1c6d0fdcde3607dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526b3ca3f37cdf3a9adb065bc62ab274d599c38d58186b73eaedd9f1273e0c4`

```dockerfile
```

-	Layers:
	-	`sha256:9695883e9f56e8332fcf7d82cc85c9d21765669145120d62e97b786a2389b4fb`  
		Last Modified: Thu, 11 Sep 2025 02:53:25 GMT  
		Size: 19.0 KB (19014 bytes)  
		MIME: application/vnd.in-toto+json
