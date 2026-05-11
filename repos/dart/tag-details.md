<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `dart`

-	[`dart:3`](#dart3)
-	[`dart:3-sdk`](#dart3-sdk)
-	[`dart:3.11`](#dart311)
-	[`dart:3.11-sdk`](#dart311-sdk)
-	[`dart:3.11.6`](#dart3116)
-	[`dart:3.11.6-sdk`](#dart3116-sdk)
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
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3-sdk`

```console
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11`

```console
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11-sdk`

```console
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.6`

```console
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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

### `dart:3.11.6` - linux; amd64

```console
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.11.6-sdk`

```console
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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

### `dart:3.11.6-sdk` - linux; amd64

```console
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.11.6-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.11.6-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.13.0-103.1.beta`

```console
$ docker pull dart@sha256:72c6de367dbd29f1f7e547655ff160ed3d6086c955b9b2226a97be78268668dd
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
$ docker pull dart@sha256:8b154bb0537e809eb6a274b1043a56799b2124a7f0a02ebefab6aa1ba084b2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311865357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3f5e2351fb920d21e318c8f4de4f257dbf3bdf269b7ed4844e8fe4712a29e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:28 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:28 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092f09bec1bee84db0a209f8e408f14bbdb2d9531f7fde7c45bedd3387338f1b`  
		Last Modified: Fri, 08 May 2026 19:42:13 GMT  
		Size: 42.5 MB (42501670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081155158f96012d07f30d5dddb7cb2b9e0faa603c1898307fbb361cdeb0efb0`  
		Last Modified: Fri, 08 May 2026 19:42:11 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ec03aae636de9cf4ac915d65797db673d087d42a44aec1cb8473a0e6471b36`  
		Last Modified: Fri, 08 May 2026 19:42:17 GMT  
		Size: 237.7 MB (237713858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:6a8a3226d06667b9a81af297ba81011e3876d8cd84a2efd9ef5e13f528eb7d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05f659edfa89d1a3c9f59d9dda96cb80a5eae429d98fdf619444686521da860`

```dockerfile
```

-	Layers:
	-	`sha256:d865bc2239ef5e860ca6d4cc3a3734de0fa7b25b4d8b08e34b89a663306edec7`  
		Last Modified: Fri, 08 May 2026 19:42:11 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:e0637ace0c2e5d05a184f5e0a6047e21b059fad18da985c1d6da20e5e2e4c84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226609126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ccadca45cbbe6f1fbc13be8aa3315872ae4492f06e922250266627c10547a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:20 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:20 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c397f78e7cc2537e75904f25729ec5dba7faef504c3e5c252d1a5002cb7b51`  
		Last Modified: Fri, 08 May 2026 19:45:51 GMT  
		Size: 37.5 MB (37495343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f6665a0d68a8f335082af00f76179f9edc46554e97b0d1b653c7e52bdf9293`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47abf148c5b483759071bc1a739e4bd39ad00582e479db7508632b941aee80ea`  
		Last Modified: Fri, 08 May 2026 19:45:54 GMT  
		Size: 161.6 MB (161625679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:ba00119c541b5bbccf496d853b6c3d0e455f25c3a382bce4ff63f6efcca9ca97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0302ae0294b448ee831ac5b8d8af4afdb677362938a9558aaec95c9c0ed90`

```dockerfile
```

-	Layers:
	-	`sha256:a4a8db3dac533e52d15d9938f2e60f68193e58194ae649f168595f25726b0afb`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 19.0 KB (19027 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:177fc14c3b5fe9cdee875ed9e999d1cda004f488b01ec57926076e44084aeacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310468156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bafca3464d98938d54efe43148bda4e96624f52a6e1830501829e527863f38d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:18 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:18 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a2fb915c6222a2ae9101a4fe6b2c919e77cfd7e17346706b021b3c098f3a94`  
		Last Modified: Fri, 08 May 2026 19:44:04 GMT  
		Size: 42.3 MB (42281839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361cd22d8bb01688583f4a5e14a606310648019f8075e9b09a80c972f662e0f8`  
		Last Modified: Fri, 08 May 2026 19:44:02 GMT  
		Size: 1.6 MB (1564347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173af7c5673cebfe01ed77d2ba01e04a6bc0b194fc0460d4956307338265cf3a`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 236.5 MB (236478296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:61825f087be3dff94d3b87986108ffdba78536579c6754fed1df50fc1fe5590c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fede15183b7f7316259599bcc2b746691d74c0ea508ccd4536ecf8ba200cad44`

```dockerfile
```

-	Layers:
	-	`sha256:89324f4753f8bc4b667083e77e84de3059ea51c078964f18130cae1322d8adc1`  
		Last Modified: Fri, 08 May 2026 19:44:02 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta` - linux; riscv64

```console
$ docker pull dart@sha256:6e7f3bf208fc36edb717cde32b6f70d8ef762f7fa7e461ea6abe3843c5c65900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249070092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d14d3055c105f6e5407b3ac58d6e3a71b650af4acb5c3657cd1aedfb72c4a8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:16:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d4e7505852f448a449ce5385d217bd87481d51c1d4f0c1b0bc1f90f765b77`  
		Last Modified: Mon, 11 May 2026 01:21:11 GMT  
		Size: 177.7 MB (177653946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta` - unknown; unknown

```console
$ docker pull dart@sha256:cd48c5becbeb0db15a2a2441b58c53873edca8f21ba58946f83667ca9ce3a692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9faeabd8102b65f8c817c09d44e0e0dee141bfd47ff363f18cfe63b304c0d3e6`

```dockerfile
```

-	Layers:
	-	`sha256:3c205f87b681476829b897eb4f83b32f207072f29e3a36a516b5e5eee33e024c`  
		Last Modified: Mon, 11 May 2026 01:20:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:3.13.0-103.1.beta-sdk`

```console
$ docker pull dart@sha256:72c6de367dbd29f1f7e547655ff160ed3d6086c955b9b2226a97be78268668dd
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
$ docker pull dart@sha256:8b154bb0537e809eb6a274b1043a56799b2124a7f0a02ebefab6aa1ba084b2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311865357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3f5e2351fb920d21e318c8f4de4f257dbf3bdf269b7ed4844e8fe4712a29e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:28 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:28 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092f09bec1bee84db0a209f8e408f14bbdb2d9531f7fde7c45bedd3387338f1b`  
		Last Modified: Fri, 08 May 2026 19:42:13 GMT  
		Size: 42.5 MB (42501670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081155158f96012d07f30d5dddb7cb2b9e0faa603c1898307fbb361cdeb0efb0`  
		Last Modified: Fri, 08 May 2026 19:42:11 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ec03aae636de9cf4ac915d65797db673d087d42a44aec1cb8473a0e6471b36`  
		Last Modified: Fri, 08 May 2026 19:42:17 GMT  
		Size: 237.7 MB (237713858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6a8a3226d06667b9a81af297ba81011e3876d8cd84a2efd9ef5e13f528eb7d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05f659edfa89d1a3c9f59d9dda96cb80a5eae429d98fdf619444686521da860`

```dockerfile
```

-	Layers:
	-	`sha256:d865bc2239ef5e860ca6d4cc3a3734de0fa7b25b4d8b08e34b89a663306edec7`  
		Last Modified: Fri, 08 May 2026 19:42:11 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e0637ace0c2e5d05a184f5e0a6047e21b059fad18da985c1d6da20e5e2e4c84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226609126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ccadca45cbbe6f1fbc13be8aa3315872ae4492f06e922250266627c10547a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:20 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:20 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c397f78e7cc2537e75904f25729ec5dba7faef504c3e5c252d1a5002cb7b51`  
		Last Modified: Fri, 08 May 2026 19:45:51 GMT  
		Size: 37.5 MB (37495343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f6665a0d68a8f335082af00f76179f9edc46554e97b0d1b653c7e52bdf9293`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47abf148c5b483759071bc1a739e4bd39ad00582e479db7508632b941aee80ea`  
		Last Modified: Fri, 08 May 2026 19:45:54 GMT  
		Size: 161.6 MB (161625679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ba00119c541b5bbccf496d853b6c3d0e455f25c3a382bce4ff63f6efcca9ca97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0302ae0294b448ee831ac5b8d8af4afdb677362938a9558aaec95c9c0ed90`

```dockerfile
```

-	Layers:
	-	`sha256:a4a8db3dac533e52d15d9938f2e60f68193e58194ae649f168595f25726b0afb`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 19.0 KB (19027 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:177fc14c3b5fe9cdee875ed9e999d1cda004f488b01ec57926076e44084aeacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310468156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bafca3464d98938d54efe43148bda4e96624f52a6e1830501829e527863f38d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:18 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:18 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a2fb915c6222a2ae9101a4fe6b2c919e77cfd7e17346706b021b3c098f3a94`  
		Last Modified: Fri, 08 May 2026 19:44:04 GMT  
		Size: 42.3 MB (42281839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361cd22d8bb01688583f4a5e14a606310648019f8075e9b09a80c972f662e0f8`  
		Last Modified: Fri, 08 May 2026 19:44:02 GMT  
		Size: 1.6 MB (1564347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173af7c5673cebfe01ed77d2ba01e04a6bc0b194fc0460d4956307338265cf3a`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 236.5 MB (236478296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:61825f087be3dff94d3b87986108ffdba78536579c6754fed1df50fc1fe5590c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fede15183b7f7316259599bcc2b746691d74c0ea508ccd4536ecf8ba200cad44`

```dockerfile
```

-	Layers:
	-	`sha256:89324f4753f8bc4b667083e77e84de3059ea51c078964f18130cae1322d8adc1`  
		Last Modified: Fri, 08 May 2026 19:44:02 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:3.13.0-103.1.beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:6e7f3bf208fc36edb717cde32b6f70d8ef762f7fa7e461ea6abe3843c5c65900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249070092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d14d3055c105f6e5407b3ac58d6e3a71b650af4acb5c3657cd1aedfb72c4a8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:16:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d4e7505852f448a449ce5385d217bd87481d51c1d4f0c1b0bc1f90f765b77`  
		Last Modified: Mon, 11 May 2026 01:21:11 GMT  
		Size: 177.7 MB (177653946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:3.13.0-103.1.beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cd48c5becbeb0db15a2a2441b58c53873edca8f21ba58946f83667ca9ce3a692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9faeabd8102b65f8c817c09d44e0e0dee141bfd47ff363f18cfe63b304c0d3e6`

```dockerfile
```

-	Layers:
	-	`sha256:3c205f87b681476829b897eb4f83b32f207072f29e3a36a516b5e5eee33e024c`  
		Last Modified: Mon, 11 May 2026 01:20:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta`

```console
$ docker pull dart@sha256:72c6de367dbd29f1f7e547655ff160ed3d6086c955b9b2226a97be78268668dd
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
$ docker pull dart@sha256:8b154bb0537e809eb6a274b1043a56799b2124a7f0a02ebefab6aa1ba084b2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311865357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3f5e2351fb920d21e318c8f4de4f257dbf3bdf269b7ed4844e8fe4712a29e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:28 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:28 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092f09bec1bee84db0a209f8e408f14bbdb2d9531f7fde7c45bedd3387338f1b`  
		Last Modified: Fri, 08 May 2026 19:42:13 GMT  
		Size: 42.5 MB (42501670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081155158f96012d07f30d5dddb7cb2b9e0faa603c1898307fbb361cdeb0efb0`  
		Last Modified: Fri, 08 May 2026 19:42:11 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ec03aae636de9cf4ac915d65797db673d087d42a44aec1cb8473a0e6471b36`  
		Last Modified: Fri, 08 May 2026 19:42:17 GMT  
		Size: 237.7 MB (237713858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:6a8a3226d06667b9a81af297ba81011e3876d8cd84a2efd9ef5e13f528eb7d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05f659edfa89d1a3c9f59d9dda96cb80a5eae429d98fdf619444686521da860`

```dockerfile
```

-	Layers:
	-	`sha256:d865bc2239ef5e860ca6d4cc3a3734de0fa7b25b4d8b08e34b89a663306edec7`  
		Last Modified: Fri, 08 May 2026 19:42:11 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:e0637ace0c2e5d05a184f5e0a6047e21b059fad18da985c1d6da20e5e2e4c84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226609126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ccadca45cbbe6f1fbc13be8aa3315872ae4492f06e922250266627c10547a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:20 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:20 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c397f78e7cc2537e75904f25729ec5dba7faef504c3e5c252d1a5002cb7b51`  
		Last Modified: Fri, 08 May 2026 19:45:51 GMT  
		Size: 37.5 MB (37495343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f6665a0d68a8f335082af00f76179f9edc46554e97b0d1b653c7e52bdf9293`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47abf148c5b483759071bc1a739e4bd39ad00582e479db7508632b941aee80ea`  
		Last Modified: Fri, 08 May 2026 19:45:54 GMT  
		Size: 161.6 MB (161625679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:ba00119c541b5bbccf496d853b6c3d0e455f25c3a382bce4ff63f6efcca9ca97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0302ae0294b448ee831ac5b8d8af4afdb677362938a9558aaec95c9c0ed90`

```dockerfile
```

-	Layers:
	-	`sha256:a4a8db3dac533e52d15d9938f2e60f68193e58194ae649f168595f25726b0afb`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 19.0 KB (19027 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:177fc14c3b5fe9cdee875ed9e999d1cda004f488b01ec57926076e44084aeacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310468156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bafca3464d98938d54efe43148bda4e96624f52a6e1830501829e527863f38d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:18 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:18 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a2fb915c6222a2ae9101a4fe6b2c919e77cfd7e17346706b021b3c098f3a94`  
		Last Modified: Fri, 08 May 2026 19:44:04 GMT  
		Size: 42.3 MB (42281839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361cd22d8bb01688583f4a5e14a606310648019f8075e9b09a80c972f662e0f8`  
		Last Modified: Fri, 08 May 2026 19:44:02 GMT  
		Size: 1.6 MB (1564347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173af7c5673cebfe01ed77d2ba01e04a6bc0b194fc0460d4956307338265cf3a`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 236.5 MB (236478296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:61825f087be3dff94d3b87986108ffdba78536579c6754fed1df50fc1fe5590c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fede15183b7f7316259599bcc2b746691d74c0ea508ccd4536ecf8ba200cad44`

```dockerfile
```

-	Layers:
	-	`sha256:89324f4753f8bc4b667083e77e84de3059ea51c078964f18130cae1322d8adc1`  
		Last Modified: Fri, 08 May 2026 19:44:02 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; riscv64

```console
$ docker pull dart@sha256:6e7f3bf208fc36edb717cde32b6f70d8ef762f7fa7e461ea6abe3843c5c65900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249070092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d14d3055c105f6e5407b3ac58d6e3a71b650af4acb5c3657cd1aedfb72c4a8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:16:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d4e7505852f448a449ce5385d217bd87481d51c1d4f0c1b0bc1f90f765b77`  
		Last Modified: Mon, 11 May 2026 01:21:11 GMT  
		Size: 177.7 MB (177653946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:cd48c5becbeb0db15a2a2441b58c53873edca8f21ba58946f83667ca9ce3a692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9faeabd8102b65f8c817c09d44e0e0dee141bfd47ff363f18cfe63b304c0d3e6`

```dockerfile
```

-	Layers:
	-	`sha256:3c205f87b681476829b897eb4f83b32f207072f29e3a36a516b5e5eee33e024c`  
		Last Modified: Mon, 11 May 2026 01:20:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:beta-sdk`

```console
$ docker pull dart@sha256:72c6de367dbd29f1f7e547655ff160ed3d6086c955b9b2226a97be78268668dd
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
$ docker pull dart@sha256:8b154bb0537e809eb6a274b1043a56799b2124a7f0a02ebefab6aa1ba084b2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311865357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3f5e2351fb920d21e318c8f4de4f257dbf3bdf269b7ed4844e8fe4712a29e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:28 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:28 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:28 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:28 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:40 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092f09bec1bee84db0a209f8e408f14bbdb2d9531f7fde7c45bedd3387338f1b`  
		Last Modified: Fri, 08 May 2026 19:42:13 GMT  
		Size: 42.5 MB (42501670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081155158f96012d07f30d5dddb7cb2b9e0faa603c1898307fbb361cdeb0efb0`  
		Last Modified: Fri, 08 May 2026 19:42:11 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ec03aae636de9cf4ac915d65797db673d087d42a44aec1cb8473a0e6471b36`  
		Last Modified: Fri, 08 May 2026 19:42:17 GMT  
		Size: 237.7 MB (237713858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:6a8a3226d06667b9a81af297ba81011e3876d8cd84a2efd9ef5e13f528eb7d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05f659edfa89d1a3c9f59d9dda96cb80a5eae429d98fdf619444686521da860`

```dockerfile
```

-	Layers:
	-	`sha256:d865bc2239ef5e860ca6d4cc3a3734de0fa7b25b4d8b08e34b89a663306edec7`  
		Last Modified: Fri, 08 May 2026 19:42:11 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:e0637ace0c2e5d05a184f5e0a6047e21b059fad18da985c1d6da20e5e2e4c84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226609126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23ccadca45cbbe6f1fbc13be8aa3315872ae4492f06e922250266627c10547a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:20 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:20 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:28 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c397f78e7cc2537e75904f25729ec5dba7faef504c3e5c252d1a5002cb7b51`  
		Last Modified: Fri, 08 May 2026 19:45:51 GMT  
		Size: 37.5 MB (37495343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f6665a0d68a8f335082af00f76179f9edc46554e97b0d1b653c7e52bdf9293`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 1.3 MB (1273160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47abf148c5b483759071bc1a739e4bd39ad00582e479db7508632b941aee80ea`  
		Last Modified: Fri, 08 May 2026 19:45:54 GMT  
		Size: 161.6 MB (161625679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ba00119c541b5bbccf496d853b6c3d0e455f25c3a382bce4ff63f6efcca9ca97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b0302ae0294b448ee831ac5b8d8af4afdb677362938a9558aaec95c9c0ed90`

```dockerfile
```

-	Layers:
	-	`sha256:a4a8db3dac533e52d15d9938f2e60f68193e58194ae649f168595f25726b0afb`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 19.0 KB (19027 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:177fc14c3b5fe9cdee875ed9e999d1cda004f488b01ec57926076e44084aeacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310468156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bafca3464d98938d54efe43148bda4e96624f52a6e1830501829e527863f38d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:18 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:18 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:18 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:18 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:32 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a2fb915c6222a2ae9101a4fe6b2c919e77cfd7e17346706b021b3c098f3a94`  
		Last Modified: Fri, 08 May 2026 19:44:04 GMT  
		Size: 42.3 MB (42281839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361cd22d8bb01688583f4a5e14a606310648019f8075e9b09a80c972f662e0f8`  
		Last Modified: Fri, 08 May 2026 19:44:02 GMT  
		Size: 1.6 MB (1564347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173af7c5673cebfe01ed77d2ba01e04a6bc0b194fc0460d4956307338265cf3a`  
		Last Modified: Fri, 08 May 2026 19:44:08 GMT  
		Size: 236.5 MB (236478296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:61825f087be3dff94d3b87986108ffdba78536579c6754fed1df50fc1fe5590c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fede15183b7f7316259599bcc2b746691d74c0ea508ccd4536ecf8ba200cad44`

```dockerfile
```

-	Layers:
	-	`sha256:89324f4753f8bc4b667083e77e84de3059ea51c078964f18130cae1322d8adc1`  
		Last Modified: Fri, 08 May 2026 19:44:02 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:6e7f3bf208fc36edb717cde32b6f70d8ef762f7fa7e461ea6abe3843c5c65900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249070092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d14d3055c105f6e5407b3ac58d6e3a71b650af4acb5c3657cd1aedfb72c4a8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:16:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=b09a455c98a59469f58a0b4cf7221290e7f79843a077831545f0332c2f4396ee;             SDK_ARCH="x64";;         armhf)             DART_SHA256=c902ac4859fcd62f445fe028f8ace678b8694cd8c7566f785bd5e8681cd458a6;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3f9f26d4561c8d6c48ce6db1dfca0eb9befaba04c4ed62b557ff58af5c976113;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e2c7e8658365bdde9b868ffedbbe36a4f3813187eed05ccd4b9097edab43129f;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.13.0-103.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d4e7505852f448a449ce5385d217bd87481d51c1d4f0c1b0bc1f90f765b77`  
		Last Modified: Mon, 11 May 2026 01:21:11 GMT  
		Size: 177.7 MB (177653946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:cd48c5becbeb0db15a2a2441b58c53873edca8f21ba58946f83667ca9ce3a692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9faeabd8102b65f8c817c09d44e0e0dee141bfd47ff363f18cfe63b304c0d3e6`

```dockerfile
```

-	Layers:
	-	`sha256:3c205f87b681476829b897eb4f83b32f207072f29e3a36a516b5e5eee33e024c`  
		Last Modified: Mon, 11 May 2026 01:20:44 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:latest`

```console
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:latest` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:latest` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:sdk`

```console
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable`

```console
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json

## `dart:stable-sdk`

```console
$ docker pull dart@sha256:2ed474dc085f267ca692261ce35b23a0ae039e317beebef854be886c8b57832d
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
$ docker pull dart@sha256:79e142e3ed3ff453dd1997eec27bd084d2eeac90b32f2a1333f2dbe3d6596355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307114427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1359216d1335df3f9a1977734520e5b54f865979cf5433cc7d63eddc216819`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:41:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:41:17 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:41:17 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:41:17 GMT
WORKDIR /root
# Fri, 08 May 2026 19:41:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc981ba7f90810c57983ea10aa09282b5f100842064ac6993d73380e0ab8342`  
		Last Modified: Fri, 08 May 2026 19:42:01 GMT  
		Size: 42.5 MB (42501650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce412d25824262972dd85be52d72a196bd26ab8f590aec16ee618ddbc3ca93`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 1.9 MB (1869567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4174c93d86185ffbd0bdd66c6b76a0c06ef903dd3fe10dc77624bc59c61e10`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 233.0 MB (232962952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:70abf350ebb7b3f684c3443aab17d675259d4e373a1dcb9c21b6afb8fcc51f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1fc8b0d1f6d78cb9d6371e4e02b7ace530377abcd1790a8c34bdbcf70b6941`

```dockerfile
```

-	Layers:
	-	`sha256:fc587912a0733b606382b058df5ab761487e20e13914f35027299e5df9167075`  
		Last Modified: Fri, 08 May 2026 19:41:59 GMT  
		Size: 20.6 KB (20616 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:157bfdafcce3db4248de42b91d611ae7a82f734cee85f7dd70125918f7d66c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222902279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe58d123649bbbdc580a1cb77f8ddb346e50995f0b1d00e52c306b731f1cf180`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:15 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:45:15 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:45:15 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:45:15 GMT
WORKDIR /root
# Fri, 08 May 2026 19:45:25 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b13eed7035ef15a7c046531d2529d298170d9819286fdc16c2890f0d69cc4c0`  
		Last Modified: Fri, 08 May 2026 19:45:46 GMT  
		Size: 37.5 MB (37495261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da992328967dae4fd3ffbd2843e1b866d1c6e3cc17f686a1af227aaab844f0`  
		Last Modified: Fri, 08 May 2026 19:45:45 GMT  
		Size: 1.3 MB (1273171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f75ab15165d09d3fdb4cb1e63fca2a8ff662b8b92e933af82fc5e0d88b051a1`  
		Last Modified: Fri, 08 May 2026 19:45:49 GMT  
		Size: 157.9 MB (157918903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:4b577dd8394e2dbe49ddae9432e4627597a98de373573715940d38b656e24bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5fc62089bdb2dbfe4cf8197d62618aa119a51ebeb7d5b71b7e4c5d3393ed52`

```dockerfile
```

-	Layers:
	-	`sha256:cdce725c3844f08a17adc84fa24cd4805aacf3454bcc58b1fbcb3be690b1b426`  
		Last Modified: Fri, 08 May 2026 19:45:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:eed59411148416325bec9dd059db167e792efccc658f1287121b27d4cbd3f1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305470883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c6edb63e7bacad0c1b30fb8621ca5ff8aa71d8237e0afa3c78c674e120060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Fri, 08 May 2026 19:43:06 GMT
ENV DART_SDK=/usr/lib/dart
# Fri, 08 May 2026 19:43:06 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:06 GMT
WORKDIR /root
# Fri, 08 May 2026 19:43:17 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b554852d66a9642d8333ab3837de13867d25c93a53be4659670d30cd4977b`  
		Last Modified: Fri, 08 May 2026 19:43:46 GMT  
		Size: 42.3 MB (42281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da68acad7348dc1891b43ddaed85061bb91bfd6d647e0fb3262f7980caa5d08`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 1.6 MB (1564351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41608a031eb7fc5e3376993c1297511a5b3dffad47cf282ce99752f1c862a11b`  
		Last Modified: Fri, 08 May 2026 19:43:50 GMT  
		Size: 231.5 MB (231481247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:419ecc8a6d77e0f2974199da9fdd1137c0e57440840fc18931acdefbf998baf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd9da535b37d0ab34050a831e8fde36fa6b2384bb9d21c9cefefdb012292ea3`

```dockerfile
```

-	Layers:
	-	`sha256:43e5d3b81745cdbba311bee89399dca248f4907212ec5c879ce05ebe0353edd7`  
		Last Modified: Fri, 08 May 2026 19:43:44 GMT  
		Size: 20.8 KB (20822 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:stable-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:8f80cc4474767692f5c1529859890a3e9016d7129430275b7f9a153a30885292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251917939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c270d48107aa8d4931ae2d0f43615d74ab1167684af6daf8a2b57c10cdcc24`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 01:09:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 01:09:35 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Mon, 11 May 2026 01:09:36 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 11 May 2026 01:09:36 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 01:09:36 GMT
WORKDIR /root
# Mon, 11 May 2026 01:10:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=ea0ff2396ea5af402ba3598a9139a0f4b1b3471d9d7e834882d1559622760add;             SDK_ARCH="x64";;         armhf)             DART_SHA256=ba594177d23c372c02a80dbeacd418094f78f44bfb67a60636cc32eafb662185;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3c1299f468eba0fd77cf9b82d7e768382c1e980837b60ca774a2ceb4f9d7db4b;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=e851173310f74901423b8ebab27fccd15d0f166f682b346fb8c553b1c39bac09;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/stable/release/3.11.6/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d634a513fcd794ececd26147a98618b5c5221ff1c54868c7b6e5b6da4652926`  
		Last Modified: Mon, 11 May 2026 01:14:52 GMT  
		Size: 41.6 MB (41571482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9adbb6515f8ccbf983504652539ee3cd1ba5b6f18ce411b7ae7f68a3fc25d`  
		Last Modified: Mon, 11 May 2026 01:14:40 GMT  
		Size: 1.6 MB (1564400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c8f6c195b7f57776726e888623a039a308774e3a76ee9f90bc350f0dffa4c`  
		Last Modified: Mon, 11 May 2026 01:15:11 GMT  
		Size: 180.5 MB (180501793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:stable-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:0b3d019b1027028dd829589dd0c84c2a728ad0a8fa03fcb055930d21148ceda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 KB (20700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380e57d567ee2a8504c7b7df0bb13320e2ce1a3826dc7964e063b7c2b64bcbfa`

```dockerfile
```

-	Layers:
	-	`sha256:6e5ef5e5463c5fced011fdd65d8731329223c614a4474b95055676c06720b768`  
		Last Modified: Mon, 11 May 2026 01:14:39 GMT  
		Size: 20.7 KB (20700 bytes)  
		MIME: application/vnd.in-toto+json
